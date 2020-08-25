#CSS
##The General Rule
```
selector {
  property: value;
  anotherProperty: value;
}
```

EX:

```
/*Make All h1's purple and 56px font*/
h1 {
  color: purple;
  font-size: 56px;
}

/*Give All img's a 3px red border*/

img {
  border-color: red;
  border-width: 3px;
}
```

![](https://github.com/JohnnyYeee/Photohub/blob/master/git/CSS%20norder.png?raw=true)

####text划线
![](https://github.com/JohnnyYeee/Photohub/blob/master/git/text%20划线.png?raw=true)

###inline //not good way
```<h3 style="color: pink;">blah blah blah </h3>
<h3 style="color: pink;">knock knock </h3>

<p style="color: yellow;">blah blah blah </p>
```
###style tag // not good way
```<html>
<head>
    <title>About Rusty</title>
    <style type="text/css">
        li {
	    color: red;
	}
    </style>
</head>
```
##In separate CSS file, use <link> tag
```
<!DOCTYPE html>
<html>
<head>
    <title>Demo Page</title>
    <link rel="stylesheet" type="text/css" href="app.css">
</head>
<body>
	
</body>
</html>
```

In css file

```
h1 {
  color: purple;
}

h3 {
 color: pink;
}
```

##Color in CSS
###Hexadecimal
```h1 {
  color: red;
}

h2 {
  color: cornflowerBlue;
}

h3 {
  color: darkOrchid;
}
```
###RGB
```
h1 {
  color: rgb(0,255,0);
}

h2 {
  color: rgb(100, 0, 100);
}

h3 {
  color: rgb(11, 99, 150);
}
```
###RGBA
```
h1 {
  color: rgba(11, 99, 150, 1);
}

h2 {
  color: rgba(11, 99, 150, .6);
}

h3 {
  color: rgba(11, 99, 150, .2);
}
```
##Color and background
```
body {
  background: #95a5a6;
}

div{
  background: #3498db;
}

p {
  color: #ecf0f1;
}
```
##Background and Image
```
body {
  background: url(http://3dprint.com/wp
   -content/uploads/2014/11/-
   Rainbow_Ocean__by_Thelma1.jpg);
}

div{
  background: rgba(0,0,0,.7);
}

p {
  color: #ecf0f1;
}
```

![](https://github.com/JohnnyYeee/Photohub/blob/master/git/CSS%20background.png?raw=true)
#Selector
##Element selector
Select all instances of a given element

```
<div>
  <p>You say yes</p>
  <p>I say no</p>
</div>

<div>
  <p>You say goodbye</p>
  <p>I say hello </p>
</div>
```

```
div{
  background: purple;
}

p {
  color: yellow;
}
```
##ID Selector
Selects an element with a given ID.  Only one per page!

```
<div>
  <p>You say yes</p>
  <p>I say no</p>
</div>

<div>
  <p>You say goodbye</p>
  <p id="special">I say hello </p>
</div>
```

```
div{
  background: purple;
}

#special {
  color: yellow;
}
```

##Class Selector
Selects all elements with a given class

```
<div>
  <p class="highlight">You say yes</p>
  <p>I say no</p>
</div>

<div>
  <p class="highlight">You say goodbye</p>
  <p>I say hello </p>
</div>
```

```
div{
  background: purple;
}

.highlight {
  background: yellow;
}
```
###more selector
```
/*Element*/
li {

}
/*class*/
.hello {

}
/*id*/
#name {

}

/*Star*/

* {
	border: 1px solid lightgrey;
}

/*Descendant Selector*/

li a {
	color: red;
}

/*Adjacent Selector*/

h4 + ul {
	border: 4px solid red;
}


/*Attribute Selector*/

a[href="http://www.google.com"] {
	background: blue;
}

/*nth of type*/

li:nth-of-type(odd){
	background: purple;
}
```

##font family and font size

```
/*font-family*/

p {
	font-family: Arial;
}

h1 {
	font-family: Georgia;
}

/*font-size*/

body {
	font-size: 10px;
}

h1 {
	font-size: 5.0em;
}

p {
	font-size: 2.0em;
}

span {
	font-size: 2.0em;
}
```

##More font propertyx
```
/*font-family*/

p {
	font-family: Arial;
}

h1 {
	font-family: Georgia;
}

/*font-size*/

body {
	font-size: 10px;
}

h1 {
	font-size: 5.0em;
}

p {
	font-size: 2.0em;
}

span {
	font-size: 2.0em;
}

/*font-weight*/

p{
	font-weight: normal;
}

/*line-height*/

p {
	line-height: 1.5;
}

/*text-align*/

h1 {
	text-align: right;
}

p {
	text-align: center;
}

/*text-decoration*/

p {
	text-decoration: underline;
}

h1 {
	text-decoration: line-through;
}
```

##Box Model
![](https://github.com/JohnnyYeee/Photohub/blob/master/git/box%20model.png?raw=true)

```
p {

/*Content - Width and Height*/

width: 50%;
/*Border*/

border: 2px solid blue;

/*Padding*/

/*padding: 10px;*/
padding-left: 40px;

/*Margin*/
/*margin: 100px;*/
/*margin-top: 500px;*/
/*margin: 20px 40px 500px 100px;*/
/*margin: 0 auto 0 auto;*/
margin: 0 auto;
margin: 50px 20px;
}
```
####float left
```
{
float:left;
}
//向左对齐
```

####width

```
max-width: 700px;  //最多多少px
width:80% // always 80% of width
```

####letter spacing
`letter-spacing：0.2rem；`
rem accoding to root element
em according to parent element


####horizontal rule
<hr>

##blog example
```
<!DOCTYPE html>
<html>
<head>
	<title>My Blog</title>
	<link rel="stylesheet" type="text/css" href="blog.css">
	<link href='http://fonts.googleapis.com/css?family=Source+Sans+Pro:400,700,400italic|Source+Code+Pro:400,700' rel='stylesheet' type='text/css'>
</head>
<body>



<div class="post">
	 
	<div class="date">November 23 2015</div>
	<h2>This Is My First Article</h2>

	<p class="quote">
	Bacon ipsum dolor amet capicola strip steak landjaeger, biltong spare ribs rump cow ground round andouille sirloin pork. Short ribs pig prosciutto swine. Flank turducken turkey rump, leberkas shoulder bresaola ham hock tail drumstick corned beef. Venison pork chop beef jowl short ribs.
	</p>

	<p>Bresaola short ribs pastrami, beef ribs spare ribs kielbasa ham tongue kevin landjaeger chicken ball tip. Pork chop beef kevin strip steak, chicken pork belly pastrami ham hock flank shoulder chuck turkey ribeye andouille ball tip. Leberkas ham ham hock pork loin. Filet mignon bacon pancetta leberkas turducken fatback tongue frankfurter jowl. Shoulder tenderloin chicken shank bacon shankle sirloin.</p>

	<p>Pork pig pork loin prosciutto meatball turkey beef ribs ground round. Pork belly salami shank pork chop turducken ribeye swine shoulder tri-tip fatback cupim short loin chuck strip steak. Rump pork chop t-bone.</p>
	<hr>
</div>

<!-- <hr> -->

<div class="post">
	<div class="date">December 11 2015</div>
	<h2>This Is Another Article</h2>

	<p class="quote">
	Bacon ipsum dolor amet capicola strip steak landjaeger, biltong spare ribs rump cow ground round andouille sirloin pork. Short ribs pig prosciutto swine. Flank turducken turkey rump, leberkas shoulder bresaola ham hock tail drumstick corned beef. Venison pork chop beef jowl short ribs.
	</p>

	<p>Shankle beef ribs tongue strip steak flank landjaeger capicola hamburger chuck pancetta kevin. Sirloin landjaeger chicken, bresaola brisket swine short ribs turkey short loin ball tip porchetta ham hock. Capicola frankfurter jowl short loin. Kevin flank hamburger, beef venison shankle short loin bresaola frankfurter</p>

	<p>Bresaola short ribs pastrami, beef ribs spare ribs kielbasa ham tongue kevin landjaeger chicken ball tip. Pork chop beef kevin strip steak, chicken pork belly pastrami ham hock flank shoulder chuck turkey ribeye andouille ball tip. Leberkas ham ham hock pork loin. Filet mignon bacon pancetta leberkas turducken fatback tongue frankfurter jowl. Shoulder tenderloin chicken shank bacon shankle sirloin.</p>
</div>

</body>
</html>
```

```
@import url(https://fonts.googleapis.com/css?family=Source+Sans+Pro:400,700);

body {
  width: 80%;
  border: 20px solid #bdc3c7;
  font-family: 'Source Sans Pro', sans-serif;
  padding: 20px;
  margin: 20px auto;
  max-width: 700px;
}

.post {
  margin-bottom: 20px;
}

.date {
  color: #3498db;
  letter-spacing: 0.2rem;
  text-transform: uppercase;
}

.quote{
  border-left: 5px solid #bdc3c7;
  padding-left: 5px;
}

h2 {
  font-size: 2.0rem;
  font-weight: bold;
  color: #2c3e50;
}

hr{
    border: 0;
    height: 0;
    border-top: 1px solid rgba(0, 0, 0, 0.1);
    border-bottom: 1px solid rgba(255, 255, 255, 0.3);
}
```











