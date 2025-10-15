# Repro of fingerprint issue

Using an icons object on expo.ios.icon results in this error: `CommandError: The "paths[1]" argument must be of type string. Received an instance of Object`

Produces error:
```
...
"icon": {
  "light": "./assets/images/icon.png",
  "dark": "./assets/images/icon.png",
   "tinted": "./assets/images/icon.png"
},
```

Works fine:
```
"icon": ./assets/images/icon.png",
```

Tested this using:
npx @expo/fingerprint fingerprint:generate

First became clear to me when I was going to build with EAS.
