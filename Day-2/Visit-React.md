# Re-Visit React

It is necessary to re-visit or have some basic understanding of React when you are starting with React Native. As all the React Native components utilizes React components in order to create views for native platforms.

Let's consider a simple Fish component:

```
import React from 'react';
import { Text } from 'react-native';

const Fish = () => {
    return (
        <Text>Hello, I am a fish!</Text>
    );
}

export default Fish;
```

Let's break down this simple code. First, we ``` import ``` React and React Native's ```Text``` component. Second, we created a function Fish which returns a text "Hello, I am a fish!". Now, notice the return statement of the function. We have written HTML inside our JS code. This is known as **JSX**.

## JSX

JSX stands for JavaScript XML. It is used to write HTML code inside JS. It is mostly used by React and React Native. 

In our above example, the return statement is a JSX. We can write any JS expression inside JSX by using ```{ JS_expression } ```.

As JSX is included in React library, so you won't be able to use it in React Native until and unless you import React.

## Custom Components

We learnt about core components of React Native in introduction. So, custom components are simply a combination of these core components put together in different manners to create some new component. Each of these components can be reused whenever required by using their name inside angle brackets. For example, we can use Fish component as ```<Fish />``` in any other component. 

A component containing another component inside it is known as parent component. And the inner component is known as child component.

We can customize our custom component using props in different components as per our requirement.

## Props

In React and React Native, properties are called props. We can pass different values to props and customize our components. For example, we can pass different Fish name to our Fish component as follows:-

```
import React from 'react';
import { Text, View } from 'react-native';

const Fish = ( props ) => {
    return (
        "Hello, I am { props.name }."
    );
}

const Pond = () => {
    reutrn (
        <View>
            <Fist name="Nemo" />
            <Fist name="Baiely" />
            <Fist name="Terrisa" />
        </View>
    );
}

export default Pond;
```

You can also customize React Native's core components using props. Like you can customize ```Image``` tag by passing object to ```style``` prop, you can pass object to ```source``` in order to pass the url of image file, and many others.

