# TSCodeTalk > Misc > Show Custom Dialog

This function displays and editor dialog in a Google Doc.

---

```js
/**
 * Shows a custom HTML user interface in a dialog above the Google Docs editor.
 */
function showDialog() {
  DocumentApp.getUi().showDialog(
      HtmlService
          .createHtmlOutput('<p>Hello from Google Apps Script!</p>')
          .setTitle('My custom dialog')
          .setWidth(400 /* pixels */)
          .setHeight(300 /* pixels */));
}
```
