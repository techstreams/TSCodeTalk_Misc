# TSCodeTalk > Misc > Show Prompt

This function displays a prompt inside a Google Doc.

---

```js
/**
 * Shows an input box in the Google Docs editor.
 */
function showPrompt() {
  // Displays a dialog box with "OK" and "Cancel" buttons, as well as a text box
  // allowing the user to enter a response to a question.
  var result = DocumentApp.getUi().prompt('Upgrade your user experience!',
      'Please enter your name:', DocumentApp.getUi().ButtonSet.OK_CANCEL);

  // Process the user's response:
  if (result.getSelectedButton() == DocumentApp.getUi().Button.OK) {
    // The user clicked the "OK" button.
    DocumentApp.getUi().alert('The user\'s name is ' +
        result.getResponseText() + '. (And what a lovely name that is!)');
  } else if (result.getSelectedButton() == DocumentApp.getUi().Button.CANCEL) {
    // The user clicked the "Cancel" button.
    DocumentApp.getUi().alert('The user didn\'t want to provide a name.');
  } else if (result.getSelectedButton() == DocumentApp.getUi().Button.CLOSE) {
    // The user clicked the dialog's close button.
    DocumentApp.getUi().alert(
        'The user clicked the close button in the dialog\'s title bar.');
  }
}
```
