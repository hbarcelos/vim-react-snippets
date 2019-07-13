# Vim React Snippets

A Vim snippet library for React in ES6. You may also want to check out [vim-es2015-snippets](https://github.com/epilande/vim-es2015-snippets).

Requires [UltiSnips](https://github.com/SirVer/ultisnips).

![vim-react-snippets](https://i.imgur.com/y1wcKVy.gif)

## Installation

Using [vim-plug](https://github.com/junegunn/vim-plug):

```vim
" ES2015 code snippets (Optional)
Plug 'epilande/vim-es2015-snippets'

" React code snippets
Plug 'hbarcelos/vim-react-snippets'

" Ultisnips
Plug 'SirVer/ultisnips'
```

## Usage
In a JavaScript or JSX file, type a trigger name while in Insert mode, then press Ultisnips trigger key. In my case I have it mapped to `<C-c>`.

For example, let's say we have `ListItem.js`

In Insert mode

```javascript
rfc<C-c>
```

Will expand to

```javascript
import React from 'react';
import PropTypes from 'prop-types';

function ListItem({ ...props }) {
  return (
    <div>

    </div>
  );
}

ListItem.defaultProps = {
};

ListItem.propTypes = {
};

export default ListItem;
```

Check out [`UltiSnips/javascript.snippets`](UltiSnips/javascript.snippets) to see all snippets.


## Snippets

#### Skeleton

| Trigger  | Content |
| -------: | ------- |
| `rrcc→`  | React Redux Class Component |
| `rcc→`   | React Class Component |
| `rfc→`   | React Functional Component |
| `rsc→`   | React Styled Component |
| `rsci→`   | React Styled Component Interpolation |


#### Lifecycle

| Trigger  | Content |
| -------: | ------- |
| `cwm→`   | `componentWillMount() {...}` |
| `cdm→`   | `componentDidMount() {...}` |
| `cwrp→`  | `componentWillReceiveProps(nextProps) {...}` |
| `scup→`  | `shouldComponentUpdate(nextProps, nextState) {...}` |
| `cwup→`  | `componentWillUpdate(nextProps, nextState) {...}` |
| `cdup→`  | `componentDidUpdate(prevProps, prevState) {...}` |
| `cwu→`   | `componentWillUnmount() {...}` |
| `ren→`   | `render() {...}` |


#### PropTypes

| Trigger    | Content |
| -------:   | ------- |
| `pt→`      | `propTypes {...}` |
| `pt_a→`    | `PropTypes.array` |
| `pt_b→`    | `PropTypes.bool` |
| `pt_f→`    | `PropTypes.func` |
| `pt_n→`    | `PropTypes.number` |
| `pt_o→`    | `PropTypes.object` |
| `pt_s→`    | `PropTypes.string` |
| `pt_no→`   | `PropTypes.node` |
| `pt_e→`    | `PropTypes.element` |
| `pt_io→`   | `PropTypes.instanceOf` |
| `pt_one→`  | `PropTypes.oneOf` |
| `pt_onet→` | `PropTypes.oneOfType (Union)` |
| `pt_ao→`   | `PropTypes.arrayOf (Instances)` |
| `pt_oo→`   | `PropTypes.objectOf` |
| `pt_sh→`   | `PropTypes.shape` |
| `ir→`      | `isRequired` |

#### Others

| Trigger  | Content |
| -------: | ------- |
| `props→` | `this.props` |
| `state→` | `this.state` |
| `set→`   | `this.setState(...)` |
| `dp→`    | `defaultProps {...}` |
| `cn→`    | `className` |
| `ref→`   | `ref` |
| `pp→`    | `${props => props}` |

#### Hooks

| Trigger  | Content |
| -------: | ------- |
| `us_s→`  | `const [state, setState] = useState('');` |
| `us_e→`  | `useEffect(() => { });`                   |
| `us_er→` | `useEffect(() => { return () => {}; });`  |
| `us_c→`  | `const context = useContext(ctx);`        |
| `us_r→`  | `const [store, dispatch] = useReducer(storeReducer, initialState);` |
| `us_cb→` | `useCallback(() => {  }, []);` |
| `us_m→`  | `const memo = useMemo(() => {  }, []);` |
