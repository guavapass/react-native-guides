## React Native Guides

Guidelines to build React Native applications in [GuavaPass](https://www.guavapass.com).

### Project Structure

Our React Native application is structured as follow:

```
.
├── __mocks__                       # Testing mocks
├── __tests__                       # Top level tests
├── build                           # All build-related code
├── src                             # Application source code
│   ├── config                      # Configuration files
│   │   ├── settings.js
│   │   ├── routes.js
│   │   └── colors.js
│   │
│   ├── shared                      # Shared
│   │  ├── images                   # Shared images
│   │  │   └── activity_icons
│   │  │       └── yoga.png
│   │  │       └── hiit.png
│   │  └── components               # Shared React components
│   │
│   ├── routes
│   │   ├── index.js                # Route definitions
│   │   ├── Home
│   │   │   ├── __tests__           # Unit tests
│   │   │   ├── images              # Images for the components
│   │   │   │   └── header.png
│   │   │   ├── index.js            # Just import `HomeScreen.js`
│   │   │   ├── HomeScreen.js       # Redux container + layout
│   │   │   ├── Header.js           # React component
│   │   │   └── Tabs                # Huge component could be break into sub-components with its own directory
│   │   │   │    ├── ProfileTab.js   # React component
│   │   │   │    ├── NewsTab.js      # React component
│   │   │   │    └── index.js        # React component
│   │   │   ├── Tabs.js             # React component
│   │   │   ├── LogoutButton.js     # React component
│   │   │   ├── actions.js          # Redux action creators
│   │   │   └── reducers.js         # Redux reducers
│   │   │
│   │   └── Lesson
│   │       ├── __tests__           # Unit tests
│   │       ├── images              # Images for the components
│   │       ├── index.js            # Redux container
│   │       ├── Header.js           # React component
│   │       ├── actions.js          # Redux action creators
│   │       └── reducers.js         # Redux reducers
│   │
│   ├── actions                     # Actions for global store
│   │   └── membership.js           # Global actions
│   │    
│   ├── store                       # Redux store
│   │   ├── createStore.js          # Create and instrument redux store
│   │   └── membership.js           # Global store
│   │
│   └── libs                        # Libraries
│       ├── adapters                # Adapters for 3rd Party Modules
│       ├── helpers                 # Helper methods
│       ├── modules                 # 3rd Party Native Modules
│       └── I18n                    # Translations
│
├── index.ios.js                    # iOS entry point
└── index.android.js                # Android entry point
```

This structure shares a lot of similarities and inspired by [React Redux Starter Kit](https://github.com/davezuko/react-redux-starter-kit)'s [Fractal Project Structure](https://github.com/davezuko/react-redux-starter-kit/wiki/Fractal-Project-Structure).

### Naming of Files and Directories

1. Source Files (.js)

    It could be **upper/lower camel case**, depends on the `export default`.

    e.g.

    ```javascript
    //
    // SignUpButton.js
    //

    export default class SignUpButton extends React.Components {
      ...
    }

    //
    // createStore.js
    //

    export default class createStore {
      ...
    }
    ```

    If it doesn't have an export default, use **lower camel case**.

2. Directories

    Top level directories are fixed, which are single word in **lower case**.

    Any directory that contains React components use **upper camel case**.
