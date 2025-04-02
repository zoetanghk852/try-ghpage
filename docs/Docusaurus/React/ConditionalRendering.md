---

sidebar_label: 'Conditional rendering'
sidebar_position: 3

---
```jsx
# Conditional rendering

 Conditional operator ? , :

{isPacked ? name + ' ✔' : name}
```

```jsx
case 1
function Item({ name, isPacked }) {
  if (isPacked) {
    return <li className="item">{name} ✔</li>;
  }
  return <li className="item">{name}</li>;
}

case 2
//uncommon situations.
function Item({ name, isPacked }) {
  if (isPacked) {
    return null;
  }
  return <li className="item">{name}</li>;
}
```

```jsx
 Logical AND operator (&&)

* { isPacked && '✔' }
 *Don’t put numbers on the left side of &&.

❌  messageCount && New messages
✔ messageCount > 0 && New messages

```