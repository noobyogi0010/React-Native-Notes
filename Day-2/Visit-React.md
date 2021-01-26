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

You can also customize React Native's core components using props. Like you can customize ```image``` tag by passing object to ```style``` prop, you can pass object to ```source``` in order to pass the url of image file, and many others.

## States

States in React Native can be considered as local storage for components. Let's see it with an example, you have an empty bucket and your have to fill water in it. Here, empty bucket is your component, and capacity of bucket is your prop. Now, you can't keep filling the bucket forever. You have to stop at certain point, specifically when the bucket is full or half full.

In order to keep track of whether your bucket is filled completely or half, you will need someone/something to observe that. Here comes our saviour **sates**. You can create a state with the name ```isFull``` and set it to 0 initially. And keep increasing it with 1 for each 1 litre of water poured in it. This way when the value of ```isFull``` is equal to capacity of bucket we can say that bucket is filled completely and stop.

In order to use states in your code you'll require a variable to store the value. And a function that set's the state for that variable. Following is an example of **states** in our fish pond example:-

```
import React, { useState } from 'react';
import { View, Text, Button } from 'react-native';

const Fish = (props) => {
    const [isEaten, setIsEaten] = useState(false);

    return (
        <View>
            <Text>
                I see a { props.food }. I { isEaten? 'ate': 'will eat' } it.
            </Text>
            <Button
                onPress={() => {
                    setIsEaten(true);
                }}
                disabled={ isEaten }
                title={ isEaten: 'Thank you': 'Please help me eat it' }
            />
        </View>
    );
}

const Pond = () => {
    <View>
        <Fish food='bread crums'></Fish>
        <Fish food='grass'></Fish>
    </View>
};

export default Pond;
```

Here, ```useState``` is used to keep track of the data inside ```isEaten```. And ```setIsEaten``` is used to set/change the state of ```isEaten```.