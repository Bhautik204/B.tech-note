go in search & reporting >search`index=*`  and select all time > after this select sourcetype=cctv_log 

now click extract new fields > select 1st sample >  click ==next==
select regular expression > click next
select time and give **Timestamp**
select logout and give **Event**
select no and give **User_id**
select byte and give **Username**
select last and give **Session_id**
then next > next > finish
now click **explore field i just created in search** > change time to **All time** and search 

hide unnecssary fields

click settings > fields > click field extraction
after this fliter > cctv and search >  and delete cctv : Extract
open field extractor > sorcetype : **cctv_log** , time range: **all time **
`^(?P<timestamp>\d+\-\d+\-\d+\s+\d+:\d+:\d+)\s+(?P<Event>(Login\s\w+|\w+))\s+(?P<user_id>\d+)?\s?(?P<UserName>\w+)\s+.*?(?P<Session_id>\w+)$` for perfer regex > save > finish
now click **explore field i just created in search** > change time to **All time** and search 

`index=cctv_feed | stats count(Events) by UserName`
`index=cctv_feed | stats count by Event
`index=cctv_feed *failed*` > now replaced failed with repeat session id
`index=web_logs *session id*` > add clientip,file,status
now remove session id and add clientip
`index=cctv_feed *new session id*`

