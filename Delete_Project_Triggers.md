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

---

This script deletes the project clock triggers.

```javascript
/*
 * Delete existing clock based triggers
 */
function deleteExistingClockTriggers() {
   ScriptApp.getProjectTriggers().forEach(trigger {
     if (trigger.getEventType() == ScriptApp.EventType.CLOCK) {
       ScriptApp.deleteTrigger(trigger);
     }
   }
}
```
