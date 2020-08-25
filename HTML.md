#shortcut key
tab

command +control +D  copy the line

hold command and click diff position to write same coding in diff pos

#HTML
format : Doctype


```
<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body>

</body>
</html>
```

`<tagName> Some Content </tagName>`

`<!-- This is a comment.  It doesn't do anything! -->`

#common tag
```
<h1>I'm a header </h1>
<h2>I'm a slightly smaller header </h2>
<h6>I'm the smallest header </h6>

<p>I'm a paragraph</p>

<button>I'm a button!</button>

<ul>
	<li>List Item 1</li>
	<li>List Item 2</li>
</ul>


<ol>
	<li>List Item 1</li>
	<li>List Item 2</li>
</ol>
```


`<h1>` header from 1 tot 6, largest to samllest

`<em>` emphasis

`<strong>` strong

`<ol>` order list

`<ul>` unorder list

`<li>` list


`<div>`  Generic Container and block level element

`<span>`  Generic Container,inline element, 

`<img>` image no closing tag


`src="    "` 

ex: `<img src="......">` 


#self closing tag
```
<!-- No closing tag or inner text needed -->

<img src="corgi.png">

<link href="style.css">

<!-- Don't worry about what these tags do yet -->

```

#attributes
```
<tag name="value"></tag>
```

```
<img src="corgi.png">

<p class="selected">woof woof</p>

<a href="www.google.com">Click me to go to Google</a>

<link rel="stylesheet" type="text/css" href="style.css">
```
##image

`<img src="corgi.png">`

##Links
`<a href="url">Link Text</a>`

`<a href="www.google.com">Click me to go to Google</a>`

`<a href="www.reddit.com">Click me to go to Reddit</a>`



#table
 ``` <table>

 <thead>
 	 	<tr>
			<th>Name</th> 	
			<th>Age</th> 	
			<th>Breed</th> 	
 		</tr>
 </thead>
 <tbody>
 	<tr>
 		<td>Rusty</td>
 		<td>2</td>
 		<td>Mutt</td>
 	</tr>
 	<tr>
 		<td>Wyatt</td>
 		<td>13</td>
 		<td>Golden</td>
 	</tr>
 </tbody>
 </table>
 ```
 
  <table>

 <thead>
 	 	<tr>
			<th>Name</th> 	
			<th>Age</th> 	
			<th>Breed</th> 	
 		</tr>
 </thead>
 <tbody>
 	<tr>
 		<td>Rusty</td>
 		<td>2</td>
 		<td>Mutt</td>
 	</tr>
 	<tr>
 		<td>Wyatt</td>
 		<td>13</td>
 		<td>Golden</td>
 	</tr>
 </tbody>
 </table>
 
 #objectivs

* Use the <form></form> tag
* Use the <input> tag
* Use the <label></label> tag
* Write Simple Validations


##form tag
```
<form action="/my-form-submitting-page" method="post">
    <!-- All our inputs will go in here -->
</form>

```
* action - the URL to send form data to
* method - the type of HTTP request 

##input tag

```<input type="text">
<input type="date">
<input type="color">
<input type="file">
<input type="checkbox">
```
<input type="text">
<input type="date">
<input type="color">
<input type="file">
<input type="checkbox">


##EX:
```<h1>Sign In</h1>

<form action="/sign-in-url" method="post">
    <input type="text">
    <input type="password">
    <button>Login</button>
</form>
```

##labels
```<form action="/sign-in-url" method="post">
    <label>Username: <input type="text"></label>
    <label>Password: <input type="password"></label>
    <button>Login</button>
</form>
```
alternate syntax, use "for" and "id"

```<form action="/sign-in-url" method="post">
    <label for="username">Username:</label>
    <input id="username" type="text">
    <label for="password">Password:</label>
    <input id="password" type="password">
    <button>Login</button>
</form>
```
##simple validation
```<form action="/sign-in-url" method="post">
    <label for="email">Email:</label>
    <input id="email" type="email" required>
    <label for="password">Password:</label>
    <input id="password" type="password" required>
    <button>Login</button>
</form>
```
* The 'required' attribute validates that an input is not empty
* There are also type validations.  Try changing "type" from "text" to "email"

##complicate example
```<form action="/some-server-somewhere" method="post">
  <div>
    <label for="name">Text Input:</label>
    <input type="text" id="name" placeholder="Doc Brown" />
  </div>

    <label for="radio-choice-1">Choice 1</label>
    <input type="radio" id="radio-choice-1" value="choice-1" />

    <label for="radio-choice-2">Choice 2</label>
    <input type="radio" id="radio-choice-2" value="choice-2" />
 

  <div>
    <label for="select-choice">Select Dropdown Choice:</label>
    <select id="select-choice">
      <option value="Dogs">Dogs</option>
      <option value="Cats">Cats</option>
      <option value="Both">Both</option>
    </select>
  </div>

  <div>
    <label for="textarea">Textarea:</label>
    <textarea cols="40" rows="4" id="textarea"></textarea>
  </div>

  <div>
    <label for="checkbox">Checkbox:</label>
    <input type="checkbox" id="checkbox" />
  </div>

  <div>
    <input type="submit" value="Submit" />
  </div>
</form>  
```

<form action="/some-server-somewhere" method="post">
  <div>
    <label for="name">Text Input:</label>
    <input type="text" id="name" placeholder="Doc Brown" />
  </div>

    <label for="radio-choice-1">Choice 1</label>
    <input type="radio" id="radio-choice-1" value="choice-1" />

    <label for="radio-choice-2">Choice 2</label>
    <input type="radio" id="radio-choice-2" value="choice-2" />
 


  <div>
    <label for="select-choice">Select Dropdown Choice:</label>
    <select id="select-choice">
      <option value="Dogs">Dogs</option>
      <option value="Cats">Cats</option>
      <option value="Both">Both</option>
    </select>
  </div>

  <div>
    <label for="textarea">Textarea:</label>
    <textarea cols="40" rows="4" id="textarea"></textarea>
  </div>

  <div>
    <label for="checkbox">Checkbox:</label>
    <input type="checkbox" id="checkbox" />
  </div>

  <div>
    <input type="submit" value="Submit" />
  </div>
</form>  

 
 
 
 
 
 
 