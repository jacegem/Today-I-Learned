file upload 를 구현한다.

DB 에 입력되는 것을 디스크에 저장되도록 수정한다.

글로벌 프로퍼티 설정

```xml
# for JFile properties
system.uploadpath = /upload
```

```java
@Value("#{global['system.uploadpath']}")
private String fileBasePath;
```

UMap map = commonFileService.selectFileView\(rmap, model\);

String file\_path = map.getStr\("FILE\_PATH"\);

String real\_path = context.getRealPath\(""\)+file\_path;




