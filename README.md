[![npm][npm]][npm-url]
[![Github forks](https://img.shields.io/github/forks/Zimtir/svelte-item-list)]()
[![Github stars](https://img.shields.io/github/stars/Zimtir/svelte-item-list)]()
[![Github Downloads (total)](https://img.shields.io/github/downloads/Zimtir/svelte-item-list/total.svg)]()
[![GitHub Downloads (montly)](https://img.shields.io/github/downloads/Zimtir/svelte-item-list/latest/total.svg)]()
[![Github Issues](https://img.shields.io/github/issues/Zimtir/svelte-item-list)]()
[![Github license](https://img.shields.io/github/license/Zimtir/svelte-item-list)]()
[![Twitter](https://img.shields.io/twitter/url?url=https%3A%2F%2Fgithub.com%2FZimtir%2Fsvelte-item-list)]()

Svelte. Item list.

## Screenshot

![Screenshot](https://raw.githubusercontent.com/Zimtir/svelte-item-list/master/assets/example.png 'Screenshot')

## Install

```bash
npm install --save svelte-item-list
```

## Example

Look at the [example folder][example-folder-url] for a basic working example.

## Usage

```html
<!-- App.html -->
<ItemList
  needPag={true}
  endpoint={async () => {
    return [
      {
        name: 'Item name',
        icon: '/favicon.png',
        description: '',
        point: 100
      }
    ]
  }}>
  <div slot="loading">...loading</div>
</ItemList>

<script>
  import ItemList from 'svelte-item-list';
</script>
```

## Pagination was parsed and reconfigured from

https://github.com/TahaSh/svelte-paginate

## API

The item list component is the only export of the module.

```javascript
import ItemList from 'svelte-item-list'
```

###### Properties

| Property          | Default Value | Description                                               |
| :---------------- | :------------ | :-------------------------------------------------------- |
| `endpoint`        | undefined     | The endpoint function with return of values               |
| `nameProp`        | `name`        | The key of name property in the object by endpoint.       |
| `descProp`        | `description` | The key of description property in the object by endpoint |
| `pointProp`       | `point`       | The key of point property in the object by endpoint.      |
| `iconProp`        | `icon`        | The key of icon property in the object by endpoint.       |
| `lightProp`       | `light`       | The key of light property in the object by endpoint.      |
| `needPag`         | true          | Enable pagination under list of items or no               |
| `currentPage`     | 1             | Number of selected page by default at pagination          |
| `pageSize`        | 10            | Count of items at one page inside pagination              |
| `needIndex`       | true          | Enable or disable indexes at left of item                 |
| `boldIndex`       | 5             | Count of items with bold name                             |
| `needPoint`       | true          | Show point field                                          |
| `sortFunc`        | point - point | Function to sort list of items                            |
| `clickFunc`       | return        | Function to catch the click at item                       |
| `needIcon`        | true          | Show icon field                                           |
| `needTimeago`     | false         | Enable or disable format point field through timeago      |
| `isVisible`       | true          | (!IMPORTANT param) Enable or disable visibility of tool   |
| `endpointIsStore` | false         | Subscribe to endpoint when it provided as store           |
| `descIsHTML`      | false         | Make a description to html view                           |
| `limit`           | 1             | Make limited options for the numbers                      |
| `needBody`        | true          | Need display list by default view or use slot             |


[npm]: https://img.shields.io/npm/v/svelte-item-list.svg
[npm-url]: https://npmjs.com/package/svelte-item-list
[example-folder-url]: https://github.com/Zimtir/svelte-item-list/tree/master/example
