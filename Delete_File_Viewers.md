# TSCodeTalk > Misc > Delete File Viewers


This script removes viewers of all files in a given folder for a particular file mime type. 

---

```javascript
function removeViewers() {
  const folder = DriveApp.getFolderById('<FOLDER ID>');
  const owner = Session.getEffectiveUser().getEmail();
  let files = folder.getFilesByType(MimeType.GOOGLE_DOCS);
  
  while (files.hasNext()) {
    let f = files.next();
    f.getViewers().forEach((viewer) => {
       if (viewer.getEmail() !== owner) {
          f.removeViewer(viewer.getEmail());
       }
    });
  } 
}
```
