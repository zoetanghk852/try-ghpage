---

sidebar_label: 'Rendering Lists'
sidebar_position: 4

---

# Rendering List

Arrow functions have implicitly(隱含地) return the expression right after =>, so we didn’t need a `return (=>)` statement right after.

However, if `(=>)` is followed by a `{`  curly brace ,**return** statement should be written

```jsx
- map()

const listItems = people.map(person =>
    <li key={person.id}>
      <img
        src={getImageUrl(person)}
        alt={person.name}
      />
    </li>
  );
```

```jsx
- filter()

const chemists = people.filter(person =>
    person.profession === 'chemist'
  );
```
