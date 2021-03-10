# Clarity React Binding

This project an unofficial implementation of [VMware Clarity Design](https://clarity.design) in React. It leverages CSS, icons and images from the Clarity project. 

## Installation

#### Append to package.json
```package.json
"@dell/clarity-react": "https://github.com/EMCECS/clarity-react/archive/0.22.5.tar.gz"
```

### In your project directory
```bash
$ npm install @dell/clarity-react
$ cd node_modules/@dell/clarity-react && make && cd -
```
## Usage in React projects

Import styles and globals from peer dependencies:

#### `index.tsx`
```typescript
import "@webcomponents/custom-elements/custom-elements.min.js";
import "@clr/icons/clr-icons.min.css";
import "@clr/icons/clr-icons-lite.min.js";
import "@clr/ui/clr-ui.min.css"
import "@clr/icons/shapes/technology-shapes.js";

...
```

And make use of the components in your app:
#### `App.tsx`
```typescript jsx
import React, {Component} from 'react';
import MainContainer from "@dell/dist/clarity-react/layout/main-container/MainContainer";

const initialState = {
};

type MainPageProps = {
    token?: string
    level?: string
    message?: string
}

export type MainPageState = Readonly<typeof initialState>;

export default class MainPage extends Component<MainPageProps> {
    readonly state: MainPageState = initialState;

    render() {
        return(
            <MainContainer title="Title">
                Hello
            </MainContainer>
        );
    }
}
```

## Storybook

This project includes [Storybook](https://storybook.js.org/) as a component browser. To fire up storybook, download the project in Git:
```shell
$ git clone https://github.com/EMCECS/clarity-react.git
```

Install the dependencies with `yarn`, `npm`, etc.
```sbtshell
$ cd clarity-react

# Using yarn
$ yarn

# Using NPM
$ npm install
```

Any run the "storybook" script:
```shell
# Using yarn
$ yarn run storybook

# Using NPM
$ npm run storybook
```

## Licenses
* Clarity React components is licensed under Apache 2.0 License.
* The VMware Clarity Design System is licensed under the MIT license.
