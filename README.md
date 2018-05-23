# vue-status

Vue component for detecting the network status - online or offline


## Requirements

* Vue.js 2.x

## Installation

`yarn add vue-status`

or 

`npm install vue-status`

## Usage

To use it locally in your component

`import VueStatus from 'vue-status' ` 

```javascript
export default {
  components: {
      VueStatus
    }
}
```

```html
<vue-status>
    <h2 slot="online">You are online (Any online content can be put here)</h2>
    <h2 slot="offline">You are offline (Any Offline content can be put here)</h2>
 </vue-status>
```
