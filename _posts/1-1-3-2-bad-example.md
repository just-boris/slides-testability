## Bad practice

```
 // noty
 $(function(){
    var notificationData = { notif: {} };
    var notifications = {
        news: 0,
        friends: 0,
        mess: notificationData.notif.newmsg || 0,
        feed: 0
     };
    noty.update(notifications);
    topper && topper.init();
 });
  $(function(){
    $("#user_name").focus();
  });
```

*complicated signalization img*