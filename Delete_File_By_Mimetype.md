# TSCodeTalk > Misc > Delete File By Mimetype


This script removes all files in a given folder for a particular file mime type. 

---

```javascript
function removeFiles() {
  const folder = DriveApp.getFolderById('<FOLDER ID>');
  let files = folder.getFilesByType(MimeType.GOOGLE_DOCS);
  
  while (files.hasNext()) {
    let f = files.next();
    f.setTrashed(true);
  }
}
```
