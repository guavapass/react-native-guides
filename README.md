## React Native Guides

Guidelines to create React Native applications in [GuavaPass](https://www.guavapass.com)

### Project Structure

Our React Native application is structured as follow:

```
.
├── __mocks__                       # Testing mocks
├── __tests__                       # Top level tets
├── build                           # All build-related code
├── assets                          # Static public assets (not imported anywhere in source code)
├── src                             # Application source code
│   ├── config                      # Configuration files
│   │   ├── Settings.js
│   │   ├── Routes.js
│   │   └── Colors.js
│   │
│   ├── shared                      # Shared React components
│   ├── routes
│   │   ├── index.js                # Main route definitions and async split points
│   │   │
│   │   ├── Home                    # Fractal route
│   │   │   ├── __tests__           # Unit tests
│   │   │   ├── index.js            # Route definitions and async split points
│   │   │   ├── components.js       # React components
│   │   │   ├── actions.js          # Redux action creators
│   │   │   └── reducers.js         # Redux reducers
│   │   │
│   │   └── Lesson                  # Fractal route
│   │       ├── __tests__           # Unit tests
│   │       ├── index.js            # Route definitions and async split points
│   │       ├── components.js       # React components
│   │       ├── actions.js          # Redux action creators
│   │       └── reducers.js         # Redux reducers
│   │
│   ├── store                       # Redux-specific pieces
│   │   ├── createStore.js          # Create and instrument redux store
│   │   └── reducers.js             # Reducer registry and injection
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
