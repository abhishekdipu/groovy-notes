# groovy-notes

### random string generation
```js
import org.apache.commons.lang.RandomStringUtils

String charset = (('A'..'Z') + ('0'..'9')).join()
Integer length = 9
String randomString = RandomStringUtils.random(length, charset.toCharArray())
```

### date handeling

#### getting date
```js
def format = "yyyy-MM-dd"
println new Date().format(format) //O/P: 2021-01-13
```
#### [Available formates](https://rmr.fandom.com/wiki/Groovy_Date_Parsing_and_Formatting)
```js
year : y(LowerCase) 
yy -> 21
yyyy-> 2021

month : M(UpperCase)
M -> 1
MM -> 01
MMM -> Jan
MMMM -> January

day: d(LowerCase) 
d -> 9
dd -> 09

hour : h (for 12 hr format), H (for 24 hr format)
minute : m
second : s 
AM/PM : a 
timeZone : z
```

#### changing date format
```js
def oldDate = '09-JAN-1996'
def parsedDate = Date.parse( 'dd-MMM-yyyy', oldDate )
def newDate = parsedDate.format( 'yyyy-MM-dd' )

println newDate //O/P: 1996-01-09
```
