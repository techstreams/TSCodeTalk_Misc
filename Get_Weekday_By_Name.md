# TSCodeTalk > Misc > Get Weekday By Name


This script retrieves the name of the weekday corresponding to "today".


---

```javascript
function getDayByName() {
  const d = new Date();
  const weekday = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
  Logger.log(weekday[d.getDay()]);
}
```
