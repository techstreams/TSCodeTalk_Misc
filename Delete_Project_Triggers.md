# TSCodeTalk > Misc > Delete Project Triggers


This script deletes all project triggers.


---

```javascript
function deleteProjectTriggers() {
  ScriptApp.getProjectTriggers().forEach(trigger => ScriptApp.deleteTrigger(trigger));
}
```

---

This script deletes all the project triggers and creates a new one.

```javascript
function configureNewTrigger() {  
  ScriptApp.getProjectTriggers().forEach(trigger => ScriptApp.deleteTrigger(trigger)); 
  ScriptApp.newTrigger("sendToGoogleDrive").timeBased().everyMinutes(5).create();  
  Browser.msgBox("Initialized", "The program is now running.", Browser.Buttons.OK);  
}
```
