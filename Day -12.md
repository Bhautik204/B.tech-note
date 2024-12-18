open burp suite > setting > burp'browser >select run without sandbox(keep intersecp off)
now , open url > login with credential
on account 111 send $500
send this transfer proxy to repeater
go to extension > Bapp store > search : turbo intruder > install
send dashboard to repeater > change it to POST and put x=1 > send it
open wireshark >start ENS5  > apply HTTP
now in suit, send POST Dashboard req > extension > turbo intruder

now in turbo intruder > conncurrentconnection=10 & requestperConnectio=1 
range (10)
	engine.queue(target,req)
def
	table.add(req)
and attack 

now create group > select 2 > press ctrl+r do it for 10 times
now select sent group in parallel
now create new group > select 1 > press ctrl+r do it for 9 times
select sent group in parallel

now log out > login with  101 & glitch
send $1000 on 111
now send res to repeater > create group > select 21  >  press ctrl+r 9 times > select sent group in parallel
#AOC 