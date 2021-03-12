# TSCodeTalk > Misc > Get ID From URL


This script retrieves a Google Doc File ID from the URL.


---

```javascript
function getFileIdFromUrl() {
  const url = "https://docs.google.com/spreadsheets/d/1_K417gej_fNthqjPZ20Nm_W3onJTu6siyTh08Od6ttt/edit#gid=0";
  const res = url.match(/\/d\/(.+)\//gi);
  const id = res[0].slice(3,-1);
}
```

---

This script retrieves a Google Drive Folder ID from the URL.

```javascript
function getFolderIdFromUrl() {
   const url = "https://drive.google.com/drive/folders/0B-Hia093Kr3ELUZjWFl3Mk1XHRT";
   const res = url.match(/\/folders\/(.+)$/gi);
   const id = res[0].slice(9);

}
```
