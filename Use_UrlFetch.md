# TSCodeTalk > Misc > Use UrlFetch


This script uses UrlFetch.

---

```javascript
funtion useUrlFetch(e) {
   const url = PropertiesService.getScriptProperties().getProperty('WEBHOOK_URL');
   try {
     const payload = e.response;
     const options = {
       'method' : 'post',
       'contentType': 'application/json; charset=UTF-8',
       'payload' : JSON.stringify(payload)
     };
     UrlFetchApp.fetch(url, options); 
   } catch(err) {
     console.log('Error ' + err.message);
   }
}
```
