# TSCodeTalk > Misc > Create onFormSubmit() Trigger


This script adds an onFormSubmit() trigger to a Google Form

---

```javascript
function enableSubmitTrigger(triggerFunction = 'mySubmitTrigger') {
  ScriptApp.getProjectTriggers()
      .filter(trigger => trigger.getEventType() === ScriptApp.EventType.ON_FORM_SUBMIT && trigger.getHandlerFunction() === triggerFunction);   
  if (submitTriggers.length < 1) {
    ScriptApp.newTrigger(triggerFunction).forForm(FormApp.getActiveForm()).onFormSubmit().create();
  }  
}
```
