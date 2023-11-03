# React

To add an event handler, you will first define a function and then pass it as a prop to the appropriate JSX tag.

```javascript
export default function Button() {
  function handleClick() {
    alert('You clicked me!');
  }

  return (
    <button onClick={handleClick}>
      Click me
    </button>
  );
}
```

Note:

Event handlers must be passed, not called! onClick={handleClick}, not onClick={handleClick()}

passing a function (correct)
```javascript
<button onClick={handleClick}>
<button onClick={() => alert('...')}>
```

calling a function (incorrect)
```javascript
// This alert fires when the component renders, not when clicked!
<button onClick={handleClick()}>
<button onClick={alert('...')}>
```

# Angular

```javascript
<button type="button" (click)="deleteHero()">Delete hero</button>

<button type="button" (click)="onSave($event)">Save</button>
<button type="button" *ngFor="let hero of heroes" (click)="deleteHero(hero)">{{hero.name}}</button>
<form #heroForm (ngSubmit)="onSubmit(heroForm)"> ... </form>
```

# HTML

```javascript
<form>
  <input type="checkbox" id="myCheck" onClick="myFunction()">
</form>

<script>
function myFunction() {
  alert(1);
}
</script>
```
