## Angular snippets for Sublime Text
some snippet for sublime
## Installation
- Package Control : install package 'Angular snippets FN'
- Manual: download the zip file and decompression in the package directory

## Snippets
**ngctrl**
```javascript
(function(){
    var module, moduleName = '${1: ngModule}',
        ctrlName = '${2: controllerName}';
    try{
        module = angular.module(moduleName, []);
    }catch(e){
        module = angular.module(moduleName)
    }

    module.controller(ctrlName, ${2: controllerName});

    function ${2: controllerName}{
        ${3:}
    }

})();
```
**ngdirect**
```javascript
(function(){
    var module, moduleName = '${1: ngModule}',
        factoryName = '${2: directiveName}';
    try{
        module = angular.module(moduleName, []);
    }catch(e){
        module = angular.module(moduleName)
    }
    
    module.directive(factoryName, ${2: directiveName});

    function ${2: directiveName}{
        ${3:}
    }

})();
```
**ngfac**
```javascript
(function(){
    var module, moduleName = '${1: ngModule}',
        factoryName = '${2: factoryName}';
    try{
        module = angular.module(moduleName, []);
    }catch(e){
        module = angular.module(moduleName)
    }
    
    module.factory(factoryName, ${2: factoryName});

    function ${2: factoryName}{
        ${3:}
    }

})();
```
