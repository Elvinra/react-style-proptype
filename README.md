Validates style objects by ensuring the keys are valid css property names (in camelcase form).


```js
var stylePropType = require('react-style-proptype');

var Comp = React.createClass({
  propTypes: {
    myStyle: stylePropType,
  },
  render(){ ... }
});
```

You can use stylePropType.isRequired similar to the built in proptypes.

## Flow

We also expose a flow type definition. It doesn't use an 'exact' type definition due to a bug in flow, so it'll allow invalid properties. The main purpose of this type is to improve the editor experience for custom components that accept a style prop.

```jsx
import { type Style } from 'react-style-proptype/src/Style.flow.js';

type Props = {
  style: Style,
};
```

## Arrays

With react-native styles can be passed an array of objects. You can use this variant with
`stylePropTypes.supportingArrays`.

