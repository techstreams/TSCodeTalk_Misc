# TSCodeTalk > Misc > Create onOpen() Menu From Array


This script adds an onOpen() menu from a menu array.  

*Example shows a menu configuration for Google Sheets.*


---

```javascript
function onOpen() {  
  const menu = [    
    { name: "Step 1: Authorize",   functionName: "configure" },
    { name: "Step 2: Run Program", functionName: "configure" },
    { name: "Uninstall (Stop)",    functionName: "reset"     }
  ];  
  SpreadsheetApp.getActiveSpreadsheet().addMenu("Gmail Attachments", menu);
}
```
