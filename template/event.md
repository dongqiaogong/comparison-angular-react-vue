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
