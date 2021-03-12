# TSCodeTalk > Misc > Delete Project Triggers


This script deletes all project triggers.


---

```javascript
function deleteProjectTriggers() {
  ScriptApp.getProjectTriggers().forEach(trigger => ScriptApp.deleteTrigger(trigger));
}
```
