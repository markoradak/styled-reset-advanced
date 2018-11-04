# 💅 styled-reset-advanced

> Extended version of [reset.css](https://meyerweb.com/eric/tools/css/reset/) for
[styled-components](https://github.com/styled-components/styled-components) adding `border-box` reset,  
as well as additional link/button resets, font antialiasing, focused user-select, etc.

> Also see [styled-reset](https://github.com/zacanger/styled-reset)
from [Zac Anger](https://github.com/zacagner) and
[styled-normalize](https://www.npmjs.com/package/styled-normalize)
from [Sergey Sova](https://github.com/sergeysova).

--------

## Installation

With NPM: `npm i styled-reset-advanced` (use the `-S` flag if you're on npm 4 or earlier).  
With Yarn: `yarn add styled-reset-advanced`.

## Usage

```jsx
import React, { Fragment } from 'react';
import { createGlobalStyle } from 'styled-components';
import reset from 'styled-reset-advanced';

const GlobalStyle = createGlobalStyle`
  ${reset}
  /* other styles */
`;

const App = () => (
  <Fragment>
    <GlobalStyle />
    <div>Hi, I'm an app!</div>
  </Fragment>
);

export default App
```

If you're using Styled Components version 3.x or 2.x, you'll need to use the
`injectGlobal` api instead:

```jsx
import { injectGlobal } from 'styled-components';
import reset from 'styled-reset';
injectGlobal`
  ${reset}
`;
```

`reset` is also available as a named export:

```jsx
import { reset } from 'styled-reset-advanced';
```

## Credits

Credit goes to Eric Meyer for coming up with reset.css and Paul Irish for box model reset.  
Reset.css is public domain (unlicensed).

## License

Licensed under [MIT](./LICENSE.md) license.
