#### Donatello Handout

# Learning Objectives
- Learn the history of React JS
- Learn how HTML and JavaScript combine within React
- Learn how to split the UI into independent, reusable pieces
- Learn how React renders elements
- Learn how the React DOM works
- Learn how state works in React
- Learn how to create a state object to store component values 
- Learn how to reuse stateful logic with hooks

# Cheatsheet

CREDIT FOR CHEAT SHEET: SheCodes (cheatsheets.shecodes.io/react) and W3Schools (https://www.w3schools.com/REACT/default.asp) 

##  JSX
### JSX Element
```
let element = <h1>Hello, world!</h1>;
let emptyHeading = <h1 />;
```

### JSX Expressions
```
let name = 'Josh Perez';
let element = <h1>Hello, {name}</h1>;

function fullName(firstName, lastName) {
  return firstName + ' ' + lastName;
}

let element = <h1>Hello, {fullName('Julie', 'Johnson')}</h1>
```

### JSX Attributes
```
const element = <img src={user.avatarUrl} />;
const element = <button className="btn">Click me</button>;
```

### JSX Functions
```
name() {
  return "Julie";
}

return (
  <h1>
    Hi {name()}!
  </h1>
)
```

### JSX Conditional Rendering
```
import React from "react";
export default function Weather(props) {
  if (props.temperature >= 20) {
    return (
      <p>
        It is {props.temperature}°C (Warm) in {props.city}
      </p>
    );
  } else {
    return (
      <p>
        It is {props.temperature}°C in {props.city}
      </p>
    );
  }
}
```

##  Components
### Functional component
```
import React from 'react';

export default function UserProfile() {
  return (
      <div className="UserProfile">
        <div>Hello</div>  
        <div>World</div>
      </div>
  );
}
```

### Embed an internal component
```
import React from 'react';
import UserAvatar from "./UserAvatar";

export default function UserProfile() {
  return (
      <div className="UserProfile">
        <UserAvatar />
        <UserAvatar />
      </div>
  );
}
```

### Embed an external component
```
import React from 'react';
import ComponentName from 'component-name';

export default function UserProfile() {
  return (
      <div className="UserProfile">
        <ComponentName />
      </div>
  );
}
```

### Advanced functional component
```
import React from "react";

export default function Hello(props) {
  function fullName() {
    return `${props.firstName} ${props.lastName}`;
  }
  return (
    <p>
      {fullName()}
    </p>
  );
}

<Hello firstName="Matt" lastName="Delac" />
```

##  Rendering/DOM
### Display a paragraph inside an element with the id of "root"
`ReactDOM.render(<p>Hello</p>, document.getElementById('root'));`

### Create a variable that contains HTML code and display it in the "root" node:
```
const myelement = (
  <table>
    <tr>
      <th>Name</th>
    </tr>
    <tr>
      <td>John</td>
    </tr>
    <tr>
      <td>Elsa</td>
    </tr>
  </table>
);

ReactDOM.render(myelement, document.getElementById('root'));
```

##  State
### React state
```
import React, { useState } from "react";

export default function Hello(props) {
  let [name, setName] = useState("Julie");
  function updateName() {
    let newName = prompt("What is your name?");
    setName(newName);
  }

  return (
    <h1>
      {name}
    </h1>
    <button onClick={updateName}>
      Update name
    </button>
  );
}
```

##  Properties
### Passing properties to a component
```
<Student firstName="Julie" lastName="Johnson" age={23} pro={true} />
```

### Accessing the properties from a component
```
import React from "react";

export default function Student(props) {
  return (
    <h1>
      {props.firstName} {props.lastName} is {props.age}.
    </h1>
  )
}
```

##  CSS
### CSS in a React Component
```
import React from "react";
import "./Student.css";

export default function Student() {
  return (
    <div className="Student">
      Julie Johnson
    </div>
  )
}
```

##  Events
### Event listener
```
import React from "react";

export default function Hello() {
  function handleClick(event) {
    event.preventDefault();
    alert("Hello World");
  }

  return (
    <a href="/" onClick={handleClick}>
      Say Hi
    </a>
  );
}
```

##  Forms
### React forms
```
import React, { useState } from "react";

export default function LoginForm() {
  let [username, setUsername] = useState("");
  let [password, setPassword] = useState("");

  function handleSubmit(event) {
    event.preventDefault();
    alert(`Loging in with ${username} and ${password}`);
  }

  function updateUsername(event) {
    setUsername(event.target.value);
  }

  function updatePassword(event) {
    setPassword(event.target.value);
  }

  return (
    <form onSubmit={handleSubmit}>
      <input type="text" placeholder="Username" onChange={updateUsername} />
      <input type="password" placeholder="Password" onChange={updatePassword} />
      <input type="submit" value="Login" />
    </form>
  );
}
```

##  Loops
### Looping through an array
```
let elements = ['one', 'two', 'three'];

return (
  <ul>
    {elements.map(function(value, index) {
      return <li key={index}>{value}</li>
    })}
  </ul>
);
```

### Looping through an array of objects
```
let elements = [{
    name: 'one',
    value: 1
  },
  {
    name: 'two',
    value: 2
  },
  {
    name: 'three',
    value: 3
  }
}]
return (
  <ul>
    {elements.map(function(element, index) {
      return <li key={index}>The value for {element.name} is {element.value}</li>
    })}
  </ul>
);
```



