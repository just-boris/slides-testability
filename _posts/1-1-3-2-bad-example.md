## Bad practice

<div class="scheme-wrap">
<pre><code class="javascript">$(function(){
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
</code></pre>
<div class="scheme-wrap_img">
![complicated alarm](img/alarm_complicated.svg){% include fragment.html %}
</div>
</div>