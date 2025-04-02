---

sidebar_label: 'Styling'
sidebar_position: 2

---

# Styling

```jsx
 CSS Modules
> import React from 'react';
> import styles from './sth.module.css';  
```

```jsx
import styles from './index.module.css';

const person = {
  name: 'Gregorio Y. Zara',
  theme: {
    backgroundColor: 'black',
    color: 'pink'
  }
};

export default function TodoList() {
  return (
    <div className={styles.flexBox}>>
      <h1>{person.name}'s Todo</h1>
      <img
        className="avatar"
        src="https://i.imgur.com/7vQD0fPs.jpg"
        alt="Gregorio Y. Zara"
      />
      <ul>
        <li>Improve the videophone</li>
        <li>Prepare aeronautics lectures</li>
        <li>Work on the alcohol-fuelled engine</li>
      </ul>
    </div>
  );
}

```
