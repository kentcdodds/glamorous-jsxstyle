# jsxstyle Components

This package exports jsxstyle components generated with [`glamorous`](https://github.com/paypal/glamorous/)

# Install

Install with `npm`:

`npm install --save glamorous-jsxstyle`

This also has peer dependencies of `react` and `glamor`, so install those too:

`npm install --save react glamor`


You can then use one of the module formats:

* `main`: dist/glamorous-jsxstyle.cjs.js - exports itself as a CommonJS module
* `global`: dist/glamorous-jsxstyle.umd.js - exports itself as a `umd` module.
* `jsnext:main` and `module`: dist/glamorous-jsxstyle.es.js - exports itself using the ES modules specification, you'll need to configure `webpack` to make use of this file.

# Usage

To use this module via CommonJS:

```js
const { View } = require('glamorous-jsxstyle')
```

If you're transpiling (and/or using the `jsnext:main`):

```js
import { Flex, Block } from 'glamorous-jsxstyle'
```

An example use case

```js
import React  from 'react'
import { Flex, InlineBlock } from 'glamorous-jsxstyle'

export default class Example extends React.Component {
  render() {
    return (
      <div>
        <Flex>
          Content in a `div` with `display: 'flex'`
        </Flex>

        <InlineBlock>
          Content in a `div` with `display: 'inline-block'`
        </InlineBlock>

        // add more styles as you like
        <InlineBlock style={{color: 'blue'}}>
          Blue content in a `div` with `display: 'inline-block'`
        </InlineBlock>
      </div>
    )
  }
}

```

---

© 2017 Paul Molluzzo

MIT
