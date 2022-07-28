# React-Native-Bottom-Action-Menu

# Introduction

This is an Example to make React Native Bottom Action Menu. To make Bottom Action Menu, we are going to use ActionSheet component from react-native-actionsheet library.

This can be mostly seen by the IOS developers as it looks like a default select option in IOS. With the help of Bottom Action Menu, you can provide the facility to select from multiple options.

# Demo 

![action_sheet](https://user-images.githubusercontent.com/86215353/181410408-5343dffc-7d52-4c8c-897d-0bdd93ebf2d1.gif)


# Installation
```

npm install react-native-actionsheet --save

```

# Example
```js

import React, { useRef } from 'react';
// import all the components we are going to use
import {
  SafeAreaView,
  StyleSheet,
  View,
  TouchableHighlight,
  Text,
} from 'react-native';

// import ActionSheet
import ActionSheet from 'react-native-actionsheet';

const App = () => {

  let actionSheet = useRef();
  var optionArray = ['Option 1', 'Option 2', 'Option 3', 'Option 4', 'Cancel'];

  const showActionSheet = () => {
    //To show the Bottom ActionSheet
    actionSheet.current.show();
  };

  return (
    <SafeAreaView style={styles.container}>
      <View style={styles.container}>
        <TouchableHighlight
          style={styles.buttonStyle}
          onPress={showActionSheet}>
          <Text style={styles.buttonTextStyle}>Open Buttom ActionSheet</Text>
        </TouchableHighlight>
        <ActionSheet
        useNativeDriver="true"
          ref={actionSheet}
          // Title of the Bottom Sheet
          title={'Which one do you like ?'}
          // Options Array to show in bottom sheet
          options={optionArray}
          // Define cancel button index in the option array
          // This will take the cancel option in bottom
          // and will highlight it
          cancelButtonIndex={4}
          // Highlight any specific option
          destructiveButtonIndex={1}
          onPress={(index) => {
            // Clicking on the option will give you alert
            alert(optionArray[index]);
          }}
        />
      </View>
    </SafeAreaView>
  );
};
export default App;

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignContent: 'center',
    textAlign: 'center',
    paddingTop: 30,
    backgroundColor: '#307ecc',
    padding: 16,
  },
  buttonStyle: {
    width: '100%',
    height: 40,
    padding: 10,
    backgroundColor: '#f5821f',
    marginTop: 30,
  },
  buttonTextStyle: {
    color: 'white',
    textAlign: 'center',
  },

});

```

# Tutorial

Coming Soon...
