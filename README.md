## react-native-element-dropdown
A React Native dropdown component easy to customize for both iOS and Android.

## Features
* Dropdown and Multiselect in one package
* Easy to use
* Consistent look and feel on iOS and Android
* Customizable font size, colors and animation duration
* Implemented with typescript

## Getting started
```js
    npm install react-native-element-dropdown --save
```
or

```js
    yarn add react-native-element-dropdown
```

### RN Version < 0.60
```js
    react-native link react-native-element-dropdown
```
### Run IOS
```js
    pod install
    react-native run-ios
```
### Run Android
```js
    react-native run-android
```


#### Source code demo
[react-native-template-components](https://github.com/hoaphantn7604/react-native-template-components) A beautiful template for React Native.
#### Demo
![](https://github.com/hoaphantn7604/file-upload/blob/master/document/dropdown/demo.gif)

#### Dropdown Props
| Props              | Params                                          | isRequire | Description                                                         |
| ------------------ | ----------------------------------------------- | --------- | ------------------------------------------------------------------- |
| data               | Array                                           | Yes       | Data is a plain array                                               |
| labelField         | String                                          | Yes       | Extract the label from the data item                                |
| valueField         | String                                          | Yes       | Extract the primary key from the data item                          |
| onChange           | (item) => void                                  | Yes       | Selection callback                                                  |
| value              | Item                                            | No        | Selected value                                                      |
| placeholder        | String                                          | No        | The string that will be rendered before dropdown has been selected  |
| placeholderStyle   | TextStyle                                       | No        | Styling for text placeholder                                        |
| selectedTextStyle  | TextStyle                                       | No        | Styling for selected text                                           |
| selectedTextProps  | TextProps                                       | No        | Text Props for selected text. Ex: numberOfLines={1}                 |
| style              | ViewStyle                                       | No        | Styling for container view                                          |
| containerStyle     | ViewStyle                                       | No        | Styling for container list                                          |
| maxHeight          | Number                                          | No        | Customize height for container list                                 |
| fontFamily         | String                                          | No        | Customize font style                                                |
| iconColor          | String                                          | No        | Color of icons                                                      |
| activeColor        | String                                          | No        | Background color for item selected in container list                |
| search             | Boolean                                         | No        | Show or hide input search                                           |
| inputSearchStyle   | ViewStyle                                       | No        | Styling for input search                                            |
| searchPlaceholder  | String                                          | No        | The string that will be rendered before text input has been entered |
| renderInputSearch  | (onSearch: (text:string) => void) => JSX.Element| No        | Customize TextInput search                                          |
| disable            | Boolean                                         | No        | Specifies the disabled state of the Dropdown                        |
| dropdownPosition   | 'auto' or 'top' or 'bottom'                     | No        | Dropdown list position. Default is 'auto'                           |
| autoScroll         | Boolean                                         | No        | Auto scroll to index item selected, default is true                 |
| showsVerticalScrollIndicator | Boolean                               | No        | When true, shows a vertical scroll indicator, default is true       |
| renderLeftIcon     | () => JSX.Element                               | No        | Customize left icon for dropdown                                    |
| renderRightIcon    | () => JSX.Element                               | No        | Customize right icon for dropdown                                   |
| renderItem         | (item) => JSX.Element                           | No        | Takes an item from data and renders it into the list                |
| onFocus            | () => void                                      | No        | Callback that is called when the dropdown is focused                |
| onBlur             | () => void                                      | No        | Callback that is called when the dropdown is blurred                | 


#### MultiSelect Props
| Props              | Params                                               | isRequire | Description                                                         |
| ------------------ | -----------------------------------------------------| --------- | ------------------------------------------------------------------- |
| data               | Array                                                | Yes       | Data is a plain array                                               |
| labelField         | String                                               | Yes       | Extract the label from the data item                                |
| valueField         | String                                               | Yes       | Extract the primary key from the data item                          |
| onChange           | (value[]) => void                                    | Yes       | Selection callback                                                  |
| value              | Item[]                                               | No        | Selected value                                                      |
| placeholder        | String                                               | No        | The string that will be rendered before dropdown has been selected  |
| placeholderStyle   | TextStyle                                            | No        | Styling for text placeholder                                        |
| style              | ViewStyle                                            | No        | Styling for container view                                          |
| containerStyle     | ViewStyle                                            | No        | Styling for container list                                          |
| maxHeight          | Number                                               | No        | Customize height for container list                                 |
| fontFamily         | String                                               | No        | Customize font style                                                |
| iconColor          | String                                               | No        | Color of icons                                                      |
| activeColor        | String                                               | No        | Background color for item selected in container list                |
| selectedStyle      | ViewStyle                                            | No        | Styling for selected view                                           |
| selectedTextStyle  | TextStyle                                            | No        | Styling for selected text                                           |
| renderSelectedItem | (item, unSelect?: (item) => void) => JSX.Element     | No        | Takes an item from data and renders it into the list selected       |
| search             | Boolean                                              | No        | Show or hide input search                                           |
| inputSearchStyle   | ViewStyle                                            | No        | Styling for input search                                            |
| searchPlaceholder  | String                                               | No        | The string that will be rendered before text input has been entered |
| renderInputSearch  | (onSearch: (text:string) => void) => JSX.Element     | No        | Customize TextInput search                                          |
| disable            | Boolean                                              | No        | Specifies the disabled state of the Dropdown                        |
| dropdownPosition   | 'auto' or 'top' or 'bottom'                          | No        | Dropdown list position. Default is 'auto'                           |
| showsVerticalScrollIndicator | Boolean                                    | No        | When true, shows a vertical scroll indicator, default is true       |
| renderLeftIcon     | () => JSX.Element                                    | No        | Customize left icon for dropdown                                    |
| renderRightIcon    | () => JSX.Element                                    | No        | Customize right icon for dropdown                                   |
| renderItem         | (item) => JSX.Element                                | No        | Takes an item from data and renders it into the list                |
| onFocus            | () => void                                           | No        | Callback that is called when the dropdown is focused                |
| onBlur             | () => void                                           | No        | Callback that is called when the dropdown is blurred                |


#### SelectCountry extends Dropdown 
| Props              | Params               | isRequire | Description                          |
| ------------------ | -------------------- | --------- | ------------------------------------ |
| imageField         | String               | Yes       | Extract the image from the data item |
| imageStyle         | ImageStyle           | No        | Styling for image                    |


### Dropdown exmaple 1
![](https://github.com/hoaphantn7604/file-upload/blob/master/document/dropdown/example1.png)
```javascript
  import React, { useState } from 'react';
  import { StyleSheet } from 'react-native';
  import { Dropdown } from 'react-native-element-dropdown';
  import AntDesign from 'react-native-vector-icons/AntDesign';

  const data = [
    { label: 'Item 1', value: '1' },
    { label: 'Item 2', value: '2' },
    { label: 'Item 3', value: '3' },
    { label: 'Item 4', value: '4' },
    { label: 'Item 5', value: '5' },
    { label: 'Item 6', value: '6' },
    { label: 'Item 7', value: '7' },
    { label: 'Item 8', value: '8' },
  ];

  const DropdownComponent = () => {
    const [value, setValue] = useState(null);

    return (
      <Dropdown
        style={styles.dropdown}
        data={data}
        search
        labelField="label"
        valueField="value"
        placeholder="Select item"
        searchPlaceholder="Search..."
        value={value}
        onChange={item => {
          setValue(item.value);
        }}
        renderLeftIcon={() => (
          <AntDesign style={styles.icon} color="black" name="Safety" size={20} />
        )}
      />
    );
  };

  export default DropdownComponent;

  const styles = StyleSheet.create({
    dropdown: {
      height: 50,
      borderBottomColor: 'gray',
      borderBottomWidth: 0.5,
      margin: 20,
    },
    icon: {
      marginRight: 5,
    },
  });
```

### Dropdown exmaple 2
![](https://github.com/hoaphantn7604/file-upload/blob/master/document/dropdown/example2.png)
```javascript
  import React, { useState } from 'react';
  import { StyleSheet, View, Text } from 'react-native';
  import { Dropdown } from 'react-native-element-dropdown';
  import AntDesign from 'react-native-vector-icons/AntDesign';

  const data = [
    { label: 'Item 1', value: '1' },
    { label: 'Item 2', value: '2' },
    { label: 'Item 3', value: '3' },
    { label: 'Item 4', value: '4' },
    { label: 'Item 5', value: '5' },
    { label: 'Item 6', value: '6' },
    { label: 'Item 7', value: '7' },
    { label: 'Item 8', value: '8' },
  ];

  const DropdownComponent = () => {
    const [value, setValue] = useState(null);

    const renderItem = (item: any) => {
      return (
        <View style={styles.item}>
          <Text style={styles.textItem}>{item.label}</Text>
          {item.value === value && (
            <AntDesign
              style={styles.icon}
              color="black"
              name="Safety"
              size={20}
            />
          )}
        </View>
      );
    };

    return (
      <Dropdown
        style={styles.dropdown}
        data={data}
        search
        labelField="label"
        valueField="value"
        placeholder="Select item"
        searchPlaceholder="Search..."
        value={value}
        onChange={item => {
          setValue(item.value);
        }}
        renderLeftIcon={() => (
          <AntDesign style={styles.icon} color="black" name="Safety" size={20} />
        )}
        renderItem={renderItem}
      />
    );
  };

  export default DropdownComponent;

  const styles = StyleSheet.create({
    dropdown: {
      height: 50,
      margin: 20,
      backgroundColor: 'white',
      borderRadius: 12,
      padding: 12,
      shadowColor: '#000',
      shadowOffset: {
        width: 0,
        height: 1,
      },
      shadowOpacity: 0.2,
      shadowRadius: 1.41,

      elevation: 2,
    },
    icon: {
      marginRight: 5,
    },
    item: {
      padding: 17,
      flexDirection: 'row',
      justifyContent: 'space-between',
      alignItems: 'center',
    },
    textItem: {
      flex: 1,
      fontSize: 16,
    },
  });
```

### MultiSelect example 1
![](https://github.com/hoaphantn7604/file-upload/blob/master/document/dropdown/example3.png)
```js
  import React, { useState } from 'react';
  import { StyleSheet, View } from 'react-native';
  import { MultiSelect } from 'react-native-element-dropdown';
  import AntDesign from 'react-native-vector-icons/AntDesign';

  const data = [
    { label: 'Item 1', value: '1' },
    { label: 'Item 2', value: '2' },
    { label: 'Item 3', value: '3' },
    { label: 'Item 4', value: '4' },
    { label: 'Item 5', value: '5' },
    { label: 'Item 6', value: '6' },
    { label: 'Item 7', value: '7' },
    { label: 'Item 8', value: '8' },
  ];

  const MultiSelectComponent = () => {
    const [selected, setSelected] = useState([]);

    return (
      <View style={styles.container}>
        <MultiSelect
          style={styles.dropdown}
          data={data}
          labelField="label"
          valueField="value"
          placeholder="Select item"
          value={selected}
          onChange={item => {
            setSelected(item);
          }}
          renderLeftIcon={() => (
            <AntDesign
              style={styles.icon}
              color="black"
              name="Safety"
              size={20}
            />
          )}
          selectedStyle={styles.selectedStyle}
        />
      </View>
    );
  };

  export default MultiSelectComponent;

  const styles = StyleSheet.create({
    container: { margin: 16 },
    dropdown: {
      height: 50,
      backgroundColor: 'transparent',
      borderBottomColor: 'gray',
      borderBottomWidth: 0.5,
    },
    icon: {
      marginRight: 5,
    },
    selectedStyle: {
      borderRadius: 14,
    },
  });
```

### MultiSelect example 2
![](https://github.com/hoaphantn7604/file-upload/blob/master/document/dropdown/example4.png)
```js
  import React, { useState } from 'react';
  import { StyleSheet, View, TouchableOpacity, Text } from 'react-native';
  import { MultiSelect } from 'react-native-element-dropdown';
  import AntDesign from 'react-native-vector-icons/AntDesign';

  const data = [
    { label: 'Item 1', value: '1' },
    { label: 'Item 2', value: '2' },
    { label: 'Item 3', value: '3' },
    { label: 'Item 4', value: '4' },
    { label: 'Item 5', value: '5' },
    { label: 'Item 6', value: '6' },
    { label: 'Item 7', value: '7' },
    { label: 'Item 8', value: '8' },
  ];

  const MultiSelectComponent = () => {
    const [selected, setSelected] = useState([]);

    const renderItem = (item: any) => {
      return (
        <View style={styles.item}>
          <Text style={styles.textItem}>{item.label}</Text>
          <AntDesign style={styles.icon} color="black" name="Safety" size={20} />
        </View>
      );
    };

    return (
      <View style={styles.container}>
        <MultiSelect
          style={styles.dropdown}
          data={data}
          labelField="label"
          valueField="value"
          placeholder="Select item"
          value={selected}
          onChange={item => {
            setSelected(item);
          }}
          renderLeftIcon={() => (
            <AntDesign
              style={styles.icon}
              color="black"
              name="Safety"
              size={20}
            />
          )}
          renderItem={renderItem}
          renderSelectedItem={(item, unSelect) => (
            <TouchableOpacity onPress={() => unSelect && unSelect(item)}>
              <View style={styles.selectedStyle}>
                <Text style={styles.textSelectedStyle}>{item.label}</Text>
                <AntDesign color="black" name="delete" size={17} />
              </View>
            </TouchableOpacity>
          )}
        />
      </View>
    );
  };

  export default MultiSelectComponent;

  const styles = StyleSheet.create({
    container: { margin: 16 },
    dropdown: {
      height: 50,
      backgroundColor: 'white',
      borderRadius: 12,
      padding: 12,
      shadowColor: '#000',
      shadowOffset: {
        width: 0,
        height: 1,
      },
      shadowOpacity: 0.2,
      shadowRadius: 1.41,

      elevation: 2,
    },
    icon: {
      marginRight: 5,
    },
    item: {
      padding: 17,
      flexDirection: 'row',
      justifyContent: 'space-between',
      alignItems: 'center',
    },
    textItem: {
      flex: 1,
      fontSize: 16,
    },
    selectedStyle: {
      flexDirection: 'row',
      justifyContent: 'center',
      alignItems: 'center',
      borderRadius: 14,
      backgroundColor: 'white',
      shadowColor: '#000',
      marginTop: 8,
      marginRight: 12,
      paddingHorizontal: 12,
      paddingVertical: 8,
      shadowOffset: {
        width: 0,
        height: 1,
      },
      shadowOpacity: 0.2,
      shadowRadius: 1.41,

      elevation: 2,
    },
    textSelectedStyle: {
      marginRight: 5,
    },
  });
```