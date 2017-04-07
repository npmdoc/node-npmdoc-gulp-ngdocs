# api documentation for  [gulp-ngdocs (v0.3.0)](https://github.com/nikhilmodak/gulp-ngdocs#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-gulp-ngdocs.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-gulp-ngdocs) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-gulp-ngdocs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-gulp-ngdocs)
#### gulp plugin for angularjs documentation

[![NPM](https://nodei.co/npm/gulp-ngdocs.png?downloads=true)](https://www.npmjs.com/package/gulp-ngdocs)

[![apidoc](https://npmdoc.github.io/node-npmdoc-gulp-ngdocs/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-gulp-ngdocs_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-gulp-ngdocs/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-gulp-ngdocs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-gulp-ngdocs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "nikhilmodak"
    },
    "bugs": {
        "url": "https://github.com/nikhilmodak/gulp-ngdocs/issues"
    },
    "dependencies": {
        "angular": "~1.3.1",
        "angular-animate": "~1.3.1",
        "canonical-path": "0.0.2",
        "extend": "1.3.0",
        "gulp-util": "3.0.0",
        "lodash": "2.4.1",
        "marked": "0.3.2",
        "merge-stream": "0.1.5",
        "path": "0.4.9",
        "string_decoder": "0.10.31",
        "through2": "0.6.1",
        "vinyl-fs": "0.3.7"
    },
    "description": "gulp plugin for angularjs documentation",
    "devDependencies": {
        "del": "^1.1.1",
        "gulp": "^3.8.10",
        "jasmine-node": "^1.14.5"
    },
    "directories": {},
    "dist": {
        "shasum": "27b67a425eb3875226345ab89604d737f6357c21",
        "tarball": "https://registry.npmjs.org/gulp-ngdocs/-/gulp-ngdocs-0.3.0.tgz"
    },
    "gitHead": "e2e67c2e7812f1d2653e95d9f5af63ef551b212d",
    "homepage": "https://github.com/nikhilmodak/gulp-ngdocs#readme",
    "keywords": [
        "gulpplugin",
        "angular",
        "gulp",
        "ngdocs",
        "documention"
    ],
    "license": "MIT",
    "main": "index",
    "maintainers": [
        {
            "name": "nikhilmodak",
            "email": "nikhil.modak@gmail.com"
        },
        {
            "name": "andyperlitch",
            "email": "andyperlitch@gmail.com"
        }
    ],
    "name": "gulp-ngdocs",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/nikhilmodak/gulp-ngdocs.git"
    },
    "scripts": {
        "test": "jasmine-node --color spec"
    },
    "version": "0.3.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module gulp-ngdocs](#apidoc.module.gulp-ngdocs)
1.  [function <span class="apidocSignatureSpan">gulp-ngdocs.</span>process (opts)](#apidoc.element.gulp-ngdocs.process)
1.  [function <span class="apidocSignatureSpan">gulp-ngdocs.</span>sections (sects)](#apidoc.element.gulp-ngdocs.sections)
1.  object <span class="apidocSignatureSpan">gulp-ngdocs.</span>dom
1.  object <span class="apidocSignatureSpan">gulp-ngdocs.</span>ngdoc
1.  object <span class="apidocSignatureSpan">gulp-ngdocs.</span>reader

#### [module gulp-ngdocs.dom](#apidoc.module.gulp-ngdocs.dom)
1.  [function <span class="apidocSignatureSpan">gulp-ngdocs.dom.</span>DOM ()](#apidoc.element.gulp-ngdocs.dom.DOM)
1.  [function <span class="apidocSignatureSpan">gulp-ngdocs.dom.</span>htmlEscape (text)](#apidoc.element.gulp-ngdocs.dom.htmlEscape)
1.  [function <span class="apidocSignatureSpan">gulp-ngdocs.dom.</span>normalizeHeaderToId (header)](#apidoc.element.gulp-ngdocs.dom.normalizeHeaderToId)

#### [module gulp-ngdocs.ngdoc](#apidoc.module.gulp-ngdocs.ngdoc)
1.  [function <span class="apidocSignatureSpan">gulp-ngdocs.ngdoc.</span>Doc (text, file, line, options)](#apidoc.element.gulp-ngdocs.ngdoc.Doc)
1.  [function <span class="apidocSignatureSpan">gulp-ngdocs.ngdoc.</span>checkBrokenLinks (docs, apis, options)](#apidoc.element.gulp-ngdocs.ngdoc.checkBrokenLinks)
1.  [function <span class="apidocSignatureSpan">gulp-ngdocs.ngdoc.</span>merge (docs)](#apidoc.element.gulp-ngdocs.ngdoc.merge)
1.  [function <span class="apidocSignatureSpan">gulp-ngdocs.ngdoc.</span>metadata (docs)](#apidoc.element.gulp-ngdocs.ngdoc.metadata)
1.  [function <span class="apidocSignatureSpan">gulp-ngdocs.ngdoc.</span>scenarios (docs)](#apidoc.element.gulp-ngdocs.ngdoc.scenarios)
1.  [function <span class="apidocSignatureSpan">gulp-ngdocs.ngdoc.</span>trim (text)](#apidoc.element.gulp-ngdocs.ngdoc.trim)

#### [module gulp-ngdocs.reader](#apidoc.module.gulp-ngdocs.reader)
1.  [function <span class="apidocSignatureSpan">gulp-ngdocs.reader.</span>process (content, file, section, options)](#apidoc.element.gulp-ngdocs.reader.process)
1.  object <span class="apidocSignatureSpan">gulp-ngdocs.reader.</span>docs



# <a name="apidoc.module.gulp-ngdocs"></a>[module gulp-ngdocs](#apidoc.module.gulp-ngdocs)

#### <a name="apidoc.element.gulp-ngdocs.process"></a>[function <span class="apidocSignatureSpan">gulp-ngdocs.</span>process (opts)](#apidoc.element.gulp-ngdocs.process)
- description and source-code
```javascript
function processDoc(opts) {
  opts = opts || {};

  var options = extend({
    startPage: '/api',
    scripts: [],
    styles: [],
    title: 'API Documentation',
    html5Mode: true,
    editExample: true,
    navTemplate: false,
    navContent: '',
    navTemplateData: {}
  }, opts);

  setup.pages = [];
  //Extend loadDefaults
  options.loadDefaults = extend({
      angular: true,
      angularAnimate: true,
      marked: true
    }, opts.loadDefaults);

  if (options.scripts && !(options.scripts instanceof Array)) {
    options.scripts = [options.scripts];
  }
  if (options.styles && !(options.styles instanceof Array)) {
    options.styles = [options.styles];
  }
  var defaultSection = 'api';
  var defaultScripts = [];

  //Default root paths for scripts
  var scriptPaths = {
    angular : [
      'angular/angular.min.js',
      'angular/angular.min.js.map'
    ],
    angularAnimate: [
      'angular-animate/angular-animate.min.js',
      'angular-animate/angular-animate.min.js.map'
    ],
    marked: [
      'marked/lib/marked.js'
    ]
  };

  //Sets default script paths
  function joinNodeModules(jsPaths){
    _.each(jsPaths, function(jsPath){
      var libPath = path.join(nodeModules, jsPath),
          flattenedLibPath = path.join(flattenedNodeModules, jsPath);

      if (fs.existsSync(libPath)) {
        defaultScripts.push(libPath);
      } else if (fs.existsSync(flattenedLibPath)) {
        defaultScripts.push(flattenedLibPath);
      } else {
        console.error('Could not find ' + jsPath);
      }
    });
  }
  //Iterate and checks to join paths
  _.each(scriptPaths, function(paths, key){
    if(options.loadDefaults[key])
      joinNodeModules(paths);
  });

  function writeSetup() {
    var options = setup.__options,
        content, data = {
          scripts: options.scripts,
          styles: options.styles,
          sections: _.keys(setup.sections).join('|'),
          discussions: options.discussions,
          analytics: options.analytics,
          navContent: options.navContent,
          title: options.title,
          image: options.image,
          titleLink: options.titleLink,
          imageLink: options.imageLink,
          bestMatch: options.bestMatch,
          deferLoad: !!options.deferLoad
        };

    // create index.html
    var index = path.resolve(templates, 'index.tmpl');
    if (options.template && path.resolve(options.template)) {
      index = options.template;
    }
    content = fs.readFileSync(index, 'utf8');
    content = _.template(content, data);
    docsStream.push(new File({
      base: fakeDest,
      cwd: fakeDest,
      path: path.join(fakeDest, 'index.html'),
      contents: new Buffer(content, 'utf8')
    }));
    // create setup file
    setup.html5Mode = options.html5Mode;
    setup.editExample = options.editExample;
    setup.startPage = options.startPage;
    setup.discussions = options.discussions;
    setup.scripts = options.scripts;
    docsStream.push(new File({
      base: fakeDest,
      cwd: fakeDest,
      path: setup.__file,
      contents: new Buffer('NG_DOCS=' + JSON.stringify(setup, null, 2) + ';', 'utf8')
    }));
  }

  function transformFunction (file, enc, callback) {
    if (file.isNull()) {
      callback(null);
      return; // ignore
    }
    if (file.isStream()) {
      callback(new gutil.PluginError('gulp-ngdocs', 'Streaming not supported'));
      return;
    }
    if (file.contents) {
      if (!merged) {
        merged = merge(fstreams.map(function (f) {
          var s = f();
          s.on('data', function (file) {
            docsStream.push(file);
          });
          return s;
        }));

        merged.on('end', function () {
          mergedEnded = true;
          if (docsStreamEndCb) {
            docsStreamEndCb(null);
          }
        });
      }
      var content = decoder.write(file.contents);
      if (!file.section) {
        file.section = defaultSection;
      }
      reader.process(content, file.path, file.section, options);
    }
    callback(null);
  }

  function flushFunction (cb) {
    if (merged) { ...
```
- example usage
```shell
...

Create a 'ngdocs' gulp task

'''js
gulp.task('ngdocs', [], function () {
  var gulpDocs = require('gulp-ngdocs');
  return gulp.src('path/to/src/*.js')
    .pipe(gulpDocs.process())
    .pipe(gulp.dest('./docs'));
});
'''
Create a 'ngdocs' gulp task with options

'''js
gulp.task('ngdocs', [], function () {
...
```

#### <a name="apidoc.element.gulp-ngdocs.sections"></a>[function <span class="apidocSignatureSpan">gulp-ngdocs.</span>sections (sects)](#apidoc.element.gulp-ngdocs.sections)
- description and source-code
```javascript
function sections(sects) {
  return merge(_.map(sects, function (data, key) {
    if (data instanceof String) {
      data = {glob: data};
    }
    if (!data.hasOwnProperty('glob')) {
      throw new PluginError('gulp-ngdocs', 'Invalid sections, please refer to the documentation.');
    }
    if (!data.hasOwnProperty('title')) {
      data.title = key;
    }
    if (!data.hasOwnProperty('api')) {
      data.api = true;
    }
    var glob = data.glob;
    var opts = data.globOpts;
    setup.sections[key] = data.title;
    setup.apis[key] = data.api;
    return vfs.src(glob, opts)
      .pipe(through2.obj(
        function (file, enc, cb) {
          file.section = key;
          this.push(file);
          cb(null);
        }
      ));
    }));
}
```
- example usage
```shell
...

'''js
gulp.task('ngdocs', [], function () {
var gulpDocs = require('gulp-ngdocs');
var options = {
  //options
}
return gulpDocs.sections({
  api: {
    glob:['src/**/*.js', '!src/**/*.spec.js'],
    api: true,
    title: 'API Documentation'
  },
  tutorial: {
    glob: ['content/tutorial/*.ngdoc'],
...
```



# <a name="apidoc.module.gulp-ngdocs.dom"></a>[module gulp-ngdocs.dom](#apidoc.module.gulp-ngdocs.dom)

#### <a name="apidoc.element.gulp-ngdocs.dom.DOM"></a>[function <span class="apidocSignatureSpan">gulp-ngdocs.dom.</span>DOM ()](#apidoc.element.gulp-ngdocs.dom.DOM)
- description and source-code
```javascript
function DOM() {
  this.out = [];
  this.headingDepth = 0;
  this.currentHeaders = [];
  this.anchors = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.gulp-ngdocs.dom.htmlEscape"></a>[function <span class="apidocSignatureSpan">gulp-ngdocs.dom.</span>htmlEscape (text)](#apidoc.element.gulp-ngdocs.dom.htmlEscape)
- description and source-code
```javascript
function htmlEscape(text){
  return text
          .replace(/&/g, '&amp;')
          .replace(/</g, '&lt;')
          .replace(/>/g, '&gt;')
          .replace(/\{\{/g, '<span>{{</span>')
          .replace(/\}\}/g, '<span>}}</span>');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.gulp-ngdocs.dom.normalizeHeaderToId"></a>[function <span class="apidocSignatureSpan">gulp-ngdocs.dom.</span>normalizeHeaderToId (header)](#apidoc.element.gulp-ngdocs.dom.normalizeHeaderToId)
- description and source-code
```javascript
function normalizeHeaderToId(header) {
  if (typeof header !== 'string') {
    return '';
  }

  return header.toLowerCase()
      .replace(/<.*>/g, '')         // html tags
      .replace(/[\!\?\:\.\']/g, '') // special characters
      .replace(/&#\d\d;/g, '')      // html entities
      .replace(/\(.*\)/mg, '')      // stuff in parenthesis
      .replace(/\s$/, '')           // trailing spaces
      .replace(/\s+/g, '-');        // replace whitespaces with dashes
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.gulp-ngdocs.ngdoc"></a>[module gulp-ngdocs.ngdoc](#apidoc.module.gulp-ngdocs.ngdoc)

#### <a name="apidoc.element.gulp-ngdocs.ngdoc.Doc"></a>[function <span class="apidocSignatureSpan">gulp-ngdocs.ngdoc.</span>Doc (text, file, line, options)](#apidoc.element.gulp-ngdocs.ngdoc.Doc)
- description and source-code
```javascript
function Doc(text, file, line, options) {
  if (typeof text == 'object') {
    for ( var key in text) {
      this[key] = text[key];
    }
  } else {
    this.text = text;
    this.file = file;
    this.line = line;
  }
  this.options = options || {};
  this.scenarios = this.scenarios || [];
  this.requires = this.requires || [];
  this.param = this.param || [];
  this.properties = this.properties || [];
  this.methods = this.methods || [];
  this.events = this.events || [];
  this.links = this.links || [];
  this.anchors = this.anchors || [];
}
```
- example usage
```shell
...
// console.log('')
if (/\.js|.ts$/.test(file)) {
  processJsFile(content, file, section, options).forEach(function(doc) {
    exports.docs.push(doc);
  });
} else if (file.match(/\.ngdoc$/)) {
  var header = '@section ' + section + '\n';
  exports.docs.push(new ngdoc.Doc(header + content.toString(),file, 1, options).parse());
}
}

function processJsFile(content, file, section, options) {
var docs = [];
var lines = content.toString().split(NEW_LINE);
var text;
...
```

#### <a name="apidoc.element.gulp-ngdocs.ngdoc.checkBrokenLinks"></a>[function <span class="apidocSignatureSpan">gulp-ngdocs.ngdoc.</span>checkBrokenLinks (docs, apis, options)](#apidoc.element.gulp-ngdocs.ngdoc.checkBrokenLinks)
- description and source-code
```javascript
function checkBrokenLinks(docs, apis, options) {
  var byFullId = Object.create(null);

  docs.forEach(function(doc) {
    byFullId[doc.section + '/' + doc.id] = doc;
    if (apis[doc.section]) {
      doc.anchors.push('directive', 'service', 'filter', 'function');
    }
  });

  docs.forEach(function(doc) {
    doc.links.forEach(function(link) {
      if (options && !options.html5Mode) {
        link = link.substring(2);
      }
      // convert #id to path#id
      if (link[0] == '#') {
        link = doc.section + '/' + doc.id.split('#').shift() + link;
      }

      var parts = link.split('#');
      var pageLink = parts[0];
      var anchorLink = parts[1];
      var linkedPage = byFullId[pageLink];

      if (!linkedPage) {
        console.log('WARNING: ' + doc.section + '/' + doc.id + ' (defined in ' + doc.file + ') points to a non existing page "' +
link + '"!');
      } else if (anchorLink && linkedPage.anchors.indexOf(anchorLink) === -1) {
        console.log('WARNING: ' + doc.section + '/' + doc.id + ' (defined in ' + doc.file + ') points to a non existing anchor "' +
link + '"!');
      }
    });
  });
}
```
- example usage
```shell
...
      var cause = docError.name + ': ' + docError.message,
          placement = doc.file + ':' + doc.line,
          message = cause + ' at ' + placement;
      throw new Error(message);
    }
  });

  ngdoc.checkBrokenLinks(reader.docs, setup.apis, options);

  setup.pages = _.union(setup.pages, ngdoc.metadata(reader.docs));
} catch (flushError) {
  console.log(flushError);
  cb(flushError);
}
writeSetup(this);
...
```

#### <a name="apidoc.element.gulp-ngdocs.ngdoc.merge"></a>[function <span class="apidocSignatureSpan">gulp-ngdocs.ngdoc.</span>merge (docs)](#apidoc.element.gulp-ngdocs.ngdoc.merge)
- description and source-code
```javascript
function merge(docs){
  var byFullId = {};

  docs.forEach(function(doc) {
    byFullId[doc.section + '/' + doc.id] = doc;
  });

  for(var i = 0; i < docs.length;) {
    if (findParent(docs[i], 'method') || findParent(docs[i], 'property') || findParent(docs[i], 'event')) {
      docs.splice(i, 1);
    } else {
      i++;
    }
  }

  function findParent(doc, name) {
    var parentName = doc[name + 'Of'];
    if (!parentName) return false;

    var parent = byFullId[doc.section + '/' + parentName];
    if (!parent)
      throw new Error("No parent named '" + parentName + "' for '" +
        doc.name + "' in @" + name + "Of.");

    var listName = (name + 's').replace(/ys$/, 'ies');
    var list = parent[listName] = (parent[listName] || []);
    list.push(doc);
    list.sort(orderByName);
    return true;
  }

  function orderByName(a, b){
    return a.name < b.name ? -1 : (a.name > b.name ? 1 : 0);
  }
}
```
- example usage
```shell
...

  function flushFunction (cb) {
if (merged) {
  docsStreamEndCb = cb;
  // IMPORTANT: If you do not want an error here to destroy a gulp watch,
  // see: http://stackoverflow.com/questions/23971388/prevent-errors-from-breaking-crashing-gulp-watch
  try{
    ngdoc.merge(reader.docs);
    reader.docs.forEach(function(doc){
      try {
        // this hack is here because on OSX angular.module and angular.Module map to the same file.
        var id = doc.id.replace('angular.Module', 'angular.IModule').replace(':', '.'),
            file = path.join(fakeDest, 'partials', doc.section, id + '.html'),
            dir = path.join(fakeDest, 'partials', doc.section);
        docsStream.push(new File({
...
```

#### <a name="apidoc.element.gulp-ngdocs.ngdoc.metadata"></a>[function <span class="apidocSignatureSpan">gulp-ngdocs.ngdoc.</span>metadata (docs)](#apidoc.element.gulp-ngdocs.ngdoc.metadata)
- description and source-code
```javascript
function metadata(docs){
  var pages = [];
  docs.forEach(function(doc){
    var path = (doc.name || '').split(/(\:\s*)/);
    for ( var i = 1; i < path.length; i++) {
      path.splice(i, 1);
    }
    var shortName = path.pop().trim();

    if (path.pop() == 'input') {
      shortName = 'input [' + shortName + ']';
    }

    pages.push({
      section: doc.section,
      id: doc.id,
      name: title(doc),
      shortName: shortName,
      type: doc.ngdoc,
      moduleName: doc.moduleName,
      shortDescription: doc.shortDescription(),
      keywords: doc.keywords()
    });
  });
  pages.sort(sidebarSort);
  return pages;
}
```
- example usage
```shell
...
          message = cause + ' at ' + placement;
      throw new Error(message);
    }
  });

  ngdoc.checkBrokenLinks(reader.docs, setup.apis, options);

  setup.pages = _.union(setup.pages, ngdoc.metadata(reader.docs));
} catch (flushError) {
  console.log(flushError);
  cb(flushError);
}
writeSetup(this);

if (mergedEnded) {
...
```

#### <a name="apidoc.element.gulp-ngdocs.ngdoc.scenarios"></a>[function <span class="apidocSignatureSpan">gulp-ngdocs.ngdoc.</span>scenarios (docs)](#apidoc.element.gulp-ngdocs.ngdoc.scenarios)
- description and source-code
```javascript
function scenarios(docs){
  var specs = [];

  specs.push('describe("angular+jqlite", function() {');
  appendSpecs('index-nocache.html#!/');
  specs.push('});');

  specs.push('');
  specs.push('');

  specs.push('describe("angular+jquery", function() {');
  appendSpecs('index-jq-nocache.html#!/');
  specs.push('});');

  return specs.join('\n');

  function appendSpecs(urlPrefix) {
    docs.forEach(function(doc){
      specs.push('  describe("' + doc.section + '/' + doc.id + '", function() {');
      specs.push('    beforeEach(function() {');
      specs.push('      browser().navigateTo("' + urlPrefix + doc.section + '/' + doc.id + '");');
      specs.push('    });');
      specs.push('  ');
      doc.scenarios.forEach(function(scenario){
        specs.push(indentCode(trim(scenario), 4));
        specs.push('');
      });
      specs.push('});');
      specs.push('');
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.gulp-ngdocs.ngdoc.trim"></a>[function <span class="apidocSignatureSpan">gulp-ngdocs.ngdoc.</span>trim (text)](#apidoc.element.gulp-ngdocs.ngdoc.trim)
- description and source-code
```javascript
function trim(text) {
  var MAX_INDENT = 9999;
  var empty = RegExp.prototype.test.bind(/^\s*$/);
  var lines = text.split('\n');
  var minIndent = MAX_INDENT;
  var indentRegExp;
  var ignoreLine = (lines[0][0] != ' '  && lines.length > 1);
  // ignore first line if it has no indentation and there is more than one line

  lines.forEach(function(line){
    if (ignoreLine) {
      ignoreLine = false;
      return;
    }

    var indent = line.match(/^\s*/)[0].length;
    if (indent > 0 || minIndent == MAX_INDENT) {
      minIndent = Math.min(minIndent, indent);
    }
  });

  indentRegExp = new RegExp('^\\s{0,' + minIndent + '}');

  for ( var i = 0; i < lines.length; i++) {
    lines[i] = lines[i].replace(indentRegExp, '');
  }

  // remove leading lines
  while (empty(lines[0])) {
    lines.shift();
  }

  // remove trailing
  while (empty(lines[lines.length - 1])) {
    lines.pop();
  }
  return lines.join('\n');
}
```
- example usage
```shell
...
  } else {
    if (atName) {
      atText.push(line);
    }
  }
});
flush();
this.shortName = this.name ? this.name.split(/[\.:#]/).pop().trim() : '';
this.id = this.id || // if we have an id just use it
  (this.ngdoc === 'error' ? this.name : '') ||
  (((this.file||'').match(/.*(\/|\\)([^(\/|\\)]*)\.ngdoc/)||{})[2]) || // try to extract it from file name
  this.name; // default to name
this.description = this.markdown(this.description);
this.example = this.markdown(this.example);
this['this'] = this.markdown(this['this']);
...
```



# <a name="apidoc.module.gulp-ngdocs.reader"></a>[module gulp-ngdocs.reader](#apidoc.module.gulp-ngdocs.reader)

#### <a name="apidoc.element.gulp-ngdocs.reader.process"></a>[function <span class="apidocSignatureSpan">gulp-ngdocs.reader.</span>process (content, file, section, options)](#apidoc.element.gulp-ngdocs.reader.process)
- description and source-code
```javascript
function process(content, file, section, options) {
  // console.log('-file-----\n' + file)
  // console.log('-section-----\n' + section)
  // console.log('-options-----\n' + JSON.stringify(options, null, 2))
  // console.log('')
  if (/\.js|.ts$/.test(file)) {
    processJsFile(content, file, section, options).forEach(function(doc) {
      exports.docs.push(doc);
    });
  } else if (file.match(/\.ngdoc$/)) {
    var header = '@section ' + section + '\n';
    exports.docs.push(new ngdoc.Doc(header + content.toString(),file, 1, options).parse());
  }
}
```
- example usage
```shell
...

Create a 'ngdocs' gulp task

'''js
gulp.task('ngdocs', [], function () {
  var gulpDocs = require('gulp-ngdocs');
  return gulp.src('path/to/src/*.js')
    .pipe(gulpDocs.process())
    .pipe(gulp.dest('./docs'));
});
'''
Create a 'ngdocs' gulp task with options

'''js
gulp.task('ngdocs', [], function () {
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
