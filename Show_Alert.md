# TSCodeTalk > Misc > Show Alert

This function shows and alert in a Google Doc.

---

```js
/**
 * Shows a message box in the Google Docs editor.
 */
function showAlert() {
  // Displays a dialog box with "Yes" and "No" buttons. Script execution will be
  // halted until the dialog is dismissed.
  var result = DocumentApp.getUi().alert(
      'Dialog title',
      'Are you sure you want to continue?',
      DocumentApp.getUi().ButtonSet.YES_NO);

  // Process the user's response.
  if (result == DocumentApp.getUi().Button.YES) {
    // The user clicked the "Yes" button.
    DocumentApp.getUi().alert('Proceeding with the operation...');
  } else {
    // The user clicked the "No" button or the dialog's close button.
    DocumentApp.getUi().alert('Canceling the operation...');
  }
}
```
