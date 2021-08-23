# TSCodeTalk > Misc > Show Sidebar

This function shows and editor sidebar inside a Google Doc.

---

```js
/**
 * Shows a custom HTML user interface in a sidebar in the Google Docs editor.
 */
function showSidebar() {
  DocumentApp.getUi().showSidebar(
      HtmlService
          .createHtmlOutput('<p>A change of speed, a change of style...</p>')
          .setTitle('My custom sidebar')
          .setWidth(350 /* pixels */));
}
```
