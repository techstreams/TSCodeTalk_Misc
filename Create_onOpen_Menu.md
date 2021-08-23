# TSCodeTalk > Misc > Create onOpen() Menu From Array


This script adds an onOpen() menu to a Google Sheet from a menu array. 

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

---

This script adds an onOpen() menu to a Google Sheet, Doc or Form.

```javascript
function onOpen() {
  // Or DocumentApp or FormApp.
  const ui = SpreadsheetApp.getUi().createMenu('Custom Menu')
      .addItem('First item', 'menuItem1')
      .addSeparator()
      .addItem('Second item', 'menuItem2')
      .addToUi();
}
```

---

This function adds an onOpen menu to a Google Sheet, Doc or Form with a submenu

```js
function onOpen() {
  // Or SpreadsheetApp or FormApp.
  DocumentApp.getUi().createMenu('Sample')
      .addItem('Show alert', 'showAlert')
      .addItem('Show prompt', 'showPrompt')
      .addSeparator()
      .addItem('Show dialog', 'showDialog')
      .addItem('Show sidebar', 'showSidebar')
      .addSeparator()
      .addSubMenu(DocumentApp.getUi().createMenu('Document interaction')
          .addItem('Search and replace', 'searchAndReplace')
          .addItem('Insert at cursor', 'insertAtCursor')
          .addItem('Turn selection purple', 'turnSelectionPurple')
          .addItem('Create report in document', 'createReport'))
      .addToUi();
```
