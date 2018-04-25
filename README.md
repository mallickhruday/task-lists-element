# &lt;task-lists&gt; element

Drag and drop task list items.

## Installation

```
$ npm install --save @github/task-lists-element
```

## Usage

```js
import '@github/task-lists-element'
```

```html
<task-lists sortable>
  <ul class="contains-task-list">
    <li class="task-list-item">
      <input type="checkbox" class="task-list-item-checkbox">
      Hubot
    </li>
    <li class="task-list-item">
      <input type="checkbox" class="task-list-item-checkbox">
      Bender
    </li>
  </ul>

  <ul class="contains-task-list">
    <li class="task-list-item">
      <input type="checkbox" class="task-list-item-checkbox">
      BB-8
    </li>
    <li class="task-list-item">
      <input type="checkbox" class="task-list-item-checkbox">
      WALL-E
    </li>
  </ul>
</task-lists>
```

## Events

```js
const list = document.querySelector('task-lists')

list.addEventListener('task-lists:check', function(event) {
  const {position, checked} = event.detail
  console.log(position, checked)
})

list.addEventListener('task-lists:move', function(event) {
  const {src, dst} = event.detail
  console.log(src, dst)
})
```

## Browser support

- Chrome
- Firefox
- Safari 9+
- Internet Explorer 11
- Microsoft Edge

## Development

```
npm install
npm test
```

## License

Distributed under the MIT license. See LICENSE for details.
