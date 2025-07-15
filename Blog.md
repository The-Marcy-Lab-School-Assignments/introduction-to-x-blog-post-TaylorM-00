Intro to React Native

By Taylor Marshall

## Introduction

- Hello and Welcome to an introduction of React Native. This article will be going over the fundamentals of react native and I will sharing the basics of React Native needed to create a skeleton that can be used for the development of any app.

If you are looking to learn React Native, then it is highly encouraged that you learn React in advanced since the two have similar syntax and user interface softwares. React and React Native should not be used or mistaken for the one another. The main difference between the two is React is used to build applications that utilize a web browser, while React Native is used to build mobile applications that run on both IOS and Android Devices.

<!-- what is it build on, are you a react native app, when and how to use, if you know react this is good to know,  -->

## Environment Setup / Expo Setup

- In order to properly start we must make sure when have all the flowing (applications) are downloaded and up to date.

- 1 is Visual Studio Code or VS Code for short.
  VS Code is a free code editor that was designed to help users create web or cloud applications. This platform is also compatible with a variety of programming languages.
  -> https://code.visualstudio.com/ (link to download vs code)

  - 2 Node.JS install
    Node.js is a cross-platform JavaScript runtime environment. This will allow users to have access to the JavaScript libraries, this gives users access to method, functions, and objects for common programming task. As well as helps users simplify and accelerate the web development process.
    -> https://nodejs.org/en (link to download node.js)

- 3 Download Expo
  Expo is a framework that is available to download on ios and android devices. What this means is that instead of using a sim

## Core Components

- In this section we will be going over the syntax of some of the core components in React Native. These components are the most basic functions needed for a proper mobile app. React Native has built in components that you can quickly set up in an application.

## View

- View, a fundamental building block for User Interface. View is a container component comparable to <div> tag in HTML.
  Its important to know that <View> doesn't display any content on it own. This component is meant to support the layout with Flexbox, Styles, and Touch and accessibility

  ## Text

  - The <Text> component is used for displaying text on the user screen. <Text> is comparable to the <p> tag in HTML. This component also supports actions like nesting, styling and touch handling. Nesting means that you are able to put a <Text> inside another <Text>. Styling with <Text> users are able to change things like font size, color, text alignment, and more. Lastly touch handling means that the <Text> can detect and respond to user touches, and example of this are taps and clicks.

  <!-- Example for both View and Text component -->

  ```js
  import { View, Text } from "react-native";

  export default function App() {
    return (
      <View>
        <Text> This is an example on how view can be used </Text>
      </View>
    );
  }
  ```

  ## TextInput

  - The <TextInput> not to be confused with <Text> is another fundamental component that is used to input text into an app with a keyboard. Properties that are used with <TextInput> are value, onChangeText, and placeholder. The value property is used to display text inside of the input box. When using the onChangeText property it uses a function that gets called when users type or edit. This allows for automatic updates of a new text. Lastly the placeholder property allows for a hint text to appears inside the input when its empty. Its helpful to know that this will disappear when users type, if there is no value added.

  ```js
  import React from "react";
  import { View, Text, TextInput } from "react-native";
  const [text, onChangeText] = useState("");

  export default function App() {
    return (
      <View>
        <Text> Enter you Name </Text>
        <TextInput
          placeholder="Enter Name"
          value={text}
          onChangeText={onChangeText}
        />
      </View>
    );
  }
  ```

  ## ScrollView

  - The <ScrollView> component helps users display content thats bigger than the screen, and allows users scroll either vertically or horizontally. A limitation of this is that if you plan to have extra long list of items display on the screen, this will lead to slow rendering and an increase of memory usage. To help with this users are encouraged to use <FlatList>. <FlatList> renders items "lazily", which means items will only render when they are about to appear, and are removed when they are scrolled off screen. This helps to save memory and cuts down the processing time. It is also important to note that the items in <ScrollView> will not render unless given a bounded height. What this means is that users have to define the maximum height that its allowed to occupy.

  ```js
  import React from "react";
  import { View, ScrollView, Text, StyleSheet } from "react-native";
   export default function App() {
    return (
      <View style={{ flex: 1}}>
      <ScrollView contentContainerStyle={styles.content}>
        {Array.from({ length: 30}).map((_, i) => (
          <Text key={i} style={styles.item}> Item {i+1}</Text>
        ))}
      </ScrollView>
      </View>

    )
  }

  const styles = StyleSheet.create({
    content: {
      padding: 20,
    }
    item: {
      marginVertical: 10,
      fontSize: 18,
    }
  })
  ```

## Button

- The <Button> component is a built-in function in React Native, this method is also the simplest way to add a clickable button for any app. Users can add advance styling and interactions by using features like <TouchableOpacity> and <Pressable>.
  <TouchableOpacity> allows users to make any element on a page pressable.
  <Pressable> allows users to detect touch interactions and customize the feedback for presses.

```js
import React from 'react'
import {View, Button} from 'react-native';

export default function App() {
  return(
<View style={{flex: 1, justifyContent: 'center', alignItems: 'center'}}>
<Button title="Press Me" onPress={() => alert('Button pressed!')}>
</View>
  )
}

```
