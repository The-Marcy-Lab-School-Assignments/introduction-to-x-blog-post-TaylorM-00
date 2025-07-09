Intro to React Native

By Taylor Marshall

## Introduction

- Hello and Welcome to the Introduction of React Native. This article will be going over the fundamentals of react native and will share with readers the basic need to create a skeleton for any type of app development.

( Compare & Contrast ) - If you are looking into React Native, then I'm and going to strongly assume that you have heard of React.JS. While these have similar syntax and user Interface softwares. One should not be used or mistaken for the other. The main difference between the two is React.JS is used to build application that utilize a web browser, while React Native is used to build applications that run on both IOS and Android Devices.

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

image , , button , , combining

- In this section we will be going over the core components in React Native. These components are the most basic functions needed for a proper mobile app.

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

## Button

## Image

## Styling Components

## Navigation

## Conclusion & Tips to Learn
