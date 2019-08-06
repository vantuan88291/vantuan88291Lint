# vantuan88291lint

### Please install list packages following:
npm install:

` vantuan88291lint`

` eslint`

` eslint-plugin-jest`

` eslint-plugin-react`

` eslint-plugin-header`

` prop-types`

**After installed these packages:**

Create _.eslintrc.json_ at root project and paste this content following:

```
{
   "extends": [
     "./node_modules/vantuan88291lint/.eslintrc.json",
     "./node_modules/vantuan88291lint/.eslintrc-react.json"
   ],
   "settings": {
     "react": {
       "pragma": "React",
       "version": "16.5"
     }
   },
   "env": {
     "jest": true
   },
   "globals": {
     "__DEV__": true
   },
   "rules": {
     "global-require": 0,
     "react/display-name": [2, { "ignoreTranspilerName": false }],
     "react/jsx-filename-extension": [2, {"extensions": [".js"]}]
   },
   "overrides": [
     {
       "files": ["*.test.js", "*.test.jsx"],
       "env": {
         "jest": true
       }
     }
   ]
 }
```

**And add this line in _.editorConfig_** file following:

`[{package.json,.eslintrc.json}]`

**Result like this:**

```# EditorConfig is awesome: http://EditorConfig.org
 
 # top-most EditorConfig file
 root = true
 
 # Unix-style newlines with a newline ending every file
 [*]
 end_of_line = lf
 insert_final_newline = true
 indent_style = space
 indent_size = 2
 [{package.json,.eslintrc.json}]
 charset = utf-8
 trim_trailing_whitespace = true
 
 
 [*.gradle]
 indent_size = 4
```

On PHPStorm: Setting(Preferences on Macos) -> Languages & Framework -> JavaScript -> Code quality tools -> ESlint -> Disable and Enable again. 
