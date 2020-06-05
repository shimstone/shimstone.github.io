# iOS 나이스 페이 본인인증시 한글 인코딩 문제

이번 프로젝트에서 처음으로 본인인증을 붙여보게 되었는데 사실 구현자체는 서버쪽에서 알려준 링크를 웹뷰에 띄우기만 하면 되는 거라 어려울 것은 전혀 없었다.



문제는 예상 밖의 인코딩 문제. 



몇 시간 동안 헤맨 끝에 데이터가 utf-8이 아니라 euc-kr로 내려온다는 사실을 확인했다.

문제는 swift에서 기본적으로 euc-kr 인코딩이 지원되지 않는다는 것. 

utf-8처럼 그냥 removingPercentEncoding을 사용하면 nil이 반환된다.



4~5시간 동안 Stack Overflow와 구글링을 한 끝에 iOS 오픈채팅방에서 답을 얻어 메서드를 작성해서 공유해 본다.



```swift
extension String.Encoding {
    static let euc_kr = String.Encoding(rawValue: CFStringConvertEncodingToNSStringEncoding(CFStringEncoding(CFStringEncodings.EUC_KR.rawValue)))
}

extension String {
    func bytesByRemovingPercentEncoding(using encoding: String.Encoding) -> Data {
        struct My {
            static let regex = try! NSRegularExpression(pattern: "(%[0-9A-F]{2})|(.)", options: .caseInsensitive)
        }
        var bytes = Data()
        let nsSelf = self as NSString
        for match in My.regex.matches(in: self, range: NSRange(0..<self.utf16.count)) {
            if match.range(at:1).location != NSNotFound {
                let hexString = nsSelf.substring(with: NSMakeRange(match.range(at:1).location+1, 2))
                bytes.append(UInt8(hexString, radix: 16)!)
            } else {
                let singleChar = nsSelf.substring(with: match.range(at:2))
                bytes.append(singleChar.data(using: encoding) ?? "?".data(using: .ascii)!)
            }
        }
        return bytes
    }
    
    func removingPercentEncoding(using encoding: String.Encoding) -> String? {
        return String(data: bytesByRemovingPercentEncoding(using: encoding), encoding: encoding)
    }
}
```



사용 예

```swift
var str: String = "인코딩된 값"
str.removingPercentEncoding(using: .euc_kr)
```



