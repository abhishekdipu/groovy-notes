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

[Available formates](https://rmr.fandom.com/wiki/Groovy_Date_Parsing_and_Formatting)
year:y 
yy -> 21
yyyy-> 2021



```
#### changing date format
```js
def oldDate = '09-JAN-1996'
def parsedDate = Date.parse( 'dd-MMM-yyyy', oldDate )
def newDate = parsedDate.format( 'yyyy-MM-dd' )

println newDate //O/P: 1996-01-09
```
