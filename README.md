## React Native Guides

Guidelines to create React Native applications in [GuavaPass](https://www.guavapass.com)

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
│   │  ├── components               # Shared React components
│   │
│   ├── routes
│   │   ├── index.js                # Main route definitions and async split points
│   │   │
│   │   ├── Home
│   │   │   ├── __tests__           # Unit tests
│   │   │   ├── images              # Images for the components
│   │   │   ├── index.js            # Redux container
│   │   │   ├── Header.js           # React component
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
│   ├── store                       # Redux store
│   │   ├── createStore.js          # Create and instrument redux store
│   │
│   └── libs                        # Libraries
│       ├── adapters                # Adapters for 3rd Party Modules
│       ├── helpers                 # Helper methods
│       ├── modules                 # 3rd Party Native Modules
│       └── I18n                    # Translations
│
├── index.ios.js                    # App entry points
└── index.android.js                # App entry points
```

This structure shares a lot of similarities and inspired by [React Redux Starter Kit](https://github.com/davezuko/react-redux-starter-kit)'s [Fractal Project Structure](https://github.com/davezuko/react-redux-starter-kit/wiki/Fractal-Project-Structure).
