---
layout: "post"
title: "Android笔记"
date: "2019-01-08 11:44"
---

##### 开启语音增强

>mAudioManager.setParameters("volume_boost=on");

---

##### RecyclerView

> item布局直接使用ConstraintLayout会出现滑动时重复调用onCreateViewHolder方法导致卡顿

---

##### 6.0危险权限
```
日历数据
android.permission-group.CALENDAR
android.permission.READ_CALENDAR
android.permission.WRITE_CALENDAR
相机
android.permission-group.CAMERA
android.permission.CAMERA
联系人
android.permission-group.CONTACTS
android.permission.READ_CONTACTS
android.permission.WRITE_CONTACTS
android.permission.GET_ACCOUNTS
位置
android.permission-group.LOCATION
android.permission.ACCESS_FINE_LOCATION
android.permission.ACCESS_COARSE_LOCATION
麦克风
android.permission-group.MICROPHONE
android.permission.RECORD_AUDIO
电话
android.permission-group.PHONE
android.permission.READ_PHONE_STATE
android.permission.CALL_PHONE
android.permission.READ_CALL_LOG
android.permission.WRITE_CALL_LOG
com.android.voicemail.permission.ADD_VOICEMAIL
android.permission.USE_SIP
android.permission.PROCESS_OUTGOING_CALLS
传感器
android.permission-group.SENSORS
android.permission.BODY_SENSORS
短信
android.permission-group.SMS
android.permission.SEND_SMS
android.permission.RECEIVE_SMS
android.permission.READ_SMS
android.permission.RECEIVE_WAP_PUSH
android.permission.RECEIVE_MMS
android.permission.READ_CELL_BROADCASTS
存储
android.permission-group.STORAGE
android.permission.READ_EXTERNAL_STORAGE
android.permission.WRITE_EXTERNAL_STORAGE
```
