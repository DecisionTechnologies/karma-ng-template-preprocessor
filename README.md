# karma-ng-template-script-to-template-cache-preprocessor

> Preprocessor for taking HTML files that have `<script type="ng/template"`> and putting them into the Angularjs Template Cache 
> Thanks to [karma-ng-html2js-preprocessor](https://github.com/karma-runner/karma-ng-html2js-preprocessor) for the idea and code snippets

## Installation

```bash
$ npm install karma-ng-template-preprocessor --save-dev
```

## Karma config
```js
module.exports = function(config) {
  config.set({
    preprocessors: {
      '**/*.html': ['ng-template'],
      '**/*.cshtml': ['ng-template']
    },

    files: [
      '**/*.html',
      '**/*.cshtml'
    ],

    // if you have defined plugins explicitly, add karma-ng-template-script-to-template-cache-preprocessor
    // plugins: ['karma-ng-template-preprocessor']

    ngTemplatePreprocessor: {
      //optional module name , templates by default
      //moduleName: 'specialTemplates'
    }
  })
}
```



## Using it in your tests
```js
  describe('example test', function(){
    beforeEach(module('templates'));    
  });
```

Used on the sites
[Broadbandchoices](https://www.broadbandchoices.co.uk) [Schlaubi] (https://www.schlaubi.de)

Interested in working at [Decision.tech](decision.tech/vacancies/) please visit our site for the latest vacancies.
