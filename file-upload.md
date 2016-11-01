file upload 를 구현한다.

DB 에 입력되는 것을 디스크에 저장되도록 수정한다.

글로벌 프로퍼티 설정

```xml
# for JFile properties
system.uploadpath = /upload
```

자바에서 해당 값을 주입합니다.

```java
@Value("#{global['system.uploadpath']}")
private String fileBasePath;
```

Value 어노테이션 사용을 위해 임포트를 추가합니다. 
```java
import org.springframework.beans.factory.annotation.Value;
```

리퀘스트 맵핑을 등록하고 함수를 구현합니다. 

```java
@RequestMapping("/fileUploadDisk.json")
public void fileUploadDisk(RMap rmap, ModelMap model, @RequestParam("file") MultipartFile file) throws IOException {
    //
}
```

@RequestParam("file")를 통해서 멀티파트파일 정보는 file 변수에 담기게 됩니다. 

업로드 대상 URL 정보를 위에서 설정한 주소로 변경합니다.

```javascript
url : "/web/common/file/fileUploadDisk.json"
```

jQuery.uploadfile 플러그인을 사용중이므로 아래와 같이 설정합니다. 

```javascript
// 파일 업로드
upload = $("#spreadRegistFile").uploadFile({
	url : "/web/common/file/fileUploadDisk.json",
	fileName : "file",
	autoSubmit : false,
	dragDropStr : '',
	uploadStr : '등록',
	showQueueDiv : 'spreadRegistFileQueue',
	dragdropWidth : 150,
	statusBarWidth : 140,
	maxFileCount : 5,
	showError : false,
	showProgress : false,
	onSuccess : function(files, data, xhr, pd) {
		toast.push(Object.toJSON(files));
		upload.reset();
	},
	onError : function(files, status, errMsg, pd) {
		toast.push(errMsg);
	}
});
```


![](https://goo.gl/cbOJ36)


## controller 구현

## service 구현

```java
public int insertAttachFileInfo(RMap rmap, ModelMap model) {
	rmap.put("user_id", rmap.getSession().getAttribute("user_id"));
	return dao.insert("web.common.insertAttachFileInfo", rmap);
}
```

## mybatis 구현

insert 태그 추가 
```xml
<insert id="insertAttachFileInfo">
		/* web.common.insertFile */
       ...
</insert>
```

저장할 대상
- #{file_seq}
- #{file_size} 
- #{file_type}
- #{original_file_name}
- #{attach_file_name}
- #{attach_file_path}














