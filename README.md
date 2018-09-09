# react-thailand-address-autocomplete
Autocomplete Thailand address input component for React.js

[Project's Github](https://github.com/winChawakorn/react-thailand-address-autocomplete)


<img src="https://raw.githubusercontent.com/winChawakorn/react-thailand-address-autocomplete/master/assets/react-thailand-address-autocomplete.gif" height="350px" />

## Insallation
**yarn**
```
yarn add react-thailand-address-autocomplete
```
**npm**
```
npm install --save react-thailand-address-autocomplete
```
## Basic Usage
```js
import InputAddress from 'react-thailand-address-autocomplete'
```
```js
  onChange(e) {
    this.setState({
      [e.target.name]: e.target.value
    })
  }

  onSelect(fullAddress) {
    const { subdistrict, district, province, zipcode } = fullAddress
    this.setState({
      subdistrict,
      district,
      province,
      zipcode
    })
  }

  render() {
    return (
      <div>
        แขวง / ตำบล
        <InputAddress
          address="subdistrict"
          value={this.state.subdistrict}
          onChange={this.onChange}
          onSelect={this.onSelect}
        />
        เขต / อำเภอ
        <InputAddress
          address="district"
          value={this.state.district}
          onChange={this.onChange}
          onSelect={this.onSelect}
        />
      </div>
    );
  }
```

## Props
**address: String**

- Type of input address, including `subdistrict`, `district`, `province`, and `zipcode`.

- Default value: `subdistrict`

**value: String**

- The input content value.

**onChange: Function**

- The callback function that is triggered when the input content is changed.

**onSelect: Function**

- The callback function that is triggered when an autocomplete suggestion item is selected.

**delimiter: String**

- The delimiter in autocomplete suggestion items that separate each part of address.

- Default value: `, `

**placeholder: String**

- Placeholder of the input.

**highlight: String**

- Highlight color of an autocomplete suggestion item when a cursor on.

- Default value: `#eee`

**unhighlight: String**

- Color of an autocomplete suggestion item when no cursor on.

- Default value: `white`

**style: Object**

- Inline style to apply to the input.

**renderStyle: Object**

- Inline style to apply to the box of autocomplete suggestion items.

## Original idea
[zapkub](https://github.com/zapkub/react-thailand-address-typeahead) and [earthchie](https://github.com/earthchie/jquery.Thailand.js)

## License
MIT
