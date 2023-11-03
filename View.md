Here the 'View' stands for the 'View' in MVC framework.

# React

React handle View with JSX and Render function.

## Use curly braces in JSX to embed JavaScript

### Where to use curly braces 

You can only use curly braces in two ways inside JSX:

1. As text directly inside a JSX tag

```javascript
<h1>{name}'s To Do List</h1>
```

2. As attributes immediately following the = sign

src={avatar} will read the avatar variable, but src="{avatar}" will pass the string "{avatar}".

```javascript
<img className="avatar" src={avatar} alt={description} />
```

### What types of Javascipt expression can be used in curly braces

1. variable
```javascript
<h1 className={titleClass}>{name}'s To Do List</h1>
```
2. function
```javascript
<h1>To Do List for {formatDate(today)}</h1>
```
3. object
```html
<ul style={{
      backgroundColor: 'black',
      color: 'pink'
    }}>
      <li>Improve the videophone</li>
      <li>Prepare aeronautics lectures</li>
      <li>Work on the alcohol-fuelled engine</li>
    </ul>
```
Actually, it is:
```javascript
<ul style={
  {
    backgroundColor: 'black',
    color: 'pink'
  }
}>
```

# Angular

In Angular, a template is a blueprint for a fragment of a user interface (UI). Templates are written in HTML, and special syntax can be used within a template to build on many of Angular's features.

Angular uses the double curly braces {{ and }} as delimiters.

```javascript
<p>{{title}}</p>
<div><img alt="item" src="{{itemImageUrl}}"></div>
```

Note:
Please notice the attribution differences between React and Angular.

React:
```javascript
<img src={itemImageUrl} />
```

Angular:
```javascript
<img src="{{itemImageUrl}}" />
```






