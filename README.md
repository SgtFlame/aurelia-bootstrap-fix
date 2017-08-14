# Bootstrap 4 fix for Aurelia

Bootstrap 4 has a dependency on Tether, but it assumes Tether is set as window.Tether.

## Installation

```
npm install aurelia-bootstrap-fix --save
```
Add this dependency to aurelia.json.

```
          {
            "name": "aurelia-bootstrap-fix",
            "path": "../node_modules/aurelia-bootstrap-fix/dist/amd",
            "main": "aurelia-bootstrap-fix"
          },
```

And set this as a dependency to bootstrap.

```
{
          {
            "name": "bootstrap",
            "path": "../node_modules/bootstrap/dist",
            "main": "js/bootstrap",
            "deps": ["jquery", "tether", "aurelia-bootstrap-fix"],
            "exports": "$",
            "resources": [
              "css/bootstrap.css"
            ]
          }
```

## TODO

Need to create build scripts and target other loaders.

Hopefully this script won't be required long enough to warrant putting any more effort into it.
