file upload 를 구현한다.

DB 에 입력되는 것을 디스크에 저장되도록 수정한다.

```java
rmap.put\("file", file\);
rmap.put\("file\_size", size\);
rmap.put\("file\_type", type\);
```



UMap map = commonFileService.selectFileView\(rmap, model\);

 String file\_path = map.getStr\("FILE\_PATH"\);

 String real\_path = context.getRealPath\(""\)+file\_path;





