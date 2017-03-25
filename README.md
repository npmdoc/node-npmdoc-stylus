# api documentation for  [stylus (v0.54.5)](https://github.com/stylus/stylus)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-stylus.svg)](https://travis-ci.org/npmdoc/node-npmdoc-stylus)
#### Robust, expressive, and feature-rich CSS superset

[![NPM](https://nodei.co/npm/stylus.png?downloads=true)](https://www.npmjs.com/package/stylus)

[![apidoc](https://npmdoc.github.io/node-npmdoc-stylus/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-stylus_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-stylus/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-stylus/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "TJ Holowaychuk",
        "email": "tj@vision-media.ca"
    },
    "bin": {
        "stylus": "./bin/stylus"
    },
    "browserify": "./lib/browserify.js",
    "bugs": {
        "url": "https://github.com/stylus/stylus/issues"
    },
    "dependencies": {
        "css-parse": "1.7.x",
        "debug": "*",
        "glob": "7.0.x",
        "mkdirp": "0.5.x",
        "sax": "0.5.x",
        "source-map": "0.1.x"
    },
    "description": "Robust, expressive, and feature-rich CSS superset",
    "devDependencies": {
        "jscoverage": "0.3.8",
        "mocha": "*",
        "should": "8.x"
    },
    "directories": {
        "doc": "docs",
        "example": "examples",
        "test": "test"
    },
    "dist": {
        "shasum": "42b9560931ca7090ce8515a798ba9e6aa3d6dc79",
        "tarball": "https://registry.npmjs.org/stylus/-/stylus-0.54.5.tgz"
    },
    "engines": {
        "node": "*"
    },
    "gitHead": "5aff5ed0e3f482ed48f30110e24fccad7f5559ab",
    "homepage": "https://github.com/stylus/stylus",
    "keywords": [
        "css",
        "parser",
        "style",
        "stylesheets",
        "jade",
        "language"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "kizu",
            "email": "kizmarh@ya.ru"
        },
        {
            "name": "panya",
            "email": "panyakor@gmail.com"
        },
        {
            "name": "tjholowaychuk",
            "email": "tj@vision-media.ca"
        }
    ],
    "name": "stylus",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/stylus/stylus.git"
    },
    "scripts": {
        "prepublish": "npm prune",
        "test": "mocha test/ test/middleware/ --require should --bail --check-leaks --reporter dot",
        "test-cov": "mocha test/ test/middleware/ --require should --bail --reporter html-cov > coverage.html"
    },
    "version": "0.54.5"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module stylus](#apidoc.module.stylus)
1.  [function <span class="apidocSignatureSpan">stylus.</span>Compiler (root, options)](#apidoc.element.stylus.Compiler)
1.  [function <span class="apidocSignatureSpan">stylus.</span>Evaluator (root, options)](#apidoc.element.stylus.Evaluator)
1.  [function <span class="apidocSignatureSpan">stylus.</span>Normalizer (root, options)](#apidoc.element.stylus.Normalizer)
1.  [function <span class="apidocSignatureSpan">stylus.</span>Parser (str, options)](#apidoc.element.stylus.Parser)
1.  [function <span class="apidocSignatureSpan">stylus.</span>Visitor (root)](#apidoc.element.stylus.Visitor)
1.  [function <span class="apidocSignatureSpan">stylus.</span>convertCSS (css)](#apidoc.element.stylus.convertCSS)
1.  [function <span class="apidocSignatureSpan">stylus.</span>lexer (str, options)](#apidoc.element.stylus.lexer)
1.  [function <span class="apidocSignatureSpan">stylus.</span>middleware (options)](#apidoc.element.stylus.middleware)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Arguments ()](#apidoc.element.stylus.nodes.Arguments)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Atblock ()](#apidoc.element.stylus.nodes.Atblock)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Atrule (type)](#apidoc.element.stylus.nodes.Atrule)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.BinOp (op, left, right)](#apidoc.element.stylus.nodes.BinOp)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Block (parent, node)](#apidoc.element.stylus.nodes.Block)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Boolean (val)](#apidoc.element.stylus.nodes.Boolean)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Call (name, args)](#apidoc.element.stylus.nodes.Call)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Charset (val)](#apidoc.element.stylus.nodes.Charset)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Comment (str, suppress, inline)](#apidoc.element.stylus.nodes.Comment)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Each (val, key, expr, block)](#apidoc.element.stylus.nodes.Each)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Expression (isList)](#apidoc.element.stylus.nodes.Expression)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Extend (selectors)](#apidoc.element.stylus.nodes.Extend)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Feature (segs)](#apidoc.element.stylus.nodes.Feature)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Function (name, params, body)](#apidoc.element.stylus.nodes.Function)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Group ()](#apidoc.element.stylus.nodes.Group)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.HSLA (h, s, l, a)](#apidoc.element.stylus.nodes.HSLA)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Ident (name, val, mixin)](#apidoc.element.stylus.nodes.Ident)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.If (cond, negate)](#apidoc.element.stylus.nodes.If)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Import (expr, once)](#apidoc.element.stylus.nodes.Import)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Keyframes (segs, prefix)](#apidoc.element.stylus.nodes.Keyframes)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Literal (str)](#apidoc.element.stylus.nodes.Literal)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Media (val)](#apidoc.element.stylus.nodes.Media)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Member (left, right)](#apidoc.element.stylus.nodes.Member)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Namespace (val, prefix)](#apidoc.element.stylus.nodes.Namespace)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Node ()](#apidoc.element.stylus.nodes.Node)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Null ()](#apidoc.element.stylus.nodes.Null)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Object ()](#apidoc.element.stylus.nodes.Object)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Params ()](#apidoc.element.stylus.nodes.Params)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Property (segs, expr)](#apidoc.element.stylus.nodes.Property)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Query ()](#apidoc.element.stylus.nodes.Query)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.QueryList ()](#apidoc.element.stylus.nodes.QueryList)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.RGBA (r, g, b, a)](#apidoc.element.stylus.nodes.RGBA)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Return (expr)](#apidoc.element.stylus.nodes.Return)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Root ()](#apidoc.element.stylus.nodes.Root)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Selector (segs)](#apidoc.element.stylus.nodes.Selector)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.String (val, quote)](#apidoc.element.stylus.nodes.String)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Supports (condition)](#apidoc.element.stylus.nodes.Supports)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Ternary (cond, trueExpr, falseExpr)](#apidoc.element.stylus.nodes.Ternary)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.UnaryOp (op, expr)](#apidoc.element.stylus.nodes.UnaryOp)
1.  [function <span class="apidocSignatureSpan">stylus.</span>nodes.Unit (val, type)](#apidoc.element.stylus.nodes.Unit)
1.  [function <span class="apidocSignatureSpan">stylus.</span>render (str, options, fn)](#apidoc.element.stylus.render)
1.  [function <span class="apidocSignatureSpan">stylus.</span>renderer (str, options)](#apidoc.element.stylus.renderer)
1.  [function <span class="apidocSignatureSpan">stylus.</span>resolver (options)](#apidoc.element.stylus.resolver)
1.  [function <span class="apidocSignatureSpan">stylus.</span>selector_parser (str, stack, parts)](#apidoc.element.stylus.selector_parser)
1.  [function <span class="apidocSignatureSpan">stylus.</span>stack ()](#apidoc.element.stylus.stack)
1.  [function <span class="apidocSignatureSpan">stylus.</span>token (type, val)](#apidoc.element.stylus.token)
1.  [function <span class="apidocSignatureSpan">stylus.</span>url (options)](#apidoc.element.stylus.url)
1.  object <span class="apidocSignatureSpan">stylus.</span>Compiler.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>Evaluator.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>Normalizer.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>Parser.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>Visitor.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>errors
1.  object <span class="apidocSignatureSpan">stylus.</span>functions
1.  object <span class="apidocSignatureSpan">stylus.</span>lexer.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Arguments.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Atblock.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Atrule.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.BinOp.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Block.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Boolean.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Call.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Charset.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Comment.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Each.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Expression.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Extend.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Feature.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Function.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Group.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.HSLA.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Ident.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.If.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Import.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Keyframes.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Literal.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Media.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Member.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Namespace.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Node.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Null.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Object.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Params.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Property.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Query.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.QueryList.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.RGBA.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Return.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Root.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Selector.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.String.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Supports.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Ternary.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.UnaryOp.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>nodes.Unit.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>renderer.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>selector_parser.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>stack.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>token.prototype
1.  object <span class="apidocSignatureSpan">stylus.</span>utils
1.  string <span class="apidocSignatureSpan">stylus.</span>version

#### [module stylus.Compiler](#apidoc.module.stylus.Compiler)
1.  [function <span class="apidocSignatureSpan">stylus.</span>Compiler (root, options)](#apidoc.element.stylus.Compiler.Compiler)

#### [module stylus.Compiler.prototype](#apidoc.module.stylus.Compiler.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>compile ()](#apidoc.element.stylus.Compiler.prototype.compile)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>debugInfo (node)](#apidoc.element.stylus.Compiler.prototype.debugInfo)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>needBrackets (node)](#apidoc.element.stylus.Compiler.prototype.needBrackets)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>out (str, node)](#apidoc.element.stylus.Compiler.prototype.out)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitArguments (expr)](#apidoc.element.stylus.Compiler.prototype.visitArguments)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitAtrule (atrule)](#apidoc.element.stylus.Compiler.prototype.visitAtrule)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitBlock (block)](#apidoc.element.stylus.Compiler.prototype.visitBlock)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitBoolean (bool)](#apidoc.element.stylus.Compiler.prototype.visitBoolean)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitCall (call)](#apidoc.element.stylus.Compiler.prototype.visitCall)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitCharset (charset)](#apidoc.element.stylus.Compiler.prototype.visitCharset)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitComment (comment)](#apidoc.element.stylus.Compiler.prototype.visitComment)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitExpression (expr)](#apidoc.element.stylus.Compiler.prototype.visitExpression)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitFeature (node)](#apidoc.element.stylus.Compiler.prototype.visitFeature)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitFunction (fn)](#apidoc.element.stylus.Compiler.prototype.visitFunction)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitGroup (group)](#apidoc.element.stylus.Compiler.prototype.visitGroup)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitHSLA (hsla)](#apidoc.element.stylus.Compiler.prototype.visitHSLA)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitIdent (ident)](#apidoc.element.stylus.Compiler.prototype.visitIdent)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitImport (imported)](#apidoc.element.stylus.Compiler.prototype.visitImport)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitKeyframes (node)](#apidoc.element.stylus.Compiler.prototype.visitKeyframes)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitLiteral (lit)](#apidoc.element.stylus.Compiler.prototype.visitLiteral)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitMedia (media)](#apidoc.element.stylus.Compiler.prototype.visitMedia)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitNamespace (namespace)](#apidoc.element.stylus.Compiler.prototype.visitNamespace)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitNull (node)](#apidoc.element.stylus.Compiler.prototype.visitNull)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitProperty (prop)](#apidoc.element.stylus.Compiler.prototype.visitProperty)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitQuery (node)](#apidoc.element.stylus.Compiler.prototype.visitQuery)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitQueryList (queries)](#apidoc.element.stylus.Compiler.prototype.visitQueryList)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitRGBA (rgba)](#apidoc.element.stylus.Compiler.prototype.visitRGBA)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitRoot (block)](#apidoc.element.stylus.Compiler.prototype.visitRoot)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitString (string)](#apidoc.element.stylus.Compiler.prototype.visitString)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitSupports (node)](#apidoc.element.stylus.Compiler.prototype.visitSupports)
1.  [function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitUnit (unit)](#apidoc.element.stylus.Compiler.prototype.visitUnit)

#### [module stylus.Evaluator](#apidoc.module.stylus.Evaluator)
1.  [function <span class="apidocSignatureSpan">stylus.</span>Evaluator (root, options)](#apidoc.element.stylus.Evaluator.Evaluator)

#### [module stylus.Evaluator.prototype](#apidoc.module.stylus.Evaluator.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>_mixin (items, dest, block)](#apidoc.element.stylus.Evaluator.prototype._mixin)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>cast (expr)](#apidoc.element.stylus.Evaluator.prototype.cast)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>castable (expr)](#apidoc.element.stylus.Evaluator.prototype.castable)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>eval (vals)](#apidoc.element.stylus.Evaluator.prototype.eval)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>evaluate ()](#apidoc.element.stylus.Evaluator.prototype.evaluate)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>interpolate (node)](#apidoc.element.stylus.Evaluator.prototype.interpolate)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>invoke (body, stack, filename)](#apidoc.element.stylus.Evaluator.prototype.invoke)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>invokeBuiltin (fn, args)](#apidoc.element.stylus.Evaluator.prototype.invokeBuiltin)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>invokeFunction (fn, args, content)](#apidoc.element.stylus.Evaluator.prototype.invokeFunction)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>isDefined (node)](#apidoc.element.stylus.Evaluator.prototype.isDefined)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>literalCall (call)](#apidoc.element.stylus.Evaluator.prototype.literalCall)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>lookup (name)](#apidoc.element.stylus.Evaluator.prototype.lookup)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>lookupFunction (name)](#apidoc.element.stylus.Evaluator.prototype.lookupFunction)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>lookupProperty (name)](#apidoc.element.stylus.Evaluator.prototype.lookupProperty)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>mixin (nodes, block)](#apidoc.element.stylus.Evaluator.prototype.mixin)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>mixinNode (node)](#apidoc.element.stylus.Evaluator.prototype.mixinNode)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>mixinObject (object)](#apidoc.element.stylus.Evaluator.prototype.mixinObject)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>populateGlobalScope ()](#apidoc.element.stylus.Evaluator.prototype.populateGlobalScope)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>propertyExpression (prop, name)](#apidoc.element.stylus.Evaluator.prototype.propertyExpression)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>setup ()](#apidoc.element.stylus.Evaluator.prototype.setup)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>unvendorize (prop)](#apidoc.element.stylus.Evaluator.prototype.unvendorize)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visit (node)](#apidoc.element.stylus.Evaluator.prototype.visit)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitArguments (expr)](#apidoc.element.stylus.Evaluator.prototype.visitArguments)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitAtblock (atblock)](#apidoc.element.stylus.Evaluator.prototype.visitAtblock)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitAtrule (atrule)](#apidoc.element.stylus.Evaluator.prototype.visitAtrule)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitBinOp (binop)](#apidoc.element.stylus.Evaluator.prototype.visitBinOp)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitBlock (block)](#apidoc.element.stylus.Evaluator.prototype.visitBlock)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitCall (call)](#apidoc.element.stylus.Evaluator.prototype.visitCall)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitEach (each)](#apidoc.element.stylus.Evaluator.prototype.visitEach)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitExpression (expr)](#apidoc.element.stylus.Evaluator.prototype.visitExpression)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitExtend (extend)](#apidoc.element.stylus.Evaluator.prototype.visitExtend)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitFeature (node)](#apidoc.element.stylus.Evaluator.prototype.visitFeature)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitFunction (fn)](#apidoc.element.stylus.Evaluator.prototype.visitFunction)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitGroup (group)](#apidoc.element.stylus.Evaluator.prototype.visitGroup)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitIdent (ident)](#apidoc.element.stylus.Evaluator.prototype.visitIdent)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitIf (node)](#apidoc.element.stylus.Evaluator.prototype.visitIf)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitImport (imported)](#apidoc.element.stylus.Evaluator.prototype.visitImport)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitKeyframes (keyframes)](#apidoc.element.stylus.Evaluator.prototype.visitKeyframes)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitMedia (media)](#apidoc.element.stylus.Evaluator.prototype.visitMedia)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitMember (node)](#apidoc.element.stylus.Evaluator.prototype.visitMember)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitObject (obj)](#apidoc.element.stylus.Evaluator.prototype.visitObject)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitProperty (prop)](#apidoc.element.stylus.Evaluator.prototype.visitProperty)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitQuery (node)](#apidoc.element.stylus.Evaluator.prototype.visitQuery)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitQueryList (queries)](#apidoc.element.stylus.Evaluator.prototype.visitQueryList)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitReturn (ret)](#apidoc.element.stylus.Evaluator.prototype.visitReturn)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitRoot (block)](#apidoc.element.stylus.Evaluator.prototype.visitRoot)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitSupports (node)](#apidoc.element.stylus.Evaluator.prototype.visitSupports)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitTernary (ternary)](#apidoc.element.stylus.Evaluator.prototype.visitTernary)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitUnaryOp (unary)](#apidoc.element.stylus.Evaluator.prototype.visitUnaryOp)
1.  [function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>warn (msg)](#apidoc.element.stylus.Evaluator.prototype.warn)

#### [module stylus.Normalizer](#apidoc.module.stylus.Normalizer)
1.  [function <span class="apidocSignatureSpan">stylus.</span>Normalizer (root, options)](#apidoc.element.stylus.Normalizer.Normalizer)

#### [module stylus.Normalizer.prototype](#apidoc.module.stylus.Normalizer.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>bubble (node)](#apidoc.element.stylus.Normalizer.prototype.bubble)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>closestGroup (block)](#apidoc.element.stylus.Normalizer.prototype.closestGroup)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>extend (group, selectors)](#apidoc.element.stylus.Normalizer.prototype.extend)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>normalize ()](#apidoc.element.stylus.Normalizer.prototype.normalize)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitAtrule (node)](#apidoc.element.stylus.Normalizer.prototype.visitAtrule)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitBlock (block)](#apidoc.element.stylus.Normalizer.prototype.visitBlock)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitCharset (node)](#apidoc.element.stylus.Normalizer.prototype.visitCharset)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitExpression (expr)](#apidoc.element.stylus.Normalizer.prototype.visitExpression)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitFunction ()](#apidoc.element.stylus.Normalizer.prototype.visitFunction)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitGroup (group)](#apidoc.element.stylus.Normalizer.prototype.visitGroup)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitImport (node)](#apidoc.element.stylus.Normalizer.prototype.visitImport)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitKeyframes (node)](#apidoc.element.stylus.Normalizer.prototype.visitKeyframes)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitMedia (media)](#apidoc.element.stylus.Normalizer.prototype.visitMedia)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitProperty (prop)](#apidoc.element.stylus.Normalizer.prototype.visitProperty)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitRoot (block)](#apidoc.element.stylus.Normalizer.prototype.visitRoot)
1.  [function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitSupports (node)](#apidoc.element.stylus.Normalizer.prototype.visitSupports)

#### [module stylus.Parser](#apidoc.module.stylus.Parser)
1.  [function <span class="apidocSignatureSpan">stylus.</span>Parser (str, options)](#apidoc.element.stylus.Parser.Parser)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.</span>getCache (options)](#apidoc.element.stylus.Parser.getCache)

#### [module stylus.Parser.prototype](#apidoc.module.stylus.Parser.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>accept (type)](#apidoc.element.stylus.Parser.prototype.accept)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>additive ()](#apidoc.element.stylus.Parser.prototype.additive)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>args ()](#apidoc.element.stylus.Parser.prototype.args)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>assignAtblock (expr)](#apidoc.element.stylus.Parser.prototype.assignAtblock)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>assignment ()](#apidoc.element.stylus.Parser.prototype.assignment)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>atblock (node)](#apidoc.element.stylus.Parser.prototype.atblock)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>atrule ()](#apidoc.element.stylus.Parser.prototype.atrule)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>block (node, scope)](#apidoc.element.stylus.Parser.prototype.block)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>charset ()](#apidoc.element.stylus.Parser.prototype.charset)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>comment ()](#apidoc.element.stylus.Parser.prototype.comment)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>constructor (str, options)](#apidoc.element.stylus.Parser.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>currentState ()](#apidoc.element.stylus.Parser.prototype.currentState)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>defined ()](#apidoc.element.stylus.Parser.prototype.defined)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>equality ()](#apidoc.element.stylus.Parser.prototype.equality)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>error (msg)](#apidoc.element.stylus.Parser.prototype.error)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>expect (type)](#apidoc.element.stylus.Parser.prototype.expect)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>expression ()](#apidoc.element.stylus.Parser.prototype.expression)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>extend ()](#apidoc.element.stylus.Parser.prototype.extend)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>feature ()](#apidoc.element.stylus.Parser.prototype.feature)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>for ()](#apidoc.element.stylus.Parser.prototype.for)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>function ()](#apidoc.element.stylus.Parser.prototype.function)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>functionCall ()](#apidoc.element.stylus.Parser.prototype.functionCall)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>functionDefinition ()](#apidoc.element.stylus.Parser.prototype.functionDefinition)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>id ()](#apidoc.element.stylus.Parser.prototype.id)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>ident ()](#apidoc.element.stylus.Parser.prototype.ident)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>if ()](#apidoc.element.stylus.Parser.prototype.if)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>import ()](#apidoc.element.stylus.Parser.prototype.import)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>in ()](#apidoc.element.stylus.Parser.prototype.in)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>interpolate ()](#apidoc.element.stylus.Parser.prototype.interpolate)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>isPseudoSelector (n)](#apidoc.element.stylus.Parser.prototype.isPseudoSelector)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>isSelectorToken (n)](#apidoc.element.stylus.Parser.prototype.isSelectorToken)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>keyframes ()](#apidoc.element.stylus.Parser.prototype.keyframes)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>lineContains (type)](#apidoc.element.stylus.Parser.prototype.lineContains)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>list ()](#apidoc.element.stylus.Parser.prototype.list)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>literal ()](#apidoc.element.stylus.Parser.prototype.literal)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>logical ()](#apidoc.element.stylus.Parser.prototype.logical)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>lookahead (n)](#apidoc.element.stylus.Parser.prototype.lookahead)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>looksLikeAttributeSelector (n)](#apidoc.element.stylus.Parser.prototype.looksLikeAttributeSelector)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>looksLikeFunctionDefinition (i)](#apidoc.element.stylus.Parser.prototype.looksLikeFunctionDefinition)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>looksLikeKeyframe ()](#apidoc.element.stylus.Parser.prototype.looksLikeKeyframe)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>looksLikeSelector (fromProperty)](#apidoc.element.stylus.Parser.prototype.looksLikeSelector)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>media ()](#apidoc.element.stylus.Parser.prototype.media)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>member ()](#apidoc.element.stylus.Parser.prototype.member)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>mozdocument ()](#apidoc.element.stylus.Parser.prototype.mozdocument)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>multiplicative ()](#apidoc.element.stylus.Parser.prototype.multiplicative)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>namespace ()](#apidoc.element.stylus.Parser.prototype.namespace)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>negation ()](#apidoc.element.stylus.Parser.prototype.negation)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>next ()](#apidoc.element.stylus.Parser.prototype.next)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>object ()](#apidoc.element.stylus.Parser.prototype.object)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>params ()](#apidoc.element.stylus.Parser.prototype.params)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>parse ()](#apidoc.element.stylus.Parser.prototype.parse)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>peek ()](#apidoc.element.stylus.Parser.prototype.peek)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>previousState ()](#apidoc.element.stylus.Parser.prototype.previousState)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>primary ()](#apidoc.element.stylus.Parser.prototype.primary)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>property ()](#apidoc.element.stylus.Parser.prototype.property)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>queries ()](#apidoc.element.stylus.Parser.prototype.queries)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>query ()](#apidoc.element.stylus.Parser.prototype.query)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>range ()](#apidoc.element.stylus.Parser.prototype.range)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>relational ()](#apidoc.element.stylus.Parser.prototype.relational)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>require ()](#apidoc.element.stylus.Parser.prototype.require)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>return ()](#apidoc.element.stylus.Parser.prototype.return)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>scope ()](#apidoc.element.stylus.Parser.prototype.scope)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>selector ()](#apidoc.element.stylus.Parser.prototype.selector)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>selectorParts ()](#apidoc.element.stylus.Parser.prototype.selectorParts)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>selectorToken ()](#apidoc.element.stylus.Parser.prototype.selectorToken)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>skip (tokens)](#apidoc.element.stylus.Parser.prototype.skip)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>skipNewlines ()](#apidoc.element.stylus.Parser.prototype.skipNewlines)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>skipSpaces ()](#apidoc.element.stylus.Parser.prototype.skipSpaces)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>skipSpacesAndComments ()](#apidoc.element.stylus.Parser.prototype.skipSpacesAndComments)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>skipWhitespace ()](#apidoc.element.stylus.Parser.prototype.skipWhitespace)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>stateAllowsSelector ()](#apidoc.element.stylus.Parser.prototype.stateAllowsSelector)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>statement ()](#apidoc.element.stylus.Parser.prototype.statement)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>stmt ()](#apidoc.element.stylus.Parser.prototype.stmt)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>subscript ()](#apidoc.element.stylus.Parser.prototype.subscript)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>supports ()](#apidoc.element.stylus.Parser.prototype.supports)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>supportsCondition ()](#apidoc.element.stylus.Parser.prototype.supportsCondition)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>supportsFeature ()](#apidoc.element.stylus.Parser.prototype.supportsFeature)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>supportsNegation ()](#apidoc.element.stylus.Parser.prototype.supportsNegation)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>supportsOp ()](#apidoc.element.stylus.Parser.prototype.supportsOp)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>ternary ()](#apidoc.element.stylus.Parser.prototype.ternary)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>typecheck ()](#apidoc.element.stylus.Parser.prototype.typecheck)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>unary ()](#apidoc.element.stylus.Parser.prototype.unary)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>unless ()](#apidoc.element.stylus.Parser.prototype.unless)
1.  [function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>url ()](#apidoc.element.stylus.Parser.prototype.url)

#### [module stylus.Visitor](#apidoc.module.stylus.Visitor)
1.  [function <span class="apidocSignatureSpan">stylus.</span>Visitor (root)](#apidoc.element.stylus.Visitor.Visitor)

#### [module stylus.Visitor.prototype](#apidoc.module.stylus.Visitor.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.Visitor.prototype.</span>visit (node, fn)](#apidoc.element.stylus.Visitor.prototype.visit)

#### [module stylus.errors](#apidoc.module.stylus.errors)
1.  [function <span class="apidocSignatureSpan">stylus.errors.</span>ParseError (msg)](#apidoc.element.stylus.errors.ParseError)
1.  [function <span class="apidocSignatureSpan">stylus.errors.</span>SyntaxError (msg)](#apidoc.element.stylus.errors.SyntaxError)

#### [module stylus.functions](#apidoc.module.stylus.functions)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>add-property (name, expr)](#apidoc.element.stylus.functions.add-property)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>adjust (color, prop, amount)](#apidoc.element.stylus.functions.adjust)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>alpha (color, value)](#apidoc.element.stylus.functions.alpha)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>append (expr)](#apidoc.element.stylus.functions.append)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>base-convert (num, base, width)](#apidoc.element.stylus.functions.base-convert)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>basename (p, ext)](#apidoc.element.stylus.functions.basename)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>blend (top, bottom)](#apidoc.element.stylus.functions.blend)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>blue (color, value)](#apidoc.element.stylus.functions.blue)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>clone (expr)](#apidoc.element.stylus.functions.clone)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>component (color, name)](#apidoc.element.stylus.functions.component)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>contrast (top, bottom)](#apidoc.element.stylus.functions.contrast)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>convert (str)](#apidoc.element.stylus.functions.convert)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>current-media ()](#apidoc.element.stylus.functions.current-media)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>define (name, expr, global)](#apidoc.element.stylus.functions.define)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>dirname (p)](#apidoc.element.stylus.functions.dirname)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>error (msg)](#apidoc.element.stylus.functions.error)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>extend (dest)](#apidoc.element.stylus.functions.extend)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>extname (p)](#apidoc.element.stylus.functions.extname)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>green (color, value)](#apidoc.element.stylus.functions.green)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>hsl (hue, saturation, lightness)](#apidoc.element.stylus.functions.hsl)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>hsla (hue, saturation, lightness, alpha)](#apidoc.element.stylus.functions.hsla)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>hue (color, value)](#apidoc.element.stylus.functions.hue)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>image-size (img, ignoreErr)](#apidoc.element.stylus.functions.image-size)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>json (path, local, namePrefix)](#apidoc.element.stylus.functions.json)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>length (expr)](#apidoc.element.stylus.functions.length)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>lightness (color, value)](#apidoc.element.stylus.functions.lightness)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>list-separator (list)](#apidoc.element.stylus.functions.list-separator)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>lookup (name)](#apidoc.element.stylus.functions.lookup)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>luminosity (color)](#apidoc.element.stylus.functions.luminosity)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>match (pattern, val, flags)](#apidoc.element.stylus.functions.match)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>math (n, fn)](#apidoc.element.stylus.functions.math)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>merge (dest)](#apidoc.element.stylus.functions.merge)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>operate (op, left, right)](#apidoc.element.stylus.functions.operate)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>opposite-position (positions)](#apidoc.element.stylus.functions.opposite-position)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>p ()](#apidoc.element.stylus.functions.p)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>pathjoin ()](#apidoc.element.stylus.functions.pathjoin)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>pop (expr)](#apidoc.element.stylus.functions.pop)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>prepend (expr)](#apidoc.element.stylus.functions.prepend)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>push (expr)](#apidoc.element.stylus.functions.push)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>range (start, stop, step)](#apidoc.element.stylus.functions.range)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>red (color, value)](#apidoc.element.stylus.functions.red)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>remove (object, key)](#apidoc.element.stylus.functions.remove)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>replace (pattern, replacement, val)](#apidoc.element.stylus.functions.replace)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>rgb (red, green, blue)](#apidoc.element.stylus.functions.rgb)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>rgba (red, green, blue, alpha)](#apidoc.element.stylus.functions.rgba)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>s (fmt)](#apidoc.element.stylus.functions.s)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>saturation (color, value)](#apidoc.element.stylus.functions.saturation)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>selector ()](#apidoc.element.stylus.functions.selector)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>selector-exists (sel)](#apidoc.element.stylus.functions.selector-exists)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>selectors ()](#apidoc.element.stylus.functions.selectors)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>shift (expr)](#apidoc.element.stylus.functions.shift)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>slice (val, start, end)](#apidoc.element.stylus.functions.slice)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>split (delim, val)](#apidoc.element.stylus.functions.split)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>substr (val, start, length)](#apidoc.element.stylus.functions.substr)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>tan (angle)](#apidoc.element.stylus.functions.tan)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>trace ()](#apidoc.element.stylus.functions.trace)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>transparentify (top, bottom, alpha)](#apidoc.element.stylus.functions.transparentify)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>type (node)](#apidoc.element.stylus.functions.type)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>type-of (node)](#apidoc.element.stylus.functions.type-of)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>typeof (node)](#apidoc.element.stylus.functions.typeof)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>unit (unit, type)](#apidoc.element.stylus.functions.unit)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>unquote (string)](#apidoc.element.stylus.functions.unquote)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>unshift (expr)](#apidoc.element.stylus.functions.unshift)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>use (plugin, options)](#apidoc.element.stylus.functions.use)
1.  [function <span class="apidocSignatureSpan">stylus.functions.</span>warn (msg)](#apidoc.element.stylus.functions.warn)

#### [module stylus.lexer](#apidoc.module.stylus.lexer)
1.  [function <span class="apidocSignatureSpan">stylus.</span>lexer (str, options)](#apidoc.element.stylus.lexer.lexer)

#### [module stylus.lexer.prototype](#apidoc.module.stylus.lexer.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>advance ()](#apidoc.element.stylus.lexer.prototype.advance)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>anonFunc ()](#apidoc.element.stylus.lexer.prototype.anonFunc)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>atrule ()](#apidoc.element.stylus.lexer.prototype.atrule)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>boolean ()](#apidoc.element.stylus.lexer.prototype.boolean)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>brace ()](#apidoc.element.stylus.lexer.prototype.brace)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>color ()](#apidoc.element.stylus.lexer.prototype.color)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>comment ()](#apidoc.element.stylus.lexer.prototype.comment)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>eol ()](#apidoc.element.stylus.lexer.prototype.eol)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>eos ()](#apidoc.element.stylus.lexer.prototype.eos)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>escaped ()](#apidoc.element.stylus.lexer.prototype.escaped)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>function ()](#apidoc.element.stylus.lexer.prototype.function)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>ident ()](#apidoc.element.stylus.lexer.prototype.ident)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>important ()](#apidoc.element.stylus.lexer.prototype.important)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>inspect ()](#apidoc.element.stylus.lexer.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>isPartOfSelector ()](#apidoc.element.stylus.lexer.prototype.isPartOfSelector)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>keyword ()](#apidoc.element.stylus.lexer.prototype.keyword)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>literal ()](#apidoc.element.stylus.lexer.prototype.literal)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>lookahead (n)](#apidoc.element.stylus.lexer.prototype.lookahead)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>move (str)](#apidoc.element.stylus.lexer.prototype.move)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>n ()](#apidoc.element.stylus.lexer.prototype.n)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>namedop ()](#apidoc.element.stylus.lexer.prototype.namedop)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>newline ()](#apidoc.element.stylus.lexer.prototype.newline)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>next ()](#apidoc.element.stylus.lexer.prototype.next)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>nn ()](#apidoc.element.stylus.lexer.prototype.nn)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>null ()](#apidoc.element.stylus.lexer.prototype.null)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>op ()](#apidoc.element.stylus.lexer.prototype.op)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>paren ()](#apidoc.element.stylus.lexer.prototype.paren)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>peek ()](#apidoc.element.stylus.lexer.prototype.peek)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>rgb ()](#apidoc.element.stylus.lexer.prototype.rgb)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>rgba ()](#apidoc.element.stylus.lexer.prototype.rgba)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>rrggbb ()](#apidoc.element.stylus.lexer.prototype.rrggbb)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>rrggbbaa ()](#apidoc.element.stylus.lexer.prototype.rrggbbaa)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>selector ()](#apidoc.element.stylus.lexer.prototype.selector)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>sep ()](#apidoc.element.stylus.lexer.prototype.sep)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>skip (len)](#apidoc.element.stylus.lexer.prototype.skip)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>space ()](#apidoc.element.stylus.lexer.prototype.space)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>stashed ()](#apidoc.element.stylus.lexer.prototype.stashed)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>string ()](#apidoc.element.stylus.lexer.prototype.string)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>unicode ()](#apidoc.element.stylus.lexer.prototype.unicode)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>unit ()](#apidoc.element.stylus.lexer.prototype.unit)
1.  [function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>urlchars ()](#apidoc.element.stylus.lexer.prototype.urlchars)

#### [module stylus.nodes](#apidoc.module.stylus.nodes)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Arguments ()](#apidoc.element.stylus.nodes.Arguments)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Atblock ()](#apidoc.element.stylus.nodes.Atblock)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Atrule (type)](#apidoc.element.stylus.nodes.Atrule)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>BinOp (op, left, right)](#apidoc.element.stylus.nodes.BinOp)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Block (parent, node)](#apidoc.element.stylus.nodes.Block)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Boolean (val)](#apidoc.element.stylus.nodes.Boolean)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Call (name, args)](#apidoc.element.stylus.nodes.Call)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Charset (val)](#apidoc.element.stylus.nodes.Charset)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Comment (str, suppress, inline)](#apidoc.element.stylus.nodes.Comment)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Each (val, key, expr, block)](#apidoc.element.stylus.nodes.Each)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Expression (isList)](#apidoc.element.stylus.nodes.Expression)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Extend (selectors)](#apidoc.element.stylus.nodes.Extend)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Feature (segs)](#apidoc.element.stylus.nodes.Feature)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Function (name, params, body)](#apidoc.element.stylus.nodes.Function)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Group ()](#apidoc.element.stylus.nodes.Group)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>HSLA (h, s, l, a)](#apidoc.element.stylus.nodes.HSLA)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Ident (name, val, mixin)](#apidoc.element.stylus.nodes.Ident)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>If (cond, negate)](#apidoc.element.stylus.nodes.If)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Import (expr, once)](#apidoc.element.stylus.nodes.Import)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Keyframes (segs, prefix)](#apidoc.element.stylus.nodes.Keyframes)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Literal (str)](#apidoc.element.stylus.nodes.Literal)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Media (val)](#apidoc.element.stylus.nodes.Media)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Member (left, right)](#apidoc.element.stylus.nodes.Member)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Namespace (val, prefix)](#apidoc.element.stylus.nodes.Namespace)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Node ()](#apidoc.element.stylus.nodes.Node)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Null ()](#apidoc.element.stylus.nodes.Null)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Object ()](#apidoc.element.stylus.nodes.Object)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Params ()](#apidoc.element.stylus.nodes.Params)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Property (segs, expr)](#apidoc.element.stylus.nodes.Property)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Query ()](#apidoc.element.stylus.nodes.Query)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>QueryList ()](#apidoc.element.stylus.nodes.QueryList)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>RGBA (r, g, b, a)](#apidoc.element.stylus.nodes.RGBA)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Return (expr)](#apidoc.element.stylus.nodes.Return)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Root ()](#apidoc.element.stylus.nodes.Root)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Selector (segs)](#apidoc.element.stylus.nodes.Selector)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>String (val, quote)](#apidoc.element.stylus.nodes.String)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Supports (condition)](#apidoc.element.stylus.nodes.Supports)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Ternary (cond, trueExpr, falseExpr)](#apidoc.element.stylus.nodes.Ternary)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>UnaryOp (op, expr)](#apidoc.element.stylus.nodes.UnaryOp)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Unit (val, type)](#apidoc.element.stylus.nodes.Unit)
1.  object <span class="apidocSignatureSpan">stylus.nodes.</span>false
1.  object <span class="apidocSignatureSpan">stylus.nodes.</span>null
1.  object <span class="apidocSignatureSpan">stylus.nodes.</span>true

#### [module stylus.nodes.Arguments](#apidoc.module.stylus.nodes.Arguments)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Arguments ()](#apidoc.element.stylus.nodes.Arguments.Arguments)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Arguments.</span>fromExpression (expr)](#apidoc.element.stylus.nodes.Arguments.fromExpression)

#### [module stylus.nodes.Arguments.prototype](#apidoc.module.stylus.nodes.Arguments.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Arguments.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Arguments.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Arguments.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Arguments.prototype.toJSON)

#### [module stylus.nodes.Atblock](#apidoc.module.stylus.nodes.Atblock)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Atblock ()](#apidoc.element.stylus.nodes.Atblock.Atblock)

#### [module stylus.nodes.Atblock.prototype](#apidoc.module.stylus.nodes.Atblock.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Atblock.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Atblock.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Atblock.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Atblock.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Atblock.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Atblock.prototype.toString)

#### [module stylus.nodes.Atrule](#apidoc.module.stylus.nodes.Atrule)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Atrule (type)](#apidoc.element.stylus.nodes.Atrule.Atrule)

#### [module stylus.nodes.Atrule.prototype](#apidoc.module.stylus.nodes.Atrule.prototype)
1.  boolean <span class="apidocSignatureSpan">stylus.nodes.Atrule.prototype.</span>hasOnlyProperties
1.  boolean <span class="apidocSignatureSpan">stylus.nodes.Atrule.prototype.</span>hasOutput
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Atrule.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Atrule.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Atrule.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Atrule.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Atrule.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Atrule.prototype.toString)

#### [module stylus.nodes.BinOp](#apidoc.module.stylus.nodes.BinOp)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>BinOp (op, left, right)](#apidoc.element.stylus.nodes.BinOp.BinOp)

#### [module stylus.nodes.BinOp.prototype](#apidoc.module.stylus.nodes.BinOp.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.BinOp.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.BinOp.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.BinOp.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.BinOp.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.BinOp.prototype.</span>toString ()](#apidoc.element.stylus.nodes.BinOp.prototype.toString)

#### [module stylus.nodes.Block](#apidoc.module.stylus.nodes.Block)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Block (parent, node)](#apidoc.element.stylus.nodes.Block.Block)

#### [module stylus.nodes.Block.prototype](#apidoc.module.stylus.nodes.Block.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Block.prototype.</span>clone (parent, node)](#apidoc.element.stylus.nodes.Block.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Block.prototype.</span>push (node)](#apidoc.element.stylus.nodes.Block.prototype.push)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Block.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Block.prototype.toJSON)

#### [module stylus.nodes.Boolean](#apidoc.module.stylus.nodes.Boolean)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Boolean (val)](#apidoc.element.stylus.nodes.Boolean.Boolean)

#### [module stylus.nodes.Boolean.prototype](#apidoc.module.stylus.nodes.Boolean.prototype)
1.  boolean <span class="apidocSignatureSpan">stylus.nodes.Boolean.prototype.</span>isFalse
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Boolean.prototype.</span>inspect ()](#apidoc.element.stylus.nodes.Boolean.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Boolean.prototype.</span>negate ()](#apidoc.element.stylus.nodes.Boolean.prototype.negate)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Boolean.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.Boolean.prototype.toBoolean)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Boolean.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Boolean.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Boolean.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Boolean.prototype.toString)

#### [module stylus.nodes.Call](#apidoc.module.stylus.nodes.Call)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Call (name, args)](#apidoc.element.stylus.nodes.Call.Call)

#### [module stylus.nodes.Call.prototype](#apidoc.module.stylus.nodes.Call.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Call.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Call.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Call.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Call.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Call.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Call.prototype.toString)

#### [module stylus.nodes.Charset](#apidoc.module.stylus.nodes.Charset)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Charset (val)](#apidoc.element.stylus.nodes.Charset.Charset)

#### [module stylus.nodes.Charset.prototype](#apidoc.module.stylus.nodes.Charset.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Charset.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Charset.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Charset.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Charset.prototype.toString)

#### [module stylus.nodes.Comment](#apidoc.module.stylus.nodes.Comment)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Comment (str, suppress, inline)](#apidoc.element.stylus.nodes.Comment.Comment)

#### [module stylus.nodes.Comment.prototype](#apidoc.module.stylus.nodes.Comment.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Comment.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Comment.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Comment.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Comment.prototype.toString)

#### [module stylus.nodes.Each](#apidoc.module.stylus.nodes.Each)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Each (val, key, expr, block)](#apidoc.element.stylus.nodes.Each.Each)

#### [module stylus.nodes.Each.prototype](#apidoc.module.stylus.nodes.Each.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Each.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Each.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Each.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Each.prototype.toJSON)

#### [module stylus.nodes.Expression](#apidoc.module.stylus.nodes.Expression)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Expression (isList)](#apidoc.element.stylus.nodes.Expression.Expression)

#### [module stylus.nodes.Expression.prototype](#apidoc.module.stylus.nodes.Expression.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Expression.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Expression.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Expression.prototype.</span>operate (op, right, val)](#apidoc.element.stylus.nodes.Expression.prototype.operate)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Expression.prototype.</span>push (node)](#apidoc.element.stylus.nodes.Expression.prototype.push)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Expression.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.Expression.prototype.toBoolean)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Expression.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Expression.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Expression.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Expression.prototype.toString)

#### [module stylus.nodes.Extend](#apidoc.module.stylus.nodes.Extend)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Extend (selectors)](#apidoc.element.stylus.nodes.Extend.Extend)

#### [module stylus.nodes.Extend.prototype](#apidoc.module.stylus.nodes.Extend.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Extend.prototype.</span>clone ()](#apidoc.element.stylus.nodes.Extend.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Extend.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Extend.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Extend.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Extend.prototype.toString)

#### [module stylus.nodes.Feature](#apidoc.module.stylus.nodes.Feature)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Feature (segs)](#apidoc.element.stylus.nodes.Feature.Feature)

#### [module stylus.nodes.Feature.prototype](#apidoc.module.stylus.nodes.Feature.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Feature.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Feature.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Feature.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Feature.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Feature.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Feature.prototype.toString)

#### [module stylus.nodes.Function](#apidoc.module.stylus.nodes.Function)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Function (name, params, body)](#apidoc.element.stylus.nodes.Function.Function)

#### [module stylus.nodes.Function.prototype](#apidoc.module.stylus.nodes.Function.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Function.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Function.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Function.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Function.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Function.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Function.prototype.toString)
1.  string <span class="apidocSignatureSpan">stylus.nodes.Function.prototype.</span>hash

#### [module stylus.nodes.Group](#apidoc.module.stylus.nodes.Group)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Group ()](#apidoc.element.stylus.nodes.Group.Group)

#### [module stylus.nodes.Group.prototype](#apidoc.module.stylus.nodes.Group.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Group.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Group.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Group.prototype.</span>push (selector)](#apidoc.element.stylus.nodes.Group.prototype.push)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Group.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Group.prototype.toJSON)

#### [module stylus.nodes.HSLA](#apidoc.module.stylus.nodes.HSLA)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>HSLA (h, s, l, a)](#apidoc.element.stylus.nodes.HSLA.HSLA)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.HSLA.</span>fromRGBA (rgba)](#apidoc.element.stylus.nodes.HSLA.fromRGBA)

#### [module stylus.nodes.HSLA.prototype](#apidoc.module.stylus.nodes.HSLA.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>add (h, s, l)](#apidoc.element.stylus.nodes.HSLA.prototype.add)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>adjustHue (deg)](#apidoc.element.stylus.nodes.HSLA.prototype.adjustHue)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>adjustLightness (percent)](#apidoc.element.stylus.nodes.HSLA.prototype.adjustLightness)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.HSLA.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.HSLA.prototype.operate)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>sub (h, s, l)](#apidoc.element.stylus.nodes.HSLA.prototype.sub)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.HSLA.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>toString ()](#apidoc.element.stylus.nodes.HSLA.prototype.toString)
1.  object <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>rgba
1.  string <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>hash

#### [module stylus.nodes.Ident](#apidoc.module.stylus.nodes.Ident)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Ident (name, val, mixin)](#apidoc.element.stylus.nodes.Ident.Ident)

#### [module stylus.nodes.Ident.prototype](#apidoc.module.stylus.nodes.Ident.prototype)
1.  boolean <span class="apidocSignatureSpan">stylus.nodes.Ident.prototype.</span>isEmpty
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Ident.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Ident.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Ident.prototype.</span>coerce (other)](#apidoc.element.stylus.nodes.Ident.prototype.coerce)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Ident.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.Ident.prototype.operate)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Ident.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Ident.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Ident.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Ident.prototype.toString)

#### [module stylus.nodes.If](#apidoc.module.stylus.nodes.If)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>If (cond, negate)](#apidoc.element.stylus.nodes.If.If)

#### [module stylus.nodes.If.prototype](#apidoc.module.stylus.nodes.If.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.If.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.If.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.If.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.If.prototype.toJSON)

#### [module stylus.nodes.Import](#apidoc.module.stylus.nodes.Import)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Import (expr, once)](#apidoc.element.stylus.nodes.Import.Import)

#### [module stylus.nodes.Import.prototype](#apidoc.module.stylus.nodes.Import.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Import.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Import.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Import.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Import.prototype.toJSON)

#### [module stylus.nodes.Keyframes](#apidoc.module.stylus.nodes.Keyframes)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Keyframes (segs, prefix)](#apidoc.element.stylus.nodes.Keyframes.Keyframes)

#### [module stylus.nodes.Keyframes.prototype](#apidoc.module.stylus.nodes.Keyframes.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Keyframes.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Keyframes.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Keyframes.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Keyframes.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Keyframes.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Keyframes.prototype.toString)

#### [module stylus.nodes.Literal](#apidoc.module.stylus.nodes.Literal)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Literal (str)](#apidoc.element.stylus.nodes.Literal.Literal)

#### [module stylus.nodes.Literal.prototype](#apidoc.module.stylus.nodes.Literal.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Literal.prototype.</span>coerce (other)](#apidoc.element.stylus.nodes.Literal.prototype.coerce)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Literal.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.Literal.prototype.operate)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Literal.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Literal.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Literal.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Literal.prototype.toString)

#### [module stylus.nodes.Media](#apidoc.module.stylus.nodes.Media)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Media (val)](#apidoc.element.stylus.nodes.Media.Media)

#### [module stylus.nodes.Media.prototype](#apidoc.module.stylus.nodes.Media.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Media.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Media.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Media.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Media.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Media.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Media.prototype.toString)

#### [module stylus.nodes.Member](#apidoc.module.stylus.nodes.Member)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Member (left, right)](#apidoc.element.stylus.nodes.Member.Member)

#### [module stylus.nodes.Member.prototype](#apidoc.module.stylus.nodes.Member.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Member.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Member.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Member.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Member.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Member.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Member.prototype.toString)

#### [module stylus.nodes.Namespace](#apidoc.module.stylus.nodes.Namespace)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Namespace (val, prefix)](#apidoc.element.stylus.nodes.Namespace.Namespace)

#### [module stylus.nodes.Namespace.prototype](#apidoc.module.stylus.nodes.Namespace.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Namespace.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Namespace.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Namespace.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Namespace.prototype.toString)

#### [module stylus.nodes.Node](#apidoc.module.stylus.nodes.Node)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Node ()](#apidoc.element.stylus.nodes.Node.Node)

#### [module stylus.nodes.Node.prototype](#apidoc.module.stylus.nodes.Node.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>clone ()](#apidoc.element.stylus.nodes.Node.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>coerce (other)](#apidoc.element.stylus.nodes.Node.prototype.coerce)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>constructor ()](#apidoc.element.stylus.nodes.Node.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>eval ()](#apidoc.element.stylus.nodes.Node.prototype.eval)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.Node.prototype.operate)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>shouldCoerce (op)](#apidoc.element.stylus.nodes.Node.prototype.shouldCoerce)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.Node.prototype.toBoolean)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>toExpression ()](#apidoc.element.stylus.nodes.Node.prototype.toExpression)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Node.prototype.toJSON)
1.  object <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>first
1.  string <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>nodeName

#### [module stylus.nodes.Null](#apidoc.module.stylus.nodes.Null)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Null ()](#apidoc.element.stylus.nodes.Null.Null)

#### [module stylus.nodes.Null.prototype](#apidoc.module.stylus.nodes.Null.prototype)
1.  boolean <span class="apidocSignatureSpan">stylus.nodes.Null.prototype.</span>isNull
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Null.prototype.</span>inspect ()](#apidoc.element.stylus.nodes.Null.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Null.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.Null.prototype.toBoolean)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Null.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Null.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Null.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Null.prototype.toString)
1.  object <span class="apidocSignatureSpan">stylus.nodes.Null.prototype.</span>hash

#### [module stylus.nodes.Object](#apidoc.module.stylus.nodes.Object)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Object ()](#apidoc.element.stylus.nodes.Object.Object)

#### [module stylus.nodes.Object.prototype](#apidoc.module.stylus.nodes.Object.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Object.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>get (key)](#apidoc.element.stylus.nodes.Object.prototype.get)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>has (key)](#apidoc.element.stylus.nodes.Object.prototype.has)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.Object.prototype.operate)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>set (key, val)](#apidoc.element.stylus.nodes.Object.prototype.set)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>toBlock ()](#apidoc.element.stylus.nodes.Object.prototype.toBlock)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.Object.prototype.toBoolean)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Object.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Object.prototype.toString)

#### [module stylus.nodes.Params](#apidoc.module.stylus.nodes.Params)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Params ()](#apidoc.element.stylus.nodes.Params.Params)

#### [module stylus.nodes.Params.prototype](#apidoc.module.stylus.nodes.Params.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Params.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Params.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Params.prototype.</span>push (node)](#apidoc.element.stylus.nodes.Params.prototype.push)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Params.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Params.prototype.toJSON)

#### [module stylus.nodes.Property](#apidoc.module.stylus.nodes.Property)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Property (segs, expr)](#apidoc.element.stylus.nodes.Property.Property)

#### [module stylus.nodes.Property.prototype](#apidoc.module.stylus.nodes.Property.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Property.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Property.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Property.prototype.</span>operate (op, right, val)](#apidoc.element.stylus.nodes.Property.prototype.operate)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Property.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Property.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Property.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Property.prototype.toString)

#### [module stylus.nodes.Query](#apidoc.module.stylus.nodes.Query)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Query ()](#apidoc.element.stylus.nodes.Query.Query)

#### [module stylus.nodes.Query.prototype](#apidoc.module.stylus.nodes.Query.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Query.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Query.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Query.prototype.</span>merge (other)](#apidoc.element.stylus.nodes.Query.prototype.merge)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Query.prototype.</span>push (feature)](#apidoc.element.stylus.nodes.Query.prototype.push)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Query.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Query.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Query.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Query.prototype.toString)

#### [module stylus.nodes.QueryList](#apidoc.module.stylus.nodes.QueryList)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>QueryList ()](#apidoc.element.stylus.nodes.QueryList.QueryList)

#### [module stylus.nodes.QueryList.prototype](#apidoc.module.stylus.nodes.QueryList.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.QueryList.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.QueryList.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.QueryList.prototype.</span>merge (other)](#apidoc.element.stylus.nodes.QueryList.prototype.merge)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.QueryList.prototype.</span>push (node)](#apidoc.element.stylus.nodes.QueryList.prototype.push)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.QueryList.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.QueryList.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.QueryList.prototype.</span>toString ()](#apidoc.element.stylus.nodes.QueryList.prototype.toString)

#### [module stylus.nodes.RGBA](#apidoc.module.stylus.nodes.RGBA)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>RGBA (r, g, b, a)](#apidoc.element.stylus.nodes.RGBA.RGBA)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.RGBA.</span>fromHSLA (hsla)](#apidoc.element.stylus.nodes.RGBA.fromHSLA)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.RGBA.</span>withoutClamping (r, g, b, a)](#apidoc.element.stylus.nodes.RGBA.withoutClamping)

#### [module stylus.nodes.RGBA.prototype](#apidoc.module.stylus.nodes.RGBA.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>add (r, g, b, a)](#apidoc.element.stylus.nodes.RGBA.prototype.add)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>clone ()](#apidoc.element.stylus.nodes.RGBA.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>divide (n)](#apidoc.element.stylus.nodes.RGBA.prototype.divide)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>multiply (n)](#apidoc.element.stylus.nodes.RGBA.prototype.multiply)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.RGBA.prototype.operate)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>sub (r, g, b, a)](#apidoc.element.stylus.nodes.RGBA.prototype.sub)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.RGBA.prototype.toBoolean)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.RGBA.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>toString ()](#apidoc.element.stylus.nodes.RGBA.prototype.toString)
1.  object <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>hsla

#### [module stylus.nodes.Return](#apidoc.module.stylus.nodes.Return)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Return (expr)](#apidoc.element.stylus.nodes.Return.Return)

#### [module stylus.nodes.Return.prototype](#apidoc.module.stylus.nodes.Return.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Return.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Return.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Return.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Return.prototype.toJSON)

#### [module stylus.nodes.Root](#apidoc.module.stylus.nodes.Root)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Root ()](#apidoc.element.stylus.nodes.Root.Root)

#### [module stylus.nodes.Root.prototype](#apidoc.module.stylus.nodes.Root.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Root.prototype.</span>clone ()](#apidoc.element.stylus.nodes.Root.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Root.prototype.</span>push (node)](#apidoc.element.stylus.nodes.Root.prototype.push)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Root.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Root.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Root.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Root.prototype.toString)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Root.prototype.</span>unshift (node)](#apidoc.element.stylus.nodes.Root.prototype.unshift)

#### [module stylus.nodes.Selector](#apidoc.module.stylus.nodes.Selector)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Selector (segs)](#apidoc.element.stylus.nodes.Selector.Selector)

#### [module stylus.nodes.Selector.prototype](#apidoc.module.stylus.nodes.Selector.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Selector.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Selector.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Selector.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Selector.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Selector.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Selector.prototype.toString)

#### [module stylus.nodes.String](#apidoc.module.stylus.nodes.String)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>String (val, quote)](#apidoc.element.stylus.nodes.String.String)

#### [module stylus.nodes.String.prototype](#apidoc.module.stylus.nodes.String.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.String.prototype.</span>clone ()](#apidoc.element.stylus.nodes.String.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.String.prototype.</span>coerce (other)](#apidoc.element.stylus.nodes.String.prototype.coerce)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.String.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.String.prototype.operate)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.String.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.String.prototype.toBoolean)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.String.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.String.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.String.prototype.</span>toString ()](#apidoc.element.stylus.nodes.String.prototype.toString)

#### [module stylus.nodes.Supports](#apidoc.module.stylus.nodes.Supports)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Supports (condition)](#apidoc.element.stylus.nodes.Supports.Supports)

#### [module stylus.nodes.Supports.prototype](#apidoc.module.stylus.nodes.Supports.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Supports.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Supports.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Supports.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Supports.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Supports.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Supports.prototype.toString)

#### [module stylus.nodes.Ternary](#apidoc.module.stylus.nodes.Ternary)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Ternary (cond, trueExpr, falseExpr)](#apidoc.element.stylus.nodes.Ternary.Ternary)

#### [module stylus.nodes.Ternary.prototype](#apidoc.module.stylus.nodes.Ternary.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Ternary.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Ternary.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Ternary.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Ternary.prototype.toJSON)

#### [module stylus.nodes.UnaryOp](#apidoc.module.stylus.nodes.UnaryOp)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>UnaryOp (op, expr)](#apidoc.element.stylus.nodes.UnaryOp.UnaryOp)

#### [module stylus.nodes.UnaryOp.prototype](#apidoc.module.stylus.nodes.UnaryOp.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.UnaryOp.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.UnaryOp.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.UnaryOp.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.UnaryOp.prototype.toJSON)

#### [module stylus.nodes.Unit](#apidoc.module.stylus.nodes.Unit)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.</span>Unit (val, type)](#apidoc.element.stylus.nodes.Unit.Unit)

#### [module stylus.nodes.Unit.prototype](#apidoc.module.stylus.nodes.Unit.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Unit.prototype.</span>clone ()](#apidoc.element.stylus.nodes.Unit.prototype.clone)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Unit.prototype.</span>coerce (other)](#apidoc.element.stylus.nodes.Unit.prototype.coerce)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Unit.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.Unit.prototype.operate)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Unit.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.Unit.prototype.toBoolean)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Unit.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Unit.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">stylus.nodes.Unit.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Unit.prototype.toString)

#### [module stylus.renderer](#apidoc.module.stylus.renderer)
1.  [function <span class="apidocSignatureSpan">stylus.</span>renderer (str, options)](#apidoc.element.stylus.renderer.renderer)
1.  object <span class="apidocSignatureSpan">stylus.renderer.</span>events

#### [module stylus.renderer.prototype](#apidoc.module.stylus.renderer.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>define (name, fn, raw)](#apidoc.element.stylus.renderer.prototype.define)
1.  [function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>deps (filename)](#apidoc.element.stylus.renderer.prototype.deps)
1.  [function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>get (key)](#apidoc.element.stylus.renderer.prototype.get)
1.  [function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>import (file)](#apidoc.element.stylus.renderer.prototype.import)
1.  [function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>include (path)](#apidoc.element.stylus.renderer.prototype.include)
1.  [function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>render (fn)](#apidoc.element.stylus.renderer.prototype.render)
1.  [function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>set (key, val)](#apidoc.element.stylus.renderer.prototype.set)
1.  [function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>use (fn)](#apidoc.element.stylus.renderer.prototype.use)

#### [module stylus.selector_parser](#apidoc.module.stylus.selector_parser)
1.  [function <span class="apidocSignatureSpan">stylus.</span>selector_parser (str, stack, parts)](#apidoc.element.stylus.selector_parser.selector_parser)

#### [module stylus.selector_parser.prototype](#apidoc.module.stylus.selector_parser.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>advance ()](#apidoc.element.stylus.selector_parser.prototype.advance)
1.  [function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>char ()](#apidoc.element.stylus.selector_parser.prototype.char)
1.  [function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>escaped ()](#apidoc.element.stylus.selector_parser.prototype.escaped)
1.  [function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>initial ()](#apidoc.element.stylus.selector_parser.prototype.initial)
1.  [function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>number ()](#apidoc.element.stylus.selector_parser.prototype.number)
1.  [function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>parent ()](#apidoc.element.stylus.selector_parser.prototype.parent)
1.  [function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>parse ()](#apidoc.element.stylus.selector_parser.prototype.parse)
1.  [function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>partial ()](#apidoc.element.stylus.selector_parser.prototype.partial)
1.  [function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>range ()](#apidoc.element.stylus.selector_parser.prototype.range)
1.  [function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>relative (multi)](#apidoc.element.stylus.selector_parser.prototype.relative)
1.  [function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>root ()](#apidoc.element.stylus.selector_parser.prototype.root)
1.  [function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>skip (len)](#apidoc.element.stylus.selector_parser.prototype.skip)
1.  [function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>skipSpaces ()](#apidoc.element.stylus.selector_parser.prototype.skipSpaces)

#### [module stylus.stack](#apidoc.module.stylus.stack)
1.  [function <span class="apidocSignatureSpan">stylus.</span>stack ()](#apidoc.element.stylus.stack.stack)

#### [module stylus.stack.prototype](#apidoc.module.stylus.stack.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.stack.prototype.</span>getBlockFrame (block)](#apidoc.element.stylus.stack.prototype.getBlockFrame)
1.  [function <span class="apidocSignatureSpan">stylus.stack.prototype.</span>inspect ()](#apidoc.element.stylus.stack.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">stylus.stack.prototype.</span>lookup (name)](#apidoc.element.stylus.stack.prototype.lookup)
1.  [function <span class="apidocSignatureSpan">stylus.stack.prototype.</span>push (frame)](#apidoc.element.stylus.stack.prototype.push)
1.  [function <span class="apidocSignatureSpan">stylus.stack.prototype.</span>toString ()](#apidoc.element.stylus.stack.prototype.toString)

#### [module stylus.token](#apidoc.module.stylus.token)
1.  [function <span class="apidocSignatureSpan">stylus.</span>token (type, val)](#apidoc.element.stylus.token.token)

#### [module stylus.token.prototype](#apidoc.module.stylus.token.prototype)
1.  [function <span class="apidocSignatureSpan">stylus.token.prototype.</span>inspect ()](#apidoc.element.stylus.token.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">stylus.token.prototype.</span>toString ()](#apidoc.element.stylus.token.prototype.toString)

#### [module stylus.utils](#apidoc.module.stylus.utils)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>absolute (path)](#apidoc.element.stylus.utils.absolute)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>assertColor (node, param)](#apidoc.element.stylus.utils.assertColor)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>assertPresent (node, name)](#apidoc.element.stylus.utils.assertPresent)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>assertString (node, param)](#apidoc.element.stylus.utils.assertString)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>assertType (node, type, param)](#apidoc.element.stylus.utils.assertType)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>coerce (val, raw)](#apidoc.element.stylus.utils.coerce)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>coerceArray (val, raw)](#apidoc.element.stylus.utils.coerceArray)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>coerceObject (obj, raw)](#apidoc.element.stylus.utils.coerceObject)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>compileSelectors (arr, leaveHidden)](#apidoc.element.stylus.utils.compileSelectors)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>find (path, paths, ignore)](#apidoc.element.stylus.utils.find)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>formatException (err, options)](#apidoc.element.stylus.utils.formatException)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>lookup (path, paths, ignore)](#apidoc.element.stylus.utils.lookup)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>lookupIndex (name, paths, filename)](#apidoc.element.stylus.utils.lookupIndex)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>merge (a, b, deep)](#apidoc.element.stylus.utils.merge)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>params (fn)](#apidoc.element.stylus.utils.params)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>parseString (str)](#apidoc.element.stylus.utils.parseString)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>uniq (arr)](#apidoc.element.stylus.utils.uniq)
1.  [function <span class="apidocSignatureSpan">stylus.utils.</span>unwrap (expr)](#apidoc.element.stylus.utils.unwrap)



# <a name="apidoc.module.stylus"></a>[module stylus](#apidoc.module.stylus)

#### <a name="apidoc.element.stylus.Compiler"></a>[function <span class="apidocSignatureSpan">stylus.</span>Compiler (root, options)](#apidoc.element.stylus.Compiler)
- description and source-code
```javascript
function Compiler(root, options) {
  options = options || {};
  this.compress = options.compress;
  this.firebug = options.firebug;
  this.linenos = options.linenos;
  this.spaces = options['indent spaces'] || 2;
  this.indents = 1;
  Visitor.call(this, root);
  this.stack = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator"></a>[function <span class="apidocSignatureSpan">stylus.</span>Evaluator (root, options)](#apidoc.element.stylus.Evaluator)
- description and source-code
```javascript
function Evaluator(root, options) {
  options = options || {};
  Visitor.call(this, root);
  var functions = this.functions = options.functions || {};
  this.stack = new Stack;
  this.imports = options.imports || [];
  this.globals = options.globals || {};
  this.paths = options.paths || [];
  this.prefix = options.prefix || '';
  this.filename = options.filename;
  this.includeCSS = options['include css'];
  this.resolveURL = functions.url
    && 'resolver' == functions.url.name
    && functions.url.options;
  this.paths.push(dirname(options.filename || '.'));
  this.stack.push(this.global = new Frame(root));
  this.warnings = options.warn;
  this.options = options;
  this.calling = []; // TODO: remove, use stack
  this.importStack = [];
  this.requireHistory = {};
  this.return = 0;
}
```
- example usage
```shell
...

  try {
nodes.filename = this.options.filename;
// parse
var ast = parser.parse();

// evaluate
this.evaluator = new this.options.Evaluator(ast, this.options);
this.nodes = nodes;
this.evaluator.renderer = this;
ast = this.evaluator.evaluate();

// normalize
var normalizer = new Normalizer(ast, this.options);
ast = normalizer.normalize();
...
```

#### <a name="apidoc.element.stylus.Normalizer"></a>[function <span class="apidocSignatureSpan">stylus.</span>Normalizer (root, options)](#apidoc.element.stylus.Normalizer)
- description and source-code
```javascript
function Normalizer(root, options) {
  options = options || {};
  Visitor.call(this, root);
  this.hoist = options['hoist atrules'];
  this.stack = [];
  this.map = {};
  this.imports = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser"></a>[function <span class="apidocSignatureSpan">stylus.</span>Parser (str, options)](#apidoc.element.stylus.Parser)
- description and source-code
```javascript
function Parser(str, options) {
  var self = this;
  options = options || {};
  Parser.cache = Parser.cache || Parser.getCache(options);
  this.hash = Parser.cache.key(str, options);
  this.lexer = {};
  if (!Parser.cache.has(this.hash)) {
    this.lexer = new Lexer(str, options);
  }
  this.prefix = options.prefix || '';
  this.root = options.root || new nodes.Root;
  this.state = ['root'];
  this.stash = [];
  this.parens = 0;
  this.css = 0;
  this.state.pop = function(){
    self.prevState = [].pop.call(this);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Visitor"></a>[function <span class="apidocSignatureSpan">stylus.</span>Visitor (root)](#apidoc.element.stylus.Visitor)
- description and source-code
```javascript
function Visitor(root) {
  this.root = root;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.convertCSS"></a>[function <span class="apidocSignatureSpan">stylus.</span>convertCSS (css)](#apidoc.element.stylus.convertCSS)
- description and source-code
```javascript
convertCSS = function (css){
  return new Converter(css).stylus();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.lexer"></a>[function <span class="apidocSignatureSpan">stylus.</span>lexer (str, options)](#apidoc.element.stylus.lexer)
- description and source-code
```javascript
function Lexer(str, options) {
  options = options || {};
  this.stash = [];
  this.indentStack = [];
  this.indentRe = null;
  this.lineno = 1;
  this.column = 1;

  // HACK!
  function comment(str, val, offset, s) {
    var inComment = s.lastIndexOf('/*', offset) > s.lastIndexOf('*/', offset)
      , commentIdx = s.lastIndexOf('//', offset)
      , i = s.lastIndexOf('\n', offset)
      , double = 0
      , single = 0;

    if (~commentIdx && commentIdx > i) {
      while (i != offset) {
        if ("'" == s[i]) single ? single-- : single++;
        if ('"' == s[i]) double ? double-- : double++;

        if ('/' == s[i] && '/' == s[i + 1]) {
          inComment = !single && !double;
          break;
        }
        ++i;
      }
    }

    return inComment
      ? str
      : val + '\r';
  };

  // Remove UTF-8 BOM.
  if ('\uFEFF' == str.charAt(0)) str = str.slice(1);

  this.str = str
    .replace(/\s+$/, '\n')
    .replace(/\r\n?/g, '\n')
    .replace(/\\ *\n/g, '\r')
    .replace(/([,(:](?!\/\/[^ ])) *(?:\/\/[^\n]*|\/\*.*?\*\/)?\n\s*/g, comment)
    .replace(/\s*\n[ \t]*([,)])/g, comment);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.middleware"></a>[function <span class="apidocSignatureSpan">stylus.</span>middleware (options)](#apidoc.element.stylus.middleware)
- description and source-code
```javascript
middleware = function (options){
  options = options || {};

  // Accept src/dest dir
  if ('string' == typeof options) {
    options = { src: options };
  }

  // Force compilation
  var force = options.force;

  // Source dir required
  var src = options.src;
  if (!src) throw new Error('stylus.middleware() requires "src" directory');

  // Default dest dir to source
  var dest = options.dest || src;

  // Default compile callback
  options.compile = options.compile || function(str, path){
    // inline sourcemap
    if (options.sourcemap) {
      if ('boolean' == typeof options.sourcemap)
        options.sourcemap = {};
      options.sourcemap.inline = true;
    }

    return stylus(str)
      .set('filename', path)
      .set('compress', options.compress)
      .set('firebug', options.firebug)
      .set('linenos', options.linenos)
      .set('sourcemap', options.sourcemap);
  };

  // Middleware
  return function stylus(req, res, next){
    if ('GET' != req.method && 'HEAD' != req.method) return next();
    var path = url.parse(req.url).pathname;
    if (/\.css$/.test(path)) {

      if (typeof dest == 'string') {
        // check for dest-path overlap
        var overlap = compare(dest, path).length;
        if ('/' == path.charAt(0)) overlap++;
        path = path.slice(overlap);
      }

      var cssPath, stylusPath;
      cssPath = (typeof dest == 'function')
        ? dest(path)
        : join(dest, path);
      stylusPath = (typeof src == 'function')
        ? src(path)
        : join(src, path.replace('.css', '.styl'));

      // Ignore ENOENT to fall through as 404
      function error(err) {
        next('ENOENT' == err.code
          ? null
          : err);
      }

      // Force
      if (force) return compile();

      // Compile to cssPath
      function compile() {
        debug('read %s', cssPath);
        fs.readFile(stylusPath, 'utf8', function(err, str){
          if (err) return error(err);
          var style = options.compile(str, stylusPath);
          var paths = style.options._imports = [];
          imports[stylusPath] = null;
          style.render(function(err, css){
            if (err) return next(err);
            debug('render %s', stylusPath);
            imports[stylusPath] = paths;
            mkdirp(dirname(cssPath), parseInt('0700', 8), function(err){
              if (err) return error(err);
              fs.writeFile(cssPath, css, 'utf8', next);
            });
          });
        });
      }

      // Re-compile on server restart, disregarding
      // mtimes since we need to map imports
      if (!imports[stylusPath]) return compile();

      // Compare mtimes
      fs.stat(stylusPath, function(err, stylusStats){
        if (err) return error(err);
        fs.stat(cssPath, function(err, cssStats){
          // CSS has not been compiled, compile it!
          if (err) {
            if ('ENOENT' == err.code) {
              debug('not found %s', cssPath);
              compile();
            } else {
              next(err);
            }
          } else {
            // Source has changed, compile it
            if (stylusStats.mtime > cssStats.mtime) {
              debug('modified %s', cssPath);
              compile();
            // Already compiled, check imports
            } else {
              checkImports(stylusPath, function(changed){
                if (debug && changed.length) {
                  changed.forEach(function(path) {
                    debug('modified import %s', path);
                  });
                }
                changed.length ? compile() : next();
              });
            }
          }
        });
      });
    } else {
      next();
    }
  }
}
```
- example usage
```shell
...
* and saving .css files to _./public_. Also supplying our custom 'compile' function.
*
* Following that we have a 'static()' layer setup to serve the .css
* files generated by Stylus.
*
*      var app = connect();
*
*      app.middleware({
*          src: __dirname
*        , dest: __dirname + '/public'
*        , compile: compile
*      })
*
*      app.use(connect.static(__dirname + '/public'));
*
...
```

#### <a name="apidoc.element.stylus.nodes.Arguments"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Arguments ()](#apidoc.element.stylus.nodes.Arguments)
- description and source-code
```javascript
function Arguments(){
  nodes.Expression.call(this);
  this.map = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Atblock"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Atblock ()](#apidoc.element.stylus.nodes.Atblock)
- description and source-code
```javascript
function Atblock(){
  Node.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Atrule"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Atrule (type)](#apidoc.element.stylus.nodes.Atrule)
- description and source-code
```javascript
function Atrule(type){
  Node.call(this);
  this.type = type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.BinOp"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.BinOp (op, left, right)](#apidoc.element.stylus.nodes.BinOp)
- description and source-code
```javascript
function BinOp(op, left, right){
  Node.call(this);
  this.op = op;
  this.left = left;
  this.right = right;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Block"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Block (parent, node)](#apidoc.element.stylus.nodes.Block)
- description and source-code
```javascript
function Block(parent, node){
  Node.call(this);
  this.nodes = [];
  this.parent = parent;
  this.node = node;
  this.scope = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Boolean"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Boolean (val)](#apidoc.element.stylus.nodes.Boolean)
- description and source-code
```javascript
function Boolean(val){
  Node.call(this);
  if (this.nodeName) {
    this.val = !!val;
  } else {
    return new Boolean(val);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Call"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Call (name, args)](#apidoc.element.stylus.nodes.Call)
- description and source-code
```javascript
function Call(name, args){
  Node.call(this);
  this.name = name;
  this.args = args;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Charset"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Charset (val)](#apidoc.element.stylus.nodes.Charset)
- description and source-code
```javascript
function Charset(val){
  Node.call(this);
  this.val = val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Comment"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Comment (str, suppress, inline)](#apidoc.element.stylus.nodes.Comment)
- description and source-code
```javascript
function Comment(str, suppress, inline){
  Node.call(this);
  this.str = str;
  this.suppress = suppress;
  this.inline = inline;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Each"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Each (val, key, expr, block)](#apidoc.element.stylus.nodes.Each)
- description and source-code
```javascript
function Each(val, key, expr, block){
  Node.call(this);
  this.val = val;
  this.key = key;
  this.expr = expr;
  this.block = block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Expression"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Expression (isList)](#apidoc.element.stylus.nodes.Expression)
- description and source-code
```javascript
function Expression(isList){
  Node.call(this);
  this.nodes = [];
  this.isList = isList;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Extend"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Extend (selectors)](#apidoc.element.stylus.nodes.Extend)
- description and source-code
```javascript
function Extend(selectors){
  Node.call(this);
  this.selectors = selectors;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Feature"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Feature (segs)](#apidoc.element.stylus.nodes.Feature)
- description and source-code
```javascript
function Feature(segs){
  Node.call(this);
  this.segments = segs;
  this.expr = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Function"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Function (name, params, body)](#apidoc.element.stylus.nodes.Function)
- description and source-code
```javascript
function Function(name, params, body){
  Node.call(this);
  this.name = name;
  this.params = params;
  this.block = body;
  if ('function' == typeof params) this.fn = params;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Group"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Group ()](#apidoc.element.stylus.nodes.Group)
- description and source-code
```javascript
function Group(){
  Node.call(this);
  this.nodes = [];
  this.extends = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.HSLA"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.HSLA (h, s, l, a)](#apidoc.element.stylus.nodes.HSLA)
- description and source-code
```javascript
function HSLA(h, s, l, a){
  Node.call(this);
  this.h = clampDegrees(h);
  this.s = clampPercentage(s);
  this.l = clampPercentage(l);
  this.a = clampAlpha(a);
  this.hsla = this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Ident"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Ident (name, val, mixin)](#apidoc.element.stylus.nodes.Ident)
- description and source-code
```javascript
function Ident(name, val, mixin){
  Node.call(this);
  this.name = name;
  this.string = name;
  this.val = val || nodes.null;
  this.mixin = !!mixin;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.If"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.If (cond, negate)](#apidoc.element.stylus.nodes.If)
- description and source-code
```javascript
function If(cond, negate){
  Node.call(this);
  this.cond = cond;
  this.elses = [];
  if (negate && negate.nodeName) {
    this.block = negate;
  } else {
    this.negate = negate;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Import"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Import (expr, once)](#apidoc.element.stylus.nodes.Import)
- description and source-code
```javascript
function Import(expr, once){
  Node.call(this);
  this.path = expr;
  this.once = once || false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Keyframes"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Keyframes (segs, prefix)](#apidoc.element.stylus.nodes.Keyframes)
- description and source-code
```javascript
function Keyframes(segs, prefix){
  Atrule.call(this, 'keyframes');
  this.segments = segs;
  this.prefix = prefix || 'official';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Literal"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Literal (str)](#apidoc.element.stylus.nodes.Literal)
- description and source-code
```javascript
function Literal(str){
  Node.call(this);
  this.val = str;
  this.string = str;
  this.prefixed = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Media"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Media (val)](#apidoc.element.stylus.nodes.Media)
- description and source-code
```javascript
function Media(val){
  Atrule.call(this, 'media');
  this.val = val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Member"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Member (left, right)](#apidoc.element.stylus.nodes.Member)
- description and source-code
```javascript
function Member(left, right){
  Node.call(this);
  this.left = left;
  this.right = right;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Namespace"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Namespace (val, prefix)](#apidoc.element.stylus.nodes.Namespace)
- description and source-code
```javascript
function Namespace(val, prefix){
  Node.call(this);
  this.val = val;
  this.prefix = prefix;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Node"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Node ()](#apidoc.element.stylus.nodes.Node)
- description and source-code
```javascript
function Node(){
  this.lineno = nodes.lineno || 1;
  this.column = nodes.column || 1;
  this.filename = nodes.filename;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Null"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Null ()](#apidoc.element.stylus.nodes.Null)
- description and source-code
```javascript
function Null(){}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Object"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Object ()](#apidoc.element.stylus.nodes.Object)
- description and source-code
```javascript
function Object(){
  Node.call(this);
  this.vals = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Params"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Params ()](#apidoc.element.stylus.nodes.Params)
- description and source-code
```javascript
function Params(){
  Node.call(this);
  this.nodes = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Property"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Property (segs, expr)](#apidoc.element.stylus.nodes.Property)
- description and source-code
```javascript
function Property(segs, expr){
  Node.call(this);
  this.segments = segs;
  this.expr = expr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Query"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Query ()](#apidoc.element.stylus.nodes.Query)
- description and source-code
```javascript
function Query(){
  Node.call(this);
  this.nodes = [];
  this.type = '';
  this.predicate = '';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.QueryList"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.QueryList ()](#apidoc.element.stylus.nodes.QueryList)
- description and source-code
```javascript
function QueryList(){
  Node.call(this);
  this.nodes = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.RGBA"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.RGBA (r, g, b, a)](#apidoc.element.stylus.nodes.RGBA)
- description and source-code
```javascript
function RGBA(r, g, b, a){
  Node.call(this);
  this.r = clamp(r);
  this.g = clamp(g);
  this.b = clamp(b);
  this.a = clampAlpha(a);
  this.name = '';
  this.rgba = this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Return"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Return (expr)](#apidoc.element.stylus.nodes.Return)
- description and source-code
```javascript
function Return(expr){
  this.expr = expr || nodes.null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Root"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Root ()](#apidoc.element.stylus.nodes.Root)
- description and source-code
```javascript
function Root(){
  this.nodes = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Selector"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Selector (segs)](#apidoc.element.stylus.nodes.Selector)
- description and source-code
```javascript
function Selector(segs){
  Node.call(this);
  this.inherits = true;
  this.segments = segs;
  this.optional = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.String"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.String (val, quote)](#apidoc.element.stylus.nodes.String)
- description and source-code
```javascript
function String(val, quote){
  Node.call(this);
  this.val = val;
  this.string = val;
  this.prefixed = false;
  if (typeof quote !== 'string') {
    this.quote = "'";
  } else {
    this.quote = quote;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Supports"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Supports (condition)](#apidoc.element.stylus.nodes.Supports)
- description and source-code
```javascript
function Supports(condition){
  Atrule.call(this, 'supports');
  this.condition = condition;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Ternary"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Ternary (cond, trueExpr, falseExpr)](#apidoc.element.stylus.nodes.Ternary)
- description and source-code
```javascript
function Ternary(cond, trueExpr, falseExpr){
  Node.call(this);
  this.cond = cond;
  this.trueExpr = trueExpr;
  this.falseExpr = falseExpr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.UnaryOp"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.UnaryOp (op, expr)](#apidoc.element.stylus.nodes.UnaryOp)
- description and source-code
```javascript
function UnaryOp(op, expr){
  Node.call(this);
  this.op = op;
  this.expr = expr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Unit"></a>[function <span class="apidocSignatureSpan">stylus.</span>nodes.Unit (val, type)](#apidoc.element.stylus.nodes.Unit)
- description and source-code
```javascript
function Unit(val, type){
  Node.call(this);
  this.val = val;
  this.type = type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.render"></a>[function <span class="apidocSignatureSpan">stylus.</span>render (str, options, fn)](#apidoc.element.stylus.render)
- description and source-code
```javascript
render = function (str, options, fn){
  if ('function' == typeof options) fn = options, options = {};
  return new Renderer(str, options).render(fn);
}
```
- example usage
```shell
...
      function compile() {
debug('read %s', cssPath);
fs.readFile(stylusPath, 'utf8', function(err, str){
  if (err) return error(err);
  var style = options.compile(str, stylusPath);
  var paths = style.options._imports = [];
  imports[stylusPath] = null;
  style.render(function(err, css){
    if (err) return next(err);
    debug('render %s', stylusPath);
    imports[stylusPath] = paths;
    mkdirp(dirname(cssPath), parseInt('0700', 8), function(err){
      if (err) return error(err);
      fs.writeFile(cssPath, css, 'utf8', next);
    });
...
```

#### <a name="apidoc.element.stylus.renderer"></a>[function <span class="apidocSignatureSpan">stylus.</span>renderer (str, options)](#apidoc.element.stylus.renderer)
- description and source-code
```javascript
function Renderer(str, options) {
  options = options || {};
  options.globals = options.globals || {};
  options.functions = options.functions || {};
  options.use = options.use || [];
  options.use = Array.isArray(options.use) ? options.use : [options.use];
  options.imports = [join(__dirname, 'functions')];
  options.paths = options.paths || [];
  options.filename = options.filename || 'stylus';
  options.Evaluator = options.Evaluator || Evaluator;
  this.options = options;
  this.str = str;
  this.events = events;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.resolver"></a>[function <span class="apidocSignatureSpan">stylus.</span>resolver (options)](#apidoc.element.stylus.resolver)
- description and source-code
```javascript
resolver = function (options) {
  options = options || {};

  function resolver(url) {
    // Compile the url
    var compiler = new Compiler(url)
      , filename = url.filename;
    compiler.isURL = true;
    url = parse(url.nodes.map(function(node){
      return compiler.visit(node);
    }).join(''));

    // Parse literal
    var literal = new nodes.Literal('url("' + url.href + '")')
      , path = url.pathname
      , dest = this.options.dest
      , tail = ''
      , res;

    // Absolute or hash
    if (url.protocol || !path || '/' == path[0]) return literal;

    // Check that file exists
    if (!options.nocheck) {
      var _paths = options.paths || [];
      path = require('../utils').lookup(path, _paths.concat(this.paths));
      if (!path) return literal;
    }

    if (this.includeCSS && extname(path) == '.css')
      return new nodes.Literal(url.href);

    if (url.search) tail += url.search;
    if (url.hash) tail += url.hash;

    if (dest && extname(dest) == '.css')
      dest = dirname(dest);

    res = relative(dest || dirname(this.filename), options.nocheck
      ? join(dirname(filename), path)
      : path) + tail;

    if ('\\' == sep) res = res.replace(/\\/g, '/');

    return new nodes.Literal('url("' + res + '")');
  };

  // Expose options to Evaluator
  resolver.options = options;
  resolver.raw = true;
  return resolver;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.selector_parser"></a>[function <span class="apidocSignatureSpan">stylus.</span>selector_parser (str, stack, parts)](#apidoc.element.stylus.selector_parser)
- description and source-code
```javascript
function SelectorParser(str, stack, parts) {
  this.str = str;
  this.stack = stack || [];
  this.parts = parts || [];
  this.pos = 0;
  this.level = 2;
  this.nested = true;
  this.ignore = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.stack"></a>[function <span class="apidocSignatureSpan">stylus.</span>stack ()](#apidoc.element.stylus.stack)
- description and source-code
```javascript
function Stack() {
  Array.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.token"></a>[function <span class="apidocSignatureSpan">stylus.</span>token (type, val)](#apidoc.element.stylus.token)
- description and source-code
```javascript
function Token(type, val) {
  this.type = type;
  this.val = val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.url"></a>[function <span class="apidocSignatureSpan">stylus.</span>url (options)](#apidoc.element.stylus.url)
- description and source-code
```javascript
url = function (options) {
  options = options || {};

  var _paths = options.paths || [];
  var sizeLimit = null != options.limit ? options.limit : 30000;
  var mimes = options.mimes || defaultMimes;

<span class="apidocCodeCommentSpan">  /**
   * @param {object} url - The path to the image you want to encode.
   * @param {object} enc - The encoding for the image. Defaults to base64, the
   * other valid option is 'utf8'.
   */
</span>  function fn(url, enc){
    // Compile the url
    var compiler = new Compiler(url)
      , encoding = encodingTypes.BASE_64;

    compiler.isURL = true;
    url = url.nodes.map(function(node){
      return compiler.visit(node);
    }).join('');

    // Parse literal
    url = parse(url);
    var ext = extname(url.pathname)
      , mime = mimes[ext]
      , hash = url.hash || ''
      , literal = new nodes.Literal('url("' + url.href + '")')
      , paths = _paths.concat(this.paths)
      , buf
      , result;

    // Not supported
    if (!mime) return literal;

    // Absolute
    if (url.protocol) return literal;

    // Lookup
    var found = utils.lookup(url.pathname, paths);

    // Failed to lookup
    if (!found) {
      events.emit(
          'file not found'
        , 'File ' + literal + ' could not be found, literal url retained!'
      );

      return literal;
    }

    // Read data
    buf = fs.readFileSync(found);

    // Too large
    if (false !== sizeLimit && buf.length > sizeLimit) return literal;

    if (enc && 'utf8' == enc.first.val.toLowerCase()) {
      encoding = encodingTypes.UTF8;
      result = buf.toString('utf8').replace(/\s+/g, ' ')
        .replace(/[{}\|\\\^~\[\]'"<>#%]/g, function(match) {
          return '%' + match[0].charCodeAt(0).toString(16).toUpperCase();
        }).trim();
    } else {
      result = buf.toString(encoding) + hash;
    }

    // Encode
    return new nodes.Literal('url("data:' + mime + ';' +  encoding + ',' + result + '")');
  };

  fn.raw = true;
  return fn;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.Compiler"></a>[module stylus.Compiler](#apidoc.module.stylus.Compiler)

#### <a name="apidoc.element.stylus.Compiler.Compiler"></a>[function <span class="apidocSignatureSpan">stylus.</span>Compiler (root, options)](#apidoc.element.stylus.Compiler.Compiler)
- description and source-code
```javascript
function Compiler(root, options) {
  options = options || {};
  this.compress = options.compress;
  this.firebug = options.firebug;
  this.linenos = options.linenos;
  this.spaces = options['indent spaces'] || 2;
  this.indents = 1;
  Visitor.call(this, root);
  this.stack = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.Compiler.prototype"></a>[module stylus.Compiler.prototype](#apidoc.module.stylus.Compiler.prototype)

#### <a name="apidoc.element.stylus.Compiler.prototype.compile"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>compile ()](#apidoc.element.stylus.Compiler.prototype.compile)
- description and source-code
```javascript
compile = function (){
  return this.visit(this.root);
}
```
- example usage
```shell
...
if (force) return compile();

// Compile to cssPath
function compile() {
  debug('read %s', cssPath);
  fs.readFile(stylusPath, 'utf8', function(err, str){
    if (err) return error(err);
    var style = options.compile(str, stylusPath);
    var paths = style.options._imports = [];
    imports[stylusPath] = null;
    style.render(function(err, css){
      if (err) return next(err);
      debug('render %s', stylusPath);
      imports[stylusPath] = paths;
      mkdirp(dirname(cssPath), parseInt('0700', 8), function(err){
...
```

#### <a name="apidoc.element.stylus.Compiler.prototype.debugInfo"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>debugInfo (node)](#apidoc.element.stylus.Compiler.prototype.debugInfo)
- description and source-code
```javascript
debugInfo = function (node){

  var path = node.filename == 'stdin' ? 'stdin' : fs.realpathSync(node.filename)
    , line = (node.nodes && node.nodes.length ? node.nodes[0].lineno : node.lineno) || 1;

  if (this.linenos){
    this.buf += '\n/* ' + 'line ' + line + ' : ' + path + ' */\n';
  }

  if (this.firebug){
    // debug info for firebug, the crazy formatting is needed
    path = 'file\\\:\\\/\\\/' + path.replace(/([.:/\\])/g, function(m) {
      return '\\' + (m === '\\' ? '\/' : m)
    });
    line = '\\00003' + line;
    this.buf += '\n@media -stylus-debug-info'
      + '{filename{font-family:' + path
      + '}line{font-family:' + line + '}}\n';
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.needBrackets"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>needBrackets (node)](#apidoc.element.stylus.Compiler.prototype.needBrackets)
- description and source-code
```javascript
needBrackets = function (node){
  return 1 == this.indents
    || 'atrule' != node.nodeName
    || node.hasOnlyProperties;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.out"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>out (str, node)](#apidoc.element.stylus.Compiler.prototype.out)
- description and source-code
```javascript
out = function (str, node){
  return str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitArguments"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitArguments (expr)](#apidoc.element.stylus.Compiler.prototype.visitArguments)
- description and source-code
```javascript
visitArguments = function (expr){
  var buf = []
    , self = this
    , len = expr.nodes.length
    , nodes = expr.nodes.map(function(node){ return self.visit(node); });

  nodes.forEach(function(node, i){
    var last = i == len - 1;
    buf.push(node);
    if ('/' == nodes[i + 1] || '/' == node) return;
    if (last) return;

    var space = self.isURL || (self.isCondition
        && (')' == nodes[i + 1] || '(' == node))
        ? '' : ' ';

    buf.push(expr.isList
      ? (self.compress ? ',' : ', ')
      : space);
  });

  return buf.join('');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitAtrule"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitAtrule (atrule)](#apidoc.element.stylus.Compiler.prototype.visitAtrule)
- description and source-code
```javascript
visitAtrule = function (atrule){
  var newline = this.compress ? '' : '\n';

  this.buf += this.out(this.indent + '@' + atrule.type, atrule);

  if (atrule.val) this.buf += this.out(' ' + atrule.val.trim());

  if (atrule.block) {
    if (atrule.hasOnlyProperties) {
      this.visit(atrule.block);
    } else {
      this.buf += this.out(this.compress ? '{' : ' {\n');
      ++this.indents;
      this.visit(atrule.block);
      --this.indents;
      this.buf += this.out(this.indent + '}' + newline);
    }
  } else {
    this.buf += this.out(';' + newline);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitBlock"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitBlock (block)](#apidoc.element.stylus.Compiler.prototype.visitBlock)
- description and source-code
```javascript
visitBlock = function (block){
  var node
    , separator = this.compress ? '' : '\n'
    , needBrackets;

  if (block.hasProperties && !block.lacksRenderedSelectors) {
    needBrackets = this.needBrackets(block.node);

    if (needBrackets) {
      this.buf += this.out(this.compress ? '{' : ' {\n');
      ++this.indents;
    }
    for (var i = 0, len = block.nodes.length; i < len; ++i) {
      this.last = len - 1 == i;
      node = block.nodes[i];
      switch (node.nodeName) {
        case 'null':
        case 'expression':
        case 'function':
        case 'group':
        case 'block':
        case 'unit':
        case 'media':
        case 'keyframes':
        case 'atrule':
        case 'supports':
          continue;
        // inline comments
        case !this.compress && node.inline && 'comment':
          this.buf = this.buf.slice(0, -1);
          this.buf += this.out(' ' + this.visit(node) + '\n', node);
          break;
        case 'property':
          var ret = this.visit(node) + separator;
          this.buf += this.compress ? ret : this.out(ret, node);
          break;
        default:
          this.buf += this.out(this.visit(node) + separator, node);
      }
    }
    if (needBrackets) {
      --this.indents;
      this.buf += this.out(this.indent + '}' + separator);
    }
  }

  // Nesting
  for (var i = 0, len = block.nodes.length; i < len; ++i) {
    node = block.nodes[i];
    switch (node.nodeName) {
      case 'group':
      case 'block':
      case 'keyframes':
        if (this.linenos || this.firebug) this.debugInfo(node);
        this.visit(node);
        break;
      case 'media':
      case 'import':
      case 'atrule':
      case 'supports':
        this.visit(node);
        break;
      case 'comment':
        // only show unsuppressed comments
        if (!node.suppress) {
          this.buf += this.out(this.indent + this.visit(node) + '\n', node);
        }
        break;
      case 'charset':
      case 'literal':
      case 'namespace':
        this.buf += this.out(this.visit(node) + '\n', node);
        break;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitBoolean"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitBoolean (bool)](#apidoc.element.stylus.Compiler.prototype.visitBoolean)
- description and source-code
```javascript
visitBoolean = function (bool){
  return bool.toString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitCall"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitCall (call)](#apidoc.element.stylus.Compiler.prototype.visitCall)
- description and source-code
```javascript
visitCall = function (call){
  this.isURL = 'url' == call.name;
  var args = call.args.nodes.map(function(arg){
    return this.visit(arg);
  }, this).join(this.compress ? ',' : ', ');
  if (this.isURL) args = '"' + args + '"';
  this.isURL = false;
  return call.name + '(' + args + ')';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitCharset"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitCharset (charset)](#apidoc.element.stylus.Compiler.prototype.visitCharset)
- description and source-code
```javascript
visitCharset = function (charset){
  return '@charset ' + this.visit(charset.val) + ';';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitComment"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitComment (comment)](#apidoc.element.stylus.Compiler.prototype.visitComment)
- description and source-code
```javascript
visitComment = function (comment){
  return this.compress
    ? comment.suppress
      ? ''
      : comment.str
    : comment.str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitExpression"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitExpression (expr)](#apidoc.element.stylus.Compiler.prototype.visitExpression)
- description and source-code
```javascript
visitExpression = function (expr){
  var buf = []
    , self = this
    , len = expr.nodes.length
    , nodes = expr.nodes.map(function(node){ return self.visit(node); });

  nodes.forEach(function(node, i){
    var last = i == len - 1;
    buf.push(node);
    if ('/' == nodes[i + 1] || '/' == node) return;
    if (last) return;

    var space = self.isURL || (self.isCondition
        && (')' == nodes[i + 1] || '(' == node))
        ? '' : ' ';

    buf.push(expr.isList
      ? (self.compress ? ',' : ', ')
      : space);
  });

  return buf.join('');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitFeature"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitFeature (node)](#apidoc.element.stylus.Compiler.prototype.visitFeature)
- description and source-code
```javascript
visitFeature = function (node){
  if (!node.expr) {
    return node.name;
  } else if (node.expr.isEmpty) {
    return '(' + node.name + ')';
  } else {
    return '(' + node.name + ':' + (this.compress ? '' : ' ') + this.visit(node.expr) + ')';
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitFunction"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitFunction (fn)](#apidoc.element.stylus.Compiler.prototype.visitFunction)
- description and source-code
```javascript
visitFunction = function (fn){
  return fn.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitGroup"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitGroup (group)](#apidoc.element.stylus.Compiler.prototype.visitGroup)
- description and source-code
```javascript
visitGroup = function (group){
  var stack = this.keyframe ? [] : this.stack
    , comma = this.compress ? ',' : ',\n';

  stack.push(group.nodes);

  // selectors
  if (group.block.hasProperties) {
    var selectors = utils.compileSelectors.call(this, stack)
      , len = selectors.length;

    if (len) {
      if (this.keyframe) comma = this.compress ? ',' : ', ';

      for (var i = 0; i < len; ++i) {
        var selector = selectors[i]
          , last = (i == len - 1);

        // keyframe blocks (10%, 20% { ... })
        if (this.keyframe) selector = i ? selector.trim() : selector;

        this.buf += this.out(selector + (last ? '' : comma), group.nodes[i]);
      }
    } else {
      group.block.lacksRenderedSelectors = true;
    }
  }

  // output block
  this.visit(group.block);
  stack.pop();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitHSLA"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitHSLA (hsla)](#apidoc.element.stylus.Compiler.prototype.visitHSLA)
- description and source-code
```javascript
visitHSLA = function (hsla){
  return hsla.rgba.toString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitIdent"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitIdent (ident)](#apidoc.element.stylus.Compiler.prototype.visitIdent)
- description and source-code
```javascript
visitIdent = function (ident){
  return ident.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitImport"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitImport (imported)](#apidoc.element.stylus.Compiler.prototype.visitImport)
- description and source-code
```javascript
visitImport = function (imported){
  this.buf += this.out('@import ' + this.visit(imported.path) + ';\n', imported);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitKeyframes"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitKeyframes (node)](#apidoc.element.stylus.Compiler.prototype.visitKeyframes)
- description and source-code
```javascript
visitKeyframes = function (node){
  if (!node.frames) return;

  var prefix = 'official' == node.prefix
    ? ''
    : '-' + node.prefix + '-';

  this.buf += this.out('@' + prefix + 'keyframes '
    + this.visit(node.val)
    + (this.compress ? '{' : ' {\n'), node);

  this.keyframe = true;
  ++this.indents;
  this.visit(node.block);
  --this.indents;
  this.keyframe = false;

  this.buf += this.out('}' + (this.compress ? '' : '\n'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitLiteral"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitLiteral (lit)](#apidoc.element.stylus.Compiler.prototype.visitLiteral)
- description and source-code
```javascript
visitLiteral = function (lit){
  var val = lit.val;
  if (lit.css) val = val.replace(/^  /gm, '');
  return val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitMedia"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitMedia (media)](#apidoc.element.stylus.Compiler.prototype.visitMedia)
- description and source-code
```javascript
visitMedia = function (media){
  var val = media.val;
  if (!media.hasOutput || !val.nodes.length) return;

  this.buf += this.out('@media ', media);
  this.visit(val);
  this.buf += this.out(this.compress ? '{' : ' {\n');
  ++this.indents;
  this.visit(media.block);
  --this.indents;
  this.buf += this.out('}' + (this.compress ? '' : '\n'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitNamespace"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitNamespace (namespace)](#apidoc.element.stylus.Compiler.prototype.visitNamespace)
- description and source-code
```javascript
visitNamespace = function (namespace){
  return '@namespace '
    + (namespace.prefix ? this.visit(namespace.prefix) + ' ' : '')
    + this.visit(namespace.val) + ';';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitNull"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitNull (node)](#apidoc.element.stylus.Compiler.prototype.visitNull)
- description and source-code
```javascript
visitNull = function (node){
  return '';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitProperty"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitProperty (prop)](#apidoc.element.stylus.Compiler.prototype.visitProperty)
- description and source-code
```javascript
visitProperty = function (prop){
  var val = this.visit(prop.expr).trim()
    , name = (prop.name || prop.segments.join(''))
    , arr = [];
  arr.push(
    this.out(this.indent),
    this.out(name + (this.compress ? ':' : ': '), prop),
    this.out(val, prop.expr),
    this.out(this.compress ? (this.last ? '' : ';') : ';')
  );
  return arr.join('');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitQuery"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitQuery (node)](#apidoc.element.stylus.Compiler.prototype.visitQuery)
- description and source-code
```javascript
visitQuery = function (node){
  var len = node.nodes.length;
  if (node.predicate) this.buf += this.out(node.predicate + ' ');
  if (node.type) this.buf += this.out(node.type + (len ? ' and ' : ''));
  for (var i = 0; i < len; ++i) {
    this.buf += this.out(this.visit(node.nodes[i]));
    if (len - 1 != i) this.buf += this.out(' and ');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitQueryList"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitQueryList (queries)](#apidoc.element.stylus.Compiler.prototype.visitQueryList)
- description and source-code
```javascript
visitQueryList = function (queries){
  for (var i = 0, len = queries.nodes.length; i < len; ++i) {
    this.visit(queries.nodes[i]);
    if (len - 1 != i) this.buf += this.out(',' + (this.compress ? '' : ' '));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitRGBA"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitRGBA (rgba)](#apidoc.element.stylus.Compiler.prototype.visitRGBA)
- description and source-code
```javascript
visitRGBA = function (rgba){
  return rgba.toString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitRoot"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitRoot (block)](#apidoc.element.stylus.Compiler.prototype.visitRoot)
- description and source-code
```javascript
visitRoot = function (block){
  this.buf = '';
  for (var i = 0, len = block.nodes.length; i < len; ++i) {
    var node = block.nodes[i];
    if (this.linenos || this.firebug) this.debugInfo(node);
    var ret = this.visit(node);
    if (ret) this.buf += this.out(ret + '\n', node);
  }
  return this.buf;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitString"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitString (string)](#apidoc.element.stylus.Compiler.prototype.visitString)
- description and source-code
```javascript
visitString = function (string){
  return this.isURL
    ? string.val
    : string.toString();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitSupports"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitSupports (node)](#apidoc.element.stylus.Compiler.prototype.visitSupports)
- description and source-code
```javascript
visitSupports = function (node){
  if (!node.hasOutput) return;

  this.buf += this.out(this.indent + '@supports ', node);
  this.isCondition = true;
  this.buf += this.out(this.visit(node.condition));
  this.isCondition = false;
  this.buf += this.out(this.compress ? '{' : ' {\n');
  ++this.indents;
  this.visit(node.block);
  --this.indents;
  this.buf += this.out(this.indent + '}' + (this.compress ? '' : '\n'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Compiler.prototype.visitUnit"></a>[function <span class="apidocSignatureSpan">stylus.Compiler.prototype.</span>visitUnit (unit)](#apidoc.element.stylus.Compiler.prototype.visitUnit)
- description and source-code
```javascript
visitUnit = function (unit){
  var type = unit.type || ''
    , n = unit.val
    , float = n != (n | 0);

  // Compress
  if (this.compress) {
    // Always return '0' unless the unit is a percentage or time
    if ('%' != type && 's' != type && 'ms' != type && 0 == n) return '0';
    // Omit leading '0' on floats
    if (float && n < 1 && n > -1) {
      return n.toString().replace('0.', '.') + type;
    }
  }

  return (float ? parseFloat(n.toFixed(15)) : n).toString() + type;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.Evaluator"></a>[module stylus.Evaluator](#apidoc.module.stylus.Evaluator)

#### <a name="apidoc.element.stylus.Evaluator.Evaluator"></a>[function <span class="apidocSignatureSpan">stylus.</span>Evaluator (root, options)](#apidoc.element.stylus.Evaluator.Evaluator)
- description and source-code
```javascript
function Evaluator(root, options) {
  options = options || {};
  Visitor.call(this, root);
  var functions = this.functions = options.functions || {};
  this.stack = new Stack;
  this.imports = options.imports || [];
  this.globals = options.globals || {};
  this.paths = options.paths || [];
  this.prefix = options.prefix || '';
  this.filename = options.filename;
  this.includeCSS = options['include css'];
  this.resolveURL = functions.url
    && 'resolver' == functions.url.name
    && functions.url.options;
  this.paths.push(dirname(options.filename || '.'));
  this.stack.push(this.global = new Frame(root));
  this.warnings = options.warn;
  this.options = options;
  this.calling = []; // TODO: remove, use stack
  this.importStack = [];
  this.requireHistory = {};
  this.return = 0;
}
```
- example usage
```shell
...

  try {
nodes.filename = this.options.filename;
// parse
var ast = parser.parse();

// evaluate
this.evaluator = new this.options.Evaluator(ast, this.options);
this.nodes = nodes;
this.evaluator.renderer = this;
ast = this.evaluator.evaluate();

// normalize
var normalizer = new Normalizer(ast, this.options);
ast = normalizer.normalize();
...
```



# <a name="apidoc.module.stylus.Evaluator.prototype"></a>[module stylus.Evaluator.prototype](#apidoc.module.stylus.Evaluator.prototype)

#### <a name="apidoc.element.stylus.Evaluator.prototype._mixin"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>_mixin (items, dest, block)](#apidoc.element.stylus.Evaluator.prototype._mixin)
- description and source-code
```javascript
_mixin = function (items, dest, block){
  var node
    , len = items.length;
  for (var i = 0; i < len; ++i) {
    switch ((node = items[i]).nodeName) {
      case 'return':
        return;
      case 'block':
        this._mixin(node.nodes, dest, block);
        break;
      case 'media':
        // fix link to the parent block
        var parentNode = node.block.parent.node;
        if (parentNode && 'call' != parentNode.nodeName) {
          node.block.parent = block;
        }
      case 'property':
        var val = node.expr;
        // prevent 'block' mixin recursion
        if (node.literal && 'block' == val.first.name) {
          val = utils.unwrap(val);
          val.nodes[0] = new nodes.Literal('block');
        }
      default:
        dest.push(node);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.cast"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>cast (expr)](#apidoc.element.stylus.Evaluator.prototype.cast)
- description and source-code
```javascript
cast = function (expr){
  return new nodes.Unit(expr.first.val, expr.nodes[1].name);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.castable"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>castable (expr)](#apidoc.element.stylus.Evaluator.prototype.castable)
- description and source-code
```javascript
castable = function (expr){
  return 2 == expr.nodes.length
    && 'unit' == expr.first.nodeName
    && ~units.indexOf(expr.nodes[1].name);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.eval"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>eval (vals)](#apidoc.element.stylus.Evaluator.prototype.eval)
- description and source-code
```javascript
eval = function (vals){
  if (!vals) return nodes.null;
  var len = vals.length
    , node = nodes.null;

  try {
    for (var i = 0; i < len; ++i) {
      node = vals[i];
      switch (node.nodeName) {
        case 'if':
          if ('block' != node.block.nodeName) {
            node = this.visit(node);
            break;
          }
        case 'each':
        case 'block':
          node = this.visit(node);
          if (node.nodes) node = this.eval(node.nodes);
          break;
        default:
          node = this.visit(node);
      }
    }
  } catch (err) {
    if ('return' == err.nodeName) {
      return err.expr;
    } else {
      throw err;
    }
  }

  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.evaluate"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>evaluate ()](#apidoc.element.stylus.Evaluator.prototype.evaluate)
- description and source-code
```javascript
evaluate = function (){
  debug('eval %s', this.filename);
  this.setup();
  return this.visit(this.root);
}
```
- example usage
```shell
...
// parse
var ast = parser.parse();

// evaluate
this.evaluator = new this.options.Evaluator(ast, this.options);
this.nodes = nodes;
this.evaluator.renderer = this;
ast = this.evaluator.evaluate();

// normalize
var normalizer = new Normalizer(ast, this.options);
ast = normalizer.normalize();

// compile
var compiler = this.options.sourcemap
...
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.interpolate"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>interpolate (node)](#apidoc.element.stylus.Evaluator.prototype.interpolate)
- description and source-code
```javascript
interpolate = function (node){
  var self = this
    , isSelector = ('selector' == node.nodeName);
  function toString(node) {
    switch (node.nodeName) {
      case 'function':
      case 'ident':
        return node.name;
      case 'literal':
      case 'string':
        if (self.prefix && !node.prefixed && !node.val.nodeName) {
          node.val = node.val.replace(/\./g, '.' + self.prefix);
          node.prefixed = true;
        }
        return node.val;
      case 'unit':
        // Interpolation inside keyframes
        return '%' == node.type ? node.val + '%' : node.val;
      case 'member':
        return toString(self.visit(node));
      case 'expression':
        // Prevent cyclic 'selector()' calls.
        if (self.calling && ~self.calling.indexOf('selector') && self._selector) return self._selector;
        self.return++;
        var ret = toString(self.visit(node).first);
        self.return--;
        if (isSelector) self._selector = ret;
        return ret;
    }
  }

  if (node.segments) {
    return node.segments.map(toString).join('');
  } else {
    return toString(node);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.invoke"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>invoke (body, stack, filename)](#apidoc.element.stylus.Evaluator.prototype.invoke)
- description and source-code
```javascript
invoke = function (body, stack, filename){
  var self = this
    , ret;

  if (filename) this.paths.push(dirname(filename));

  // Return
  if (this.return) {
    ret = this.eval(body.nodes);
    if (stack) this.stack.pop();
  // Mixin
  } else {
    body = this.visit(body);
    if (stack) this.stack.pop();
    this.mixin(body.nodes, this.currentBlock);
    ret = nodes.null;
  }

  if (filename) this.paths.pop();

  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.invokeBuiltin"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>invokeBuiltin (fn, args)](#apidoc.element.stylus.Evaluator.prototype.invokeBuiltin)
- description and source-code
```javascript
invokeBuiltin = function (fn, args){
  // Map arguments to first node
  // providing a nicer js api for
  // BIFs. Functions may specify that
  // they wish to accept full expressions
  // via .raw
  if (fn.raw) {
    args = args.nodes;
  } else {
    args = utils.params(fn).reduce(function(ret, param){
      var arg = args.map[param] || args.nodes.shift()
      if (arg) {
        arg = utils.unwrap(arg);
        var len = arg.nodes.length;
        if (len > 1) {
          for (var i = 0; i < len; ++i) {
            ret.push(utils.unwrap(arg.nodes[i].first));
          }
        } else {
          ret.push(arg.first);
        }
      }
      return ret;
    }, []);
  }

  // Invoke the BIF
  var body = utils.coerce(fn.apply(this, args));

  // Always wrapping allows js functions
  // to return several values with a single
  // Expression node
  var expr = new nodes.Expression;
  expr.push(body);
  body = expr;

  // Invoke
  return this.invoke(body);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.invokeFunction"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>invokeFunction (fn, args, content)](#apidoc.element.stylus.Evaluator.prototype.invokeFunction)
- description and source-code
```javascript
invokeFunction = function (fn, args, content){
  var block = new nodes.Block(fn.block.parent);

  // Clone the function body
  // to prevent mutation of subsequent calls
  var body = fn.block.clone(block);

  // mixin block
  var mixinBlock = this.stack.currentFrame.block;

  // new block scope
  this.stack.push(new Frame(block));
  var scope = this.currentScope;

  // normalize arguments
  if ('arguments' != args.nodeName) {
    var expr = new nodes.Expression;
    expr.push(args);
    args = nodes.Arguments.fromExpression(expr);
  }

  // arguments local
  scope.add(new nodes.Ident('arguments', args));

  // mixin scope introspection
  scope.add(new nodes.Ident('mixin', this.return
    ? nodes.false
    : new nodes.String(mixinBlock.nodeName)));

  // current property
  if (this.property) {
    var prop = this.propertyExpression(this.property, fn.name);
    scope.add(new nodes.Ident('current-property', prop));
  } else {
    scope.add(new nodes.Ident('current-property', nodes.null));
  }

  // current call stack
  var expr = new nodes.Expression;
  for (var i = this.calling.length - 1; i-- ; ) {
    expr.push(new nodes.Literal(this.calling[i]));
  };
  scope.add(new nodes.Ident('called-from', expr));

  // inject arguments as locals
  var i = 0
    , len = args.nodes.length;
  fn.params.nodes.forEach(function(node){
    // rest param support
    if (node.rest) {
      node.val = new nodes.Expression;
      for (; i < len; ++i) node.val.push(args.nodes[i]);
      node.val.preserve = true;
      node.val.isList = args.isList;
    // argument default support
    } else {
      var arg = args.map[node.name] || args.nodes[i++];
      node = node.clone();
      if (arg) {
        arg.isEmpty ? args.nodes[i - 1] = this.visit(node) : node.val = arg;
      } else {
        args.push(node.val);
      }

      // required argument not satisfied
      if (node.val.isNull) {
        throw new Error('argument "' + node + '" required for ' + fn);
      }
    }

    scope.add(node);
  }, this);

  // mixin block
  if (content) scope.add(new nodes.Ident('block', content, true));

  // invoke
  return this.invoke(body, true, fn.filename);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.isDefined"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>isDefined (node)](#apidoc.element.stylus.Evaluator.prototype.isDefined)
- description and source-code
```javascript
isDefined = function (node){
  if ('ident' == node.nodeName) {
    return nodes.Boolean(this.lookup(node.name));
  } else {
    throw new Error('invalid "is defined" check on non-variable ' + node);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.literalCall"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>literalCall (call)](#apidoc.element.stylus.Evaluator.prototype.literalCall)
- description and source-code
```javascript
literalCall = function (call){
  call.args = this.visit(call.args);
  return call;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.lookup"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>lookup (name)](#apidoc.element.stylus.Evaluator.prototype.lookup)
- description and source-code
```javascript
lookup = function (name){
  var val;
  if (this.ignoreColors && name in colors) return;
  if (val = this.stack.lookup(name)) {
    return utils.unwrap(val);
  } else {
    return this.lookupFunction(name);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.lookupFunction"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>lookupFunction (name)](#apidoc.element.stylus.Evaluator.prototype.lookupFunction)
- description and source-code
```javascript
lookupFunction = function (name){
  var fn = this.functions[name] || bifs[name];
  if (fn) return new nodes.Function(name, fn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.lookupProperty"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>lookupProperty (name)](#apidoc.element.stylus.Evaluator.prototype.lookupProperty)
- description and source-code
```javascript
lookupProperty = function (name){
  var i = this.stack.length
    , index = this.currentBlock.index
    , top = i
    , nodes
    , block
    , len
    , other;

  while (i--) {
    block = this.stack[i].block;
    if (!block.node) continue;
    switch (block.node.nodeName) {
      case 'group':
      case 'function':
      case 'if':
      case 'each':
      case 'atrule':
      case 'media':
      case 'atblock':
      case 'call':
        nodes = block.nodes;
        // scan siblings from the property index up
        if (i + 1 == top) {
          while (index--) {
            // ignore current property
            if (this.property == nodes[index]) continue;
            other = this.interpolate(nodes[index]);
            if (name == other) return nodes[index].clone();
          }
        // sequential lookup for non-siblings (for now)
        } else {
          len = nodes.length;
          while (len--) {
            if ('property' != nodes[len].nodeName
              || this.property == nodes[len]) continue;
            other = this.interpolate(nodes[len]);
            if (name == other) return nodes[len].clone();
          }
        }
        break;
    }
  }

  return nodes.null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.mixin"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>mixin (nodes, block)](#apidoc.element.stylus.Evaluator.prototype.mixin)
- description and source-code
```javascript
mixin = function (nodes, block){
  if (!nodes.length) return;
  var len = block.nodes.length
    , head = block.nodes.slice(0, block.index)
    , tail = block.nodes.slice(block.index + 1, len);
  this._mixin(nodes, head, block);
  block.index = 0;
  block.nodes = head.concat(tail);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.mixinNode"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>mixinNode (node)](#apidoc.element.stylus.Evaluator.prototype.mixinNode)
- description and source-code
```javascript
mixinNode = function (node){
  node = this.visit(node.first);
  switch (node.nodeName) {
    case 'object':
      this.mixinObject(node);
      return nodes.null;
    case 'block':
    case 'atblock':
      this.mixin(node.nodes, this.currentBlock);
      return nodes.null;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.mixinObject"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>mixinObject (object)](#apidoc.element.stylus.Evaluator.prototype.mixinObject)
- description and source-code
```javascript
mixinObject = function (object){
  var Parser = require('../parser')
    , root = this.root
    , str = '$block ' + object.toBlock()
    , parser = new Parser(str, utils.merge({ root: block }, this.options))
    , block;

  try {
    block = parser.parse();
  } catch (err) {
    err.filename = this.filename;
    err.lineno = parser.lexer.lineno;
    err.column = parser.lexer.column;
    err.input = str;
    throw err;
  }

  block.parent = root;
  block.scope = false;
  var ret = this.visit(block)
    , vals = ret.first.nodes;
  for (var i = 0, len = vals.length; i < len; ++i) {
    if (vals[i].block) {
      this.mixin(vals[i].block.nodes, this.currentBlock);
      break;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.populateGlobalScope"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>populateGlobalScope ()](#apidoc.element.stylus.Evaluator.prototype.populateGlobalScope)
- description and source-code
```javascript
populateGlobalScope = function (){
  var scope = this.global.scope;

  // colors
  Object.keys(colors).forEach(function(name){
    var color = colors[name]
      , rgba = new nodes.RGBA(color[0], color[1], color[2], color[3])
      , node = new nodes.Ident(name, rgba);
    rgba.name = name;
    scope.add(node);
  });

  // expose url function
  scope.add(new nodes.Ident(
    'embedurl',
    new nodes.Function('embedurl', require('../functions/url')({
      limit: false
    }))
  ));

  // user-defined globals
  var globals = this.globals;
  Object.keys(globals).forEach(function(name){
    var val = globals[name];
    if (!val.nodeName) val = new nodes.Literal(val);
    scope.add(new nodes.Ident(name, val));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.propertyExpression"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>propertyExpression (prop, name)](#apidoc.element.stylus.Evaluator.prototype.propertyExpression)
- description and source-code
```javascript
propertyExpression = function (prop, name){
  var expr = new nodes.Expression
    , val = prop.expr.clone();

  // name
  expr.push(new nodes.String(prop.name));

  // replace cyclic call with __CALL__
  function replace(node) {
    if ('call' == node.nodeName && name == node.name) {
      return new nodes.Literal('__CALL__');
    }

    if (node.nodes) node.nodes = node.nodes.map(replace);
    return node;
  }

  replace(val);
  expr.push(val);
  return expr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.setup"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>setup ()](#apidoc.element.stylus.Evaluator.prototype.setup)
- description and source-code
```javascript
setup = function (){
  var root = this.root;
  var imports = [];

  this.populateGlobalScope();
  this.imports.forEach(function(file){
    var expr = new nodes.Expression;
    expr.push(new nodes.String(file));
    imports.push(new nodes.Import(expr));
  }, this);

  root.nodes = imports.concat(root.nodes);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.unvendorize"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>unvendorize (prop)](#apidoc.element.stylus.Evaluator.prototype.unvendorize)
- description and source-code
```javascript
unvendorize = function (prop){
  for (var i = 0, len = this.vendors.length; i < len; i++) {
    if ('official' != this.vendors[i]) {
      var vendor = '-' + this.vendors[i] + '-';
      if (~prop.indexOf(vendor)) return prop.replace(vendor, '');
    }
  }
  return prop;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visit"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visit (node)](#apidoc.element.stylus.Evaluator.prototype.visit)
- description and source-code
```javascript
visit = function (node){
  try {
    return visit.call(this, node);
  } catch (err) {
    if (err.filename) throw err;
    err.lineno = node.lineno;
    err.column = node.column;
    err.filename = node.filename;
    err.stylusStack = this.stack.toString();
    try {
      err.input = fs.readFileSync(err.filename, 'utf8');
    } catch (err) {
      // ignore
    }
    throw err;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitArguments"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitArguments (expr)](#apidoc.element.stylus.Evaluator.prototype.visitArguments)
- description and source-code
```javascript
visitArguments = function (expr){
  for (var i = 0, len = expr.nodes.length; i < len; ++i) {
    expr.nodes[i] = this.visit(expr.nodes[i]);
  }

  // support (n * 5)px etc
  if (this.castable(expr)) expr = this.cast(expr);

  return expr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitAtblock"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitAtblock (atblock)](#apidoc.element.stylus.Evaluator.prototype.visitAtblock)
- description and source-code
```javascript
visitAtblock = function (atblock){
  atblock.block = this.visit(atblock.block);
  return atblock;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitAtrule"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitAtrule (atrule)](#apidoc.element.stylus.Evaluator.prototype.visitAtrule)
- description and source-code
```javascript
visitAtrule = function (atrule){
  atrule.val = this.interpolate(atrule);
  if (atrule.block) atrule.block = this.visit(atrule.block);
  return atrule;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitBinOp"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitBinOp (binop)](#apidoc.element.stylus.Evaluator.prototype.visitBinOp)
- description and source-code
```javascript
visitBinOp = function (binop){
  // Special-case "is defined" pseudo binop
  if ('is defined' == binop.op) return this.isDefined(binop.left);

  this.return++;
  // Visit operands
  var op = binop.op
    , left = this.visit(binop.left)
    , right = ('||' == op || '&&' == op)
      ? binop.right : this.visit(binop.right);

  // HACK: ternary
  var val = binop.val
    ? this.visit(binop.val)
    : null;
  this.return--;

  // Operate
  try {
    return this.visit(left.operate(op, right, val));
  } catch (err) {
    // disregard coercion issues in equality
    // checks, and simply return false
    if ('CoercionError' == err.name) {
      switch (op) {
        case '==':
          return nodes.false;
        case '!=':
          return nodes.true;
      }
    }
    throw err;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitBlock"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitBlock (block)](#apidoc.element.stylus.Evaluator.prototype.visitBlock)
- description and source-code
```javascript
visitBlock = function (block){
  this.stack.push(new Frame(block));
  for (block.index = 0; block.index < block.nodes.length; ++block.index) {
    try {
      block.nodes[block.index] = this.visit(block.nodes[block.index]);
    } catch (err) {
      if ('return' == err.nodeName) {
        if (this.return) {
          this.stack.pop();
          throw err;
        } else {
          block.nodes[block.index] = err;
          break;
        }
      } else {
        throw err;
      }
    }
  }
  this.stack.pop();
  return block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitCall"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitCall (call)](#apidoc.element.stylus.Evaluator.prototype.visitCall)
- description and source-code
```javascript
visitCall = function (call){
  debug('call %s', call);
  var fn = this.lookup(call.name)
    , literal
    , ret;

  // url()
  this.ignoreColors = 'url' == call.name;

  // Variable function
  if (fn && 'expression' == fn.nodeName) {
    fn = fn.nodes[0];
  }

  // Not a function? try user-defined or built-ins
  if (fn && 'function' != fn.nodeName) {
    fn = this.lookupFunction(call.name);
  }

  // Undefined function? render literal CSS
  if (!fn || fn.nodeName != 'function') {
    debug('%s is undefined', call);
    // Special case for 'calc'
    if ('calc' == this.unvendorize(call.name)) {
      literal = call.args.nodes && call.args.nodes[0];
      if (literal) ret = new nodes.Literal(call.name + literal);
    } else {
      ret = this.literalCall(call);
    }
    this.ignoreColors = false;
    return ret;
  }

  this.calling.push(call.name);

  // Massive stack
  if (this.calling.length > 200) {
    throw new RangeError('Maximum stylus call stack size exceeded');
  }

  // First node in expression
  if ('expression' == fn.nodeName) fn = fn.first;

  // Evaluate arguments
  this.return++;
  var args = this.visit(call.args);

  for (var key in args.map) {
    args.map[key] = this.visit(args.map[key].clone());
  }
  this.return--;

  // Built-in
  if (fn.fn) {
    debug('%s is built-in', call);
    ret = this.invokeBuiltin(fn.fn, args);
  // User-defined
  } else if ('function' == fn.nodeName) {
    debug('%s is user-defined', call);
    // Evaluate mixin block
    if (call.block) call.block = this.visit(call.block);
    ret = this.invokeFunction(fn, args, call.block);
  }

  this.calling.pop();
  this.ignoreColors = false;
  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitEach"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitEach (each)](#apidoc.element.stylus.Evaluator.prototype.visitEach)
- description and source-code
```javascript
visitEach = function (each){
  this.return++;
  var expr = utils.unwrap(this.visit(each.expr))
    , len = expr.nodes.length
    , val = new nodes.Ident(each.val)
    , key = new nodes.Ident(each.key || '__index__')
    , scope = this.currentScope
    , block = this.currentBlock
    , vals = []
    , self = this
    , body
    , obj;
  this.return--;

  each.block.scope = false;

  function visitBody(key, val) {
    scope.add(val);
    scope.add(key);
    body = self.visit(each.block.clone());
    vals = vals.concat(body.nodes);
  }

  // for prop in obj
  if (1 == len && 'object' == expr.nodes[0].nodeName) {
    obj = expr.nodes[0];
    for (var prop in obj.vals) {
      val.val = new nodes.String(prop);
      key.val = obj.get(prop);
      visitBody(key, val);
    }
  } else {
    for (var i = 0; i < len; ++i) {
      val.val = expr.nodes[i];
      key.val = new nodes.Unit(i);
      visitBody(key, val);
    }
  }

  this.mixin(vals, block);
  return vals[vals.length - 1] || nodes.null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitExpression"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitExpression (expr)](#apidoc.element.stylus.Evaluator.prototype.visitExpression)
- description and source-code
```javascript
visitExpression = function (expr){
  for (var i = 0, len = expr.nodes.length; i < len; ++i) {
    expr.nodes[i] = this.visit(expr.nodes[i]);
  }

  // support (n * 5)px etc
  if (this.castable(expr)) expr = this.cast(expr);

  return expr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitExtend"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitExtend (extend)](#apidoc.element.stylus.Evaluator.prototype.visitExtend)
- description and source-code
```javascript
visitExtend = function (extend){
  var block = this.currentBlock;
  if ('group' != block.node.nodeName) block = this.closestGroup;
  extend.selectors.forEach(function(selector){
    block.node.extends.push({
      // Cloning the selector for when we are in a loop and don't want it to affect
      // the selector nodes and cause the values to be different to expected
      selector: this.interpolate(selector.clone()).trim(),
      optional: selector.optional,
      lineno: selector.lineno,
      column: selector.column
    });
  }, this);
  return nodes.null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitFeature"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitFeature (node)](#apidoc.element.stylus.Evaluator.prototype.visitFeature)
- description and source-code
```javascript
visitFeature = function (node){
  node.name = this.interpolate(node);
  if (node.expr) {
    this.return++;
    node.expr = this.visit(node.expr);
    this.return--;
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitFunction"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitFunction (fn)](#apidoc.element.stylus.Evaluator.prototype.visitFunction)
- description and source-code
```javascript
visitFunction = function (fn){
  // check local
  var local = this.stack.currentFrame.scope.lookup(fn.name);
  if (local) this.warn('local ' + local.nodeName + ' "' + fn.name + '" previously defined in this scope');

  // user-defined
  var user = this.functions[fn.name];
  if (user) this.warn('user-defined function "' + fn.name + '" is already defined');

  // BIF
  var bif = bifs[fn.name];
  if (bif) this.warn('built-in function "' + fn.name + '" is already defined');

  return fn;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitGroup"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitGroup (group)](#apidoc.element.stylus.Evaluator.prototype.visitGroup)
- description and source-code
```javascript
visitGroup = function (group){
  group.nodes = group.nodes.map(function(selector){
    selector.val = this.interpolate(selector);
    debug('ruleset %s', selector.val);
    return selector;
  }, this);

  group.block = this.visit(group.block);
  return group;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitIdent"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitIdent (ident)](#apidoc.element.stylus.Evaluator.prototype.visitIdent)
- description and source-code
```javascript
visitIdent = function (ident){
  var prop;
  // Property lookup
  if (ident.property) {
    if (prop = this.lookupProperty(ident.name)) {
      return this.visit(prop.expr.clone());
    }
    return nodes.null;
  // Lookup
  } else if (ident.val.isNull) {
    var val = this.lookup(ident.name);
    // Object or Block mixin
    if (val && ident.mixin) this.mixinNode(val);
    return val ? this.visit(val) : ident;
  // Assign
  } else {
    this.return++;
    ident.val = this.visit(ident.val);
    this.return--;
    this.currentScope.add(ident);
    return ident.val;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitIf"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitIf (node)](#apidoc.element.stylus.Evaluator.prototype.visitIf)
- description and source-code
```javascript
visitIf = function (node){
  var ret
    , block = this.currentBlock
    , negate = node.negate;

  this.return++;
  var ok = this.visit(node.cond).first.toBoolean();
  this.return--;

  node.block.scope = node.block.hasMedia;

  // Evaluate body
  if (negate) {
    // unless
    if (ok.isFalse) {
      ret = this.visit(node.block);
    }
  } else {
    // if
    if (ok.isTrue) {
      ret = this.visit(node.block);
    // else
    } else if (node.elses.length) {
      var elses = node.elses
        , len = elses.length
        , cond;
      for (var i = 0; i < len; ++i) {
        // else if
        if (elses[i].cond) {
          elses[i].block.scope = elses[i].block.hasMedia;
          this.return++;
          cond = this.visit(elses[i].cond).first.toBoolean();
          this.return--;
          if (cond.isTrue) {
            ret = this.visit(elses[i].block);
            break;
          }
        // else
        } else {
          elses[i].scope = elses[i].hasMedia;
          ret = this.visit(elses[i]);
        }
      }
    }
  }

  // mixin conditional statements within
  // a selector group or at-rule
  if (ret && !node.postfix && block.node
    && ~['group'
       , 'atrule'
       , 'media'
       , 'supports'
       , 'keyframes'].indexOf(block.node.nodeName)) {
    this.mixin(ret.nodes, block);
    return nodes.null;
  }

  return ret || nodes.null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitImport"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitImport (imported)](#apidoc.element.stylus.Evaluator.prototype.visitImport)
- description and source-code
```javascript
visitImport = function (imported){
  this.return++;

  var path = this.visit(imported.path).first
    , nodeName = imported.once ? 'require' : 'import'
    , found
    , literal;

  this.return--;
  debug('import %s', path);

  // url() passed
  if ('url' == path.name) {
    if (imported.once) throw new Error('You cannot @require a url');

    return imported;
  }

  // Ensure string
  if (!path.string) throw new Error('@' + nodeName + ' string expected');

  var name = path = path.string;

  // Absolute URL or hash
  if (/(?:url\s*\(\s*)?['"]?(?:#|(?:https?:)?\/\/)/i.test(path)) {
    if (imported.once) throw new Error('You cannot @require a url');
    return imported;
  }

  // Literal
  if (/\.css(?:"|$)/.test(path)) {
    literal = true;
    if (!imported.once && !this.includeCSS) {
      return imported;
    }
  }

  // support optional .styl
  if (!literal && !/\.styl$/i.test(path)) path += '.styl';

  // Lookup
  found = utils.find(path, this.paths, this.filename);
  if (!found) {
    found = utils.lookupIndex(name, this.paths, this.filename);
  }

  // Throw if import failed
  if (!found) throw new Error('failed to locate @' + nodeName + ' file ' + path);

  var block = new nodes.Block;

  for (var i = 0, len = found.length; i < len; ++i) {
    block.push(importFile.call(this, imported, found[i], literal));
  }

  return block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitKeyframes"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitKeyframes (keyframes)](#apidoc.element.stylus.Evaluator.prototype.visitKeyframes)
- description and source-code
```javascript
visitKeyframes = function (keyframes){
  var val;
  if (keyframes.fabricated) return keyframes;
  keyframes.val = this.interpolate(keyframes).trim();
  if (val = this.lookup(keyframes.val)) {
    keyframes.val = val.first.string || val.first.name;
  }
  keyframes.block = this.visit(keyframes.block);

  if ('official' != keyframes.prefix) return keyframes;

  this.vendors.forEach(function(prefix){
    // IE never had prefixes for keyframes
    if ('ms' == prefix) return;
    var node = keyframes.clone();
    node.val = keyframes.val;
    node.prefix = prefix;
    node.block = keyframes.block;
    node.fabricated = true;
    this.currentBlock.push(node);
  }, this);

  return nodes.null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitMedia"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitMedia (media)](#apidoc.element.stylus.Evaluator.prototype.visitMedia)
- description and source-code
```javascript
visitMedia = function (media){
  media.block = this.visit(media.block);
  media.val = this.visit(media.val);
  return media;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitMember"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitMember (node)](#apidoc.element.stylus.Evaluator.prototype.visitMember)
- description and source-code
```javascript
visitMember = function (node){
  var left = node.left
    , right = node.right
    , obj = this.visit(left).first;

  if ('object' != obj.nodeName) {
    throw new Error(left.toString() + ' has no property .' + right);
  }
  if (node.val) {
    this.return++;
    obj.set(right.name, this.visit(node.val));
    this.return--;
  }
  return obj.get(right.name);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitObject"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitObject (obj)](#apidoc.element.stylus.Evaluator.prototype.visitObject)
- description and source-code
```javascript
visitObject = function (obj){
  for (var key in obj.vals) {
    obj.vals[key] = this.visit(obj.vals[key]);
  }
  return obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitProperty"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitProperty (prop)](#apidoc.element.stylus.Evaluator.prototype.visitProperty)
- description and source-code
```javascript
visitProperty = function (prop){
  var name = this.interpolate(prop)
    , fn = this.lookup(name)
    , call = fn && 'function' == fn.first.nodeName
    , literal = ~this.calling.indexOf(name)
    , _prop = this.property;

  // Function of the same name
  if (call && !literal && !prop.literal) {
    var args = nodes.Arguments.fromExpression(utils.unwrap(prop.expr.clone()));
    prop.name = name;
    this.property = prop;
    this.return++;
    this.property.expr = this.visit(prop.expr);
    this.return--;
    var ret = this.visit(new nodes.Call(name, args));
    this.property = _prop;
    return ret;
  // Regular property
  } else {
    this.return++;
    prop.name = name;
    prop.literal = true;
    this.property = prop;
    prop.expr = this.visit(prop.expr);
    this.property = _prop;
    this.return--;
    return prop;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitQuery"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitQuery (node)](#apidoc.element.stylus.Evaluator.prototype.visitQuery)
- description and source-code
```javascript
visitQuery = function (node){
  node.predicate = this.visit(node.predicate);
  node.type = this.visit(node.type);
  node.nodes.forEach(this.visit, this);
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitQueryList"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitQueryList (queries)](#apidoc.element.stylus.Evaluator.prototype.visitQueryList)
- description and source-code
```javascript
visitQueryList = function (queries){
  var val, query;
  queries.nodes.forEach(this.visit, this);

  if (1 == queries.nodes.length) {
    query = queries.nodes[0];
    if (val = this.lookup(query.type)) {
      val = val.first.string;
      if (!val) return queries;
      var Parser = require('../parser')
        , parser = new Parser(val, this.options);
      queries = this.visit(parser.queries());
    }
  }
  return queries;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitReturn"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitReturn (ret)](#apidoc.element.stylus.Evaluator.prototype.visitReturn)
- description and source-code
```javascript
visitReturn = function (ret){
  ret.expr = this.visit(ret.expr);
  throw ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitRoot"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitRoot (block)](#apidoc.element.stylus.Evaluator.prototype.visitRoot)
- description and source-code
```javascript
visitRoot = function (block){
  // normalize cached imports
  if (block != this.root) {
    block.constructor = nodes.Block;
    return this.visit(block);
  }

  for (var i = 0; i < block.nodes.length; ++i) {
    block.index = i;
    block.nodes[i] = this.visit(block.nodes[i]);
  }
  return block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitSupports"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitSupports (node)](#apidoc.element.stylus.Evaluator.prototype.visitSupports)
- description and source-code
```javascript
visitSupports = function (node){
  var condition = node.condition
    , val;

  this.return++;
  node.condition = this.visit(condition);
  this.return--;

  val = condition.first;
  if (1 == condition.nodes.length
    && 'string' == val.nodeName) {
    node.condition = val.string;
  }
  node.block = this.visit(node.block);
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitTernary"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitTernary (ternary)](#apidoc.element.stylus.Evaluator.prototype.visitTernary)
- description and source-code
```javascript
visitTernary = function (ternary){
  var ok = this.visit(ternary.cond).toBoolean();
  return ok.isTrue
    ? this.visit(ternary.trueExpr)
    : this.visit(ternary.falseExpr);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.visitUnaryOp"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>visitUnaryOp (unary)](#apidoc.element.stylus.Evaluator.prototype.visitUnaryOp)
- description and source-code
```javascript
visitUnaryOp = function (unary){
  var op = unary.op
    , node = this.visit(unary.expr);

  if ('!' != op) {
    node = node.first.clone();
    utils.assertType(node, 'unit');
  }

  switch (op) {
    case '-':
      node.val = -node.val;
      break;
    case '+':
      node.val = +node.val;
      break;
    case '~':
      node.val = ~node.val;
      break;
    case '!':
      return node.toBoolean().negate();
  }

  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Evaluator.prototype.warn"></a>[function <span class="apidocSignatureSpan">stylus.Evaluator.prototype.</span>warn (msg)](#apidoc.element.stylus.Evaluator.prototype.warn)
- description and source-code
```javascript
warn = function (msg){
  if (!this.warnings) return;
  console.warn('\u001b[33mWarning:\u001b[0m ' + msg);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.Normalizer"></a>[module stylus.Normalizer](#apidoc.module.stylus.Normalizer)

#### <a name="apidoc.element.stylus.Normalizer.Normalizer"></a>[function <span class="apidocSignatureSpan">stylus.</span>Normalizer (root, options)](#apidoc.element.stylus.Normalizer.Normalizer)
- description and source-code
```javascript
function Normalizer(root, options) {
  options = options || {};
  Visitor.call(this, root);
  this.hoist = options['hoist atrules'];
  this.stack = [];
  this.map = {};
  this.imports = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.Normalizer.prototype"></a>[module stylus.Normalizer.prototype](#apidoc.module.stylus.Normalizer.prototype)

#### <a name="apidoc.element.stylus.Normalizer.prototype.bubble"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>bubble (node)](#apidoc.element.stylus.Normalizer.prototype.bubble)
- description and source-code
```javascript
bubble = function (node){
  var props = []
    , other = []
    , self = this;

  function filterProps(block) {
    block.nodes.forEach(function(node) {
      node = self.visit(node);

      switch (node.nodeName) {
        case 'property':
          props.push(node);
          break;
        case 'block':
          filterProps(node);
          break;
        default:
          other.push(node);
      }
    });
  }

  filterProps(node.block);

  if (props.length) {
    var selector = new nodes.Selector([new nodes.Literal('&')]);
    selector.lineno = node.lineno;
    selector.column = node.column;
    selector.filename = node.filename;
    selector.val = '&';

    var group = new nodes.Group;
    group.lineno = node.lineno;
    group.column = node.column;
    group.filename = node.filename;

    var block = new nodes.Block(node.block, group);
    block.lineno = node.lineno;
    block.column = node.column;
    block.filename = node.filename;

    props.forEach(function(prop){
      block.push(prop);
    });

    group.push(selector);
    group.block = block;

    node.block.nodes = [];
    node.block.push(group);
    other.forEach(function(n){
      node.block.push(n);
    });

    var group = this.closestGroup(node.block);
    if (group) node.group = group.clone();

    node.bubbled = true;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.closestGroup"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>closestGroup (block)](#apidoc.element.stylus.Normalizer.prototype.closestGroup)
- description and source-code
```javascript
closestGroup = function (block){
  var parent = block.parent
    , node;
  while (parent && (node = parent.node)) {
    if ('group' == node.nodeName) return node;
    parent = node.block && node.block.parent;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.extend"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>extend (group, selectors)](#apidoc.element.stylus.Normalizer.prototype.extend)
- description and source-code
```javascript
extend = function (group, selectors){
  var map = this.map
    , self = this
    , parent = this.closestGroup(group.block);

  group.extends.forEach(function(extend){
    var groups = map[extend.selector];
    if (!groups) {
      if (extend.optional) return;
      var err = new Error('Failed to @extend "' + extend.selector + '"');
      err.lineno = extend.lineno;
      err.column = extend.column;
      throw err;
    }
    selectors.forEach(function(selector){
      var node = new nodes.Selector;
      node.val = selector;
      node.inherits = false;
      groups.forEach(function(group){
        // prevent recursive extend
        if (!parent || (parent != group)) self.extend(group, selectors);
        group.push(node);
      });
    });
  });

  group.block = this.visit(group.block);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.normalize"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>normalize ()](#apidoc.element.stylus.Normalizer.prototype.normalize)
- description and source-code
```javascript
normalize = function (){
  var ret = this.visit(this.root);

  if (this.hoist) {
    // hoist @import
    if (this.imports.length) ret.nodes = this.imports.concat(ret.nodes);

    // hoist @charset
    if (this.charset) ret.nodes = [this.charset].concat(ret.nodes);
  }

  return ret;
}
```
- example usage
```shell
...
this.evaluator = new this.options.Evaluator(ast, this.options);
this.nodes = nodes;
this.evaluator.renderer = this;
ast = this.evaluator.evaluate();

// normalize
var normalizer = new Normalizer(ast, this.options);
ast = normalizer.normalize();

// compile
var compiler = this.options.sourcemap
  ? new (require('./visitor/sourcemapper'))(ast, this.options)
  : new (require('./visitor/compiler'))(ast, this.options)
  , css = compiler.compile();
...
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.visitAtrule"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitAtrule (node)](#apidoc.element.stylus.Normalizer.prototype.visitAtrule)
- description and source-code
```javascript
visitAtrule = function (node){
  if (node.block) node.block = this.visit(node.block);
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.visitBlock"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitBlock (block)](#apidoc.element.stylus.Normalizer.prototype.visitBlock)
- description and source-code
```javascript
visitBlock = function (block){
  var node;

  if (block.hasProperties) {
    for (var i = 0, len = block.nodes.length; i < len; ++i) {
      node = block.nodes[i];
      switch (node.nodeName) {
        case 'null':
        case 'expression':
        case 'function':
        case 'group':
        case 'unit':
        case 'atblock':
          continue;
        default:
          block.nodes[i] = this.visit(node);
      }
    }
  }

  // nesting
  for (var i = 0, len = block.nodes.length; i < len; ++i) {
    node = block.nodes[i];
    block.nodes[i] = this.visit(node);
  }

  return block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.visitCharset"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitCharset (node)](#apidoc.element.stylus.Normalizer.prototype.visitCharset)
- description and source-code
```javascript
visitCharset = function (node){
  this.charset = node;
  return this.hoist ? nodes.null : node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.visitExpression"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitExpression (expr)](#apidoc.element.stylus.Normalizer.prototype.visitExpression)
- description and source-code
```javascript
visitExpression = function (expr){
  expr.nodes = expr.nodes.map(function(node){
    // returns 'block' literal if mixin's block
    // is used as part of a property value
    if ('block' == node.nodeName) {
      var literal = new nodes.Literal('block');
      literal.lineno = expr.lineno;
      literal.column = expr.column;
      return literal;
    }
    return node;
  });
  return expr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.visitFunction"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitFunction ()](#apidoc.element.stylus.Normalizer.prototype.visitFunction)
- description and source-code
```javascript
visitFunction = function (){
  return nodes.null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.visitGroup"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitGroup (group)](#apidoc.element.stylus.Normalizer.prototype.visitGroup)
- description and source-code
```javascript
visitGroup = function (group){
  var stack = this.stack
    , map = this.map
    , parts;

  // normalize interpolated selectors with comma
  group.nodes.forEach(function(selector, i){
    if (!~selector.val.indexOf(',')) return;
    if (~selector.val.indexOf('\\,')) {
      selector.val = selector.val.replace(/\\,/g, ',');
      return;
    }
    parts = selector.val.split(',');
    var root = '/' == selector.val.charAt(0)
      , part, s;
    for (var k = 0, len = parts.length; k < len; ++k){
      part = parts[k].trim();
      if (root && k > 0 && !~part.indexOf('&')) {
        part = '/' + part;
      }
      s = new nodes.Selector([new nodes.Literal(part)]);
      s.val = part;
      s.block = group.block;
      group.nodes[i++] = s;
    }
  });
  stack.push(group.nodes);

  var selectors = utils.compileSelectors(stack, true);

  // map for extension lookup
  selectors.forEach(function(selector){
    map[selector] = map[selector] || [];
    map[selector].push(group);
  });

  // extensions
  this.extend(group, selectors);

  stack.pop();
  return group;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.visitImport"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitImport (node)](#apidoc.element.stylus.Normalizer.prototype.visitImport)
- description and source-code
```javascript
visitImport = function (node){
  this.imports.push(node);
  return this.hoist ? nodes.null : node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.visitKeyframes"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitKeyframes (node)](#apidoc.element.stylus.Normalizer.prototype.visitKeyframes)
- description and source-code
```javascript
visitKeyframes = function (node){
  var frames = node.block.nodes.filter(function(frame){
    return frame.block && frame.block.hasProperties;
  });
  node.frames = frames.length;
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.visitMedia"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitMedia (media)](#apidoc.element.stylus.Normalizer.prototype.visitMedia)
- description and source-code
```javascript
visitMedia = function (media){
  var medias = []
    , group = this.closestGroup(media.block)
    , parent;

  function mergeQueries(block) {
    block.nodes.forEach(function(node, i){
      switch (node.nodeName) {
        case 'media':
          node.val = media.val.merge(node.val);
          medias.push(node);
          block.nodes[i] = nodes.null;
          break;
        case 'block':
          mergeQueries(node);
          break;
        default:
          if (node.block && node.block.nodes)
            mergeQueries(node.block);
      }
    });
  }

  mergeQueries(media.block);
  this.bubble(media);

  if (medias.length) {
    medias.forEach(function(node){
      if (group) {
        group.block.push(node);
      } else {
        this.root.nodes.splice(++this.rootIndex, 0, node);
      }
      node = this.visit(node);
      parent = node.block.parent;
      if (node.bubbled && (!group || 'group' == parent.node.nodeName)) {
        node.group.block = node.block.nodes[0].block;
        node.block.nodes[0] = node.group;
      }
    }, this);
  }
  return media;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.visitProperty"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitProperty (prop)](#apidoc.element.stylus.Normalizer.prototype.visitProperty)
- description and source-code
```javascript
visitProperty = function (prop){
  this.visit(prop.expr);
  return prop;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.visitRoot"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitRoot (block)](#apidoc.element.stylus.Normalizer.prototype.visitRoot)
- description and source-code
```javascript
visitRoot = function (block){
  var ret = new nodes.Root
    , node;

  for (var i = 0; i < block.nodes.length; ++i) {
    node = block.nodes[i];
    switch (node.nodeName) {
      case 'null':
      case 'expression':
      case 'function':
      case 'unit':
      case 'atblock':
        continue;
      default:
        this.rootIndex = i;
        ret.push(this.visit(node));
    }
  }

  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Normalizer.prototype.visitSupports"></a>[function <span class="apidocSignatureSpan">stylus.Normalizer.prototype.</span>visitSupports (node)](#apidoc.element.stylus.Normalizer.prototype.visitSupports)
- description and source-code
```javascript
visitSupports = function (node){
  this.bubble(node);
  return node;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.Parser"></a>[module stylus.Parser](#apidoc.module.stylus.Parser)

#### <a name="apidoc.element.stylus.Parser.Parser"></a>[function <span class="apidocSignatureSpan">stylus.</span>Parser (str, options)](#apidoc.element.stylus.Parser.Parser)
- description and source-code
```javascript
function Parser(str, options) {
  var self = this;
  options = options || {};
  Parser.cache = Parser.cache || Parser.getCache(options);
  this.hash = Parser.cache.key(str, options);
  this.lexer = {};
  if (!Parser.cache.has(this.hash)) {
    this.lexer = new Lexer(str, options);
  }
  this.prefix = options.prefix || '';
  this.root = options.root || new nodes.Root;
  this.state = ['root'];
  this.stash = [];
  this.parens = 0;
  this.css = 0;
  this.state.pop = function(){
    self.prevState = [].pop.call(this);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.getCache"></a>[function <span class="apidocSignatureSpan">stylus.Parser.</span>getCache (options)](#apidoc.element.stylus.Parser.getCache)
- description and source-code
```javascript
getCache = function (options) {
  return false === options.cache
    ? cache(false)
    : cache(options.cache || 'memory', options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.Parser.prototype"></a>[module stylus.Parser.prototype](#apidoc.module.stylus.Parser.prototype)

#### <a name="apidoc.element.stylus.Parser.prototype.accept"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>accept (type)](#apidoc.element.stylus.Parser.prototype.accept)
- description and source-code
```javascript
accept = function (type){
  if (type == this.peek().type) {
    return this.next();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.additive"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>additive ()](#apidoc.element.stylus.Parser.prototype.additive)
- description and source-code
```javascript
additive = function () {
  var op
    , node = this.multiplicative();
  while (op = this.accept('+') || this.accept('-')) {
    this.operand = true;
    node = new nodes.BinOp(op.type, node, this.multiplicative());
    this.operand = false;
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.args"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>args ()](#apidoc.element.stylus.Parser.prototype.args)
- description and source-code
```javascript
args = function () {
  var args = new nodes.Arguments
    , keyword;

  do {
    // keyword
    if ('ident' == this.peek().type && ':' == this.lookahead(2).type) {
      keyword = this.next().val.string;
      this.expect(':');
      args.map[keyword] = this.expression();
    // arg
    } else {
      args.push(this.expression());
    }
  } while (this.accept(','));

  return args;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.assignAtblock"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>assignAtblock (expr)](#apidoc.element.stylus.Parser.prototype.assignAtblock)
- description and source-code
```javascript
assignAtblock = function (expr) {
  try {
    expr.push(this.atblock(expr));
  } catch(err) {
    this.error('invalid right-hand side operand in assignment, got {peek}');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.assignment"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>assignment ()](#apidoc.element.stylus.Parser.prototype.assignment)
- description and source-code
```javascript
assignment = function () {
  var op
    , node
    , name = this.id().name;

  if (op =
       this.accept('=')
    || this.accept('?=')
    || this.accept('+=')
    || this.accept('-=')
    || this.accept('*=')
    || this.accept('/=')
    || this.accept('%=')) {
    this.state.push('assignment');
    var expr = this.list();
    // @block support
    if (expr.isEmpty) this.assignAtblock(expr);
    node = new nodes.Ident(name, expr);
    this.state.pop();

    switch (op.type) {
      case '?=':
        var defined = new nodes.BinOp('is defined', node)
          , lookup = new nodes.Expression;
        lookup.push(new nodes.Ident(name));
        node = new nodes.Ternary(defined, lookup, node);
        break;
      case '+=':
      case '-=':
      case '*=':
      case '/=':
      case '%=':
        node.val = new nodes.BinOp(op.type[0], new nodes.Ident(name), expr);
        break;
    }
  }

  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.atblock"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>atblock (node)](#apidoc.element.stylus.Parser.prototype.atblock)
- description and source-code
```javascript
atblock = function (node){
  if (!node) this.expect('atblock');
  node = new nodes.Atblock;
  this.state.push('atblock');
  node.block = this.block(node, false);
  this.state.pop();
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.atrule"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>atrule ()](#apidoc.element.stylus.Parser.prototype.atrule)
- description and source-code
```javascript
atrule = function (){
  var type = this.expect('atrule').val
    , node = new nodes.Atrule(type)
    , tok;
  this.skipSpacesAndComments();
  node.segments = this.selectorParts();
  this.skipSpacesAndComments();
  tok = this.peek().type;
  if ('indent' == tok || '{' == tok || ('newline' == tok
    && '{' == this.lookahead(2).type)) {
    this.state.push('atrule');
    node.block = this.block(node);
    this.state.pop();
  }
  return node;
}
```
- example usage
```shell
...
|| this.urlchars()
|| this.comment()
|| this.newline()
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
|| this.string()
|| this.unit()
|| this.namedop()
...
```

#### <a name="apidoc.element.stylus.Parser.prototype.block"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>block (node, scope)](#apidoc.element.stylus.Parser.prototype.block)
- description and source-code
```javascript
block = function (node, scope) {
  var delim
    , stmt
    , next
    , block = this.parent = new nodes.Block(this.parent, node);

  if (false === scope) block.scope = false;

  this.accept('newline');

  // css-style
  if (this.accept('{')) {
    this.css++;
    delim = '}';
    this.skipWhitespace();
  } else {
    delim = 'outdent';
    this.expect('indent');
  }

  while (delim != this.peek().type) {
    // css-style
    if (this.css) {
      if (this.accept('newline') || this.accept('indent')) continue;
      stmt = this.statement();
      this.accept(';');
      this.skipWhitespace();
    } else {
      if (this.accept('newline')) continue;
      // skip useless indents and comments
      next = this.lookahead(2).type;
      if ('indent' == this.peek().type
        && ~['outdent', 'newline', 'comment'].indexOf(next)) {
        this.skip(['indent', 'outdent']);
        continue;
      }
      if ('eos' == this.peek().type) return block;
      stmt = this.statement();
      this.accept(';');
    }
    if (!stmt) this.error('unexpected token {peek} in block');
    block.push(stmt);
  }

  // css-style
  if (this.css) {
    this.skipWhitespace();
    this.expect('}');
    this.skipSpaces();
    this.css--;
  } else {
    this.expect('outdent');
  }

  this.parent = block.parent;
  return block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.charset"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>charset ()](#apidoc.element.stylus.Parser.prototype.charset)
- description and source-code
```javascript
charset = function () {
  this.expect('charset');
  var str = this.expect('string').val;
  this.allowPostfix = true;
  return new nodes.Charset(str);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.comment"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>comment ()](#apidoc.element.stylus.Parser.prototype.comment)
- description and source-code
```javascript
comment = function (){
  var node = this.next().val;
  this.skipSpaces();
  return node;
}
```
- example usage
```shell
...
    var column = this.column
, line = this.lineno
, tok = this.eos()
|| this.null()
|| this.sep()
|| this.keyword()
|| this.urlchars()
|| this.comment()
|| this.newline()
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
...
```

#### <a name="apidoc.element.stylus.Parser.prototype.constructor"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>constructor (str, options)](#apidoc.element.stylus.Parser.prototype.constructor)
- description and source-code
```javascript
function Parser(str, options) {
  var self = this;
  options = options || {};
  Parser.cache = Parser.cache || Parser.getCache(options);
  this.hash = Parser.cache.key(str, options);
  this.lexer = {};
  if (!Parser.cache.has(this.hash)) {
    this.lexer = new Lexer(str, options);
  }
  this.prefix = options.prefix || '';
  this.root = options.root || new nodes.Root;
  this.state = ['root'];
  this.stash = [];
  this.parens = 0;
  this.css = 0;
  this.state.pop = function(){
    self.prevState = [].pop.call(this);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.currentState"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>currentState ()](#apidoc.element.stylus.Parser.prototype.currentState)
- description and source-code
```javascript
currentState = function () {
  return this.state[this.state.length - 1];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.defined"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>defined ()](#apidoc.element.stylus.Parser.prototype.defined)
- description and source-code
```javascript
defined = function () {
  var node = this.unary();
  if (this.accept('is defined')) {
    if (!node) this.error('illegal unary "is defined", missing left-hand operand');
    node = new nodes.BinOp('is defined', node);
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.equality"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>equality ()](#apidoc.element.stylus.Parser.prototype.equality)
- description and source-code
```javascript
equality = function () {
  var op
    , node = this.in();
  while (op = this.accept('==') || this.accept('!=')) {
    this.operand = true;
    if (!node) this.error('illegal unary "' + op + '", missing left-hand operand');
    node = new nodes.BinOp(op.type, node, this.in());
    this.operand = false;
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.error"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>error (msg)](#apidoc.element.stylus.Parser.prototype.error)
- description and source-code
```javascript
error = function (msg){
  var type = this.peek().type
    , val = undefined == this.peek().val
      ? ''
      : ' ' + this.peek().toString();
  if (val.trim() == type.trim()) val = '';
  throw new errors.ParseError(msg.replace('{peek}', '"' + type + val + '"'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.expect"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>expect (type)](#apidoc.element.stylus.Parser.prototype.expect)
- description and source-code
```javascript
expect = function (type){
  if (type != this.peek().type) {
    this.error('expected "' + type + '", got {peek}');
  }
  return this.next();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.expression"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>expression ()](#apidoc.element.stylus.Parser.prototype.expression)
- description and source-code
```javascript
expression = function () {
  var node
    , expr = new nodes.Expression;
  this.state.push('expression');
  while (node = this.negation()) {
    if (!node) this.error('unexpected token {peek} in expression');
    expr.push(node);
  }
  this.state.pop();
  if (expr.nodes.length) {
    expr.lineno = expr.nodes[0].lineno;
    expr.column = expr.nodes[0].column;
  }
  return expr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.extend"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>extend ()](#apidoc.element.stylus.Parser.prototype.extend)
- description and source-code
```javascript
extend = function (){
  var tok = this.expect('extend')
    , selectors = []
    , sel
    , node
    , arr;

  do {
    arr = this.selectorParts();

    if (!arr.length) continue;

    sel = new nodes.Selector(arr);
    selectors.push(sel);

    if ('!' !== this.peek().type) continue;

    tok = this.lookahead(2);
    if ('ident' !== tok.type || 'optional' !== tok.val.name) continue;

    this.skip(['!', 'ident']);
    sel.optional = true;
  } while(this.accept(','));

  node = new nodes.Extend(selectors);
  node.lineno = tok.lineno;
  node.column = tok.column;
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.feature"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>feature ()](#apidoc.element.stylus.Parser.prototype.feature)
- description and source-code
```javascript
feature = function () {
  this.skipSpacesAndComments();
  this.expect('(');
  this.skipSpacesAndComments();
  var node = new nodes.Feature(this.interpolate());
  this.skipSpacesAndComments();
  this.accept(':')
  this.skipSpacesAndComments();
  this.inProperty = true;
  node.expr = this.list();
  this.inProperty = false;
  this.skipSpacesAndComments();
  this.expect(')');
  this.skipSpacesAndComments();
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.for"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>for ()](#apidoc.element.stylus.Parser.prototype.for)
- description and source-code
```javascript
for = function () {
  this.expect('for');
  var key
    , val = this.id().name;
  if (this.accept(',')) key = this.id().name;
  this.expect('in');
  this.state.push('for');
  this.cond = true;
  var each = new nodes.Each(val, key, this.expression());
  this.cond = false;
  each.block = this.block(each, false);
  this.state.pop();
  return each;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.function"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>function ()](#apidoc.element.stylus.Parser.prototype.function)
- description and source-code
```javascript
function = function () {
  var parens = 1
    , i = 2
    , tok;

  // Lookahead and determine if we are dealing
  // with a function call or definition. Here
  // we pair parens to prevent false negatives
  out:
  while (tok = this.lookahead(i++)) {
    switch (tok.type) {
      case 'function':
      case '(':
        ++parens;
        break;
      case ')':
        if (!--parens) break out;
        break;
      case 'eos':
        this.error('failed to find closing paren ")"');
    }
  }

  // Definition or call
  switch (this.currentState()) {
    case 'expression':
      return this.functionCall();
    default:
      return this.looksLikeFunctionDefinition(i)
        ? this.functionDefinition()
        : this.expression();
  }
}
```
- example usage
```shell
...
|| this.comment()
|| this.newline()
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
|| this.string()
|| this.unit()
|| this.namedop()
|| this.boolean()
...
```

#### <a name="apidoc.element.stylus.Parser.prototype.functionCall"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>functionCall ()](#apidoc.element.stylus.Parser.prototype.functionCall)
- description and source-code
```javascript
functionCall = function () {
  var withBlock = this.accept('+');
  if ('url' == this.peek().val.name) return this.url();
  var name = this.expect('function').val.name;
  this.state.push('function arguments');
  this.parens++;
  var args = this.args();
  this.expect(')');
  this.parens--;
  this.state.pop();
  var call = new nodes.Call(name, args);
  if (withBlock) {
    this.state.push('function');
    call.block = this.block(call);
    this.state.pop();
  }
  return call;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.functionDefinition"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>functionDefinition ()](#apidoc.element.stylus.Parser.prototype.functionDefinition)
- description and source-code
```javascript
functionDefinition = function () {
  var name = this.expect('function').val.name;

  // params
  this.state.push('function params');
  this.skipWhitespace();
  var params = this.params();
  this.skipWhitespace();
  this.expect(')');
  this.state.pop();

  // Body
  this.state.push('function');
  var fn = new nodes.Function(name, params);
  fn.block = this.block(fn);
  this.state.pop();
  return new nodes.Ident(name, fn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.id"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>id ()](#apidoc.element.stylus.Parser.prototype.id)
- description and source-code
```javascript
id = function () {
  var tok = this.expect('ident');
  this.accept('space');
  return tok.val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.ident"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>ident ()](#apidoc.element.stylus.Parser.prototype.ident)
- description and source-code
```javascript
ident = function () {
  var i = 2
    , la = this.lookahead(i).type;

  while ('space' == la) la = this.lookahead(++i).type;

  switch (la) {
    // Assignment
    case '=':
    case '?=':
    case '-=':
    case '+=':
    case '*=':
    case '/=':
    case '%=':
      return this.assignment();
    // Member
    case '.':
      if ('space' == this.lookahead(i - 1).type) return this.selector();
      if (this._ident == this.peek()) return this.id();
      while ('=' != this.lookahead(++i).type
        && !~['[', ',', 'newline', 'indent', 'eos'].indexOf(this.lookahead(i).type)) ;
      if ('=' == this.lookahead(i).type) {
        this._ident = this.peek();
        return this.expression();
      } else if (this.looksLikeSelector() && this.stateAllowsSelector()) {
        return this.selector();
      }
    // Assignment []=
    case '[':
      if (this._ident == this.peek()) return this.id();
      while (']' != this.lookahead(i++).type
        && 'selector' != this.lookahead(i).type
        && 'eos' != this.lookahead(i).type) ;
      if ('=' == this.lookahead(i).type) {
        this._ident = this.peek();
        return this.expression();
      } else if (this.looksLikeSelector() && this.stateAllowsSelector()) {
        return this.selector();
      }
    // Operation
    case '-':
    case '+':
    case '/':
    case '*':
    case '%':
    case '**':
    case '&&':
    case '||':
    case '>':
    case '<':
    case '>=':
    case '<=':
    case '!=':
    case '==':
    case '?':
    case 'in':
    case 'is a':
    case 'is defined':
      // Prevent cyclic .ident, return literal
      if (this._ident == this.peek()) {
        return this.id();
      } else {
        this._ident = this.peek();
        switch (this.currentState()) {
          // unary op or selector in property / for
          case 'for':
          case 'selector':
            return this.property();
          // Part of a selector
          case 'root':
          case 'atblock':
          case 'atrule':
            return '[' == la
              ? this.subscript()
              : this.selector();
          case 'function':
          case 'conditional':
            return this.looksLikeSelector()
              ? this.selector()
              : this.expression();
          // Do not disrupt the ident when an operand
          default:
            return this.operand
              ? this.id()
              : this.expression();
        }
      }
    // Selector or property
    default:
      switch (this.currentState()) {
        case 'root':
          return this.selector();
        case 'for':
        case 'selector':
        case 'function':
        case 'conditional':
        case 'atblock':
        case 'atrule':
          return this.property();
        default:
          var id = this.id();
          if ('interpolation' == this.previousState()) id.mixin = true;
          return id;
      }
  }
}
```
- example usage
```shell
...
  || this.paren()
  || this.color()
  || this.string()
  || this.unit()
  || this.namedop()
  || this.boolean()
  || this.unicode()
  || this.ident()
  || this.op()
  || this.eol()
  || this.space()
  || this.selector();
tok.lineno = line;
tok.column = column;
return tok;
...
```

#### <a name="apidoc.element.stylus.Parser.prototype.if"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>if ()](#apidoc.element.stylus.Parser.prototype.if)
- description and source-code
```javascript
if = function () {
  this.expect('if');
  this.state.push('conditional');
  this.cond = true;
  var node = new nodes.If(this.expression())
    , cond
    , block;
  this.cond = false;
  node.block = this.block(node, false);
  this.skip(['newline', 'comment']);
  while (this.accept('else')) {
    if (this.accept('if')) {
      this.cond = true;
      cond = this.expression();
      this.cond = false;
      block = this.block(node, false);
      node.elses.push(new nodes.If(cond, block));
    } else {
      node.elses.push(this.block(node, false));
      break;
    }
    this.skip(['newline', 'comment']);
  }
  this.state.pop();
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.import"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>import ()](#apidoc.element.stylus.Parser.prototype.import)
- description and source-code
```javascript
import = function () {
  this.expect('import');
  this.allowPostfix = true;
  return new nodes.Import(this.expression(), false);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.in"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>in ()](#apidoc.element.stylus.Parser.prototype.in)
- description and source-code
```javascript
in = function () {
  var node = this.relational();
  while (this.accept('in')) {
    this.operand = true;
    if (!node) this.error('illegal unary "in", missing left-hand operand');
    node = new nodes.BinOp('in', node, this.relational());
    this.operand = false;
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.interpolate"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>interpolate ()](#apidoc.element.stylus.Parser.prototype.interpolate)
- description and source-code
```javascript
interpolate = function () {
  var node
    , segs = []
    , star;

  star = this.accept('*');
  if (star) segs.push(new nodes.Literal('*'));

  while (true) {
    if (this.accept('{')) {
      this.state.push('interpolation');
      segs.push(this.expression());
      this.expect('}');
      this.state.pop();
    } else if (node = this.accept('-')){
      segs.push(new nodes.Literal('-'));
    } else if (node = this.accept('ident')){
      segs.push(node.val);
    } else {
      break;
    }
  }
  if (!segs.length) this.expect('ident');
  return segs;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.isPseudoSelector"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>isPseudoSelector (n)](#apidoc.element.stylus.Parser.prototype.isPseudoSelector)
- description and source-code
```javascript
isPseudoSelector = function (n){
  var val = this.lookahead(n).val;
  return val && ~pseudoSelectors.indexOf(val.name);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.isSelectorToken"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>isSelectorToken (n)](#apidoc.element.stylus.Parser.prototype.isSelectorToken)
- description and source-code
```javascript
isSelectorToken = function (n) {
  var la = this.lookahead(n).type;
  switch (la) {
    case 'for':
      return this.bracketed;
    case '[':
      this.bracketed = true;
      return true;
    case ']':
      this.bracketed = false;
      return true;
    default:
      return ~selectorTokens.indexOf(la);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.keyframes"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>keyframes ()](#apidoc.element.stylus.Parser.prototype.keyframes)
- description and source-code
```javascript
keyframes = function () {
  var tok = this.expect('keyframes')
    , keyframes;

  this.skipSpacesAndComments();
  keyframes = new nodes.Keyframes(this.selectorParts(), tok.val);
  this.skipSpacesAndComments();

  // block
  this.state.push('atrule');
  keyframes.block = this.block(keyframes);
  this.state.pop();

  return keyframes;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.lineContains"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>lineContains (type)](#apidoc.element.stylus.Parser.prototype.lineContains)
- description and source-code
```javascript
lineContains = function (type){
  var i = 1
    , la;

  while (la = this.lookahead(i++)) {
    if (~['indent', 'outdent', 'newline', 'eos'].indexOf(la.type)) return;
    if (type == la.type) return true;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.list"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>list ()](#apidoc.element.stylus.Parser.prototype.list)
- description and source-code
```javascript
list = function () {
  var node = this.expression();

  while (this.accept(',')) {
    if (node.isList) {
      list.push(this.expression());
    } else {
      var list = new nodes.Expression(true);
      list.push(node);
      list.push(this.expression());
      node = list;
    }
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.literal"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>literal ()](#apidoc.element.stylus.Parser.prototype.literal)
- description and source-code
```javascript
literal = function () {
  return this.expect('literal').val;
}
```
- example usage
```shell
...
|| this.sep()
|| this.keyword()
|| this.urlchars()
|| this.comment()
|| this.newline()
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
|| this.string()
...
```

#### <a name="apidoc.element.stylus.Parser.prototype.logical"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>logical ()](#apidoc.element.stylus.Parser.prototype.logical)
- description and source-code
```javascript
logical = function () {
  var op
    , node = this.typecheck();
  while (op = this.accept('&&') || this.accept('||')) {
    node = new nodes.BinOp(op.type, node, this.typecheck());
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.lookahead"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>lookahead (n)](#apidoc.element.stylus.Parser.prototype.lookahead)
- description and source-code
```javascript
lookahead = function (n){
  return this.lexer.lookahead(n);
}
```
- example usage
```shell
...
 * Lookahead a single token.
 *
 * @return {Token}
 * @api private
 */

peek: function() {
  return this.lookahead(1);
},

/**
 * Return the next possibly stashed token.
 *
 * @return {Token}
 * @api private
...
```

#### <a name="apidoc.element.stylus.Parser.prototype.looksLikeAttributeSelector"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>looksLikeAttributeSelector (n)](#apidoc.element.stylus.Parser.prototype.looksLikeAttributeSelector)
- description and source-code
```javascript
looksLikeAttributeSelector = function (n) {
  var type = this.lookahead(n).type;
  if ('=' == type && this.bracketed) return true;
  return ('ident' == type || 'string' == type)
    && ']' == this.lookahead(n + 1).type
    && ('newline' == this.lookahead(n + 2).type || this.isSelectorToken(n + 2))
    && !this.lineContains(':')
    && !this.lineContains('=');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.looksLikeFunctionDefinition"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>looksLikeFunctionDefinition (i)](#apidoc.element.stylus.Parser.prototype.looksLikeFunctionDefinition)
- description and source-code
```javascript
looksLikeFunctionDefinition = function (i) {
  return 'indent' == this.lookahead(i).type
    || '{' == this.lookahead(i).type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.looksLikeKeyframe"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>looksLikeKeyframe ()](#apidoc.element.stylus.Parser.prototype.looksLikeKeyframe)
- description and source-code
```javascript
looksLikeKeyframe = function () {
  var i = 2
    , type;
  switch (this.lookahead(i).type) {
    case '{':
    case 'indent':
    case ',':
      return true;
    case 'newline':
      while ('unit' == this.lookahead(++i).type
          || 'newline' == this.lookahead(i).type) ;
      type = this.lookahead(i).type;
      return 'indent' == type || '{' == type;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.looksLikeSelector"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>looksLikeSelector (fromProperty)](#apidoc.element.stylus.Parser.prototype.looksLikeSelector)
- description and source-code
```javascript
looksLikeSelector = function (fromProperty) {
  var i = 1
    , brace;

  // Real property
  if (fromProperty && ':' == this.lookahead(i + 1).type
    && (this.lookahead(i + 1).space || 'indent' == this.lookahead(i + 2).type))
    return false;

  // Assume selector when an ident is
  // followed by a selector
  while ('ident' == this.lookahead(i).type
    && ('newline' == this.lookahead(i + 1).type
       || ',' == this.lookahead(i + 1).type)) i += 2;

  while (this.isSelectorToken(i)
    || ',' == this.lookahead(i).type) {

    if ('selector' == this.lookahead(i).type)
      return true;

    if ('&' == this.lookahead(i + 1).type)
      return true;

    if ('.' == this.lookahead(i).type && 'ident' == this.lookahead(i + 1).type)
      return true;

    if ('*' == this.lookahead(i).type && 'newline' == this.lookahead(i + 1).type)
      return true;

    // Pseudo-elements
    if (':' == this.lookahead(i).type
      && ':' == this.lookahead(i + 1).type)
      return true;

    // #a after an ident and newline
    if ('color' == this.lookahead(i).type
      && 'newline' == this.lookahead(i - 1).type)
      return true;

    if (this.looksLikeAttributeSelector(i))
      return true;

    if (('=' == this.lookahead(i).type || 'function' == this.lookahead(i).type)
      && '{' == this.lookahead(i + 1).type)
      return false;

    // Hash values inside properties
    if (':' == this.lookahead(i).type
      && !this.isPseudoSelector(i + 1)
      && this.lineContains('.'))
      return false;

    // the ':' token within braces signifies
    // a selector. ex: "foo{bar:'baz'}"
    if ('{' == this.lookahead(i).type) brace = true;
    else if ('}' == this.lookahead(i).type) brace = false;
    if (brace && ':' == this.lookahead(i).type) return true;

    // '{' preceded by a space is considered a selector.
    // for example "foo{bar}{baz}" may be a property,
    // however "foo{bar} {baz}" is a selector
    if ('space' == this.lookahead(i).type
      && '{' == this.lookahead(i + 1).type)
      return true;

    // Assume pseudo selectors are NOT properties
    // as 'td:th-child(1)' may look like a property
    // and function call to the parser otherwise
    if (':' == this.lookahead(i++).type
      && !this.lookahead(i-1).space
      && this.isPseudoSelector(i))
      return true;

    // Trailing space
    if ('space' == this.lookahead(i).type
      && 'newline' == this.lookahead(i + 1).type
      && '{' == this.lookahead(i + 2).type)
      return true;

    if (',' == this.lookahead(i).type
      && 'newline' == this.lookahead(i + 1).type)
      return true;
  }

  // Trailing comma
  if (',' == this.lookahead(i).type
    && 'newline' == this.lookahead(i + 1).type)
    return true;

  // Trailing brace
  if ('{' == this.lookahead(i).type
    && 'newline' == this.lookahead(i + 1).type)
    return true;

  // css-style mode, false on ; }
  if (this.css) {
    if (';' == this.lookahead(i).type ||
        '}' == this.lookahead(i - 1).type)
      return false;
  }

  // Trailing separators
  while (!~[
      'indent'
    , 'outdent'
    , 'newline'
    , 'for'
    , 'if'
    , ';'
    , '}'
    , 'eos'].indexOf(this.lookahead(i).type))
    ++i;

  if ('indent' == this.lookahead(i).type)
    return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.media"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>media ()](#apidoc.element.stylus.Parser.prototype.media)
- description and source-code
```javascript
media = function () {
  this.expect('media');
  this.state.push('atrule');
  var media = new nodes.Media(this.queries());
  media.block = this.block(media);
  this.state.pop();
  return media;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.member"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>member ()](#apidoc.element.stylus.Parser.prototype.member)
- description and source-code
```javascript
member = function () {
  var node = this.primary();
  if (node) {
    while (this.accept('.')) {
      var id = new nodes.Ident(this.expect('ident').val.string);
      node = new nodes.Member(node, id);
    }
    this.skipSpaces();
    if (this.accept('=')) {
      node.val = this.list();
      // @block support
      if (node.val.isEmpty) this.assignAtblock(node.val);
    }
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.mozdocument"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>mozdocument ()](#apidoc.element.stylus.Parser.prototype.mozdocument)
- description and source-code
```javascript
mozdocument = function (){
  this.expect('-moz-document');
  var mozdocument = new nodes.Atrule('-moz-document')
    , calls = [];
  do {
    this.skipSpacesAndComments();
    calls.push(this.functionCall());
    this.skipSpacesAndComments();
  } while (this.accept(','));
  mozdocument.segments = [new nodes.Literal(calls.join(', '))];
  this.state.push('atrule');
  mozdocument.block = this.block(mozdocument, false);
  this.state.pop();
  return mozdocument;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.multiplicative"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>multiplicative ()](#apidoc.element.stylus.Parser.prototype.multiplicative)
- description and source-code
```javascript
multiplicative = function () {
  var op
    , node = this.defined();
  while (op =
       this.accept('**')
    || this.accept('*')
    || this.accept('/')
    || this.accept('%')) {
    this.operand = true;
    if ('/' == op && this.inProperty && !this.parens) {
      this.stash.push(new Token('literal', new nodes.Literal('/')));
      this.operand = false;
      return node;
    } else {
      if (!node) this.error('illegal unary "' + op + '", missing left-hand operand');
      node = new nodes.BinOp(op.type, node, this.defined());
      this.operand = false;
    }
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.namespace"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>namespace ()](#apidoc.element.stylus.Parser.prototype.namespace)
- description and source-code
```javascript
namespace = function () {
  var str
    , prefix;
  this.expect('namespace');

  this.skipSpacesAndComments();
  if (prefix = this.accept('ident')) {
    prefix = prefix.val;
  }
  this.skipSpacesAndComments();

  str = this.accept('string') || this.url();
  this.allowPostfix = true;
  return new nodes.Namespace(str, prefix);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.negation"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>negation ()](#apidoc.element.stylus.Parser.prototype.negation)
- description and source-code
```javascript
negation = function () {
  if (this.accept('not')) {
    return new nodes.UnaryOp('!', this.negation());
  }
  return this.ternary();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.next"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>next ()](#apidoc.element.stylus.Parser.prototype.next)
- description and source-code
```javascript
next = function () {
  var tok = this.stash.length
    ? this.stash.pop()
    : this.lexer.next()
    , line = tok.lineno
    , column = tok.column || 1;

  if (tok.val && tok.val.nodeName) {
    tok.val.lineno = line;
    tok.val.column = column;
  }
  nodes.lineno = line;
  nodes.column = column;
  debug.lexer('%s %s', tok.type, tok.val || '');
  return tok;
}
```
- example usage
```shell
...
 * Custom inspect.
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
...
```

#### <a name="apidoc.element.stylus.Parser.prototype.object"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>object ()](#apidoc.element.stylus.Parser.prototype.object)
- description and source-code
```javascript
object = function (){
  var obj = new nodes.Object
    , id, val, comma;
  this.expect('{');
  this.skipWhitespace();

  while (!this.accept('}')) {
    if (this.accept('comment')
      || this.accept('newline')) continue;

    if (!comma) this.accept(',');
    id = this.accept('ident') || this.accept('string');
    if (!id) this.error('expected "ident" or "string", got {peek}');
    id = id.val.hash;
    this.skipSpacesAndComments();
    this.expect(':');
    val = this.expression();
    obj.set(id, val);
    comma = this.accept(',');
    this.skipWhitespace();
  }

  return obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.params"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>params ()](#apidoc.element.stylus.Parser.prototype.params)
- description and source-code
```javascript
params = function () {
  var tok
    , node
    , params = new nodes.Params;
  while (tok = this.accept('ident')) {
    this.accept('space');
    params.push(node = tok.val);
    if (this.accept('...')) {
      node.rest = true;
    } else if (this.accept('=')) {
      node.val = this.expression();
    }
    this.skipWhitespace();
    this.accept(',');
    this.skipWhitespace();
  }
  return params;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.parse"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>parse ()](#apidoc.element.stylus.Parser.prototype.parse)
- description and source-code
```javascript
parse = function (){
  var block = this.parent = this.root;
  if (Parser.cache.has(this.hash)) {
    block = Parser.cache.get(this.hash);
    // normalize cached imports
    if ('block' == block.nodeName) block.constructor = nodes.Root;
  } else {
    while ('eos' != this.peek().type) {
      this.skipWhitespace();
      if ('eos' == this.peek().type) break;
      var stmt = this.statement();
      this.accept(';');
      if (!stmt) this.error('unexpected token {peek}, not allowed at the root level');
      block.push(stmt);
    }
    Parser.cache.set(this.hash, block);
  }
  return block;
}
```
- example usage
```shell
...
.set('linenos', options.linenos)
.set('sourcemap', options.sourcemap);
  };

  // Middleware
  return function stylus(req, res, next){
    if ('GET' != req.method && 'HEAD' != req.method) return next();
    var path = url.parse(req.url).pathname;
    if (/\.css$/.test(path)) {

if (typeof dest == 'string') {
  // check for dest-path overlap
  var overlap = compare(dest, path).length;
  if ('/' == path.charAt(0)) overlap++;
  path = path.slice(overlap);
...
```

#### <a name="apidoc.element.stylus.Parser.prototype.peek"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>peek ()](#apidoc.element.stylus.Parser.prototype.peek)
- description and source-code
```javascript
peek = function () {
  return this.lexer.peek();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.previousState"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>previousState ()](#apidoc.element.stylus.Parser.prototype.previousState)
- description and source-code
```javascript
previousState = function () {
  return this.state[this.state.length - 2];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.primary"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>primary ()](#apidoc.element.stylus.Parser.prototype.primary)
- description and source-code
```javascript
primary = function () {
  var tok;
  this.skipSpaces();

  // Parenthesis
  if (this.accept('(')) {
    ++this.parens;
    var expr = this.expression()
      , paren = this.expect(')');
    --this.parens;
    if (this.accept('%')) expr.push(new nodes.Ident('%'));
    tok = this.peek();
    // (1 + 2)px, (1 + 2)em, etc.
    if (!paren.space
      && 'ident' == tok.type
      && ~units.indexOf(tok.val.string)) {
      expr.push(new nodes.Ident(tok.val.string));
      this.next();
    }
    return expr;
  }

  tok = this.peek();

  // Primitive
  switch (tok.type) {
    case 'null':
    case 'unit':
    case 'color':
    case 'string':
    case 'literal':
    case 'boolean':
    case 'comment':
      return this.next().val;
    case !this.cond && '{':
      return this.object();
    case 'atblock':
      return this.atblock();
    // property lookup
    case 'atrule':
      var id = new nodes.Ident(this.next().val);
      id.property = true;
      return id;
    case 'ident':
      return this.ident();
    case 'function':
      return tok.anonymous
        ? this.functionDefinition()
        : this.functionCall();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.property"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>property ()](#apidoc.element.stylus.Parser.prototype.property)
- description and source-code
```javascript
property = function () {
  if (this.looksLikeSelector(true)) return this.selector();

  // property
  var ident = this.interpolate()
    , prop = new nodes.Property(ident)
    , ret = prop;

  // optional ':'
  this.accept('space');
  if (this.accept(':')) this.accept('space');

  this.state.push('property');
  this.inProperty = true;
  prop.expr = this.list();
  if (prop.expr.isEmpty) ret = ident[0];
  this.inProperty = false;
  this.allowPostfix = true;
  this.state.pop();

  // optional ';'
  this.accept(';');

  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.queries"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>queries ()](#apidoc.element.stylus.Parser.prototype.queries)
- description and source-code
```javascript
queries = function () {
  var queries = new nodes.QueryList
    , skip = ['comment', 'newline', 'space'];

  do {
    this.skip(skip);
    queries.push(this.query());
    this.skip(skip);
  } while (this.accept(','));
  return queries;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.query"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>query ()](#apidoc.element.stylus.Parser.prototype.query)
- description and source-code
```javascript
query = function () {
  var query = new nodes.Query
    , expr
    , pred
    , id;

  // hash values support
  if ('ident' == this.peek().type
    && ('.' == this.lookahead(2).type
    || '[' == this.lookahead(2).type)) {
    this.cond = true;
    expr = this.expression();
    this.cond = false;
    query.push(new nodes.Feature(expr.nodes));
    return query;
  }

  if (pred = this.accept('ident') || this.accept('not')) {
    pred = new nodes.Literal(pred.val.string || pred.val);

    this.skipSpacesAndComments();
    if (id = this.accept('ident')) {
      query.type = id.val;
      query.predicate = pred;
    } else {
      query.type = pred;
    }
    this.skipSpacesAndComments();

    if (!this.accept('&&')) return query;
  }

  do {
    query.push(this.feature());
  } while (this.accept('&&'));

  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.range"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>range ()](#apidoc.element.stylus.Parser.prototype.range)
- description and source-code
```javascript
range = function () {
  var op
    , node = this.additive();
  if (op = this.accept('...') || this.accept('..')) {
    this.operand = true;
    if (!node) this.error('illegal unary "' + op + '", missing left-hand operand');
    node = new nodes.BinOp(op.val, node, this.additive());
    this.operand = false;
  }
  return node;
}
```
- example usage
```shell
...
 * '^[' range ']'
 */

SelectorParser.prototype.partial = function() {
if ('^' == this.str[0] && '[' == this.str[1]) {
  this.skip(2);
  this.skipSpaces();
  var ret = this.range();
  this.skipSpaces();
  if (']' != this.str[0]) return '^[';
  this.nested = false;
  this.skip(1);
  if (ret) {
    return ret;
  } else {
...
```

#### <a name="apidoc.element.stylus.Parser.prototype.relational"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>relational ()](#apidoc.element.stylus.Parser.prototype.relational)
- description and source-code
```javascript
relational = function () {
  var op
    , node = this.range();
  while (op =
       this.accept('>=')
    || this.accept('<=')
    || this.accept('<')
    || this.accept('>')
    ) {
    this.operand = true;
    if (!node) this.error('illegal unary "' + op + '", missing left-hand operand');
    node = new nodes.BinOp(op.type, node, this.range());
    this.operand = false;
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.require"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>require ()](#apidoc.element.stylus.Parser.prototype.require)
- description and source-code
```javascript
require = function () {
  this.expect('require');
  this.allowPostfix = true;
  return new nodes.Import(this.expression(), true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.return"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>return ()](#apidoc.element.stylus.Parser.prototype.return)
- description and source-code
```javascript
return = function () {
  this.expect('return');
  var expr = this.expression();
  return expr.isEmpty
    ? new nodes.Return
    : new nodes.Return(expr);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.scope"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>scope ()](#apidoc.element.stylus.Parser.prototype.scope)
- description and source-code
```javascript
scope = function (){
  this.expect('scope');
  var selector = this.selectorParts()
    .map(function(selector) { return selector.val; })
    .join('');
  this.selectorScope = selector.trim();
  return nodes.null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.selector"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>selector ()](#apidoc.element.stylus.Parser.prototype.selector)
- description and source-code
```javascript
selector = function () {
  var arr
    , group = new nodes.Group
    , scope = this.selectorScope
    , isRoot = 'root' == this.currentState()
    , selector;

  do {
    // Clobber newline after ,
    this.accept('newline');

    arr = this.selectorParts();

    // Push the selector
    if (isRoot && scope) arr.unshift(new nodes.Literal(scope + ' '));
    if (arr.length) {
      selector = new nodes.Selector(arr);
      selector.lineno = arr[0].lineno;
      selector.column = arr[0].column;
      group.push(selector);
    }
  } while (this.accept(',') || this.accept('newline'));

  if ('selector-parts' == this.currentState()) return group.nodes;

  this.state.push('selector');
  group.block = this.block(group);
  this.state.pop();

  return group;
}
```
- example usage
```shell
...
    || this.namedop()
    || this.boolean()
    || this.unicode()
    || this.ident()
    || this.op()
    || this.eol()
    || this.space()
    || this.selector();
  tok.lineno = line;
  tok.column = column;
  return tok;
},

/**
 * Lookahead a single token.
...
```

#### <a name="apidoc.element.stylus.Parser.prototype.selectorParts"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>selectorParts ()](#apidoc.element.stylus.Parser.prototype.selectorParts)
- description and source-code
```javascript
selectorParts = function (){
  var tok
    , arr = [];

  // Selector candidates,
  // stitched together to
  // form a selector.
  while (tok = this.selectorToken()) {
    debug.selector('%s', tok);
    // Selector component
    switch (tok.type) {
      case '{':
        this.skipSpaces();
        var expr = this.expression();
        this.skipSpaces();
        this.expect('}');
        arr.push(expr);
        break;
      case this.prefix && '.':
        var literal = new nodes.Literal(tok.val + this.prefix);
        literal.prefixed = true;
        arr.push(literal);
        break;
      case 'comment':
        // ignore comments
        break;
      case 'color':
      case 'unit':
        arr.push(new nodes.Literal(tok.val.raw));
        break;
      case 'space':
        arr.push(new nodes.Literal(' '));
        break;
      case 'function':
        arr.push(new nodes.Literal(tok.val.name + '('));
        break;
      case 'ident':
        arr.push(new nodes.Literal(tok.val.name || tok.val.string));
        break;
      default:
        arr.push(new nodes.Literal(tok.val));
        if (tok.space) arr.push(new nodes.Literal(' '));
    }
  }

  return arr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.selectorToken"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>selectorToken ()](#apidoc.element.stylus.Parser.prototype.selectorToken)
- description and source-code
```javascript
selectorToken = function () {
  if (this.isSelectorToken(1)) {
    if ('{' == this.peek().type) {
      // unclosed, must be a block
      if (!this.lineContains('}')) return;
      // check if ':' is within the braces.
      // though not required by Stylus, chances
      // are if someone is using {} they will
      // use CSS-style props, helping us with
      // the ambiguity in this case
      var i = 0
        , la;
      while (la = this.lookahead(++i)) {
        if ('}' == la.type) {
          // Check empty block.
          if (i == 2 || (i == 3 && this.lookahead(i - 1).type == 'space'))
            return;
          break;
        }
        if (':' == la.type) return;
      }
    }
    return this.next();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.skip"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>skip (tokens)](#apidoc.element.stylus.Parser.prototype.skip)
- description and source-code
```javascript
skip = function (tokens) {
  while (~tokens.indexOf(this.peek().type))
    this.next();
}
```
- example usage
```shell
...
 * url char
 */

urlchars: function() {
  var captures;
  if (!this.isURL) return;
  if (captures = /^[\/:@.;?&=*!,<>#%0-9]+/.exec(this.str)) {
    this.skip(captures);
    return new Token('literal', new nodes.Literal(captures[0]));
  }
},

/**
 * ';' [ \t]*
 */
...
```

#### <a name="apidoc.element.stylus.Parser.prototype.skipNewlines"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>skipNewlines ()](#apidoc.element.stylus.Parser.prototype.skipNewlines)
- description and source-code
```javascript
skipNewlines = function () {
  while ('newline' == this.peek().type)
    this.next();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.skipSpaces"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>skipSpaces ()](#apidoc.element.stylus.Parser.prototype.skipSpaces)
- description and source-code
```javascript
skipSpaces = function () {
  while ('space' == this.peek().type)
    this.next();
}
```
- example usage
```shell
...
/**
 * '^[' range ']'
 */

SelectorParser.prototype.partial = function() {
if ('^' == this.str[0] && '[' == this.str[1]) {
  this.skip(2);
  this.skipSpaces();
  var ret = this.range();
  this.skipSpaces();
  if (']' != this.str[0]) return '^[';
  this.nested = false;
  this.skip(1);
  if (ret) {
    return ret;
...
```

#### <a name="apidoc.element.stylus.Parser.prototype.skipSpacesAndComments"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>skipSpacesAndComments ()](#apidoc.element.stylus.Parser.prototype.skipSpacesAndComments)
- description and source-code
```javascript
skipSpacesAndComments = function () {
  while ('space' == this.peek().type
    || 'comment' == this.peek().type)
    this.next();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.skipWhitespace"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>skipWhitespace ()](#apidoc.element.stylus.Parser.prototype.skipWhitespace)
- description and source-code
```javascript
skipWhitespace = function () {
  this.skip(['space', 'indent', 'outdent', 'newline']);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.stateAllowsSelector"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>stateAllowsSelector ()](#apidoc.element.stylus.Parser.prototype.stateAllowsSelector)
- description and source-code
```javascript
stateAllowsSelector = function () {
  switch (this.currentState()) {
    case 'root':
    case 'atblock':
    case 'selector':
    case 'conditional':
    case 'function':
    case 'atrule':
    case 'for':
      return true;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.statement"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>statement ()](#apidoc.element.stylus.Parser.prototype.statement)
- description and source-code
```javascript
statement = function () {
  var stmt = this.stmt()
    , state = this.prevState
    , block
    , op;

  // special-case statements since it
  // is not an expression. We could
  // implement postfix conditionals at
  // the expression level, however they
  // would then fail to enclose properties
  if (this.allowPostfix) {
    this.allowPostfix = false;
    state = 'expression';
  }

  switch (state) {
    case 'assignment':
    case 'expression':
    case 'function arguments':
      while (op =
           this.accept('if')
        || this.accept('unless')
        || this.accept('for')) {
        switch (op.type) {
          case 'if':
          case 'unless':
            stmt = new nodes.If(this.expression(), stmt);
            stmt.postfix = true;
            stmt.negate = 'unless' == op.type;
            this.accept(';');
            break;
          case 'for':
            var key
              , val = this.id().name;
            if (this.accept(',')) key = this.id().name;
            this.expect('in');
            var each = new nodes.Each(val, key, this.expression());
            block = new nodes.Block(this.parent, each);
            block.push(stmt);
            each.block = block;
            stmt = each;
        }
      }
  }

  return stmt;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.stmt"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>stmt ()](#apidoc.element.stylus.Parser.prototype.stmt)
- description and source-code
```javascript
stmt = function () {
  var type = this.peek().type;
  switch (type) {
    case 'keyframes':
      return this.keyframes();
    case '-moz-document':
      return this.mozdocument();
    case 'comment':
    case 'selector':
    case 'literal':
    case 'charset':
    case 'namespace':
    case 'import':
    case 'require':
    case 'extend':
    case 'media':
    case 'atrule':
    case 'ident':
    case 'scope':
    case 'supports':
    case 'unless':
    case 'function':
    case 'for':
    case 'if':
      return this[type]();
    case 'return':
      return this.return();
    case '{':
      return this.property();
    default:
      // Contextual selectors
      if (this.stateAllowsSelector()) {
        switch (type) {
          case 'color':
          case '~':
          case '>':
          case '<':
          case ':':
          case '&':
          case '&&':
          case '[':
          case '.':
          case '/':
            return this.selector();
          // relative reference
          case '..':
            if ('/' == this.lookahead(2).type)
              return this.selector();
          case '+':
            return 'function' == this.lookahead(2).type
              ? this.functionCall()
              : this.selector();
          case '*':
            return this.property();
          // keyframe blocks (10%, 20% { ... })
          case 'unit':
            if (this.looksLikeKeyframe()) return this.selector();
          case '-':
            if ('{' == this.lookahead(2).type)
              return this.property();
        }
      }

      // Expression fallback
      var expr = this.expression();
      if (expr.isEmpty) this.error('unexpected {peek}');
      return expr;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.subscript"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>subscript ()](#apidoc.element.stylus.Parser.prototype.subscript)
- description and source-code
```javascript
subscript = function () {
  var node = this.member()
    , id;
  while (this.accept('[')) {
    node = new nodes.BinOp('[]', node, this.expression());
    this.expect(']');
  }
  // TODO: TernaryOp :)
  if (this.accept('=')) {
    node.op += '=';
    node.val = this.list();
    // @block support
    if (node.val.isEmpty) this.assignAtblock(node.val);
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.supports"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>supports ()](#apidoc.element.stylus.Parser.prototype.supports)
- description and source-code
```javascript
supports = function (){
  this.expect('supports');
  var node = new nodes.Supports(this.supportsCondition());
  this.state.push('atrule');
  node.block = this.block(node);
  this.state.pop();
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.supportsCondition"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>supportsCondition ()](#apidoc.element.stylus.Parser.prototype.supportsCondition)
- description and source-code
```javascript
supportsCondition = function (){
  var node = this.supportsNegation()
    || this.supportsOp();
  if (!node) {
    this.cond = true;
    node = this.expression();
    this.cond = false;
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.supportsFeature"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>supportsFeature ()](#apidoc.element.stylus.Parser.prototype.supportsFeature)
- description and source-code
```javascript
supportsFeature = function (){
  this.skipSpacesAndComments();
  if ('(' == this.peek().type) {
    var la = this.lookahead(2).type;

    if ('ident' == la || '{' == la) {
      return this.feature();
    } else {
      this.expect('(');
      var node = new nodes.Expression;
      node.push(new nodes.Literal('('));
      node.push(this.supportsCondition());
      this.expect(')')
      node.push(new nodes.Literal(')'));
      this.skipSpacesAndComments();
      return node;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.supportsNegation"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>supportsNegation ()](#apidoc.element.stylus.Parser.prototype.supportsNegation)
- description and source-code
```javascript
supportsNegation = function (){
  if (this.accept('not')) {
    var node = new nodes.Expression;
    node.push(new nodes.Literal('not'));
    node.push(this.supportsFeature());
    return node;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.supportsOp"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>supportsOp ()](#apidoc.element.stylus.Parser.prototype.supportsOp)
- description and source-code
```javascript
supportsOp = function (){
  var feature = this.supportsFeature()
    , op
    , expr;
  if (feature) {
    expr = new nodes.Expression;
    expr.push(feature);
    while (op = this.accept('&&') || this.accept('||')) {
      expr.push(new nodes.Literal('&&' == op.val ? 'and' : 'or'));
      expr.push(this.supportsFeature());
    }
    return expr;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.ternary"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>ternary ()](#apidoc.element.stylus.Parser.prototype.ternary)
- description and source-code
```javascript
ternary = function () {
  var node = this.logical();
  if (this.accept('?')) {
    var trueExpr = this.expression();
    this.expect(':');
    var falseExpr = this.expression();
    node = new nodes.Ternary(node, trueExpr, falseExpr);
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.typecheck"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>typecheck ()](#apidoc.element.stylus.Parser.prototype.typecheck)
- description and source-code
```javascript
typecheck = function () {
  var op
    , node = this.equality();
  while (op = this.accept('is a')) {
    this.operand = true;
    if (!node) this.error('illegal unary "' + op + '", missing left-hand operand');
    node = new nodes.BinOp(op.type, node, this.equality());
    this.operand = false;
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.unary"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>unary ()](#apidoc.element.stylus.Parser.prototype.unary)
- description and source-code
```javascript
unary = function () {
  var op
    , node;
  if (op =
       this.accept('!')
    || this.accept('~')
    || this.accept('+')
    || this.accept('-')) {
    this.operand = true;
    node = this.unary();
    if (!node) this.error('illegal unary "' + op + '"');
    node = new nodes.UnaryOp(op.type, node);
    this.operand = false;
    return node;
  }
  return this.subscript();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.unless"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>unless ()](#apidoc.element.stylus.Parser.prototype.unless)
- description and source-code
```javascript
unless = function () {
  this.expect('unless');
  this.state.push('conditional');
  this.cond = true;
  var node = new nodes.If(this.expression(), true);
  this.cond = false;
  node.block = this.block(node, false);
  this.state.pop();
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.Parser.prototype.url"></a>[function <span class="apidocSignatureSpan">stylus.Parser.prototype.</span>url ()](#apidoc.element.stylus.Parser.prototype.url)
- description and source-code
```javascript
url = function () {
  this.expect('function');
  this.state.push('function arguments');
  var args = this.args();
  this.expect(')');
  this.state.pop();
  return new nodes.Call('url', args);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.Visitor"></a>[module stylus.Visitor](#apidoc.module.stylus.Visitor)

#### <a name="apidoc.element.stylus.Visitor.Visitor"></a>[function <span class="apidocSignatureSpan">stylus.</span>Visitor (root)](#apidoc.element.stylus.Visitor.Visitor)
- description and source-code
```javascript
function Visitor(root) {
  this.root = root;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.Visitor.prototype"></a>[module stylus.Visitor.prototype](#apidoc.module.stylus.Visitor.prototype)

#### <a name="apidoc.element.stylus.Visitor.prototype.visit"></a>[function <span class="apidocSignatureSpan">stylus.Visitor.prototype.</span>visit (node, fn)](#apidoc.element.stylus.Visitor.prototype.visit)
- description and source-code
```javascript
visit = function (node, fn){
  var method = 'visit' + node.constructor.name;
  if (this[method]) return this[method](node);
  return node;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.errors"></a>[module stylus.errors](#apidoc.module.stylus.errors)

#### <a name="apidoc.element.stylus.errors.ParseError"></a>[function <span class="apidocSignatureSpan">stylus.errors.</span>ParseError (msg)](#apidoc.element.stylus.errors.ParseError)
- description and source-code
```javascript
function ParseError(msg) {
  this.name = 'ParseError';
  this.message = msg;
  Error.captureStackTrace(this, ParseError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.errors.SyntaxError"></a>[function <span class="apidocSignatureSpan">stylus.errors.</span>SyntaxError (msg)](#apidoc.element.stylus.errors.SyntaxError)
- description and source-code
```javascript
function SyntaxError(msg) {
  this.name = 'SyntaxError';
  this.message = msg;
  Error.captureStackTrace(this, ParseError);
}
```
- example usage
```shell
...

    if (captures) {
var tok
  , indents = captures[1].length;

this.skip(captures);
if (this.str[0] === ' ' || this.str[0] === '\t') {
  throw new errors.SyntaxError('Invalid indentation. You can use tabs or spaces to indent, but not both.');
}

// Blank line
if ('\n' == this.str[0]) return this.advance();

// Outdent
if (this.indentStack.length && indents < this.indentStack[0]) {
...
```



# <a name="apidoc.module.stylus.functions"></a>[module stylus.functions](#apidoc.module.stylus.functions)

#### <a name="apidoc.element.stylus.functions.add-property"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>add-property (name, expr)](#apidoc.element.stylus.functions.add-property)
- description and source-code
```javascript
function addProperty(name, expr){
  utils.assertType(name, 'expression', 'name');
  name = utils.unwrap(name).first;
  utils.assertString(name, 'name');
  utils.assertType(expr, 'expression', 'expr');
  var prop = new nodes.Property([name], expr);
  var block = this.closestBlock;

  var len = block.nodes.length
    , head = block.nodes.slice(0, block.index)
    , tail = block.nodes.slice(block.index++, len);
  head.push(prop);
  block.nodes = head.concat(tail);

  return prop;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.adjust"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>adjust (color, prop, amount)](#apidoc.element.stylus.functions.adjust)
- description and source-code
```javascript
function adjust(color, prop, amount){
  utils.assertColor(color, 'color');
  utils.assertString(prop, 'prop');
  utils.assertType(amount, 'unit', 'amount');
  var hsl = color.hsla.clone();
  prop = { hue: 'h', saturation: 's', lightness: 'l' }[prop.string];
  if (!prop) throw new Error('invalid adjustment property');
  var val = amount.val;
  if ('%' == amount.type){
    val = 'l' == prop && val > 0
      ? (100 - hsl[prop]) * val / 100
      : hsl[prop] * (val / 100);
  }
  hsl[prop] += val;
  return hsl.rgba;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.alpha"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>alpha (color, value)](#apidoc.element.stylus.functions.alpha)
- description and source-code
```javascript
function alpha(color, value){
  color = color.rgba;
  if (value) {
    return rgba(
      new nodes.Unit(color.r),
      new nodes.Unit(color.g),
      new nodes.Unit(color.b),
      value
    );
  }
  return new nodes.Unit(color.a, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.append"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>append (expr)](#apidoc.element.stylus.functions.append)
- description and source-code
```javascript
append = function (expr){
  expr = utils.unwrap(expr);
  for (var i = 1, len = arguments.length; i < len; ++i) {
    expr.nodes.push(utils.unwrap(arguments[i]).clone());
  }
  return expr.nodes.length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.base-convert"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>base-convert (num, base, width)](#apidoc.element.stylus.functions.base-convert)
- description and source-code
```javascript
base-convert = function (num, base, width) {
  utils.assertPresent(num, 'number');
  utils.assertPresent(base, 'base');
  num = utils.unwrap(num).nodes[0].val;
  base = utils.unwrap(base).nodes[0].val;
  width = (width && utils.unwrap(width).nodes[0].val) || 2;
  var result = Number(num).toString(base);
  while (result.length < width) {
    result = '0' + result;
  }
  return new nodes.Literal(result);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.basename"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>basename (p, ext)](#apidoc.element.stylus.functions.basename)
- description and source-code
```javascript
function basename(p, ext){
  utils.assertString(p, 'path');
  return path.basename(p.val, ext && ext.val);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.blend"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>blend (top, bottom)](#apidoc.element.stylus.functions.blend)
- description and source-code
```javascript
function blend(top, bottom){
  // TODO: different blend modes like overlay etc.
  utils.assertColor(top);
  top = top.rgba;
  bottom = bottom || new nodes.RGBA(255, 255, 255, 1);
  utils.assertColor(bottom);
  bottom = bottom.rgba;

  return new nodes.RGBA(
    top.r * top.a + bottom.r * (1 - top.a),
    top.g * top.a + bottom.g * (1 - top.a),
    top.b * top.a + bottom.b * (1 - top.a),
    top.a + bottom.a - top.a * bottom.a);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.blue"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>blue (color, value)](#apidoc.element.stylus.functions.blue)
- description and source-code
```javascript
function blue(color, value){
  color = color.rgba;
  if (value) {
    return rgba(
      new nodes.Unit(color.r),
      new nodes.Unit(color.g),
      value,
      new nodes.Unit(color.a)
    );
  }
  return new nodes.Unit(color.b, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.clone"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>clone (expr)](#apidoc.element.stylus.functions.clone)
- description and source-code
```javascript
function clone(expr){
  utils.assertPresent(expr, 'expr');
  return expr.clone();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.component"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>component (color, name)](#apidoc.element.stylus.functions.component)
- description and source-code
```javascript
function component(color, name) {
  utils.assertColor(color, 'color');
  utils.assertString(name, 'name');
  var name = name.string
    , unit = unitMap[name]
    , type = typeMap[name]
    , name = componentMap[name];
  if (!name) throw new Error('invalid color component "' + name + '"');
  return new nodes.Unit(color[type][name], unit);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.contrast"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>contrast (top, bottom)](#apidoc.element.stylus.functions.contrast)
- description and source-code
```javascript
function contrast(top, bottom){
  if ('rgba' != top.nodeName && 'hsla' != top.nodeName) {
    return new nodes.Literal('contrast(' + (top.isNull ? '' : top.toString()) + ')');
  }
  var result = new nodes.Object();
  top = top.rgba;
  bottom = bottom || new nodes.RGBA(255, 255, 255, 1);
  utils.assertColor(bottom);
  bottom = bottom.rgba;
  function contrast(top, bottom) {
    if (1 > top.a) {
      top = blend(top, bottom);
    }
    var l1 = luminosity(bottom).val + 0.05
      , l2 = luminosity(top).val + 0.05
      , ratio = l1 / l2;

    if (l2 > l1) {
      ratio = 1 / ratio;
    }
    return Math.round(ratio * 10) / 10;
  }

  if (1 <= bottom.a) {
    var resultRatio = new nodes.Unit(contrast(top, bottom));
    result.set('ratio', resultRatio);
    result.set('error', new nodes.Unit(0));
    result.set('min', resultRatio);
    result.set('max', resultRatio);
  } else {
    var onBlack = contrast(top, blend(bottom, new nodes.RGBA(0, 0, 0, 1)))
      , onWhite = contrast(top, blend(bottom, new nodes.RGBA(255, 255, 255, 1)))
      , max = Math.max(onBlack, onWhite);
    function processChannel(topChannel, bottomChannel) {
      return Math.min(Math.max(0, (topChannel - bottomChannel * bottom.a) / (1 - bottom.a)), 255);
    }
    var closest = new nodes.RGBA(
      processChannel(top.r, bottom.r),
      processChannel(top.g, bottom.g),
      processChannel(top.b, bottom.b),
      1
    );
    var min = contrast(top, blend(bottom, closest));

    result.set('ratio', new nodes.Unit(Math.round((min + max) * 50) / 100));
    result.set('error', new nodes.Unit(Math.round((max - min) * 50) / 100));
    result.set('min', new nodes.Unit(min));
    result.set('max', new nodes.Unit(max));
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.convert"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>convert (str)](#apidoc.element.stylus.functions.convert)
- description and source-code
```javascript
function convert(str){
  utils.assertString(str, 'str');
  return utils.parseString(str.string);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.current-media"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>current-media ()](#apidoc.element.stylus.functions.current-media)
- description and source-code
```javascript
function currentMedia(){
  var self = this;
  return new nodes.String(lookForMedia(this.closestBlock.node) || '');

  function lookForMedia(node){
    if ('media' == node.nodeName) {
      node.val = self.visit(node.val);
      return node.toString();
    } else if (node.block.parent.node) {
      return lookForMedia(node.block.parent.node);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.define"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>define (name, expr, global)](#apidoc.element.stylus.functions.define)
- description and source-code
```javascript
function define(name, expr, global){
  utils.assertType(name, 'string', 'name');
  expr = utils.unwrap(expr);
  var scope = this.currentScope;
  if (global && global.toBoolean().isTrue) {
    scope = this.global.scope;
  }
  var node = new nodes.Ident(name.val, expr);
  scope.add(node);
  return nodes.null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.dirname"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>dirname (p)](#apidoc.element.stylus.functions.dirname)
- description and source-code
```javascript
function dirname(p){
  utils.assertString(p, 'path');
  return path.dirname(p.val).replace(/\\/g, '/');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.error"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>error (msg)](#apidoc.element.stylus.functions.error)
- description and source-code
```javascript
function error(msg){
  utils.assertType(msg, 'string', 'msg');
  var err = new Error(msg.val);
  err.fromStylus = true;
  throw err;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.extend"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>extend (dest)](#apidoc.element.stylus.functions.extend)
- description and source-code
```javascript
function merge(dest){
  utils.assertPresent(dest, 'dest');
  dest = utils.unwrap(dest).first;
  utils.assertType(dest, 'object', 'dest');

  var last = utils.unwrap(arguments[arguments.length - 1]).first
    , deep = (true === last.val);

  for (var i = 1, len = arguments.length - deep; i < len; ++i) {
    utils.merge(dest.vals, utils.unwrap(arguments[i]).first.vals, deep);
  }
  return dest;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.extname"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>extname (p)](#apidoc.element.stylus.functions.extname)
- description and source-code
```javascript
function extname(p){
  utils.assertString(p, 'path');
  return path.extname(p.val);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.green"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>green (color, value)](#apidoc.element.stylus.functions.green)
- description and source-code
```javascript
function green(color, value){
  color = color.rgba;
  if (value) {
    return rgba(
      new nodes.Unit(color.r),
      value,
      new nodes.Unit(color.b),
      new nodes.Unit(color.a)
    );
  }
  return new nodes.Unit(color.g, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.hsl"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>hsl (hue, saturation, lightness)](#apidoc.element.stylus.functions.hsl)
- description and source-code
```javascript
function hsl(hue, saturation, lightness){
  if (1 == arguments.length) {
    utils.assertColor(hue, 'color');
    return hue.hsla;
  } else {
    return hsla(
        hue
      , saturation
      , lightness
      , new nodes.Unit(1));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.hsla"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>hsla (hue, saturation, lightness, alpha)](#apidoc.element.stylus.functions.hsla)
- description and source-code
```javascript
function hsla(hue, saturation, lightness, alpha){
  switch (arguments.length) {
    case 1:
      utils.assertColor(hue);
      return hue.hsla;
    case 2:
      utils.assertColor(hue);
      var color = hue.hsla;
      utils.assertType(saturation, 'unit', 'alpha');
      var alpha = saturation.clone();
      if ('%' == alpha.type) alpha.val /= 100;
      return new nodes.HSLA(
          color.h
        , color.s
        , color.l
        , alpha.val);
    default:
      utils.assertType(hue, 'unit', 'hue');
      utils.assertType(saturation, 'unit', 'saturation');
      utils.assertType(lightness, 'unit', 'lightness');
      utils.assertType(alpha, 'unit', 'alpha');
      var alpha = alpha.clone();
      if (alpha && '%' == alpha.type) alpha.val /= 100;
      return new nodes.HSLA(
          hue.val
        , saturation.val
        , lightness.val
        , alpha.val);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.hue"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>hue (color, value)](#apidoc.element.stylus.functions.hue)
- description and source-code
```javascript
function hue(color, value){
  if (value) {
    var hslaColor = color.hsla;
    return hsla(
      value,
      new nodes.Unit(hslaColor.s),
      new nodes.Unit(hslaColor.l),
      new nodes.Unit(hslaColor.a)
    )
  }
  return component(color, new nodes.String('hue'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.image-size"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>image-size (img, ignoreErr)](#apidoc.element.stylus.functions.image-size)
- description and source-code
```javascript
function imageSize(img, ignoreErr) {
  utils.assertType(img, 'string', 'img');
  try {
    var img = new Image(this, img.string);
  } catch (err) {
    if (ignoreErr) {
      return [new nodes.Unit(0), new nodes.Unit(0)];
    } else {
      throw err;
    }
  }

  // Read size
  img.open();
  var size = img.size();
  img.close();

  // Return (w h)
  var expr = [];
  expr.push(new nodes.Unit(size[0], 'px'));
  expr.push(new nodes.Unit(size[1], 'px'));

  return expr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.json"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>json (path, local, namePrefix)](#apidoc.element.stylus.functions.json)
- description and source-code
```javascript
json = function (path, local, namePrefix){
  utils.assertString(path, 'path');

  // lookup
  path = path.string;
  var found = utils.lookup(path, this.options.paths, this.options.filename)
    , options = (local && 'object' == local.nodeName) && local;

  if (!found) {
    // optional JSON file
    if (options && options.get('optional').toBoolean().isTrue) {
      return nodes.null;
    }
    throw new Error('failed to locate .json file ' + path);
  }

  // read
  var json = JSON.parse(readFile(found, 'utf8'));

  if (options) {
    return convert(json, options);
  } else {
    oldJson.call(this, json, local, namePrefix);
  }

  function convert(obj, options){
    var ret = new nodes.Object()
      , leaveStrings = options.get('leave-strings').toBoolean();

    for (var key in obj) {
      var val = obj[key];
      if ('object' == typeof val) {
        ret.set(key, convert(val, options));
      } else {
        val = utils.coerce(val);
        if ('string' == val.nodeName && leaveStrings.isFalse) {
          val = utils.parseString(val.string);
        }
        ret.set(key, val);
      }
    }
    return ret;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.length"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>length (expr)](#apidoc.element.stylus.functions.length)
- description and source-code
```javascript
function length(expr){
  if (expr) {
    if (expr.nodes) {
      var nodes = utils.unwrap(expr).nodes;
      if (1 == nodes.length && 'object' == nodes[0].nodeName) {
        return nodes[0].length;
      } else {
        return nodes.length;
      }
    } else {
      return 1;
    }
  }
  return 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.lightness"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>lightness (color, value)](#apidoc.element.stylus.functions.lightness)
- description and source-code
```javascript
function lightness(color, value){
  if (value) {
    var hslaColor = color.hsla;
    return hsla(
      new nodes.Unit(hslaColor.h),
      new nodes.Unit(hslaColor.s),
      value,
      new nodes.Unit(hslaColor.a)
    )
  }
  return component(color, new nodes.String('lightness'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.list-separator"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>list-separator (list)](#apidoc.element.stylus.functions.list-separator)
- description and source-code
```javascript
function listSeparator(list){
  list = utils.unwrap(list);
  return new nodes.String(list.isList ? ',' : ' ');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.lookup"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>lookup (name)](#apidoc.element.stylus.functions.lookup)
- description and source-code
```javascript
function lookup(name){
  utils.assertType(name, 'string', 'name');
  var node = this.lookup(name.val);
  if (!node) return nodes.null;
  return this.visit(node);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.luminosity"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>luminosity (color)](#apidoc.element.stylus.functions.luminosity)
- description and source-code
```javascript
function luminosity(color){
  utils.assertColor(color);
  color = color.rgba;
  function processChannel(channel) {
    channel = channel / 255;
    return (0.03928 > channel)
      ? channel / 12.92
      : Math.pow(((channel + 0.055) / 1.055), 2.4);
  }
  return new nodes.Unit(
    0.2126 * processChannel(color.r)
    + 0.7152 * processChannel(color.g)
    + 0.0722 * processChannel(color.b)
  );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.match"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>match (pattern, val, flags)](#apidoc.element.stylus.functions.match)
- description and source-code
```javascript
function match(pattern, val, flags){
  utils.assertType(pattern, 'string', 'pattern');
  utils.assertString(val, 'val');
  var re = new RegExp(pattern.val, validateFlags(flags) ? flags.string : '');
  return val.string.match(re);
}
```
- example usage
```shell
...
 * Move current line and column position.
 *
 * @param {String} str
 * @api private
 */

move: function(str){
  var lines = str.match(/\n/g)
    , idx = str.lastIndexOf('\n');

  if (lines) this.lineno += lines.length;
  this.column = ~idx
    ? str.length - idx
    : this.column + str.length;
},
...
```

#### <a name="apidoc.element.stylus.functions.math"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>math (n, fn)](#apidoc.element.stylus.functions.math)
- description and source-code
```javascript
function math(n, fn){
  utils.assertType(n, 'unit', 'n');
  utils.assertString(fn, 'fn');
  return new nodes.Unit(Math[fn.string](n.val), n.type);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.merge"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>merge (dest)](#apidoc.element.stylus.functions.merge)
- description and source-code
```javascript
function merge(dest){
  utils.assertPresent(dest, 'dest');
  dest = utils.unwrap(dest).first;
  utils.assertType(dest, 'object', 'dest');

  var last = utils.unwrap(arguments[arguments.length - 1]).first
    , deep = (true === last.val);

  for (var i = 1, len = arguments.length - deep; i < len; ++i) {
    utils.merge(dest.vals, utils.unwrap(arguments[i]).first.vals, deep);
  }
  return dest;
}
```
- example usage
```shell
...
 *
 * @param {String} [filename]
 * @return {Array}
 * @api public
 */

Renderer.prototype.deps = function(filename){
var opts = utils.merge({ cache: false }, this.options);
if (filename) opts.filename = filename;

var DepsResolver = require('./visitor/deps-resolver')
  , parser = new Parser(this.str, opts);

try {
  nodes.filename = opts.filename;
...
```

#### <a name="apidoc.element.stylus.functions.operate"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>operate (op, left, right)](#apidoc.element.stylus.functions.operate)
- description and source-code
```javascript
function operate(op, left, right){
  utils.assertType(op, 'string', 'op');
  utils.assertPresent(left, 'left');
  utils.assertPresent(right, 'right');
  return left.operate(op.val, right);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.opposite-position"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>opposite-position (positions)](#apidoc.element.stylus.functions.opposite-position)
- description and source-code
```javascript
function oppositePosition(positions){
  var expr = [];
  utils.unwrap(positions).nodes.forEach(function(pos, i){
    utils.assertString(pos, 'position ' + i);
    pos = (function(){ switch (pos.string) {
      case 'top': return 'bottom';
      case 'bottom': return 'top';
      case 'left': return 'right';
      case 'right': return 'left';
      case 'center': return 'center';
      default: throw new Error('invalid position ' + pos);
    }})();
    expr.push(new nodes.Literal(pos));
  });
  return expr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.p"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>p ()](#apidoc.element.stylus.functions.p)
- description and source-code
```javascript
function p(){
  [].slice.call(arguments).forEach(function(expr){
    expr = utils.unwrap(expr);
    if (!expr.nodes.length) return;
    console.log('\u001b[90minspect:\u001b[0m %s', expr.toString().replace(/^\(|\)$/g, ''));
  })
  return nodes.null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.pathjoin"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>pathjoin ()](#apidoc.element.stylus.functions.pathjoin)
- description and source-code
```javascript
function pathjoin(){
  var paths = [].slice.call(arguments).map(function(path){
    return path.first.string;
  });
  return path.join.apply(null, paths).replace(/\\/g, '/');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.pop"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>pop (expr)](#apidoc.element.stylus.functions.pop)
- description and source-code
```javascript
function pop(expr) {
  expr = utils.unwrap(expr);
  return expr.nodes.pop();
}
```
- example usage
```shell
...

// Outdent
if (this.indentStack.length && indents < this.indentStack[0]) {
  while (this.indentStack.length && this.indentStack[0] > indents) {
    this.stash.push(new Token('outdent'));
    this.indentStack.shift();
  }
  tok = this.stash.pop();
// Indent
} else if (indents && indents != this.indentStack[0]) {
  this.indentStack.unshift(indents);
  tok = new Token('indent');
// Newline
} else {
  tok = new Token('newline');
...
```

#### <a name="apidoc.element.stylus.functions.prepend"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>prepend (expr)](#apidoc.element.stylus.functions.prepend)
- description and source-code
```javascript
prepend = function (expr){
  expr = utils.unwrap(expr);
  for (var i = 1, len = arguments.length; i < len; ++i) {
    expr.nodes.unshift(utils.unwrap(arguments[i]));
  }
  return expr.nodes.length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.push"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>push (expr)](#apidoc.element.stylus.functions.push)
- description and source-code
```javascript
push = function (expr){
  expr = utils.unwrap(expr);
  for (var i = 1, len = arguments.length; i < len; ++i) {
    expr.nodes.push(utils.unwrap(arguments[i]).clone());
  }
  return expr.nodes.length;
}
```
- example usage
```shell
...
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
 * Lookahead 'n' tokens.
...
```

#### <a name="apidoc.element.stylus.functions.range"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>range (start, stop, step)](#apidoc.element.stylus.functions.range)
- description and source-code
```javascript
function range(start, stop, step){
  utils.assertType(start, 'unit', 'start');
  utils.assertType(stop, 'unit', 'stop');
  if (step) {
    utils.assertType(step, 'unit', 'step');
    if (0 == step.val) {
      throw new Error('ArgumentError: "step" argument must not be zero');
    }
  } else {
    step = new nodes.Unit(1);
  }
  var list = new nodes.Expression;
  for (var i = start.val; i <= stop.val; i += step.val) {
    list.push(new nodes.Unit(i, start.type));
  }
  return list;
}
```
- example usage
```shell
...
 * '^[' range ']'
 */

SelectorParser.prototype.partial = function() {
if ('^' == this.str[0] && '[' == this.str[1]) {
  this.skip(2);
  this.skipSpaces();
  var ret = this.range();
  this.skipSpaces();
  if (']' != this.str[0]) return '^[';
  this.nested = false;
  this.skip(1);
  if (ret) {
    return ret;
  } else {
...
```

#### <a name="apidoc.element.stylus.functions.red"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>red (color, value)](#apidoc.element.stylus.functions.red)
- description and source-code
```javascript
function red(color, value){
  color = color.rgba;
  if (value) {
    return rgba(
      value,
      new nodes.Unit(color.g),
      new nodes.Unit(color.b),
      new nodes.Unit(color.a)
    );
  }
  return new nodes.Unit(color.r, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.remove"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>remove (object, key)](#apidoc.element.stylus.functions.remove)
- description and source-code
```javascript
function remove(object, key){
  utils.assertType(object, 'object', 'object');
  utils.assertString(key, 'key');
  delete object.vals[key.string];
  return object;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.replace"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>replace (pattern, replacement, val)](#apidoc.element.stylus.functions.replace)
- description and source-code
```javascript
function replace(pattern, replacement, val){
  utils.assertString(pattern, 'pattern');
  utils.assertString(replacement, 'replacement');
  utils.assertString(val, 'val');
  pattern = new RegExp(pattern.string, 'g');
  var res = val.string.replace(pattern, replacement.string);
  return val instanceof nodes.Ident
    ? new nodes.Ident(res)
    : new nodes.String(res);
}
```
- example usage
```shell
...
      : val + '\r';
  };

  // Remove UTF-8 BOM.
  if ('\uFEFF' == str.charAt(0)) str = str.slice(1);

  this.str = str
    .replace(/\s+$/, '\n')
    .replace(/\r\n?/g, '\n')
    .replace(/\\ *\n/g, '\r')
    .replace(/([,(:](?!\/\/[^ ])) *(?:\/\/[^\n]*|\/\*.*?\*\/)?\n\s*/g, comment)
    .replace(/\s*\n[ \t]*([,)])/g, comment);
};

/**
...
```

#### <a name="apidoc.element.stylus.functions.rgb"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>rgb (red, green, blue)](#apidoc.element.stylus.functions.rgb)
- description and source-code
```javascript
function rgb(red, green, blue){
  switch (arguments.length) {
    case 1:
      utils.assertColor(red);
      var color = red.rgba;
      return new nodes.RGBA(
          color.r
        , color.g
        , color.b
        , 1);
    default:
      return rgba(
          red
        , green
        , blue
        , new nodes.Unit(1));
  }
}
```
- example usage
```shell
...
 * #rrggbbaa | #rrggbb | #rgba | #rgb | #nn | #n
 */

color: function() {
  return this.rrggbbaa()
    || this.rrggbb()
    || this.rgba()
    || this.rgb()
    || this.nn()
    || this.n()
},

/**
 * #n
 */
...
```

#### <a name="apidoc.element.stylus.functions.rgba"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>rgba (red, green, blue, alpha)](#apidoc.element.stylus.functions.rgba)
- description and source-code
```javascript
function rgba(red, green, blue, alpha){
  switch (arguments.length) {
    case 1:
      utils.assertColor(red);
      return red.rgba;
    case 2:
      utils.assertColor(red);
      var color = red.rgba;
      utils.assertType(green, 'unit', 'alpha');
      alpha = green.clone();
      if ('%' == alpha.type) alpha.val /= 100;
      return new nodes.RGBA(
          color.r
        , color.g
        , color.b
        , alpha.val);
    default:
      utils.assertType(red, 'unit', 'red');
      utils.assertType(green, 'unit', 'green');
      utils.assertType(blue, 'unit', 'blue');
      utils.assertType(alpha, 'unit', 'alpha');
      var r = '%' == red.type ? Math.round(red.val * 2.55) : red.val
        , g = '%' == green.type ? Math.round(green.val * 2.55) : green.val
        , b = '%' == blue.type ? Math.round(blue.val * 2.55) : blue.val;

      alpha = alpha.clone();
      if (alpha && '%' == alpha.type) alpha.val /= 100;
      return new nodes.RGBA(
          r
        , g
        , b
        , alpha.val);
  }
}
```
- example usage
```shell
...
/**
 * #rrggbbaa | #rrggbb | #rgba | #rgb | #nn | #n
 */

color: function() {
  return this.rrggbbaa()
    || this.rrggbb()
    || this.rgba()
    || this.rgb()
    || this.nn()
    || this.n()
},

/**
 * #n
...
```

#### <a name="apidoc.element.stylus.functions.s"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>s (fmt)](#apidoc.element.stylus.functions.s)
- description and source-code
```javascript
function s(fmt){
  fmt = utils.unwrap(fmt).nodes[0];
  utils.assertString(fmt);
  var self = this
    , str = fmt.string
    , args = arguments
    , i = 1;

  // format
  str = str.replace(/%(s|d)/g, function(_, specifier){
    var arg = args[i++] || nodes.null;
    switch (specifier) {
      case 's':
        return new Compiler(arg, self.options).compile();
      case 'd':
        arg = utils.unwrap(arg).first;
        if ('unit' != arg.nodeName) throw new Error('%d requires a unit');
        return arg.val;
    }
  });

  return new nodes.Literal(str);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.saturation"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>saturation (color, value)](#apidoc.element.stylus.functions.saturation)
- description and source-code
```javascript
function saturation(color, value){
  if (value) {
    var hslaColor = color.hsla;
    return hsla(
      new nodes.Unit(hslaColor.h),
      value,
      new nodes.Unit(hslaColor.l),
      new nodes.Unit(hslaColor.a)
    )
  }
  return component(color, new nodes.String('saturation'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.selector"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>selector ()](#apidoc.element.stylus.functions.selector)
- description and source-code
```javascript
function selector(){
  var stack = this.selectorStack
    , args = [].slice.call(arguments);

  if (1 == args.length) {
    var expr = utils.unwrap(args[0])
      , len = expr.nodes.length;

    // selector('.a')
    if (1 == len) {
      utils.assertString(expr.first, 'selector');
      var SelectorParser = require('../selector-parser')
        , val = expr.first.string
        , parsed = new SelectorParser(val).parse().val;

      if (parsed == val) return val;

      stack.push(parse(val));
    } else if (len > 1) {
      // selector-list = '.a', '.b', '.c'
      // selector(selector-list)
      if (expr.isList) {
        pushToStack(expr.nodes, stack);
      // selector('.a' '.b' '.c')
      } else {
        stack.push(parse(expr.nodes.map(function(node){
          utils.assertString(node, 'selector');
          return node.string;
        }).join(' ')));
      }
    }
  // selector('.a', '.b', '.c')
  } else if (args.length > 1) {
    pushToStack(args, stack);
  }

  return stack.length ? utils.compileSelectors(stack).join(',') : '&';
}
```
- example usage
```shell
...
    || this.namedop()
    || this.boolean()
    || this.unicode()
    || this.ident()
    || this.op()
    || this.eol()
    || this.space()
    || this.selector();
  tok.lineno = line;
  tok.column = column;
  return tok;
},

/**
 * Lookahead a single token.
...
```

#### <a name="apidoc.element.stylus.functions.selector-exists"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>selector-exists (sel)](#apidoc.element.stylus.functions.selector-exists)
- description and source-code
```javascript
function selectorExists(sel) {
  utils.assertString(sel, 'selector');

  if (!this.__selectorsMap__) {
    var Normalizer = require('../visitor/normalizer')
      , visitor = new Normalizer(this.root.clone());
    visitor.visit(visitor.root);

    this.__selectorsMap__ = visitor.map;
  }

  return sel.string in this.__selectorsMap__;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.selectors"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>selectors ()](#apidoc.element.stylus.functions.selectors)
- description and source-code
```javascript
function selectors(){
  var stack = this.selectorStack
    , expr = new nodes.Expression(true);

  if (stack.length) {
    for (var i = 0; i < stack.length; i++) {
      var group = stack[i]
        , nested;

      if (group.length > 1) {
        expr.push(new nodes.String(group.map(function(selector) {
          nested = new Parser(selector.val).parse().nested;
          return (nested && i ? '& ' : '') + selector.val;
        }).join(',')))
      } else {
        var selector = group[0].val
        nested = new Parser(selector).parse().nested;
        expr.push(new nodes.String((nested && i ? '& ' : '') + selector));
      }
    }
  } else {
    expr.push(new nodes.String('&'));
  }
  return expr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.shift"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>shift (expr)](#apidoc.element.stylus.functions.shift)
- description and source-code
```javascript
shift = function (expr){
  expr = utils.unwrap(expr);
  return expr.nodes.shift();
}
```
- example usage
```shell
...
 * Return the next possibly stashed token.
 *
 * @return {Token}
 * @api private
 */

stashed: function() {
  return this.stash.shift();
},

/**
 * EOS | trailing outdents.
 */

eos: function() {
...
```

#### <a name="apidoc.element.stylus.functions.slice"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>slice (val, start, end)](#apidoc.element.stylus.functions.slice)
- description and source-code
```javascript
function slice(val, start, end) {
  start = start && start.nodes[0].val;
  end = end && end.nodes[0].val;

  val = utils.unwrap(val).nodes;

  if (val.length > 1) {
    return utils.coerce(val.slice(start, end), true);
  }

  var result = val[0].string.slice(start, end);

  return val[0] instanceof nodes.Ident
    ? new nodes.Ident(result)
    : new nodes.String(result);
}
```
- example usage
```shell
...

  return inComment
    ? str
    : val + '\r';
};

// Remove UTF-8 BOM.
if ('\uFEFF' == str.charAt(0)) str = str.slice(1);

this.str = str
  .replace(/\s+$/, '\n')
  .replace(/\r\n?/g, '\n')
  .replace(/\\ *\n/g, '\r')
  .replace(/([,(:](?!\/\/[^ ])) *(?:\/\/[^\n]*|\/\*.*?\*\/)?\n\s*/g, comment)
  .replace(/\s*\n[ \t]*([,)])/g, comment);
...
```

#### <a name="apidoc.element.stylus.functions.split"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>split (delim, val)](#apidoc.element.stylus.functions.split)
- description and source-code
```javascript
function split(delim, val){
  utils.assertString(delim, 'delimiter');
  utils.assertString(val, 'val');
  var splitted = val.string.split(delim.string);
  var expr = new nodes.Expression();
  var ItemNode = val instanceof nodes.Ident
    ? nodes.Ident
    : nodes.String;
  for (var i = 0, len = splitted.length; i < len; ++i) {
    expr.nodes.push(new ItemNode(splitted[i]));
  }
  return expr;
}
```
- example usage
```shell
...
}

// Multi-line
if ('/' == this.str[0] && '*' == this.str[1]) {
  var end = this.str.indexOf('*/');
  if (-1 == end) end = this.str.length;
  var str = this.str.substr(0, end + 2)
    , lines = str.split(/\n|\r/).length - 1
    , suppress = true
    , inline = false;
  this.lineno += lines;
  this.skip(end + 2);
  // output
  if ('!' == str[2]) {
    str = str.replace('*!', '*');
...
```

#### <a name="apidoc.element.stylus.functions.substr"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>substr (val, start, length)](#apidoc.element.stylus.functions.substr)
- description and source-code
```javascript
function substr(val, start, length){
  utils.assertString(val, 'val');
  utils.assertType(start, 'unit', 'start');
  length = length && length.val;
  var res = val.string.substr(start.val, length);
  return val instanceof nodes.Ident
      ? new nodes.Ident(res)
      : new nodes.String(res);
}
```
- example usage
```shell
...
 * @param {Number|Array} len
 * @api private
 */

skip: function(len){
  var chunk = len[0];
  len = chunk ? chunk.length : len;
  this.str = this.str.substr(len);
  if (chunk) {
    this.move(chunk);
  } else {
    this.column += len;
  }
},
...
```

#### <a name="apidoc.element.stylus.functions.tan"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>tan (angle)](#apidoc.element.stylus.functions.tan)
- description and source-code
```javascript
function tan(angle) {
  utils.assertType(angle, 'unit', 'angle');

  var radians = angle.val;

  if (angle.type === 'deg') {
    radians *= Math.PI / 180;
  }

  var m = Math.pow(10, 9);

  var sin = Math.round(Math.sin(radians) * m) / m
    , cos = Math.round(Math.cos(radians) * m) / m
    , tan = Math.round(m * sin / cos ) / m;

  return new nodes.Unit(tan, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.trace"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>trace ()](#apidoc.element.stylus.functions.trace)
- description and source-code
```javascript
function trace(){
  console.log(this.stack);
  return nodes.null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.transparentify"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>transparentify (top, bottom, alpha)](#apidoc.element.stylus.functions.transparentify)
- description and source-code
```javascript
function transparentify(top, bottom, alpha){
  utils.assertColor(top);
  top = top.rgba;
  // Handle default arguments
  bottom = bottom || new nodes.RGBA(255, 255, 255, 1);
  if (!alpha && bottom && !bottom.rgba) {
    alpha = bottom;
    bottom = new nodes.RGBA(255, 255, 255, 1);
  }
  utils.assertColor(bottom);
  bottom = bottom.rgba;
  var bestAlpha = ['r', 'g', 'b'].map(function(channel){
    return (top[channel] - bottom[channel]) / ((0 < (top[channel] - bottom[channel]) ? 255 : 0) - bottom[channel]);
  }).sort(function(a, b){return a < b;})[0];
  if (alpha) {
    utils.assertType(alpha, 'unit', 'alpha');
    if ('%' == alpha.type) {
      bestAlpha = alpha.val / 100;
    } else if (!alpha.type) {
      bestAlpha = alpha = alpha.val;
    }
  }
  bestAlpha = Math.max(Math.min(bestAlpha, 1), 0);
  // Calculate the resulting color
  function processChannel(channel) {
    if (0 == bestAlpha) {
      return bottom[channel]
    } else {
      return bottom[channel] + (top[channel] - bottom[channel]) / bestAlpha
    }
  }
  return new nodes.RGBA(
    processChannel('r'),
    processChannel('g'),
    processChannel('b'),
    Math.round(bestAlpha * 100) / 100
  );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.type"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>type (node)](#apidoc.element.stylus.functions.type)
- description and source-code
```javascript
function type(node){
  utils.assertPresent(node, 'expression');
  return node.nodeName;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.type-of"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>type-of (node)](#apidoc.element.stylus.functions.type-of)
- description and source-code
```javascript
function type(node){
  utils.assertPresent(node, 'expression');
  return node.nodeName;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.typeof"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>typeof (node)](#apidoc.element.stylus.functions.typeof)
- description and source-code
```javascript
function type(node){
  utils.assertPresent(node, 'expression');
  return node.nodeName;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.unit"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>unit (unit, type)](#apidoc.element.stylus.functions.unit)
- description and source-code
```javascript
function unit(unit, type){
  utils.assertType(unit, 'unit', 'unit');

  // Assign
  if (type) {
    utils.assertString(type, 'type');
    return new nodes.Unit(unit.val, type.string);
  } else {
    return unit.type || '';
  }
}
```
- example usage
```shell
...
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
|| this.string()
|| this.unit()
|| this.namedop()
|| this.boolean()
|| this.unicode()
|| this.ident()
|| this.op()
|| this.eol()
|| this.space()
...
```

#### <a name="apidoc.element.stylus.functions.unquote"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>unquote (string)](#apidoc.element.stylus.functions.unquote)
- description and source-code
```javascript
function unquote(string){
  utils.assertString(string, 'string');
  return new nodes.Literal(string.string);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.functions.unshift"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>unshift (expr)](#apidoc.element.stylus.functions.unshift)
- description and source-code
```javascript
unshift = function (expr){
  expr = utils.unwrap(expr);
  for (var i = 1, len = arguments.length; i < len; ++i) {
    expr.nodes.unshift(utils.unwrap(arguments[i]));
  }
  return expr.nodes.length;
}
```
- example usage
```shell
...
  while (this.indentStack.length && this.indentStack[0] > indents) {
    this.stash.push(new Token('outdent'));
    this.indentStack.shift();
  }
  tok = this.stash.pop();
// Indent
} else if (indents && indents != this.indentStack[0]) {
  this.indentStack.unshift(indents);
  tok = new Token('indent');
// Newline
} else {
  tok = new Token('newline');
}

return tok;
...
```

#### <a name="apidoc.element.stylus.functions.use"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>use (plugin, options)](#apidoc.element.stylus.functions.use)
- description and source-code
```javascript
function use(plugin, options){
  utils.assertString(plugin, 'plugin');

  if (options) {
    utils.assertType(options, 'object', 'options');
    options = parseObject(options);
  }

  // lookup
  plugin = plugin.string;
  var found = utils.lookup(plugin, this.options.paths, this.options.filename);
  if (!found) throw new Error('failed to locate plugin file "' + plugin + '"');

  // use
  var fn = require(path.resolve(found));
  if ('function' != typeof fn) {
    throw new Error('plugin "' + plugin + '" does not export a function');
  }
  this.renderer.use(fn(options || this.options));
}
```
- example usage
```shell
...
 *
 *      app.middleware({
 *          src: __dirname
 *        , dest: __dirname + '/public'
 *        , compile: compile
 *      })
 *
 *      app.use(connect.static(__dirname + '/public'));
 *
 * @param {Object} options
 * @return {Function}
 * @api public
 */

module.exports = function(options){
...
```

#### <a name="apidoc.element.stylus.functions.warn"></a>[function <span class="apidocSignatureSpan">stylus.functions.</span>warn (msg)](#apidoc.element.stylus.functions.warn)
- description and source-code
```javascript
function warn(msg){
  utils.assertType(msg, 'string', 'msg');
  console.warn('Warning: %s', msg.val);
  return nodes.null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.lexer"></a>[module stylus.lexer](#apidoc.module.stylus.lexer)

#### <a name="apidoc.element.stylus.lexer.lexer"></a>[function <span class="apidocSignatureSpan">stylus.</span>lexer (str, options)](#apidoc.element.stylus.lexer.lexer)
- description and source-code
```javascript
function Lexer(str, options) {
  options = options || {};
  this.stash = [];
  this.indentStack = [];
  this.indentRe = null;
  this.lineno = 1;
  this.column = 1;

  // HACK!
  function comment(str, val, offset, s) {
    var inComment = s.lastIndexOf('/*', offset) > s.lastIndexOf('*/', offset)
      , commentIdx = s.lastIndexOf('//', offset)
      , i = s.lastIndexOf('\n', offset)
      , double = 0
      , single = 0;

    if (~commentIdx && commentIdx > i) {
      while (i != offset) {
        if ("'" == s[i]) single ? single-- : single++;
        if ('"' == s[i]) double ? double-- : double++;

        if ('/' == s[i] && '/' == s[i + 1]) {
          inComment = !single && !double;
          break;
        }
        ++i;
      }
    }

    return inComment
      ? str
      : val + '\r';
  };

  // Remove UTF-8 BOM.
  if ('\uFEFF' == str.charAt(0)) str = str.slice(1);

  this.str = str
    .replace(/\s+$/, '\n')
    .replace(/\r\n?/g, '\n')
    .replace(/\\ *\n/g, '\r')
    .replace(/([,(:](?!\/\/[^ ])) *(?:\/\/[^\n]*|\/\*.*?\*\/)?\n\s*/g, comment)
    .replace(/\s*\n[ \t]*([,)])/g, comment);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.lexer.prototype"></a>[module stylus.lexer.prototype](#apidoc.module.stylus.lexer.prototype)

#### <a name="apidoc.element.stylus.lexer.prototype.advance"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>advance ()](#apidoc.element.stylus.lexer.prototype.advance)
- description and source-code
```javascript
advance = function () {
  var column = this.column
    , line = this.lineno
    , tok = this.eos()
    || this.null()
    || this.sep()
    || this.keyword()
    || this.urlchars()
    || this.comment()
    || this.newline()
    || this.escaped()
    || this.important()
    || this.literal()
    || this.anonFunc()
    || this.atrule()
    || this.function()
    || this.brace()
    || this.paren()
    || this.color()
    || this.string()
    || this.unit()
    || this.namedop()
    || this.boolean()
    || this.unicode()
    || this.ident()
    || this.op()
    || this.eol()
    || this.space()
    || this.selector();
  tok.lineno = line;
  tok.column = column;
  return tok;
}
```
- example usage
```shell
...
 * @param {Number} n
 * @return {Object}
 * @api private
 */

lookahead: function(n){
  var fetch = n - this.stash.length;
  while (fetch-- > 0) this.stash.push(this.advance());
  return this.stash[--n];
},

/**
 * Consume the given 'len'.
 *
 * @param {Number|Array} len
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.anonFunc"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>anonFunc ()](#apidoc.element.stylus.lexer.prototype.anonFunc)
- description and source-code
```javascript
anonFunc = function () {
  var tok;
  if ('@' == this.str[0] && '(' == this.str[1]) {
    this.skip(2);
    tok = new Token('function', new nodes.Ident('anonymous'));
    tok.anonymous = true;
    return tok;
  }
}
```
- example usage
```shell
...
|| this.keyword()
|| this.urlchars()
|| this.comment()
|| this.newline()
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
|| this.string()
|| this.unit()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.atrule"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>atrule ()](#apidoc.element.stylus.lexer.prototype.atrule)
- description and source-code
```javascript
atrule = function () {
  var captures;
  if (captures = /^@(?:-(\w+)-)?([a-zA-Z0-9-_]+)[ \t]*/.exec(this.str)) {
    this.skip(captures);
    var vendor = captures[1]
      , type = captures[2]
      , tok;
    switch (type) {
      case 'require':
      case 'import':
      case 'charset':
      case 'namespace':
      case 'media':
      case 'scope':
      case 'supports':
        return new Token(type);
      case 'document':
        return new Token('-moz-document');
      case 'block':
        return new Token('atblock');
      case 'extend':
      case 'extends':
        return new Token('extend');
      case 'keyframes':
        return new Token(type, vendor);
      default:
        return new Token('atrule', (vendor ? '-' + vendor + '-' + type : type));
    }
  }
}
```
- example usage
```shell
...
|| this.urlchars()
|| this.comment()
|| this.newline()
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
|| this.string()
|| this.unit()
|| this.namedop()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.boolean"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>boolean ()](#apidoc.element.stylus.lexer.prototype.boolean)
- description and source-code
```javascript
boolean = function () {
  var captures;
  if (captures = /^(true|false)\b([ \t]*)/.exec(this.str)) {
    var val = nodes.Boolean('true' == captures[1]);
    this.skip(captures);
    var tok = new Token('boolean', val);
    tok.space = captures[2];
    return tok;
  }
}
```
- example usage
```shell
...
  || this.function()
  || this.brace()
  || this.paren()
  || this.color()
  || this.string()
  || this.unit()
  || this.namedop()
  || this.boolean()
  || this.unicode()
  || this.ident()
  || this.op()
  || this.eol()
  || this.space()
  || this.selector();
tok.lineno = line;
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.brace"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>brace ()](#apidoc.element.stylus.lexer.prototype.brace)
- description and source-code
```javascript
brace = function () {
  var captures;
  if (captures = /^([{}])/.exec(this.str)) {
    this.skip(1);
    var brace = captures[1];
    return new Token(brace, brace);
  }
}
```
- example usage
```shell
...
|| this.newline()
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
|| this.string()
|| this.unit()
|| this.namedop()
|| this.boolean()
|| this.unicode()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.color"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>color ()](#apidoc.element.stylus.lexer.prototype.color)
- description and source-code
```javascript
color = function () {
  return this.rrggbbaa()
    || this.rrggbb()
    || this.rgba()
    || this.rgb()
    || this.nn()
    || this.n()
}
```
- example usage
```shell
...
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
|| this.string()
|| this.unit()
|| this.namedop()
|| this.boolean()
|| this.unicode()
|| this.ident()
|| this.op()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.comment"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>comment ()](#apidoc.element.stylus.lexer.prototype.comment)
- description and source-code
```javascript
comment = function () {
  // Single line
  if ('/' == this.str[0] && '/' == this.str[1]) {
    var end = this.str.indexOf('\n');
    if (-1 == end) end = this.str.length;
    this.skip(end);
    return this.advance();
  }

  // Multi-line
  if ('/' == this.str[0] && '*' == this.str[1]) {
    var end = this.str.indexOf('*/');
    if (-1 == end) end = this.str.length;
    var str = this.str.substr(0, end + 2)
      , lines = str.split(/\n|\r/).length - 1
      , suppress = true
      , inline = false;
    this.lineno += lines;
    this.skip(end + 2);
    // output
    if ('!' == str[2]) {
      str = str.replace('*!', '*');
      suppress = false;
    }
    if (this.prev && ';' == this.prev.type) inline = true;
    return new Token('comment', new nodes.Comment(str, suppress, inline));
  }
}
```
- example usage
```shell
...
    var column = this.column
, line = this.lineno
, tok = this.eos()
|| this.null()
|| this.sep()
|| this.keyword()
|| this.urlchars()
|| this.comment()
|| this.newline()
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.eol"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>eol ()](#apidoc.element.stylus.lexer.prototype.eol)
- description and source-code
```javascript
eol = function () {
  if ('\r' == this.str[0]) {
    ++this.lineno;
    this.skip(1);
    return this.advance();
  }
}
```
- example usage
```shell
...
    || this.string()
    || this.unit()
    || this.namedop()
    || this.boolean()
    || this.unicode()
    || this.ident()
    || this.op()
    || this.eol()
    || this.space()
    || this.selector();
  tok.lineno = line;
  tok.column = column;
  return tok;
},
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.eos"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>eos ()](#apidoc.element.stylus.lexer.prototype.eos)
- description and source-code
```javascript
eos = function () {
  if (this.str.length) return;
  if (this.indentStack.length) {
    this.indentStack.shift();
    return new Token('outdent');
  } else {
    return new Token('eos');
  }
}
```
- example usage
```shell
...
 * @return {Token}
 * @api private
 */

advance: function() {
  var column = this.column
    , line = this.lineno
    , tok = this.eos()
    || this.null()
    || this.sep()
    || this.keyword()
    || this.urlchars()
    || this.comment()
    || this.newline()
    || this.escaped()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.escaped"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>escaped ()](#apidoc.element.stylus.lexer.prototype.escaped)
- description and source-code
```javascript
escaped = function () {
  var captures;
  if (captures = /^\\(.)[ \t]*/.exec(this.str)) {
    var c = captures[1];
    this.skip(captures);
    return new Token('ident', new nodes.Literal(c));
  }
}
```
- example usage
```shell
...
, tok = this.eos()
|| this.null()
|| this.sep()
|| this.keyword()
|| this.urlchars()
|| this.comment()
|| this.newline()
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.function"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>function ()](#apidoc.element.stylus.lexer.prototype.function)
- description and source-code
```javascript
function = function () {
  var captures;
  if (captures = /^(-*[_a-zA-Z$][-\w\d$]*)\(([ \t]*)/.exec(this.str)) {
    var name = captures[1];
    this.skip(captures);
    this.isURL = 'url' == name;
    var tok = new Token('function', new nodes.Ident(name));
    tok.space = captures[2];
    return tok;
  }
}
```
- example usage
```shell
...
|| this.comment()
|| this.newline()
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
|| this.string()
|| this.unit()
|| this.namedop()
|| this.boolean()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.ident"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>ident ()](#apidoc.element.stylus.lexer.prototype.ident)
- description and source-code
```javascript
ident = function () {
  var captures;
  if (captures = /^-*[_a-zA-Z$][-\w\d$]*/.exec(this.str)) {
    this.skip(captures);
    return new Token('ident', new nodes.Ident(captures[0]));
  }
}
```
- example usage
```shell
...
  || this.paren()
  || this.color()
  || this.string()
  || this.unit()
  || this.namedop()
  || this.boolean()
  || this.unicode()
  || this.ident()
  || this.op()
  || this.eol()
  || this.space()
  || this.selector();
tok.lineno = line;
tok.column = column;
return tok;
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.important"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>important ()](#apidoc.element.stylus.lexer.prototype.important)
- description and source-code
```javascript
important = function () {
  var captures;
  if (captures = /^!important[ \t]*/.exec(this.str)) {
    this.skip(captures);
    return new Token('ident', new nodes.Literal('!important'));
  }
}
```
- example usage
```shell
...
|| this.null()
|| this.sep()
|| this.keyword()
|| this.urlchars()
|| this.comment()
|| this.newline()
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.inspect"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>inspect ()](#apidoc.element.stylus.lexer.prototype.inspect)
- description and source-code
```javascript
inspect = function (){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
}
```
- example usage
```shell
...
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
 * Lookahead 'n' tokens.
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.isPartOfSelector"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>isPartOfSelector ()](#apidoc.element.stylus.lexer.prototype.isPartOfSelector)
- description and source-code
```javascript
isPartOfSelector = function () {
  var tok = this.stash[this.stash.length - 1] || this.prev;
  switch (tok && tok.type) {
    // #for
    case 'color':
      return 2 == tok.val.raw.length;
    // .or
    case '.':
    // [is]
    case '[':
      return true;
  }
  return false;
}
```
- example usage
```shell
...
 */

null: function() {
  var captures
    , tok;
  if (captures = /^(null)\b[ \t]*/.exec(this.str)) {
    this.skip(captures);
    if (this.isPartOfSelector()) {
      tok = new Token('ident', new nodes.Ident(captures[0]));
    } else {
      tok = new Token('null', nodes.null);
    }
    return tok;
  }
},
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.keyword"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>keyword ()](#apidoc.element.stylus.lexer.prototype.keyword)
- description and source-code
```javascript
keyword = function () {
  var captures
    , tok;
  if (captures = /^(return|if|else|unless|for|in)\b[ \t]*/.exec(this.str)) {
    var keyword = captures[1];
    this.skip(captures);
    if (this.isPartOfSelector()) {
      tok = new Token('ident', new nodes.Ident(captures[0]));
    } else {
      tok = new Token(keyword, keyword);
    }
    return tok;
  }
}
```
- example usage
```shell
...

  advance: function() {
var column = this.column
  , line = this.lineno
  , tok = this.eos()
  || this.null()
  || this.sep()
  || this.keyword()
  || this.urlchars()
  || this.comment()
  || this.newline()
  || this.escaped()
  || this.important()
  || this.literal()
  || this.anonFunc()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.literal"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>literal ()](#apidoc.element.stylus.lexer.prototype.literal)
- description and source-code
```javascript
literal = function () {
  // HACK attack !!!
  var captures;
  if (captures = /^@css[ \t]*\{/.exec(this.str)) {
    this.skip(captures);
    var c
      , braces = 1
      , css = ''
      , node;
    while (c = this.str[0]) {
      this.str = this.str.substr(1);
      switch (c) {
        case '{': ++braces; break;
        case '}': --braces; break;
        case '\n':
        case '\r':
          ++this.lineno;
          break;
      }
      css += c;
      if (!braces) break;
    }
    css = css.replace(/\s*}$/, '');
    node = new nodes.Literal(css);
    node.css = true;
    return new Token('literal', node);
  }
}
```
- example usage
```shell
...
|| this.sep()
|| this.keyword()
|| this.urlchars()
|| this.comment()
|| this.newline()
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
|| this.string()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.lookahead"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>lookahead (n)](#apidoc.element.stylus.lexer.prototype.lookahead)
- description and source-code
```javascript
lookahead = function (n){
  var fetch = n - this.stash.length;
  while (fetch-- > 0) this.stash.push(this.advance());
  return this.stash[--n];
}
```
- example usage
```shell
...
 * Lookahead a single token.
 *
 * @return {Token}
 * @api private
 */

peek: function() {
  return this.lookahead(1);
},

/**
 * Return the next possibly stashed token.
 *
 * @return {Token}
 * @api private
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.move"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>move (str)](#apidoc.element.stylus.lexer.prototype.move)
- description and source-code
```javascript
move = function (str){
  var lines = str.match(/\n/g)
    , idx = str.lastIndexOf('\n');

  if (lines) this.lineno += lines.length;
  this.column = ~idx
    ? str.length - idx
    : this.column + str.length;
}
```
- example usage
```shell
...
 */

skip: function(len){
  var chunk = len[0];
  len = chunk ? chunk.length : len;
  this.str = this.str.substr(len);
  if (chunk) {
    this.move(chunk);
  } else {
    this.column += len;
  }
},

/**
 * Move current line and column position.
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.n"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>n ()](#apidoc.element.stylus.lexer.prototype.n)
- description and source-code
```javascript
n = function () {
  var captures;
  if (captures = /^#([a-fA-F0-9]{1})[ \t]*/.exec(this.str)) {
    this.skip(captures);
    var n = parseInt(captures[1] + captures[1], 16)
      , color = new nodes.RGBA(n, n, n, 1);
    color.raw = captures[0];
    return new Token('color', color);
  }
}
```
- example usage
```shell
...

color: function() {
  return this.rrggbbaa()
    || this.rrggbb()
    || this.rgba()
    || this.rgb()
    || this.nn()
    || this.n()
},

/**
 * #n
 */

n: function() {
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.namedop"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>namedop ()](#apidoc.element.stylus.lexer.prototype.namedop)
- description and source-code
```javascript
namedop = function () {
  var captures
    , tok;
  if (captures = /^(not|and|or|is a|is defined|isnt|is not|is)(?!-)\b([ \t]*)/.exec(this.str)) {
    var op = captures[1];
    this.skip(captures);
    if (this.isPartOfSelector()) {
      tok = new Token('ident', new nodes.Ident(captures[0]));
    } else {
      op = alias[op] || op;
      tok = new Token(op, op);
    }
    tok.space = captures[2];
    return tok;
  }
}
```
- example usage
```shell
...
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
|| this.string()
|| this.unit()
|| this.namedop()
|| this.boolean()
|| this.unicode()
|| this.ident()
|| this.op()
|| this.eol()
|| this.space()
|| this.selector();
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.newline"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>newline ()](#apidoc.element.stylus.lexer.prototype.newline)
- description and source-code
```javascript
newline = function () {
  var captures, re;

  // we have established the indentation regexp
  if (this.indentRe){
    captures = this.indentRe.exec(this.str);
  // figure out if we are using tabs or spaces
  } else {
    // try tabs
    re = /^\n([\t]*)[ \t]*/;
    captures = re.exec(this.str);

    // nope, try spaces
    if (captures && !captures[1].length) {
      re = /^\n([ \t]*)/;
      captures = re.exec(this.str);
    }

    // established
    if (captures && captures[1].length) this.indentRe = re;
  }


  if (captures) {
    var tok
      , indents = captures[1].length;

    this.skip(captures);
    if (this.str[0] === ' ' || this.str[0] === '\t') {
      throw new errors.SyntaxError('Invalid indentation. You can use tabs or spaces to indent, but not both.');
    }

    // Blank line
    if ('\n' == this.str[0]) return this.advance();

    // Outdent
    if (this.indentStack.length && indents < this.indentStack[0]) {
      while (this.indentStack.length && this.indentStack[0] > indents) {
        this.stash.push(new Token('outdent'));
        this.indentStack.shift();
      }
      tok = this.stash.pop();
    // Indent
    } else if (indents && indents != this.indentStack[0]) {
      this.indentStack.unshift(indents);
      tok = new Token('indent');
    // Newline
    } else {
      tok = new Token('newline');
    }

    return tok;
  }
}
```
- example usage
```shell
...
, line = this.lineno
, tok = this.eos()
|| this.null()
|| this.sep()
|| this.keyword()
|| this.urlchars()
|| this.comment()
|| this.newline()
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.next"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>next ()](#apidoc.element.stylus.lexer.prototype.next)
- description and source-code
```javascript
next = function () {
  var tok = this.stashed() || this.advance();
  this.prev = tok;
  return tok;
}
```
- example usage
```shell
...
 * Custom inspect.
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.nn"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>nn ()](#apidoc.element.stylus.lexer.prototype.nn)
- description and source-code
```javascript
nn = function () {
  var captures;
  if (captures = /^#([a-fA-F0-9]{2})[ \t]*/.exec(this.str)) {
    this.skip(captures);
    var n = parseInt(captures[1], 16)
      , color = new nodes.RGBA(n, n, n, 1);
    color.raw = captures[0];
    return new Token('color', color);
  }
}
```
- example usage
```shell
...
 */

color: function() {
  return this.rrggbbaa()
    || this.rrggbb()
    || this.rgba()
    || this.rgb()
    || this.nn()
    || this.n()
},

/**
 * #n
 */
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.null"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>null ()](#apidoc.element.stylus.lexer.prototype.null)
- description and source-code
```javascript
null = function () {
  var captures
    , tok;
  if (captures = /^(null)\b[ \t]*/.exec(this.str)) {
    this.skip(captures);
    if (this.isPartOfSelector()) {
      tok = new Token('ident', new nodes.Ident(captures[0]));
    } else {
      tok = new Token('null', nodes.null);
    }
    return tok;
  }
}
```
- example usage
```shell
...
 * @api private
 */

advance: function() {
  var column = this.column
    , line = this.lineno
    , tok = this.eos()
    || this.null()
    || this.sep()
    || this.keyword()
    || this.urlchars()
    || this.comment()
    || this.newline()
    || this.escaped()
    || this.important()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.op"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>op ()](#apidoc.element.stylus.lexer.prototype.op)
- description and source-code
```javascript
op = function () {
  var captures;
  if (captures = /^([.]{1,3}|&&|\|\||[!<>=?:]=|\*\*|[-+*\/%]=?|[,=?:!~<>&\[\]])([ \t]*)/.exec(this.str)) {
    var op = captures[1];
    this.skip(captures);
    op = alias[op] || op;
    var tok = new Token(op, op);
    tok.space = captures[2];
    this.isURL = false;
    return tok;
  }
}
```
- example usage
```shell
...
    || this.color()
    || this.string()
    || this.unit()
    || this.namedop()
    || this.boolean()
    || this.unicode()
    || this.ident()
    || this.op()
    || this.eol()
    || this.space()
    || this.selector();
  tok.lineno = line;
  tok.column = column;
  return tok;
},
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.paren"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>paren ()](#apidoc.element.stylus.lexer.prototype.paren)
- description and source-code
```javascript
paren = function () {
  var captures;
  if (captures = /^([()])([ \t]*)/.exec(this.str)) {
    var paren = captures[1];
    this.skip(captures);
    if (')' == paren) this.isURL = false;
    var tok = new Token(paren, paren);
    tok.space = captures[2];
    return tok;
  }
}
```
- example usage
```shell
...
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
|| this.string()
|| this.unit()
|| this.namedop()
|| this.boolean()
|| this.unicode()
|| this.ident()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.peek"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>peek ()](#apidoc.element.stylus.lexer.prototype.peek)
- description and source-code
```javascript
peek = function () {
  return this.lookahead(1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.lexer.prototype.rgb"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>rgb ()](#apidoc.element.stylus.lexer.prototype.rgb)
- description and source-code
```javascript
rgb = function () {
  var captures;
  if (captures = /^#([a-fA-F0-9]{3})[ \t]*/.exec(this.str)) {
    this.skip(captures);
    var rgb = captures[1]
      , r = parseInt(rgb[0] + rgb[0], 16)
      , g = parseInt(rgb[1] + rgb[1], 16)
      , b = parseInt(rgb[2] + rgb[2], 16)
      , color = new nodes.RGBA(r, g, b, 1);
    color.raw = captures[0];
    return new Token('color', color);
  }
}
```
- example usage
```shell
...
 * #rrggbbaa | #rrggbb | #rgba | #rgb | #nn | #n
 */

color: function() {
  return this.rrggbbaa()
    || this.rrggbb()
    || this.rgba()
    || this.rgb()
    || this.nn()
    || this.n()
},

/**
 * #n
 */
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.rgba"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>rgba ()](#apidoc.element.stylus.lexer.prototype.rgba)
- description and source-code
```javascript
rgba = function () {
  var captures;
  if (captures = /^#([a-fA-F0-9]{4})[ \t]*/.exec(this.str)) {
    this.skip(captures);
    var rgb = captures[1]
      , r = parseInt(rgb[0] + rgb[0], 16)
      , g = parseInt(rgb[1] + rgb[1], 16)
      , b = parseInt(rgb[2] + rgb[2], 16)
      , a = parseInt(rgb[3] + rgb[3], 16)
      , color = new nodes.RGBA(r, g, b, a/255);
    color.raw = captures[0];
    return new Token('color', color);
  }
}
```
- example usage
```shell
...
/**
 * #rrggbbaa | #rrggbb | #rgba | #rgb | #nn | #n
 */

color: function() {
  return this.rrggbbaa()
    || this.rrggbb()
    || this.rgba()
    || this.rgb()
    || this.nn()
    || this.n()
},

/**
 * #n
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.rrggbb"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>rrggbb ()](#apidoc.element.stylus.lexer.prototype.rrggbb)
- description and source-code
```javascript
rrggbb = function () {
  var captures;
  if (captures = /^#([a-fA-F0-9]{6})[ \t]*/.exec(this.str)) {
    this.skip(captures);
    var rgb = captures[1]
      , r = parseInt(rgb.substr(0, 2), 16)
      , g = parseInt(rgb.substr(2, 2), 16)
      , b = parseInt(rgb.substr(4, 2), 16)
      , color = new nodes.RGBA(r, g, b, 1);
    color.raw = captures[0];
    return new Token('color', color);
  }
}
```
- example usage
```shell
...

/**
 * #rrggbbaa | #rrggbb | #rgba | #rgb | #nn | #n
 */

color: function() {
  return this.rrggbbaa()
    || this.rrggbb()
    || this.rgba()
    || this.rgb()
    || this.nn()
    || this.n()
},

/**
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.rrggbbaa"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>rrggbbaa ()](#apidoc.element.stylus.lexer.prototype.rrggbbaa)
- description and source-code
```javascript
rrggbbaa = function () {
  var captures;
  if (captures = /^#([a-fA-F0-9]{8})[ \t]*/.exec(this.str)) {
    this.skip(captures);
    var rgb = captures[1]
      , r = parseInt(rgb.substr(0, 2), 16)
      , g = parseInt(rgb.substr(2, 2), 16)
      , b = parseInt(rgb.substr(4, 2), 16)
      , a = parseInt(rgb.substr(6, 2), 16)
      , color = new nodes.RGBA(r, g, b, a/255);
    color.raw = captures[0];
    return new Token('color', color);
  }
}
```
- example usage
```shell
...
},

/**
 * #rrggbbaa | #rrggbb | #rgba | #rgb | #nn | #n
 */

color: function() {
  return this.rrggbbaa()
    || this.rrggbb()
    || this.rgba()
    || this.rgb()
    || this.nn()
    || this.n()
},
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.selector"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>selector ()](#apidoc.element.stylus.lexer.prototype.selector)
- description and source-code
```javascript
selector = function () {
  var captures;
  if (captures = /^\^|.*?(?=\/\/(?![^\[]*\])|[,\n{])/.exec(this.str)) {
    var selector = captures[0];
    this.skip(captures);
    return new Token('selector', selector);
  }
}
```
- example usage
```shell
...
    || this.namedop()
    || this.boolean()
    || this.unicode()
    || this.ident()
    || this.op()
    || this.eol()
    || this.space()
    || this.selector();
  tok.lineno = line;
  tok.column = column;
  return tok;
},

/**
 * Lookahead a single token.
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.sep"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>sep ()](#apidoc.element.stylus.lexer.prototype.sep)
- description and source-code
```javascript
sep = function () {
  var captures;
  if (captures = /^;[ \t]*/.exec(this.str)) {
    this.skip(captures);
    return new Token(';');
  }
}
```
- example usage
```shell
...
 */

advance: function() {
  var column = this.column
    , line = this.lineno
    , tok = this.eos()
    || this.null()
    || this.sep()
    || this.keyword()
    || this.urlchars()
    || this.comment()
    || this.newline()
    || this.escaped()
    || this.important()
    || this.literal()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.skip"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>skip (len)](#apidoc.element.stylus.lexer.prototype.skip)
- description and source-code
```javascript
skip = function (len){
  var chunk = len[0];
  len = chunk ? chunk.length : len;
  this.str = this.str.substr(len);
  if (chunk) {
    this.move(chunk);
  } else {
    this.column += len;
  }
}
```
- example usage
```shell
...
 * url char
 */

urlchars: function() {
  var captures;
  if (!this.isURL) return;
  if (captures = /^[\/:@.;?&=*!,<>#%0-9]+/.exec(this.str)) {
    this.skip(captures);
    return new Token('literal', new nodes.Literal(captures[0]));
  }
},

/**
 * ';' [ \t]*
 */
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.space"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>space ()](#apidoc.element.stylus.lexer.prototype.space)
- description and source-code
```javascript
space = function () {
  var captures;
  if (captures = /^([ \t]+)/.exec(this.str)) {
    this.skip(captures);
    return new Token('space');
  }
}
```
- example usage
```shell
...
    || this.unit()
    || this.namedop()
    || this.boolean()
    || this.unicode()
    || this.ident()
    || this.op()
    || this.eol()
    || this.space()
    || this.selector();
  tok.lineno = line;
  tok.column = column;
  return tok;
},

/**
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.stashed"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>stashed ()](#apidoc.element.stylus.lexer.prototype.stashed)
- description and source-code
```javascript
stashed = function () {
  return this.stash.shift();
}
```
- example usage
```shell
...
 * Fetch next token including those stashed by peek.
 *
 * @return {Token}
 * @api private
 */

next: function() {
  var tok = this.stashed() || this.advance();
  this.prev = tok;
  return tok;
},

/**
 * Check if the current token is a part of selector.
 *
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.string"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>string ()](#apidoc.element.stylus.lexer.prototype.string)
- description and source-code
```javascript
string = function () {
  var captures;
  if (captures = /^("[^"]*"|'[^']*')[ \t]*/.exec(this.str)) {
    var str = captures[1]
      , quote = captures[0][0];
    this.skip(captures);
    str = str.slice(1,-1).replace(/\\n/g, '\n');
    return new Token('string', new nodes.String(str, quote));
  }
}
```
- example usage
```shell
...
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
|| this.string()
|| this.unit()
|| this.namedop()
|| this.boolean()
|| this.unicode()
|| this.ident()
|| this.op()
|| this.eol()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.unicode"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>unicode ()](#apidoc.element.stylus.lexer.prototype.unicode)
- description and source-code
```javascript
unicode = function () {
  var captures;
  if (captures = /^u\+[0-9a-f?]{1,6}(?:-[0-9a-f]{1,6})?/i.exec(this.str)) {
    this.skip(captures);
    return new Token('literal', new nodes.Literal(captures[0]));
  }
}
```
- example usage
```shell
...
  || this.brace()
  || this.paren()
  || this.color()
  || this.string()
  || this.unit()
  || this.namedop()
  || this.boolean()
  || this.unicode()
  || this.ident()
  || this.op()
  || this.eol()
  || this.space()
  || this.selector();
tok.lineno = line;
tok.column = column;
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.unit"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>unit ()](#apidoc.element.stylus.lexer.prototype.unit)
- description and source-code
```javascript
unit = function () {
  var captures;
  if (captures = /^(-)?(\d+\.\d+|\d+|\.\d+)(%|[a-zA-Z]+)?[ \t]*/.exec(this.str)) {
    this.skip(captures);
    var n = parseFloat(captures[2]);
    if ('-' == captures[1]) n = -n;
    var node = new nodes.Unit(n, captures[3]);
    node.raw = captures[0];
    return new Token('unit', node);
  }
}
```
- example usage
```shell
...
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
|| this.color()
|| this.string()
|| this.unit()
|| this.namedop()
|| this.boolean()
|| this.unicode()
|| this.ident()
|| this.op()
|| this.eol()
|| this.space()
...
```

#### <a name="apidoc.element.stylus.lexer.prototype.urlchars"></a>[function <span class="apidocSignatureSpan">stylus.lexer.prototype.</span>urlchars ()](#apidoc.element.stylus.lexer.prototype.urlchars)
- description and source-code
```javascript
urlchars = function () {
  var captures;
  if (!this.isURL) return;
  if (captures = /^[\/:@.;?&=*!,<>#%0-9]+/.exec(this.str)) {
    this.skip(captures);
    return new Token('literal', new nodes.Literal(captures[0]));
  }
}
```
- example usage
```shell
...
  advance: function() {
var column = this.column
  , line = this.lineno
  , tok = this.eos()
  || this.null()
  || this.sep()
  || this.keyword()
  || this.urlchars()
  || this.comment()
  || this.newline()
  || this.escaped()
  || this.important()
  || this.literal()
  || this.anonFunc()
  || this.atrule()
...
```



# <a name="apidoc.module.stylus.nodes"></a>[module stylus.nodes](#apidoc.module.stylus.nodes)

#### <a name="apidoc.element.stylus.nodes.Arguments"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Arguments ()](#apidoc.element.stylus.nodes.Arguments)
- description and source-code
```javascript
function Arguments(){
  nodes.Expression.call(this);
  this.map = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Atblock"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Atblock ()](#apidoc.element.stylus.nodes.Atblock)
- description and source-code
```javascript
function Atblock(){
  Node.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Atrule"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Atrule (type)](#apidoc.element.stylus.nodes.Atrule)
- description and source-code
```javascript
function Atrule(type){
  Node.call(this);
  this.type = type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.BinOp"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>BinOp (op, left, right)](#apidoc.element.stylus.nodes.BinOp)
- description and source-code
```javascript
function BinOp(op, left, right){
  Node.call(this);
  this.op = op;
  this.left = left;
  this.right = right;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Block"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Block (parent, node)](#apidoc.element.stylus.nodes.Block)
- description and source-code
```javascript
function Block(parent, node){
  Node.call(this);
  this.nodes = [];
  this.parent = parent;
  this.node = node;
  this.scope = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Boolean"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Boolean (val)](#apidoc.element.stylus.nodes.Boolean)
- description and source-code
```javascript
function Boolean(val){
  Node.call(this);
  if (this.nodeName) {
    this.val = !!val;
  } else {
    return new Boolean(val);
  }
}
```
- example usage
```shell
...
/**
 * 'true' | 'false'
 */

boolean: function() {
  var captures;
  if (captures = /^(true|false)\b([ \t]*)/.exec(this.str)) {
    var val = nodes.Boolean('true' == captures[1]);
    this.skip(captures);
    var tok = new Token('boolean', val);
    tok.space = captures[2];
    return tok;
  }
},
...
```

#### <a name="apidoc.element.stylus.nodes.Call"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Call (name, args)](#apidoc.element.stylus.nodes.Call)
- description and source-code
```javascript
function Call(name, args){
  Node.call(this);
  this.name = name;
  this.args = args;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Charset"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Charset (val)](#apidoc.element.stylus.nodes.Charset)
- description and source-code
```javascript
function Charset(val){
  Node.call(this);
  this.val = val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Comment"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Comment (str, suppress, inline)](#apidoc.element.stylus.nodes.Comment)
- description and source-code
```javascript
function Comment(str, suppress, inline){
  Node.call(this);
  this.str = str;
  this.suppress = suppress;
  this.inline = inline;
}
```
- example usage
```shell
...
    this.skip(end + 2);
    // output
    if ('!' == str[2]) {
      str = str.replace('*!', '*');
      suppress = false;
    }
    if (this.prev && ';' == this.prev.type) inline = true;
    return new Token('comment', new nodes.Comment(str, suppress, inline));
  }
},

/**
 * 'true' | 'false'
 */
...
```

#### <a name="apidoc.element.stylus.nodes.Each"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Each (val, key, expr, block)](#apidoc.element.stylus.nodes.Each)
- description and source-code
```javascript
function Each(val, key, expr, block){
  Node.call(this);
  this.val = val;
  this.key = key;
  this.expr = expr;
  this.block = block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Expression"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Expression (isList)](#apidoc.element.stylus.nodes.Expression)
- description and source-code
```javascript
function Expression(isList){
  Node.call(this);
  this.nodes = [];
  this.isList = isList;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Extend"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Extend (selectors)](#apidoc.element.stylus.nodes.Extend)
- description and source-code
```javascript
function Extend(selectors){
  Node.call(this);
  this.selectors = selectors;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Feature"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Feature (segs)](#apidoc.element.stylus.nodes.Feature)
- description and source-code
```javascript
function Feature(segs){
  Node.call(this);
  this.segments = segs;
  this.expr = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Function"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Function (name, params, body)](#apidoc.element.stylus.nodes.Function)
- description and source-code
```javascript
function Function(name, params, body){
  Node.call(this);
  this.name = name;
  this.params = params;
  this.block = body;
  if ('function' == typeof params) this.fn = params;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Group"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Group ()](#apidoc.element.stylus.nodes.Group)
- description and source-code
```javascript
function Group(){
  Node.call(this);
  this.nodes = [];
  this.extends = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.HSLA"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>HSLA (h, s, l, a)](#apidoc.element.stylus.nodes.HSLA)
- description and source-code
```javascript
function HSLA(h, s, l, a){
  Node.call(this);
  this.h = clampDegrees(h);
  this.s = clampPercentage(s);
  this.l = clampPercentage(l);
  this.a = clampAlpha(a);
  this.hsla = this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Ident"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Ident (name, val, mixin)](#apidoc.element.stylus.nodes.Ident)
- description and source-code
```javascript
function Ident(name, val, mixin){
  Node.call(this);
  this.name = name;
  this.string = name;
  this.val = val || nodes.null;
  this.mixin = !!mixin;
}
```
- example usage
```shell
...

null: function() {
  var captures
    , tok;
  if (captures = /^(null)\b[ \t]*/.exec(this.str)) {
    this.skip(captures);
    if (this.isPartOfSelector()) {
      tok = new Token('ident', new nodes.Ident(captures[0]));
    } else {
      tok = new Token('null', nodes.null);
    }
    return tok;
  }
},
...
```

#### <a name="apidoc.element.stylus.nodes.If"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>If (cond, negate)](#apidoc.element.stylus.nodes.If)
- description and source-code
```javascript
function If(cond, negate){
  Node.call(this);
  this.cond = cond;
  this.elses = [];
  if (negate && negate.nodeName) {
    this.block = negate;
  } else {
    this.negate = negate;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Import"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Import (expr, once)](#apidoc.element.stylus.nodes.Import)
- description and source-code
```javascript
function Import(expr, once){
  Node.call(this);
  this.path = expr;
  this.once = once || false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Keyframes"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Keyframes (segs, prefix)](#apidoc.element.stylus.nodes.Keyframes)
- description and source-code
```javascript
function Keyframes(segs, prefix){
  Atrule.call(this, 'keyframes');
  this.segments = segs;
  this.prefix = prefix || 'official';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Literal"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Literal (str)](#apidoc.element.stylus.nodes.Literal)
- description and source-code
```javascript
function Literal(str){
  Node.call(this);
  this.val = str;
  this.string = str;
  this.prefixed = false;
}
```
- example usage
```shell
...
 */

urlchars: function() {
  var captures;
  if (!this.isURL) return;
  if (captures = /^[\/:@.;?&=*!,<>#%0-9]+/.exec(this.str)) {
    this.skip(captures);
    return new Token('literal', new nodes.Literal(captures[0]));
  }
},

/**
 * ';' [ \t]*
 */
...
```

#### <a name="apidoc.element.stylus.nodes.Media"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Media (val)](#apidoc.element.stylus.nodes.Media)
- description and source-code
```javascript
function Media(val){
  Atrule.call(this, 'media');
  this.val = val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Member"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Member (left, right)](#apidoc.element.stylus.nodes.Member)
- description and source-code
```javascript
function Member(left, right){
  Node.call(this);
  this.left = left;
  this.right = right;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Namespace"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Namespace (val, prefix)](#apidoc.element.stylus.nodes.Namespace)
- description and source-code
```javascript
function Namespace(val, prefix){
  Node.call(this);
  this.val = val;
  this.prefix = prefix;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Node"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Node ()](#apidoc.element.stylus.nodes.Node)
- description and source-code
```javascript
function Node(){
  this.lineno = nodes.lineno || 1;
  this.column = nodes.column || 1;
  this.filename = nodes.filename;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Null"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Null ()](#apidoc.element.stylus.nodes.Null)
- description and source-code
```javascript
function Null(){}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Object"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Object ()](#apidoc.element.stylus.nodes.Object)
- description and source-code
```javascript
function Object(){
  Node.call(this);
  this.vals = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Params"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Params ()](#apidoc.element.stylus.nodes.Params)
- description and source-code
```javascript
function Params(){
  Node.call(this);
  this.nodes = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Property"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Property (segs, expr)](#apidoc.element.stylus.nodes.Property)
- description and source-code
```javascript
function Property(segs, expr){
  Node.call(this);
  this.segments = segs;
  this.expr = expr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Query"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Query ()](#apidoc.element.stylus.nodes.Query)
- description and source-code
```javascript
function Query(){
  Node.call(this);
  this.nodes = [];
  this.type = '';
  this.predicate = '';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.QueryList"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>QueryList ()](#apidoc.element.stylus.nodes.QueryList)
- description and source-code
```javascript
function QueryList(){
  Node.call(this);
  this.nodes = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.RGBA"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>RGBA (r, g, b, a)](#apidoc.element.stylus.nodes.RGBA)
- description and source-code
```javascript
function RGBA(r, g, b, a){
  Node.call(this);
  this.r = clamp(r);
  this.g = clamp(g);
  this.b = clamp(b);
  this.a = clampAlpha(a);
  this.name = '';
  this.rgba = this;
}
```
- example usage
```shell
...
 */

n: function() {
  var captures;
  if (captures = /^#([a-fA-F0-9]{1})[ \t]*/.exec(this.str)) {
    this.skip(captures);
    var n = parseInt(captures[1] + captures[1], 16)
      , color = new nodes.RGBA(n, n, n, 1);
    color.raw = captures[0];
    return new Token('color', color);
  }
},

/**
 * #nn
...
```

#### <a name="apidoc.element.stylus.nodes.Return"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Return (expr)](#apidoc.element.stylus.nodes.Return)
- description and source-code
```javascript
function Return(expr){
  this.expr = expr || nodes.null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Root"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Root ()](#apidoc.element.stylus.nodes.Root)
- description and source-code
```javascript
function Root(){
  this.nodes = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Selector"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Selector (segs)](#apidoc.element.stylus.nodes.Selector)
- description and source-code
```javascript
function Selector(segs){
  Node.call(this);
  this.inherits = true;
  this.segments = segs;
  this.optional = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.String"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>String (val, quote)](#apidoc.element.stylus.nodes.String)
- description and source-code
```javascript
function String(val, quote){
  Node.call(this);
  this.val = val;
  this.string = val;
  this.prefixed = false;
  if (typeof quote !== 'string') {
    this.quote = "'";
  } else {
    this.quote = quote;
  }
}
```
- example usage
```shell
...
string: function() {
  var captures;
  if (captures = /^("[^"]*"|'[^']*')[ \t]*/.exec(this.str)) {
    var str = captures[1]
      , quote = captures[0][0];
    this.skip(captures);
    str = str.slice(1,-1).replace(/\\n/g, '\n');
    return new Token('string', new nodes.String(str, quote));
  }
},

/**
 * #rrggbbaa | #rrggbb | #rgba | #rgb | #nn | #n
 */
...
```

#### <a name="apidoc.element.stylus.nodes.Supports"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Supports (condition)](#apidoc.element.stylus.nodes.Supports)
- description and source-code
```javascript
function Supports(condition){
  Atrule.call(this, 'supports');
  this.condition = condition;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Ternary"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Ternary (cond, trueExpr, falseExpr)](#apidoc.element.stylus.nodes.Ternary)
- description and source-code
```javascript
function Ternary(cond, trueExpr, falseExpr){
  Node.call(this);
  this.cond = cond;
  this.trueExpr = trueExpr;
  this.falseExpr = falseExpr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.UnaryOp"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>UnaryOp (op, expr)](#apidoc.element.stylus.nodes.UnaryOp)
- description and source-code
```javascript
function UnaryOp(op, expr){
  Node.call(this);
  this.op = op;
  this.expr = expr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Unit"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Unit (val, type)](#apidoc.element.stylus.nodes.Unit)
- description and source-code
```javascript
function Unit(val, type){
  Node.call(this);
  this.val = val;
  this.type = type;
}
```
- example usage
```shell
...

unit: function() {
  var captures;
  if (captures = /^(-)?(\d+\.\d+|\d+|\.\d+)(%|[a-zA-Z]+)?[ \t]*/.exec(this.str)) {
    this.skip(captures);
    var n = parseFloat(captures[2]);
    if ('-' == captures[1]) n = -n;
    var node = new nodes.Unit(n, captures[3]);
    node.raw = captures[0];
    return new Token('unit', node);
  }
},

/**
 * '"' [^"]+ '"' | "'"" [^']+ "'"
...
```



# <a name="apidoc.module.stylus.nodes.Arguments"></a>[module stylus.nodes.Arguments](#apidoc.module.stylus.nodes.Arguments)

#### <a name="apidoc.element.stylus.nodes.Arguments.Arguments"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Arguments ()](#apidoc.element.stylus.nodes.Arguments.Arguments)
- description and source-code
```javascript
function Arguments(){
  nodes.Expression.call(this);
  this.map = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Arguments.fromExpression"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Arguments.</span>fromExpression (expr)](#apidoc.element.stylus.nodes.Arguments.fromExpression)
- description and source-code
```javascript
fromExpression = function (expr){
  var args = new Arguments
    , len = expr.nodes.length;
  args.lineno = expr.lineno;
  args.column = expr.column;
  args.isList = expr.isList;
  for (var i = 0; i < len; ++i) {
    args.push(expr.nodes[i]);
  }
  return args;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Arguments.prototype"></a>[module stylus.nodes.Arguments.prototype](#apidoc.module.stylus.nodes.Arguments.prototype)

#### <a name="apidoc.element.stylus.nodes.Arguments.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Arguments.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Arguments.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = nodes.Expression.prototype.clone.call(this, parent);
  clone.map = {};
  for (var key in this.map) {
    clone.map[key] = this.map[key].clone(parent, clone);
  }
  clone.isList = this.isList;
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Arguments.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Arguments.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Arguments.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Arguments',
    map: this.map,
    isList: this.isList,
    preserve: this.preserve,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename,
    nodes: this.nodes
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```



# <a name="apidoc.module.stylus.nodes.Atblock"></a>[module stylus.nodes.Atblock](#apidoc.module.stylus.nodes.Atblock)

#### <a name="apidoc.element.stylus.nodes.Atblock.Atblock"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Atblock ()](#apidoc.element.stylus.nodes.Atblock.Atblock)
- description and source-code
```javascript
function Atblock(){
  Node.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Atblock.prototype"></a>[module stylus.nodes.Atblock.prototype](#apidoc.module.stylus.nodes.Atblock.prototype)

#### <a name="apidoc.element.stylus.nodes.Atblock.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Atblock.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Atblock.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Atblock;
  clone.block = this.block.clone(parent, clone);
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Atblock.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Atblock.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Atblock.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Atblock',
    block: this.block,
    lineno: this.lineno,
    column: this.column,
    fileno: this.fileno
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Atblock.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Atblock.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Atblock.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return '@block';
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Atrule"></a>[module stylus.nodes.Atrule](#apidoc.module.stylus.nodes.Atrule)

#### <a name="apidoc.element.stylus.nodes.Atrule.Atrule"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Atrule (type)](#apidoc.element.stylus.nodes.Atrule.Atrule)
- description and source-code
```javascript
function Atrule(type){
  Node.call(this);
  this.type = type;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Atrule.prototype"></a>[module stylus.nodes.Atrule.prototype](#apidoc.module.stylus.nodes.Atrule.prototype)

#### <a name="apidoc.element.stylus.nodes.Atrule.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Atrule.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Atrule.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Atrule(this.type);
  if (this.block) clone.block = this.block.clone(parent, clone);
  clone.segments = this.segments.map(function(node){ return node.clone(parent, clone); });
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Atrule.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Atrule.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Atrule.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  var json = {
    __type: 'Atrule',
    type: this.type,
    segments: this.segments,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
  if (this.block) json.block = this.block;
  return json;
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Atrule.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Atrule.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Atrule.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return '@' + this.type;
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.BinOp"></a>[module stylus.nodes.BinOp](#apidoc.module.stylus.nodes.BinOp)

#### <a name="apidoc.element.stylus.nodes.BinOp.BinOp"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>BinOp (op, left, right)](#apidoc.element.stylus.nodes.BinOp.BinOp)
- description and source-code
```javascript
function BinOp(op, left, right){
  Node.call(this);
  this.op = op;
  this.left = left;
  this.right = right;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.BinOp.prototype"></a>[module stylus.nodes.BinOp.prototype](#apidoc.module.stylus.nodes.BinOp.prototype)

#### <a name="apidoc.element.stylus.nodes.BinOp.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.BinOp.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.BinOp.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new BinOp(this.op);
  clone.left = this.left.clone(parent, clone);
  clone.right = this.right && this.right.clone(parent, clone);
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  if (this.val) clone.val = this.val.clone(parent, clone);
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.BinOp.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.BinOp.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.BinOp.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  var json = {
    __type: 'BinOp',
    left: this.left,
    right: this.right,
    op: this.op,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
  if (this.val) json.val = this.val;
  return json;
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.BinOp.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.BinOp.prototype.</span>toString ()](#apidoc.element.stylus.nodes.BinOp.prototype.toString)
- description and source-code
```javascript
toString = function () {
  return this.left.toString() + ' ' + this.op + ' ' + this.right.toString();
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Block"></a>[module stylus.nodes.Block](#apidoc.module.stylus.nodes.Block)

#### <a name="apidoc.element.stylus.nodes.Block.Block"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Block (parent, node)](#apidoc.element.stylus.nodes.Block.Block)
- description and source-code
```javascript
function Block(parent, node){
  Node.call(this);
  this.nodes = [];
  this.parent = parent;
  this.node = node;
  this.scope = true;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Block.prototype"></a>[module stylus.nodes.Block.prototype](#apidoc.module.stylus.nodes.Block.prototype)

#### <a name="apidoc.element.stylus.nodes.Block.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Block.prototype.</span>clone (parent, node)](#apidoc.element.stylus.nodes.Block.prototype.clone)
- description and source-code
```javascript
clone = function (parent, node){
  parent = parent || this.parent;
  var clone = new Block(parent, node || this.node);
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  clone.scope = this.scope;
  this.nodes.forEach(function(node){
    clone.push(node.clone(clone, clone));
  });
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Block.prototype.push"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Block.prototype.</span>push (node)](#apidoc.element.stylus.nodes.Block.prototype.push)
- description and source-code
```javascript
push = function (node){
  this.nodes.push(node);
}
```
- example usage
```shell
...
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
 * Lookahead 'n' tokens.
...
```

#### <a name="apidoc.element.stylus.nodes.Block.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Block.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Block.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Block',
    // parent: this.parent,
    // node: this.node,
    scope: this.scope,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename,
    nodes: this.nodes
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```



# <a name="apidoc.module.stylus.nodes.Boolean"></a>[module stylus.nodes.Boolean](#apidoc.module.stylus.nodes.Boolean)

#### <a name="apidoc.element.stylus.nodes.Boolean.Boolean"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Boolean (val)](#apidoc.element.stylus.nodes.Boolean.Boolean)
- description and source-code
```javascript
function Boolean(val){
  Node.call(this);
  if (this.nodeName) {
    this.val = !!val;
  } else {
    return new Boolean(val);
  }
}
```
- example usage
```shell
...
/**
 * 'true' | 'false'
 */

boolean: function() {
  var captures;
  if (captures = /^(true|false)\b([ \t]*)/.exec(this.str)) {
    var val = nodes.Boolean('true' == captures[1]);
    this.skip(captures);
    var tok = new Token('boolean', val);
    tok.space = captures[2];
    return tok;
  }
},
...
```



# <a name="apidoc.module.stylus.nodes.Boolean.prototype"></a>[module stylus.nodes.Boolean.prototype](#apidoc.module.stylus.nodes.Boolean.prototype)

#### <a name="apidoc.element.stylus.nodes.Boolean.prototype.inspect"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Boolean.prototype.</span>inspect ()](#apidoc.element.stylus.nodes.Boolean.prototype.inspect)
- description and source-code
```javascript
inspect = function (){
  return '[Boolean ' + this.val + ']';
}
```
- example usage
```shell
...
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
 * Lookahead 'n' tokens.
...
```

#### <a name="apidoc.element.stylus.nodes.Boolean.prototype.negate"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Boolean.prototype.</span>negate ()](#apidoc.element.stylus.nodes.Boolean.prototype.negate)
- description and source-code
```javascript
negate = function (){
  return new Boolean(!this.val);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Boolean.prototype.toBoolean"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Boolean.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.Boolean.prototype.toBoolean)
- description and source-code
```javascript
toBoolean = function (){
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Boolean.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Boolean.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Boolean.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Boolean',
    val: this.val
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Boolean.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Boolean.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Boolean.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return this.val
    ? 'true'
    : 'false';
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Call"></a>[module stylus.nodes.Call](#apidoc.module.stylus.nodes.Call)

#### <a name="apidoc.element.stylus.nodes.Call.Call"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Call (name, args)](#apidoc.element.stylus.nodes.Call.Call)
- description and source-code
```javascript
function Call(name, args){
  Node.call(this);
  this.name = name;
  this.args = args;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Call.prototype"></a>[module stylus.nodes.Call.prototype](#apidoc.module.stylus.nodes.Call.prototype)

#### <a name="apidoc.element.stylus.nodes.Call.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Call.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Call.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Call(this.name);
  clone.args = this.args.clone(parent, clone);
  if (this.block) clone.block = this.block.clone(parent, clone);
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Call.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Call.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Call.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  var json = {
    __type: 'Call',
    name: this.name,
    args: this.args,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
  if (this.block) json.block = this.block;
  return json;
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Call.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Call.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Call.prototype.toString)
- description and source-code
```javascript
toString = function (){
  var args = this.args.nodes.map(function(node) {
    var str = node.toString();
    return str.slice(1, str.length - 1);
  }).join(', ');

  return this.name + '(' + args + ')';
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Charset"></a>[module stylus.nodes.Charset](#apidoc.module.stylus.nodes.Charset)

#### <a name="apidoc.element.stylus.nodes.Charset.Charset"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Charset (val)](#apidoc.element.stylus.nodes.Charset.Charset)
- description and source-code
```javascript
function Charset(val){
  Node.call(this);
  this.val = val;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Charset.prototype"></a>[module stylus.nodes.Charset.prototype](#apidoc.module.stylus.nodes.Charset.prototype)

#### <a name="apidoc.element.stylus.nodes.Charset.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Charset.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Charset.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Charset',
    val: this.val,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Charset.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Charset.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Charset.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return '@charset ' + this.val;
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Comment"></a>[module stylus.nodes.Comment](#apidoc.module.stylus.nodes.Comment)

#### <a name="apidoc.element.stylus.nodes.Comment.Comment"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Comment (str, suppress, inline)](#apidoc.element.stylus.nodes.Comment.Comment)
- description and source-code
```javascript
function Comment(str, suppress, inline){
  Node.call(this);
  this.str = str;
  this.suppress = suppress;
  this.inline = inline;
}
```
- example usage
```shell
...
    this.skip(end + 2);
    // output
    if ('!' == str[2]) {
      str = str.replace('*!', '*');
      suppress = false;
    }
    if (this.prev && ';' == this.prev.type) inline = true;
    return new Token('comment', new nodes.Comment(str, suppress, inline));
  }
},

/**
 * 'true' | 'false'
 */
...
```



# <a name="apidoc.module.stylus.nodes.Comment.prototype"></a>[module stylus.nodes.Comment.prototype](#apidoc.module.stylus.nodes.Comment.prototype)

#### <a name="apidoc.element.stylus.nodes.Comment.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Comment.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Comment.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Comment',
    str: this.str,
    suppress: this.suppress,
    inline: this.inline,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Comment.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Comment.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Comment.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return this.str;
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Each"></a>[module stylus.nodes.Each](#apidoc.module.stylus.nodes.Each)

#### <a name="apidoc.element.stylus.nodes.Each.Each"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Each (val, key, expr, block)](#apidoc.element.stylus.nodes.Each.Each)
- description and source-code
```javascript
function Each(val, key, expr, block){
  Node.call(this);
  this.val = val;
  this.key = key;
  this.expr = expr;
  this.block = block;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Each.prototype"></a>[module stylus.nodes.Each.prototype](#apidoc.module.stylus.nodes.Each.prototype)

#### <a name="apidoc.element.stylus.nodes.Each.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Each.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Each.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Each(this.val, this.key);
  clone.expr = this.expr.clone(parent, clone);
  clone.block = this.block.clone(parent, clone);
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Each.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Each.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Each.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Each',
    val: this.val,
    key: this.key,
    expr: this.expr,
    block: this.block,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```



# <a name="apidoc.module.stylus.nodes.Expression"></a>[module stylus.nodes.Expression](#apidoc.module.stylus.nodes.Expression)

#### <a name="apidoc.element.stylus.nodes.Expression.Expression"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Expression (isList)](#apidoc.element.stylus.nodes.Expression.Expression)
- description and source-code
```javascript
function Expression(isList){
  Node.call(this);
  this.nodes = [];
  this.isList = isList;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Expression.prototype"></a>[module stylus.nodes.Expression.prototype](#apidoc.module.stylus.nodes.Expression.prototype)

#### <a name="apidoc.element.stylus.nodes.Expression.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Expression.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Expression.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new this.constructor(this.isList);
  clone.preserve = this.preserve;
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  clone.nodes = this.nodes.map(function(node) {
    return node.clone(parent, clone);
  });
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Expression.prototype.operate"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Expression.prototype.</span>operate (op, right, val)](#apidoc.element.stylus.nodes.Expression.prototype.operate)
- description and source-code
```javascript
operate = function (op, right, val){
  switch (op) {
    case '[]=':
      var self = this
        , range = utils.unwrap(right).nodes
        , val = utils.unwrap(val)
        , len
        , node;
      range.forEach(function(unit){
        len = self.nodes.length;
        if ('unit' == unit.nodeName) {
          var i = unit.val < 0 ? len + unit.val : unit.val
            , n = i;
          while (i-- > len) self.nodes[i] = nodes.null;
          self.nodes[n] = val;
        } else if (unit.string) {
          node = self.nodes[0];
          if (node && 'object' == node.nodeName) node.set(unit.string, val.clone());
        }
      });
      return val;
    case '[]':
      var expr = new nodes.Expression
        , vals = utils.unwrap(this).nodes
        , range = utils.unwrap(right).nodes
        , node;
      range.forEach(function(unit){
        if ('unit' == unit.nodeName) {
          node = vals[unit.val < 0 ? vals.length + unit.val : unit.val];
        } else if ('object' == vals[0].nodeName) {
          node = vals[0].get(unit.string);
        }
        if (node) expr.push(node);
      });
      return expr.isEmpty
        ? nodes.null
        : utils.unwrap(expr);
    case '||':
      return this.toBoolean().isTrue
        ? this
        : right;
    case 'in':
      return Node.prototype.operate.call(this, op, right);
    case '!=':
      return this.operate('==', right, val).negate();
    case '==':
      var len = this.nodes.length
        , right = right.toExpression()
        , a
        , b;
      if (len != right.nodes.length) return nodes.false;
      for (var i = 0; i < len; ++i) {
        a = this.nodes[i];
        b = right.nodes[i];
        if (a.operate(op, b).isTrue) continue;
        return nodes.false;
      }
      return nodes.true;
      break;
    default:
      return this.first.operate(op, right, val);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Expression.prototype.push"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Expression.prototype.</span>push (node)](#apidoc.element.stylus.nodes.Expression.prototype.push)
- description and source-code
```javascript
push = function (node){
  this.nodes.push(node);
}
```
- example usage
```shell
...
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
 * Lookahead 'n' tokens.
...
```

#### <a name="apidoc.element.stylus.nodes.Expression.prototype.toBoolean"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Expression.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.Expression.prototype.toBoolean)
- description and source-code
```javascript
toBoolean = function (){
  if (this.nodes.length > 1) return nodes.true;
  return this.first.toBoolean();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Expression.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Expression.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Expression.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Expression',
    isList: this.isList,
    preserve: this.preserve,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename,
    nodes: this.nodes
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Expression.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Expression.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Expression.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return '(' + this.nodes.map(function(node){
    return node.toString();
  }).join(this.isList ? ', ' : ' ') + ')';
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Extend"></a>[module stylus.nodes.Extend](#apidoc.module.stylus.nodes.Extend)

#### <a name="apidoc.element.stylus.nodes.Extend.Extend"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Extend (selectors)](#apidoc.element.stylus.nodes.Extend.Extend)
- description and source-code
```javascript
function Extend(selectors){
  Node.call(this);
  this.selectors = selectors;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Extend.prototype"></a>[module stylus.nodes.Extend.prototype](#apidoc.module.stylus.nodes.Extend.prototype)

#### <a name="apidoc.element.stylus.nodes.Extend.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Extend.prototype.</span>clone ()](#apidoc.element.stylus.nodes.Extend.prototype.clone)
- description and source-code
```javascript
clone = function (){
  return new Extend(this.selectors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Extend.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Extend.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Extend.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Extend',
    selectors: this.selectors,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Extend.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Extend.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Extend.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return '@extend ' + this.selectors.join(', ');
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Feature"></a>[module stylus.nodes.Feature](#apidoc.module.stylus.nodes.Feature)

#### <a name="apidoc.element.stylus.nodes.Feature.Feature"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Feature (segs)](#apidoc.element.stylus.nodes.Feature.Feature)
- description and source-code
```javascript
function Feature(segs){
  Node.call(this);
  this.segments = segs;
  this.expr = null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Feature.prototype"></a>[module stylus.nodes.Feature.prototype](#apidoc.module.stylus.nodes.Feature.prototype)

#### <a name="apidoc.element.stylus.nodes.Feature.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Feature.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Feature.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Feature;
  clone.segments = this.segments.map(function(node){ return node.clone(parent, clone); });
  if (this.expr) clone.expr = this.expr.clone(parent, clone);
  if (this.name) clone.name = this.name;
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Feature.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Feature.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Feature.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  var json = {
    __type: 'Feature',
    segments: this.segments,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
  if (this.expr) json.expr = this.expr;
  if (this.name) json.name = this.name;
  return json;
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Feature.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Feature.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Feature.prototype.toString)
- description and source-code
```javascript
toString = function (){
  if (this.expr) {
    return '(' + this.segments.join('') + ': ' + this.expr.toString() + ')';
  } else {
    return this.segments.join('');
  }
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Function"></a>[module stylus.nodes.Function](#apidoc.module.stylus.nodes.Function)

#### <a name="apidoc.element.stylus.nodes.Function.Function"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Function (name, params, body)](#apidoc.element.stylus.nodes.Function.Function)
- description and source-code
```javascript
function Function(name, params, body){
  Node.call(this);
  this.name = name;
  this.params = params;
  this.block = body;
  if ('function' == typeof params) this.fn = params;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Function.prototype"></a>[module stylus.nodes.Function.prototype](#apidoc.module.stylus.nodes.Function.prototype)

#### <a name="apidoc.element.stylus.nodes.Function.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Function.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Function.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  if (this.fn) {
    var clone = new Function(
        this.name
      , this.fn);
  } else {
    var clone = new Function(this.name);
    clone.params = this.params.clone(parent, clone);
    clone.block = this.block.clone(parent, clone);
  }
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Function.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Function.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Function.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  var json = {
    __type: 'Function',
    name: this.name,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
  if (this.fn) {
    json.fn = this.fn;
  } else {
    json.params = this.params;
    json.block = this.block;
  }
  return json;
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Function.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Function.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Function.prototype.toString)
- description and source-code
```javascript
toString = function (){
  if (this.fn) {
    return this.name
      + '('
      + this.fn.toString()
        .match(/^function *\w*\((.*?)\)/)
        .slice(1)
        .join(', ')
      + ')';
  } else {
    return this.name
      + '('
      + this.params.nodes.join(', ')
      + ')';
  }
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Group"></a>[module stylus.nodes.Group](#apidoc.module.stylus.nodes.Group)

#### <a name="apidoc.element.stylus.nodes.Group.Group"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Group ()](#apidoc.element.stylus.nodes.Group.Group)
- description and source-code
```javascript
function Group(){
  Node.call(this);
  this.nodes = [];
  this.extends = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Group.prototype"></a>[module stylus.nodes.Group.prototype](#apidoc.module.stylus.nodes.Group.prototype)

#### <a name="apidoc.element.stylus.nodes.Group.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Group.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Group.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Group;
  clone.lineno = this.lineno;
  clone.column = this.column;
  this.nodes.forEach(function(node){
    clone.push(node.clone(parent, clone));
  });
  clone.filename = this.filename;
  clone.block = this.block.clone(parent, clone);
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Group.prototype.push"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Group.prototype.</span>push (selector)](#apidoc.element.stylus.nodes.Group.prototype.push)
- description and source-code
```javascript
push = function (selector){
  this.nodes.push(selector);
}
```
- example usage
```shell
...
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
 * Lookahead 'n' tokens.
...
```

#### <a name="apidoc.element.stylus.nodes.Group.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Group.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Group.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Group',
    nodes: this.nodes,
    block: this.block,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```



# <a name="apidoc.module.stylus.nodes.HSLA"></a>[module stylus.nodes.HSLA](#apidoc.module.stylus.nodes.HSLA)

#### <a name="apidoc.element.stylus.nodes.HSLA.HSLA"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>HSLA (h, s, l, a)](#apidoc.element.stylus.nodes.HSLA.HSLA)
- description and source-code
```javascript
function HSLA(h, s, l, a){
  Node.call(this);
  this.h = clampDegrees(h);
  this.s = clampPercentage(s);
  this.l = clampPercentage(l);
  this.a = clampAlpha(a);
  this.hsla = this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.HSLA.fromRGBA"></a>[function <span class="apidocSignatureSpan">stylus.nodes.HSLA.</span>fromRGBA (rgba)](#apidoc.element.stylus.nodes.HSLA.fromRGBA)
- description and source-code
```javascript
fromRGBA = function (rgba){
  var r = rgba.r / 255
    , g = rgba.g / 255
    , b = rgba.b / 255
    , a = rgba.a;

  var min = Math.min(r,g,b)
    , max = Math.max(r,g,b)
    , l = (max + min) / 2
    , d = max - min
    , h, s;

  switch (max) {
    case min: h = 0; break;
    case r: h = 60 * (g-b) / d; break;
    case g: h = 60 * (b-r) / d + 120; break;
    case b: h = 60 * (r-g) / d + 240; break;
  }

  if (max == min) {
    s = 0;
  } else if (l < .5) {
    s = d / (2 * l);
  } else {
    s = d / (2 - 2 * l);
  }

  h %= 360;
  s *= 100;
  l *= 100;

  return new HSLA(h,s,l,a);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.HSLA.prototype"></a>[module stylus.nodes.HSLA.prototype](#apidoc.module.stylus.nodes.HSLA.prototype)

#### <a name="apidoc.element.stylus.nodes.HSLA.prototype.add"></a>[function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>add (h, s, l)](#apidoc.element.stylus.nodes.HSLA.prototype.add)
- description and source-code
```javascript
add = function (h, s, l){
  return new HSLA(
      this.h + h
    , this.s + s
    , this.l + l
    , this.a);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.HSLA.prototype.adjustHue"></a>[function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>adjustHue (deg)](#apidoc.element.stylus.nodes.HSLA.prototype.adjustHue)
- description and source-code
```javascript
adjustHue = function (deg){
  this.h = clampDegrees(this.h + deg);
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.HSLA.prototype.adjustLightness"></a>[function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>adjustLightness (percent)](#apidoc.element.stylus.nodes.HSLA.prototype.adjustLightness)
- description and source-code
```javascript
adjustLightness = function (percent){
  this.l = clampPercentage(this.l + this.l * (percent / 100));
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.HSLA.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.HSLA.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new HSLA(
      this.h
    , this.s
    , this.l
    , this.a);
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.HSLA.prototype.operate"></a>[function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.HSLA.prototype.operate)
- description and source-code
```javascript
operate = function (op, right){
  switch (op) {
    case '==':
    case '!=':
    case '<=':
    case '>=':
    case '<':
    case '>':
    case 'is a':
    case '||':
    case '&&':
      return this.rgba.operate(op, right);
    default:
      return this.rgba.operate(op, right).hsla;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.HSLA.prototype.sub"></a>[function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>sub (h, s, l)](#apidoc.element.stylus.nodes.HSLA.prototype.sub)
- description and source-code
```javascript
sub = function (h, s, l){
  return this.add(-h, -s, -l);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.HSLA.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.HSLA.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'HSLA',
    h: this.h,
    s: this.s,
    l: this.l,
    a: this.a,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.HSLA.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.HSLA.prototype.</span>toString ()](#apidoc.element.stylus.nodes.HSLA.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return 'hsla('
    + this.h + ','
    + this.s.toFixed(0) + '%,'
    + this.l.toFixed(0) + '%,'
    + this.a + ')';
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Ident"></a>[module stylus.nodes.Ident](#apidoc.module.stylus.nodes.Ident)

#### <a name="apidoc.element.stylus.nodes.Ident.Ident"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Ident (name, val, mixin)](#apidoc.element.stylus.nodes.Ident.Ident)
- description and source-code
```javascript
function Ident(name, val, mixin){
  Node.call(this);
  this.name = name;
  this.string = name;
  this.val = val || nodes.null;
  this.mixin = !!mixin;
}
```
- example usage
```shell
...

null: function() {
  var captures
    , tok;
  if (captures = /^(null)\b[ \t]*/.exec(this.str)) {
    this.skip(captures);
    if (this.isPartOfSelector()) {
      tok = new Token('ident', new nodes.Ident(captures[0]));
    } else {
      tok = new Token('null', nodes.null);
    }
    return tok;
  }
},
...
```



# <a name="apidoc.module.stylus.nodes.Ident.prototype"></a>[module stylus.nodes.Ident.prototype](#apidoc.module.stylus.nodes.Ident.prototype)

#### <a name="apidoc.element.stylus.nodes.Ident.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Ident.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Ident.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Ident(this.name);
  clone.val = this.val.clone(parent, clone);
  clone.mixin = this.mixin;
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  clone.property = this.property;
  clone.rest = this.rest;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Ident.prototype.coerce"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Ident.prototype.</span>coerce (other)](#apidoc.element.stylus.nodes.Ident.prototype.coerce)
- description and source-code
```javascript
coerce = function (other){
  switch (other.nodeName) {
    case 'ident':
    case 'string':
    case 'literal':
      return new Ident(other.string);
    case 'unit':
      return new Ident(other.toString());
    default:
      return Node.prototype.coerce.call(this, other);
  }
}
```
- example usage
```shell
...
 * @param {String} name
 * @param {Function|Node} fn
 * @return {Renderer} for chaining
 * @api public
 */

Renderer.prototype.define = function(name, fn, raw){
fn = utils.coerce(fn, raw);

if (fn.nodeName) {
  this.options.globals[name] = fn;
  return this;
}

// function
...
```

#### <a name="apidoc.element.stylus.nodes.Ident.prototype.operate"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Ident.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.Ident.prototype.operate)
- description and source-code
```javascript
operate = function (op, right){
  var val = right.first;
  switch (op) {
    case '-':
      if ('unit' == val.nodeName) {
        var expr = new nodes.Expression;
        val = val.clone();
        val.val = -val.val;
        expr.push(this);
        expr.push(val);
        return expr;
      }
    case '+':
      return new nodes.Ident(this.string + this.coerce(val).string);
  }
  return Node.prototype.operate.call(this, op, right);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Ident.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Ident.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Ident.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Ident',
    name: this.name,
    val: this.val,
    mixin: this.mixin,
    property: this.property,
    rest: this.rest,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Ident.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Ident.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Ident.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return this.name;
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.If"></a>[module stylus.nodes.If](#apidoc.module.stylus.nodes.If)

#### <a name="apidoc.element.stylus.nodes.If.If"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>If (cond, negate)](#apidoc.element.stylus.nodes.If.If)
- description and source-code
```javascript
function If(cond, negate){
  Node.call(this);
  this.cond = cond;
  this.elses = [];
  if (negate && negate.nodeName) {
    this.block = negate;
  } else {
    this.negate = negate;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.If.prototype"></a>[module stylus.nodes.If.prototype](#apidoc.module.stylus.nodes.If.prototype)

#### <a name="apidoc.element.stylus.nodes.If.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.If.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.If.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new If();
  clone.cond = this.cond.clone(parent, clone);
  clone.block = this.block.clone(parent, clone);
  clone.elses = this.elses.map(function(node){ return node.clone(parent, clone); });
  clone.negate = this.negate;
  clone.postfix = this.postfix;
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.If.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.If.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.If.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'If',
    cond: this.cond,
    block: this.block,
    elses: this.elses,
    negate: this.negate,
    postfix: this.postfix,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```



# <a name="apidoc.module.stylus.nodes.Import"></a>[module stylus.nodes.Import](#apidoc.module.stylus.nodes.Import)

#### <a name="apidoc.element.stylus.nodes.Import.Import"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Import (expr, once)](#apidoc.element.stylus.nodes.Import.Import)
- description and source-code
```javascript
function Import(expr, once){
  Node.call(this);
  this.path = expr;
  this.once = once || false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Import.prototype"></a>[module stylus.nodes.Import.prototype](#apidoc.module.stylus.nodes.Import.prototype)

#### <a name="apidoc.element.stylus.nodes.Import.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Import.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Import.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Import();
  clone.path = this.path.nodeName ? this.path.clone(parent, clone) : this.path;
  clone.once = this.once;
  clone.mtime = this.mtime;
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Import.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Import.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Import.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Import',
    path: this.path,
    once: this.once,
    mtime: this.mtime,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```



# <a name="apidoc.module.stylus.nodes.Keyframes"></a>[module stylus.nodes.Keyframes](#apidoc.module.stylus.nodes.Keyframes)

#### <a name="apidoc.element.stylus.nodes.Keyframes.Keyframes"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Keyframes (segs, prefix)](#apidoc.element.stylus.nodes.Keyframes.Keyframes)
- description and source-code
```javascript
function Keyframes(segs, prefix){
  Atrule.call(this, 'keyframes');
  this.segments = segs;
  this.prefix = prefix || 'official';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Keyframes.prototype"></a>[module stylus.nodes.Keyframes.prototype](#apidoc.module.stylus.nodes.Keyframes.prototype)

#### <a name="apidoc.element.stylus.nodes.Keyframes.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Keyframes.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Keyframes.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Keyframes;
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  clone.segments = this.segments.map(function(node) { return node.clone(parent, clone); });
  clone.prefix = this.prefix;
  clone.block = this.block.clone(parent, clone);
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Keyframes.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Keyframes.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Keyframes.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Keyframes',
    segments: this.segments,
    prefix: this.prefix,
    block: this.block,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Keyframes.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Keyframes.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Keyframes.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return '@keyframes ' + this.segments.join('');
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Literal"></a>[module stylus.nodes.Literal](#apidoc.module.stylus.nodes.Literal)

#### <a name="apidoc.element.stylus.nodes.Literal.Literal"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Literal (str)](#apidoc.element.stylus.nodes.Literal.Literal)
- description and source-code
```javascript
function Literal(str){
  Node.call(this);
  this.val = str;
  this.string = str;
  this.prefixed = false;
}
```
- example usage
```shell
...
 */

urlchars: function() {
  var captures;
  if (!this.isURL) return;
  if (captures = /^[\/:@.;?&=*!,<>#%0-9]+/.exec(this.str)) {
    this.skip(captures);
    return new Token('literal', new nodes.Literal(captures[0]));
  }
},

/**
 * ';' [ \t]*
 */
...
```



# <a name="apidoc.module.stylus.nodes.Literal.prototype"></a>[module stylus.nodes.Literal.prototype](#apidoc.module.stylus.nodes.Literal.prototype)

#### <a name="apidoc.element.stylus.nodes.Literal.prototype.coerce"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Literal.prototype.</span>coerce (other)](#apidoc.element.stylus.nodes.Literal.prototype.coerce)
- description and source-code
```javascript
coerce = function (other){
  switch (other.nodeName) {
    case 'ident':
    case 'string':
    case 'literal':
      return new Literal(other.string);
    default:
      return Node.prototype.coerce.call(this, other);
  }
}
```
- example usage
```shell
...
 * @param {String} name
 * @param {Function|Node} fn
 * @return {Renderer} for chaining
 * @api public
 */

Renderer.prototype.define = function(name, fn, raw){
fn = utils.coerce(fn, raw);

if (fn.nodeName) {
  this.options.globals[name] = fn;
  return this;
}

// function
...
```

#### <a name="apidoc.element.stylus.nodes.Literal.prototype.operate"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Literal.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.Literal.prototype.operate)
- description and source-code
```javascript
operate = function (op, right){
  var val = right.first;
  switch (op) {
    case '+':
      return new nodes.Literal(this.string + this.coerce(val).string);
    default:
      return Node.prototype.operate.call(this, op, right);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Literal.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Literal.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Literal.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Literal',
    val: this.val,
    string: this.string,
    prefixed: this.prefixed,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Literal.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Literal.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Literal.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return this.val;
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Media"></a>[module stylus.nodes.Media](#apidoc.module.stylus.nodes.Media)

#### <a name="apidoc.element.stylus.nodes.Media.Media"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Media (val)](#apidoc.element.stylus.nodes.Media.Media)
- description and source-code
```javascript
function Media(val){
  Atrule.call(this, 'media');
  this.val = val;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Media.prototype"></a>[module stylus.nodes.Media.prototype](#apidoc.module.stylus.nodes.Media.prototype)

#### <a name="apidoc.element.stylus.nodes.Media.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Media.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Media.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Media;
  clone.val = this.val.clone(parent, clone);
  clone.block = this.block.clone(parent, clone);
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Media.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Media.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Media.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Media',
    val: this.val,
    block: this.block,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Media.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Media.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Media.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return '@media ' + this.val;
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Member"></a>[module stylus.nodes.Member](#apidoc.module.stylus.nodes.Member)

#### <a name="apidoc.element.stylus.nodes.Member.Member"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Member (left, right)](#apidoc.element.stylus.nodes.Member.Member)
- description and source-code
```javascript
function Member(left, right){
  Node.call(this);
  this.left = left;
  this.right = right;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Member.prototype"></a>[module stylus.nodes.Member.prototype](#apidoc.module.stylus.nodes.Member.prototype)

#### <a name="apidoc.element.stylus.nodes.Member.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Member.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Member.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Member;
  clone.left = this.left.clone(parent, clone);
  clone.right = this.right.clone(parent, clone);
  if (this.val) clone.val = this.val.clone(parent, clone);
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Member.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Member.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Member.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  var json = {
    __type: 'Member',
    left: this.left,
    right: this.right,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
  if (this.val) json.val = this.val;
  return json;
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Member.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Member.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Member.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return this.left.toString()
    + '.' + this.right.toString();
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Namespace"></a>[module stylus.nodes.Namespace](#apidoc.module.stylus.nodes.Namespace)

#### <a name="apidoc.element.stylus.nodes.Namespace.Namespace"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Namespace (val, prefix)](#apidoc.element.stylus.nodes.Namespace.Namespace)
- description and source-code
```javascript
function Namespace(val, prefix){
  Node.call(this);
  this.val = val;
  this.prefix = prefix;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Namespace.prototype"></a>[module stylus.nodes.Namespace.prototype](#apidoc.module.stylus.nodes.Namespace.prototype)

#### <a name="apidoc.element.stylus.nodes.Namespace.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Namespace.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Namespace.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Namespace',
    val: this.val,
    prefix: this.prefix,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Namespace.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Namespace.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Namespace.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return '@namespace ' + (this.prefix ? this.prefix + ' ' : '') + this.val;
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Node"></a>[module stylus.nodes.Node](#apidoc.module.stylus.nodes.Node)

#### <a name="apidoc.element.stylus.nodes.Node.Node"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Node ()](#apidoc.element.stylus.nodes.Node.Node)
- description and source-code
```javascript
function Node(){
  this.lineno = nodes.lineno || 1;
  this.column = nodes.column || 1;
  this.filename = nodes.filename;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Node.prototype"></a>[module stylus.nodes.Node.prototype](#apidoc.module.stylus.nodes.Node.prototype)

#### <a name="apidoc.element.stylus.nodes.Node.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>clone ()](#apidoc.element.stylus.nodes.Node.prototype.clone)
- description and source-code
```javascript
clone = function (){
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Node.prototype.coerce"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>coerce (other)](#apidoc.element.stylus.nodes.Node.prototype.coerce)
- description and source-code
```javascript
coerce = function (other){
  if (other.nodeName == this.nodeName) return other;
  throw new CoercionError('cannot coerce ' + other + ' to ' + this.nodeName);
}
```
- example usage
```shell
...
 * @param {String} name
 * @param {Function|Node} fn
 * @return {Renderer} for chaining
 * @api public
 */

Renderer.prototype.define = function(name, fn, raw){
fn = utils.coerce(fn, raw);

if (fn.nodeName) {
  this.options.globals[name] = fn;
  return this;
}

// function
...
```

#### <a name="apidoc.element.stylus.nodes.Node.prototype.constructor"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>constructor ()](#apidoc.element.stylus.nodes.Node.prototype.constructor)
- description and source-code
```javascript
function Node(){
  this.lineno = nodes.lineno || 1;
  this.column = nodes.column || 1;
  this.filename = nodes.filename;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Node.prototype.eval"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>eval ()](#apidoc.element.stylus.nodes.Node.prototype.eval)
- description and source-code
```javascript
eval = function (){
  return new Evaluator(this).evaluate();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Node.prototype.operate"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.Node.prototype.operate)
- description and source-code
```javascript
operate = function (op, right){
  switch (op) {
    case 'is a':
      if ('string' == right.first.nodeName) {
        return nodes.Boolean(this.nodeName == right.val);
      } else {
        throw new Error('"is a" expects a string, got ' + right.toString());
      }
    case '==':
      return nodes.Boolean(this.hash == right.hash);
    case '!=':
      return nodes.Boolean(this.hash != right.hash);
    case '>=':
      return nodes.Boolean(this.hash >= right.hash);
    case '<=':
      return nodes.Boolean(this.hash <= right.hash);
    case '>':
      return nodes.Boolean(this.hash > right.hash);
    case '<':
      return nodes.Boolean(this.hash < right.hash);
    case '||':
      return this.toBoolean().isTrue
        ? this
        : right;
    case 'in':
      var vals = utils.unwrap(right).nodes
        , len = vals && vals.length
        , hash = this.hash;
      if (!vals) throw new Error('"in" given invalid right-hand operand, expecting an expression');

      // 'prop' in obj
      if (1 == len && 'object' == vals[0].nodeName) {
        return nodes.Boolean(vals[0].has(this.hash));
      }

      for (var i = 0; i < len; ++i) {
        if (hash == vals[i].hash) {
          return nodes.true;
        }
      }
      return nodes.false;
    case '&&':
      var a = this.toBoolean()
        , b = right.toBoolean();
      return a.isTrue && b.isTrue
        ? right
        : a.isFalse
          ? this
          : right;
    default:
      if ('[]' == op) {
        var msg = 'cannot perform '
          + this
          + '[' + right + ']';
      } else {
        var msg = 'cannot perform'
          + ' ' + this
          + ' ' + op
          + ' ' + right;
      }
      throw new Error(msg);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Node.prototype.shouldCoerce"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>shouldCoerce (op)](#apidoc.element.stylus.nodes.Node.prototype.shouldCoerce)
- description and source-code
```javascript
shouldCoerce = function (op){
  switch (op) {
    case 'is a':
    case 'in':
    case '||':
    case '&&':
      return false;
    default:
      return true;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Node.prototype.toBoolean"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.Node.prototype.toBoolean)
- description and source-code
```javascript
toBoolean = function (){
  return nodes.true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Node.prototype.toExpression"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>toExpression ()](#apidoc.element.stylus.nodes.Node.prototype.toExpression)
- description and source-code
```javascript
toExpression = function (){
  if ('expression' == this.nodeName) return this;
  var expr = new nodes.Expression;
  expr.push(this);
  return expr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Node.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Node.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Node.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```



# <a name="apidoc.module.stylus.nodes.Null"></a>[module stylus.nodes.Null](#apidoc.module.stylus.nodes.Null)

#### <a name="apidoc.element.stylus.nodes.Null.Null"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Null ()](#apidoc.element.stylus.nodes.Null.Null)
- description and source-code
```javascript
function Null(){}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Null.prototype"></a>[module stylus.nodes.Null.prototype](#apidoc.module.stylus.nodes.Null.prototype)

#### <a name="apidoc.element.stylus.nodes.Null.prototype.inspect"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Null.prototype.</span>inspect ()](#apidoc.element.stylus.nodes.Null.prototype.inspect)
- description and source-code
```javascript
inspect = function (){
  return 'null';
}
```
- example usage
```shell
...
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
 * Lookahead 'n' tokens.
...
```

#### <a name="apidoc.element.stylus.nodes.Null.prototype.toBoolean"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Null.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.Null.prototype.toBoolean)
- description and source-code
```javascript
toBoolean = function (){
  return nodes.false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Null.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Null.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Null.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Null',
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Null.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Null.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Null.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return 'null';
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Object"></a>[module stylus.nodes.Object](#apidoc.module.stylus.nodes.Object)

#### <a name="apidoc.element.stylus.nodes.Object.Object"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Object ()](#apidoc.element.stylus.nodes.Object.Object)
- description and source-code
```javascript
function Object(){
  Node.call(this);
  this.vals = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Object.prototype"></a>[module stylus.nodes.Object.prototype](#apidoc.module.stylus.nodes.Object.prototype)

#### <a name="apidoc.element.stylus.nodes.Object.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Object.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Object;
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  for (var key in this.vals) {
    clone.vals[key] = this.vals[key].clone(parent, clone);
  }
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Object.prototype.get"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>get (key)](#apidoc.element.stylus.nodes.Object.prototype.get)
- description and source-code
```javascript
get = function (key){
  return this.vals[key] || nodes.null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Object.prototype.has"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>has (key)](#apidoc.element.stylus.nodes.Object.prototype.has)
- description and source-code
```javascript
has = function (key){
  return key in this.vals;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Object.prototype.operate"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.Object.prototype.operate)
- description and source-code
```javascript
operate = function (op, right){
  switch (op) {
    case '.':
    case '[]':
      return this.get(right.hash);
    case '==':
      var vals = this.vals
        , a
        , b;
      if ('object' != right.nodeName || this.length != right.length)
        return nodes.false;
      for (var key in vals) {
        a = vals[key];
        b = right.vals[key];
        if (a.operate(op, b).isFalse)
          return nodes.false;
      }
      return nodes.true;
    case '!=':
      return this.operate('==', right).negate();
    default:
      return Node.prototype.operate.call(this, op, right);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Object.prototype.set"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>set (key, val)](#apidoc.element.stylus.nodes.Object.prototype.set)
- description and source-code
```javascript
set = function (key, val){
  this.vals[key] = val;
  return this;
}
```
- example usage
```shell
...
* set the 'compress' option, or define additional functions.
*
* By default the compile function simply sets the 'filename'
* and renders the CSS.
*
*      function compile(str, path) {
*        return stylus(str)
*          .set('filename', path)
*          .set('compress', true);
*      }
*
* Pass the middleware to Connect, grabbing .styl files from this directory
* and saving .css files to _./public_. Also supplying our custom 'compile' function.
*
* Following that we have a 'static()' layer setup to serve the .css
...
```

#### <a name="apidoc.element.stylus.nodes.Object.prototype.toBlock"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>toBlock ()](#apidoc.element.stylus.nodes.Object.prototype.toBlock)
- description and source-code
```javascript
toBlock = function (){
  var str = '{'
    , key
    , val;
  for (key in this.vals) {
    val = this.get(key);
    if ('object' == val.first.nodeName) {
      str += key + ' ' + val.first.toBlock();
    } else {
      switch (key) {
        case '@charset':
          str += key + ' ' + val.first.toString() + ';';
          break;
        default:
          str += key + ':' + toString(val) + ';';
      }
    }
  }
  str += '}';
  return str;

  function toString(node) {
    if (node.nodes) {
      return node.nodes.map(toString).join(node.isList ? ',' : ' ');
    } else if ('literal' == node.nodeName && ',' == node.val) {
      return '\\,';
    }
    return node.toString();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Object.prototype.toBoolean"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.Object.prototype.toBoolean)
- description and source-code
```javascript
toBoolean = function (){
  return nodes.Boolean(this.length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Object.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Object.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Object',
    vals: this.vals,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Object.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Object.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Object.prototype.toString)
- description and source-code
```javascript
toString = function (){
  var obj = {};
  for (var prop in this.vals) {
    obj[prop] = this.vals[prop].toString();
  }
  return JSON.stringify(obj);
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Params"></a>[module stylus.nodes.Params](#apidoc.module.stylus.nodes.Params)

#### <a name="apidoc.element.stylus.nodes.Params.Params"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Params ()](#apidoc.element.stylus.nodes.Params.Params)
- description and source-code
```javascript
function Params(){
  Node.call(this);
  this.nodes = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Params.prototype"></a>[module stylus.nodes.Params.prototype](#apidoc.module.stylus.nodes.Params.prototype)

#### <a name="apidoc.element.stylus.nodes.Params.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Params.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Params.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Params;
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  this.nodes.forEach(function(node){
    clone.push(node.clone(parent, clone));
  });
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Params.prototype.push"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Params.prototype.</span>push (node)](#apidoc.element.stylus.nodes.Params.prototype.push)
- description and source-code
```javascript
push = function (node){
  this.nodes.push(node);
}
```
- example usage
```shell
...
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
 * Lookahead 'n' tokens.
...
```

#### <a name="apidoc.element.stylus.nodes.Params.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Params.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Params.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Params',
    nodes: this.nodes,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```



# <a name="apidoc.module.stylus.nodes.Property"></a>[module stylus.nodes.Property](#apidoc.module.stylus.nodes.Property)

#### <a name="apidoc.element.stylus.nodes.Property.Property"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Property (segs, expr)](#apidoc.element.stylus.nodes.Property.Property)
- description and source-code
```javascript
function Property(segs, expr){
  Node.call(this);
  this.segments = segs;
  this.expr = expr;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Property.prototype"></a>[module stylus.nodes.Property.prototype](#apidoc.module.stylus.nodes.Property.prototype)

#### <a name="apidoc.element.stylus.nodes.Property.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Property.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Property.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Property(this.segments);
  clone.name = this.name;
  if (this.literal) clone.literal = this.literal;
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  clone.segments = this.segments.map(function(node){ return node.clone(parent, clone); });
  if (this.expr) clone.expr = this.expr.clone(parent, clone);
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Property.prototype.operate"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Property.prototype.</span>operate (op, right, val)](#apidoc.element.stylus.nodes.Property.prototype.operate)
- description and source-code
```javascript
operate = function (op, right, val){
  return this.expr.operate(op, right, val);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Property.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Property.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Property.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  var json = {
    __type: 'Property',
    segments: this.segments,
    name: this.name,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
  if (this.expr) json.expr = this.expr;
  if (this.literal) json.literal = this.literal;
  return json;
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Property.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Property.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Property.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return 'property(' + this.segments.join('') + ', ' + this.expr + ')';
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Query"></a>[module stylus.nodes.Query](#apidoc.module.stylus.nodes.Query)

#### <a name="apidoc.element.stylus.nodes.Query.Query"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Query ()](#apidoc.element.stylus.nodes.Query.Query)
- description and source-code
```javascript
function Query(){
  Node.call(this);
  this.nodes = [];
  this.type = '';
  this.predicate = '';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Query.prototype"></a>[module stylus.nodes.Query.prototype](#apidoc.module.stylus.nodes.Query.prototype)

#### <a name="apidoc.element.stylus.nodes.Query.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Query.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Query.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Query;
  clone.predicate = this.predicate;
  clone.type = this.type;
  for (var i = 0, len = this.nodes.length; i < len; ++i) {
    clone.push(this.nodes[i].clone(parent, clone));
  }
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Query.prototype.merge"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Query.prototype.</span>merge (other)](#apidoc.element.stylus.nodes.Query.prototype.merge)
- description and source-code
```javascript
merge = function (other){
  var query = new Query
    , p1 = this.resolvedPredicate
    , p2 = other.resolvedPredicate
    , t1 = this.resolvedType
    , t2 = other.resolvedType
    , type, pred;

  // Stolen from Sass :D
  t1 = t1 || t2;
  t2 = t2 || t1;
  if (('not' == p1) ^ ('not' == p2)) {
    if (t1 == t2) return;
    type = ('not' == p1) ? t2 : t1;
    pred = ('not' == p1) ? p2 : p1;
  } else if (('not' == p1) && ('not' == p2)) {
    if (t1 != t2) return;
    type = t1;
    pred = 'not';
  } else if (t1 != t2) {
    return;
  } else {
    type = t1;
    pred = p1 || p2;
  }
  query.predicate = pred;
  query.type = type;
  query.nodes = this.nodes.concat(other.nodes);
  return query;
}
```
- example usage
```shell
...
 *
 * @param {String} [filename]
 * @return {Array}
 * @api public
 */

Renderer.prototype.deps = function(filename){
var opts = utils.merge({ cache: false }, this.options);
if (filename) opts.filename = filename;

var DepsResolver = require('./visitor/deps-resolver')
  , parser = new Parser(this.str, opts);

try {
  nodes.filename = opts.filename;
...
```

#### <a name="apidoc.element.stylus.nodes.Query.prototype.push"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Query.prototype.</span>push (feature)](#apidoc.element.stylus.nodes.Query.prototype.push)
- description and source-code
```javascript
push = function (feature){
  this.nodes.push(feature);
}
```
- example usage
```shell
...
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
 * Lookahead 'n' tokens.
...
```

#### <a name="apidoc.element.stylus.nodes.Query.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Query.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Query.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Query',
    predicate: this.predicate,
    type: this.type,
    nodes: this.nodes,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Query.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Query.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Query.prototype.toString)
- description and source-code
```javascript
toString = function (){
  var pred = this.predicate ? this.predicate + ' ' : ''
    , type = this.type || ''
    , len = this.nodes.length
    , str = pred + type;
  if (len) {
    str += (type && ' and ') + this.nodes.map(function(expr){
      return expr.toString();
    }).join(' and ');
  }
  return str;
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.QueryList"></a>[module stylus.nodes.QueryList](#apidoc.module.stylus.nodes.QueryList)

#### <a name="apidoc.element.stylus.nodes.QueryList.QueryList"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>QueryList ()](#apidoc.element.stylus.nodes.QueryList.QueryList)
- description and source-code
```javascript
function QueryList(){
  Node.call(this);
  this.nodes = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.QueryList.prototype"></a>[module stylus.nodes.QueryList.prototype](#apidoc.module.stylus.nodes.QueryList.prototype)

#### <a name="apidoc.element.stylus.nodes.QueryList.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.QueryList.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.QueryList.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new QueryList;
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  for (var i = 0; i < this.nodes.length; ++i) {
    clone.push(this.nodes[i].clone(parent, clone));
  }
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.QueryList.prototype.merge"></a>[function <span class="apidocSignatureSpan">stylus.nodes.QueryList.prototype.</span>merge (other)](#apidoc.element.stylus.nodes.QueryList.prototype.merge)
- description and source-code
```javascript
merge = function (other){
  var list = new QueryList
    , merged;
  this.nodes.forEach(function(query){
    for (var i = 0, len = other.nodes.length; i < len; ++i){
      merged = query.merge(other.nodes[i]);
      if (merged) list.push(merged);
    }
  });
  return list;
}
```
- example usage
```shell
...
 *
 * @param {String} [filename]
 * @return {Array}
 * @api public
 */

Renderer.prototype.deps = function(filename){
var opts = utils.merge({ cache: false }, this.options);
if (filename) opts.filename = filename;

var DepsResolver = require('./visitor/deps-resolver')
  , parser = new Parser(this.str, opts);

try {
  nodes.filename = opts.filename;
...
```

#### <a name="apidoc.element.stylus.nodes.QueryList.prototype.push"></a>[function <span class="apidocSignatureSpan">stylus.nodes.QueryList.prototype.</span>push (node)](#apidoc.element.stylus.nodes.QueryList.prototype.push)
- description and source-code
```javascript
push = function (node){
  this.nodes.push(node);
}
```
- example usage
```shell
...
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
 * Lookahead 'n' tokens.
...
```

#### <a name="apidoc.element.stylus.nodes.QueryList.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.QueryList.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.QueryList.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'QueryList',
    nodes: this.nodes,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.QueryList.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.QueryList.prototype.</span>toString ()](#apidoc.element.stylus.nodes.QueryList.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return '(' + this.nodes.map(function(node){
    return node.toString();
  }).join(', ') + ')';
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.RGBA"></a>[module stylus.nodes.RGBA](#apidoc.module.stylus.nodes.RGBA)

#### <a name="apidoc.element.stylus.nodes.RGBA.RGBA"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>RGBA (r, g, b, a)](#apidoc.element.stylus.nodes.RGBA.RGBA)
- description and source-code
```javascript
function RGBA(r, g, b, a){
  Node.call(this);
  this.r = clamp(r);
  this.g = clamp(g);
  this.b = clamp(b);
  this.a = clampAlpha(a);
  this.name = '';
  this.rgba = this;
}
```
- example usage
```shell
...
 */

n: function() {
  var captures;
  if (captures = /^#([a-fA-F0-9]{1})[ \t]*/.exec(this.str)) {
    this.skip(captures);
    var n = parseInt(captures[1] + captures[1], 16)
      , color = new nodes.RGBA(n, n, n, 1);
    color.raw = captures[0];
    return new Token('color', color);
  }
},

/**
 * #nn
...
```

#### <a name="apidoc.element.stylus.nodes.RGBA.fromHSLA"></a>[function <span class="apidocSignatureSpan">stylus.nodes.RGBA.</span>fromHSLA (hsla)](#apidoc.element.stylus.nodes.RGBA.fromHSLA)
- description and source-code
```javascript
fromHSLA = function (hsla){
  var h = hsla.h / 360
    , s = hsla.s / 100
    , l = hsla.l / 100
    , a = hsla.a;

  var m2 = l <= .5 ? l * (s + 1) : l + s - l * s
    , m1 = l * 2 - m2;

  var r = hue(h + 1/3) * 0xff
    , g = hue(h) * 0xff
    , b = hue(h - 1/3) * 0xff;

  function hue(h) {
    if (h < 0) ++h;
    if (h > 1) --h;
    if (h * 6 < 1) return m1 + (m2 - m1) * h * 6;
    if (h * 2 < 1) return m2;
    if (h * 3 < 2) return m1 + (m2 - m1) * (2/3 - h) * 6;
    return m1;
  }

  return new RGBA(r,g,b,a);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.RGBA.withoutClamping"></a>[function <span class="apidocSignatureSpan">stylus.nodes.RGBA.</span>withoutClamping (r, g, b, a)](#apidoc.element.stylus.nodes.RGBA.withoutClamping)
- description and source-code
```javascript
withoutClamping = function (r, g, b, a){
  var rgba = new RGBA(0,0,0,0);
  rgba.r = r;
  rgba.g = g;
  rgba.b = b;
  rgba.a = a;
  return rgba;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.RGBA.prototype"></a>[module stylus.nodes.RGBA.prototype](#apidoc.module.stylus.nodes.RGBA.prototype)

#### <a name="apidoc.element.stylus.nodes.RGBA.prototype.add"></a>[function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>add (r, g, b, a)](#apidoc.element.stylus.nodes.RGBA.prototype.add)
- description and source-code
```javascript
add = function (r, g, b, a){
  return new RGBA(
      this.r + r
    , this.g + g
    , this.b + b
    , this.a + a);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.RGBA.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>clone ()](#apidoc.element.stylus.nodes.RGBA.prototype.clone)
- description and source-code
```javascript
clone = function (){
  var clone = new RGBA(
      this.r
    , this.g
    , this.b
    , this.a);
  clone.raw = this.raw;
  clone.name = this.name;
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.RGBA.prototype.divide"></a>[function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>divide (n)](#apidoc.element.stylus.nodes.RGBA.prototype.divide)
- description and source-code
```javascript
divide = function (n){
  return new RGBA(
      this.r / n
    , this.g / n
    , this.b / n
    , this.a);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.RGBA.prototype.multiply"></a>[function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>multiply (n)](#apidoc.element.stylus.nodes.RGBA.prototype.multiply)
- description and source-code
```javascript
multiply = function (n){
  return new RGBA(
      this.r * n
    , this.g * n
    , this.b * n
    , this.a);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.RGBA.prototype.operate"></a>[function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.RGBA.prototype.operate)
- description and source-code
```javascript
operate = function (op, right){
  if ('in' != op) right = right.first

  switch (op) {
    case 'is a':
      if ('string' == right.nodeName && 'color' == right.string) {
        return nodes.true;
      }
      break;
    case '+':
      switch (right.nodeName) {
        case 'unit':
          var n = right.val;
          switch (right.type) {
            case '%': return adjust(this, new nodes.String('lightness'), right);
            case 'deg': return this.hsla.adjustHue(n).rgba;
            default: return this.add(n,n,n,0);
          }
        case 'rgba':
          return this.add(right.r, right.g, right.b, right.a);
        case 'hsla':
          return this.hsla.add(right.h, right.s, right.l);
      }
      break;
    case '-':
      switch (right.nodeName) {
        case 'unit':
          var n = right.val;
          switch (right.type) {
            case '%': return adjust(this, new nodes.String('lightness'), new nodes.Unit(-n, '%'));
            case 'deg': return this.hsla.adjustHue(-n).rgba;
            default: return this.sub(n,n,n,0);
          }
        case 'rgba':
          return this.sub(right.r, right.g, right.b, right.a);
        case 'hsla':
          return this.hsla.sub(right.h, right.s, right.l);
      }
      break;
    case '*':
      switch (right.nodeName) {
        case 'unit':
          return this.multiply(right.val);
      }
      break;
    case '/':
      switch (right.nodeName) {
        case 'unit':
          return this.divide(right.val);
      }
      break;
  }
  return Node.prototype.operate.call(this, op, right);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.RGBA.prototype.sub"></a>[function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>sub (r, g, b, a)](#apidoc.element.stylus.nodes.RGBA.prototype.sub)
- description and source-code
```javascript
sub = function (r, g, b, a){
  return new RGBA(
      this.r - r
    , this.g - g
    , this.b - b
    , a == 1 ? this.a : this.a - a);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.RGBA.prototype.toBoolean"></a>[function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.RGBA.prototype.toBoolean)
- description and source-code
```javascript
toBoolean = function (){
  return nodes.true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.RGBA.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.RGBA.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'RGBA',
    r: this.r,
    g: this.g,
    b: this.b,
    a: this.a,
    raw: this.raw,
    name: this.name,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.RGBA.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.RGBA.prototype.</span>toString ()](#apidoc.element.stylus.nodes.RGBA.prototype.toString)
- description and source-code
```javascript
toString = function (){
  function pad(n) {
    return n < 16
      ? '0' + n.toString(16)
      : n.toString(16);
  }

  // special case for transparent named color
  if ('transparent' == this.name)
    return this.name;

  if (1 == this.a) {
    var r = pad(this.r)
      , g = pad(this.g)
      , b = pad(this.b);

    // Compress
    if (r[0] == r[1] && g[0] == g[1] && b[0] == b[1]) {
      return '#' + r[0] + g[0] + b[0];
    } else {
      return '#' + r + g + b;
    }
  } else {
    return 'rgba('
      + this.r + ','
      + this.g + ','
      + this.b + ','
      + (+this.a.toFixed(3)) + ')';
  }
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Return"></a>[module stylus.nodes.Return](#apidoc.module.stylus.nodes.Return)

#### <a name="apidoc.element.stylus.nodes.Return.Return"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Return (expr)](#apidoc.element.stylus.nodes.Return.Return)
- description and source-code
```javascript
function Return(expr){
  this.expr = expr || nodes.null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Return.prototype"></a>[module stylus.nodes.Return.prototype](#apidoc.module.stylus.nodes.Return.prototype)

#### <a name="apidoc.element.stylus.nodes.Return.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Return.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Return.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Return();
  clone.expr = this.expr.clone(parent, clone);
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Return.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Return.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Return.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Return',
    expr: this.expr,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```



# <a name="apidoc.module.stylus.nodes.Root"></a>[module stylus.nodes.Root](#apidoc.module.stylus.nodes.Root)

#### <a name="apidoc.element.stylus.nodes.Root.Root"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Root ()](#apidoc.element.stylus.nodes.Root.Root)
- description and source-code
```javascript
function Root(){
  this.nodes = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Root.prototype"></a>[module stylus.nodes.Root.prototype](#apidoc.module.stylus.nodes.Root.prototype)

#### <a name="apidoc.element.stylus.nodes.Root.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Root.prototype.</span>clone ()](#apidoc.element.stylus.nodes.Root.prototype.clone)
- description and source-code
```javascript
clone = function (){
  var clone = new Root();
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  this.nodes.forEach(function(node){
    clone.push(node.clone(clone, clone));
  });
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Root.prototype.push"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Root.prototype.</span>push (node)](#apidoc.element.stylus.nodes.Root.prototype.push)
- description and source-code
```javascript
push = function (node){
  this.nodes.push(node);
}
```
- example usage
```shell
...
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
 * Lookahead 'n' tokens.
...
```

#### <a name="apidoc.element.stylus.nodes.Root.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Root.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Root.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Root',
    nodes: this.nodes,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Root.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Root.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Root.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return '[Root]';
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```

#### <a name="apidoc.element.stylus.nodes.Root.prototype.unshift"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Root.prototype.</span>unshift (node)](#apidoc.element.stylus.nodes.Root.prototype.unshift)
- description and source-code
```javascript
unshift = function (node){
  this.nodes.unshift(node);
}
```
- example usage
```shell
...
  while (this.indentStack.length && this.indentStack[0] > indents) {
    this.stash.push(new Token('outdent'));
    this.indentStack.shift();
  }
  tok = this.stash.pop();
// Indent
} else if (indents && indents != this.indentStack[0]) {
  this.indentStack.unshift(indents);
  tok = new Token('indent');
// Newline
} else {
  tok = new Token('newline');
}

return tok;
...
```



# <a name="apidoc.module.stylus.nodes.Selector"></a>[module stylus.nodes.Selector](#apidoc.module.stylus.nodes.Selector)

#### <a name="apidoc.element.stylus.nodes.Selector.Selector"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Selector (segs)](#apidoc.element.stylus.nodes.Selector.Selector)
- description and source-code
```javascript
function Selector(segs){
  Node.call(this);
  this.inherits = true;
  this.segments = segs;
  this.optional = false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Selector.prototype"></a>[module stylus.nodes.Selector.prototype](#apidoc.module.stylus.nodes.Selector.prototype)

#### <a name="apidoc.element.stylus.nodes.Selector.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Selector.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Selector.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Selector;
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  clone.inherits = this.inherits;
  clone.val = this.val;
  clone.segments = this.segments.map(function(node){ return node.clone(parent, clone); });
  clone.optional = this.optional;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Selector.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Selector.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Selector.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Selector',
    inherits: this.inherits,
    segments: this.segments,
    optional: this.optional,
    val: this.val,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Selector.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Selector.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Selector.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return this.segments.join('') + (this.optional ? ' !optional' : '');
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.String"></a>[module stylus.nodes.String](#apidoc.module.stylus.nodes.String)

#### <a name="apidoc.element.stylus.nodes.String.String"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>String (val, quote)](#apidoc.element.stylus.nodes.String.String)
- description and source-code
```javascript
function String(val, quote){
  Node.call(this);
  this.val = val;
  this.string = val;
  this.prefixed = false;
  if (typeof quote !== 'string') {
    this.quote = "'";
  } else {
    this.quote = quote;
  }
}
```
- example usage
```shell
...
string: function() {
  var captures;
  if (captures = /^("[^"]*"|'[^']*')[ \t]*/.exec(this.str)) {
    var str = captures[1]
      , quote = captures[0][0];
    this.skip(captures);
    str = str.slice(1,-1).replace(/\\n/g, '\n');
    return new Token('string', new nodes.String(str, quote));
  }
},

/**
 * #rrggbbaa | #rrggbb | #rgba | #rgb | #nn | #n
 */
...
```



# <a name="apidoc.module.stylus.nodes.String.prototype"></a>[module stylus.nodes.String.prototype](#apidoc.module.stylus.nodes.String.prototype)

#### <a name="apidoc.element.stylus.nodes.String.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.String.prototype.</span>clone ()](#apidoc.element.stylus.nodes.String.prototype.clone)
- description and source-code
```javascript
clone = function (){
  var clone = new String(this.val, this.quote);
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.String.prototype.coerce"></a>[function <span class="apidocSignatureSpan">stylus.nodes.String.prototype.</span>coerce (other)](#apidoc.element.stylus.nodes.String.prototype.coerce)
- description and source-code
```javascript
coerce = function (other){
  switch (other.nodeName) {
    case 'string':
      return other;
    case 'expression':
      return new String(other.nodes.map(function(node){
        return this.coerce(node).val;
      }, this).join(' '));
    default:
      return new String(other.toString());
  }
}
```
- example usage
```shell
...
 * @param {String} name
 * @param {Function|Node} fn
 * @return {Renderer} for chaining
 * @api public
 */

Renderer.prototype.define = function(name, fn, raw){
fn = utils.coerce(fn, raw);

if (fn.nodeName) {
  this.options.globals[name] = fn;
  return this;
}

// function
...
```

#### <a name="apidoc.element.stylus.nodes.String.prototype.operate"></a>[function <span class="apidocSignatureSpan">stylus.nodes.String.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.String.prototype.operate)
- description and source-code
```javascript
operate = function (op, right){
  switch (op) {
    case '%':
      var expr = new nodes.Expression;
      expr.push(this);

      // constructargs
      var args = 'expression' == right.nodeName
        ? utils.unwrap(right).nodes
        : [right];

      // apply
      return sprintf.apply(null, [expr].concat(args));
    case '+':
      var expr = new nodes.Expression;
      expr.push(new String(this.val + this.coerce(right).val));
      return expr;
    default:
      return Node.prototype.operate.call(this, op, right);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.String.prototype.toBoolean"></a>[function <span class="apidocSignatureSpan">stylus.nodes.String.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.String.prototype.toBoolean)
- description and source-code
```javascript
toBoolean = function (){
  return nodes.Boolean(this.val.length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.String.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.String.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.String.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'String',
    val: this.val,
    quote: this.quote,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.String.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.String.prototype.</span>toString ()](#apidoc.element.stylus.nodes.String.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return this.quote + this.val + this.quote;
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Supports"></a>[module stylus.nodes.Supports](#apidoc.module.stylus.nodes.Supports)

#### <a name="apidoc.element.stylus.nodes.Supports.Supports"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Supports (condition)](#apidoc.element.stylus.nodes.Supports.Supports)
- description and source-code
```javascript
function Supports(condition){
  Atrule.call(this, 'supports');
  this.condition = condition;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Supports.prototype"></a>[module stylus.nodes.Supports.prototype](#apidoc.module.stylus.nodes.Supports.prototype)

#### <a name="apidoc.element.stylus.nodes.Supports.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Supports.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Supports.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Supports;
  clone.condition = this.condition.clone(parent, clone);
  clone.block = this.block.clone(parent, clone);
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Supports.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Supports.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Supports.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Supports',
    condition: this.condition,
    block: this.block,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Supports.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Supports.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Supports.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return '@supports ' + this.condition;
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.nodes.Ternary"></a>[module stylus.nodes.Ternary](#apidoc.module.stylus.nodes.Ternary)

#### <a name="apidoc.element.stylus.nodes.Ternary.Ternary"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Ternary (cond, trueExpr, falseExpr)](#apidoc.element.stylus.nodes.Ternary.Ternary)
- description and source-code
```javascript
function Ternary(cond, trueExpr, falseExpr){
  Node.call(this);
  this.cond = cond;
  this.trueExpr = trueExpr;
  this.falseExpr = falseExpr;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.Ternary.prototype"></a>[module stylus.nodes.Ternary.prototype](#apidoc.module.stylus.nodes.Ternary.prototype)

#### <a name="apidoc.element.stylus.nodes.Ternary.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Ternary.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.Ternary.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new Ternary();
  clone.cond = this.cond.clone(parent, clone);
  clone.trueExpr = this.trueExpr.clone(parent, clone);
  clone.falseExpr = this.falseExpr.clone(parent, clone);
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Ternary.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Ternary.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Ternary.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Ternary',
    cond: this.cond,
    trueExpr: this.trueExpr,
    falseExpr: this.falseExpr,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```



# <a name="apidoc.module.stylus.nodes.UnaryOp"></a>[module stylus.nodes.UnaryOp](#apidoc.module.stylus.nodes.UnaryOp)

#### <a name="apidoc.element.stylus.nodes.UnaryOp.UnaryOp"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>UnaryOp (op, expr)](#apidoc.element.stylus.nodes.UnaryOp.UnaryOp)
- description and source-code
```javascript
function UnaryOp(op, expr){
  Node.call(this);
  this.op = op;
  this.expr = expr;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.nodes.UnaryOp.prototype"></a>[module stylus.nodes.UnaryOp.prototype](#apidoc.module.stylus.nodes.UnaryOp.prototype)

#### <a name="apidoc.element.stylus.nodes.UnaryOp.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.UnaryOp.prototype.</span>clone (parent)](#apidoc.element.stylus.nodes.UnaryOp.prototype.clone)
- description and source-code
```javascript
clone = function (parent){
  var clone = new UnaryOp(this.op);
  clone.expr = this.expr.clone(parent, clone);
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.UnaryOp.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.UnaryOp.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.UnaryOp.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'UnaryOp',
    op: this.op,
    expr: this.expr,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```



# <a name="apidoc.module.stylus.nodes.Unit"></a>[module stylus.nodes.Unit](#apidoc.module.stylus.nodes.Unit)

#### <a name="apidoc.element.stylus.nodes.Unit.Unit"></a>[function <span class="apidocSignatureSpan">stylus.nodes.</span>Unit (val, type)](#apidoc.element.stylus.nodes.Unit.Unit)
- description and source-code
```javascript
function Unit(val, type){
  Node.call(this);
  this.val = val;
  this.type = type;
}
```
- example usage
```shell
...

unit: function() {
  var captures;
  if (captures = /^(-)?(\d+\.\d+|\d+|\.\d+)(%|[a-zA-Z]+)?[ \t]*/.exec(this.str)) {
    this.skip(captures);
    var n = parseFloat(captures[2]);
    if ('-' == captures[1]) n = -n;
    var node = new nodes.Unit(n, captures[3]);
    node.raw = captures[0];
    return new Token('unit', node);
  }
},

/**
 * '"' [^"]+ '"' | "'"" [^']+ "'"
...
```



# <a name="apidoc.module.stylus.nodes.Unit.prototype"></a>[module stylus.nodes.Unit.prototype](#apidoc.module.stylus.nodes.Unit.prototype)

#### <a name="apidoc.element.stylus.nodes.Unit.prototype.clone"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Unit.prototype.</span>clone ()](#apidoc.element.stylus.nodes.Unit.prototype.clone)
- description and source-code
```javascript
clone = function (){
  var clone = new Unit(this.val, this.type);
  clone.lineno = this.lineno;
  clone.column = this.column;
  clone.filename = this.filename;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Unit.prototype.coerce"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Unit.prototype.</span>coerce (other)](#apidoc.element.stylus.nodes.Unit.prototype.coerce)
- description and source-code
```javascript
coerce = function (other){
  if ('unit' == other.nodeName) {
    var a = this
      , b = other
      , factorA = FACTOR_TABLE[a.type]
      , factorB = FACTOR_TABLE[b.type];

    if (factorA && factorB && (factorA.label == factorB.label)) {
      var bVal = b.val * (factorB.val / factorA.val);
      return new nodes.Unit(bVal, a.type);
    } else {
      return new nodes.Unit(b.val, a.type);
    }
  } else if ('string' == other.nodeName) {
    // keyframes interpolation
    if ('%' == other.val) return new nodes.Unit(0, '%');
    var val = parseFloat(other.val);
    if (isNaN(val)) Node.prototype.coerce.call(this, other);
    return new nodes.Unit(val);
  } else {
    return Node.prototype.coerce.call(this, other);
  }
}
```
- example usage
```shell
...
 * @param {String} name
 * @param {Function|Node} fn
 * @return {Renderer} for chaining
 * @api public
 */

Renderer.prototype.define = function(name, fn, raw){
fn = utils.coerce(fn, raw);

if (fn.nodeName) {
  this.options.globals[name] = fn;
  return this;
}

// function
...
```

#### <a name="apidoc.element.stylus.nodes.Unit.prototype.operate"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Unit.prototype.</span>operate (op, right)](#apidoc.element.stylus.nodes.Unit.prototype.operate)
- description and source-code
```javascript
operate = function (op, right){
  var type = this.type || right.first.type;

  // swap color
  if ('rgba' == right.nodeName || 'hsla' == right.nodeName) {
    return right.operate(op, this);
  }

  // operate
  if (this.shouldCoerce(op)) {
    right = right.first;
    // percentages
    if ('%' != this.type && ('-' == op || '+' == op) && '%' == right.type) {
      right = new Unit(this.val * (right.val / 100), '%');
    } else {
      right = this.coerce(right);
    }

    switch (op) {
      case '-':
        return new Unit(this.val - right.val, type);
      case '+':
        // keyframes interpolation
        type = type || (right.type == '%' && right.type);
        return new Unit(this.val + right.val, type);
      case '/':
        return new Unit(this.val / right.val, type);
      case '*':
        return new Unit(this.val * right.val, type);
      case '%':
        return new Unit(this.val % right.val, type);
      case '**':
        return new Unit(Math.pow(this.val, right.val), type);
      case '..':
      case '...':
        var start = this.val
          , end = right.val
          , expr = new nodes.Expression
          , inclusive = '..' == op;
        if (start < end) {
          do {
            expr.push(new nodes.Unit(start));
          } while (inclusive ? ++start <= end : ++start < end);
        } else {
          do {
            expr.push(new nodes.Unit(start));
          } while (inclusive ? --start >= end : --start > end);
        }
        return expr;
    }
  }

  return Node.prototype.operate.call(this, op, right);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Unit.prototype.toBoolean"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Unit.prototype.</span>toBoolean ()](#apidoc.element.stylus.nodes.Unit.prototype.toBoolean)
- description and source-code
```javascript
toBoolean = function (){
  return nodes.Boolean(this.type
      ? true
      : this.val);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.nodes.Unit.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Unit.prototype.</span>toJSON ()](#apidoc.element.stylus.nodes.Unit.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (){
  return {
    __type: 'Unit',
    val: this.val,
    type: this.type,
    lineno: this.lineno,
    column: this.column,
    filename: this.filename
  };
}
```
- example usage
```shell
...
  // compile
  var compiler = this.options.sourcemap
    ? new (require('./visitor/sourcemapper'))(ast, this.options)
    : new (require('./visitor/compiler'))(ast, this.options)
    , css = compiler.compile();

  // expose sourcemap
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
...
```

#### <a name="apidoc.element.stylus.nodes.Unit.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.nodes.Unit.prototype.</span>toString ()](#apidoc.element.stylus.nodes.Unit.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return this.val + (this.type || '');
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.renderer"></a>[module stylus.renderer](#apidoc.module.stylus.renderer)

#### <a name="apidoc.element.stylus.renderer.renderer"></a>[function <span class="apidocSignatureSpan">stylus.</span>renderer (str, options)](#apidoc.element.stylus.renderer.renderer)
- description and source-code
```javascript
function Renderer(str, options) {
  options = options || {};
  options.globals = options.globals || {};
  options.functions = options.functions || {};
  options.use = options.use || [];
  options.use = Array.isArray(options.use) ? options.use : [options.use];
  options.imports = [join(__dirname, 'functions')];
  options.paths = options.paths || [];
  options.filename = options.filename || 'stylus';
  options.Evaluator = options.Evaluator || Evaluator;
  this.options = options;
  this.str = str;
  this.events = events;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.renderer.prototype"></a>[module stylus.renderer.prototype](#apidoc.module.stylus.renderer.prototype)

#### <a name="apidoc.element.stylus.renderer.prototype.define"></a>[function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>define (name, fn, raw)](#apidoc.element.stylus.renderer.prototype.define)
- description and source-code
```javascript
define = function (name, fn, raw){
  fn = utils.coerce(fn, raw);

  if (fn.nodeName) {
    this.options.globals[name] = fn;
    return this;
  }

  // function
  this.options.functions[name] = fn;
  if (undefined != raw) fn.raw = raw;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.renderer.prototype.deps"></a>[function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>deps (filename)](#apidoc.element.stylus.renderer.prototype.deps)
- description and source-code
```javascript
deps = function (filename){
  var opts = utils.merge({ cache: false }, this.options);
  if (filename) opts.filename = filename;

  var DepsResolver = require('./visitor/deps-resolver')
    , parser = new Parser(this.str, opts);

  try {
    nodes.filename = opts.filename;
    // parse
    var ast = parser.parse()
      , resolver = new DepsResolver(ast, opts);

    // resolve dependencies
    return resolver.resolve();
  } catch (err) {
    var options = {};
    options.input = err.input || this.str;
    options.filename = err.filename || opts.filename;
    options.lineno = err.lineno || parser.lexer.lineno;
    options.column = err.column || parser.lexer.column;
    throw utils.formatException(err, options);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.renderer.prototype.get"></a>[function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>get (key)](#apidoc.element.stylus.renderer.prototype.get)
- description and source-code
```javascript
get = function (key){
  return this.options[key];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.renderer.prototype.import"></a>[function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>import (file)](#apidoc.element.stylus.renderer.prototype.import)
- description and source-code
```javascript
import = function (file){
  this.options.imports.push(file);
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.renderer.prototype.include"></a>[function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>include (path)](#apidoc.element.stylus.renderer.prototype.include)
- description and source-code
```javascript
include = function (path){
  this.options.paths.push(path);
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.renderer.prototype.render"></a>[function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>render (fn)](#apidoc.element.stylus.renderer.prototype.render)
- description and source-code
```javascript
render = function (fn){
  var parser = this.parser = new Parser(this.str, this.options);

  // use plugin(s)
  for (var i = 0, len = this.options.use.length; i < len; i++) {
    this.use(this.options.use[i]);
  }

  try {
    nodes.filename = this.options.filename;
    // parse
    var ast = parser.parse();

    // evaluate
    this.evaluator = new this.options.Evaluator(ast, this.options);
    this.nodes = nodes;
    this.evaluator.renderer = this;
    ast = this.evaluator.evaluate();

    // normalize
    var normalizer = new Normalizer(ast, this.options);
    ast = normalizer.normalize();

    // compile
    var compiler = this.options.sourcemap
      ? new (require('./visitor/sourcemapper'))(ast, this.options)
      : new (require('./visitor/compiler'))(ast, this.options)
      , css = compiler.compile();

    // expose sourcemap
    if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
  } catch (err) {
    var options = {};
    options.input = err.input || this.str;
    options.filename = err.filename || this.options.filename;
    options.lineno = err.lineno || parser.lexer.lineno;
    options.column = err.column || parser.lexer.column;
    if (!fn) throw utils.formatException(err, options);
    return fn(utils.formatException(err, options));
  }

  // fire 'end' event
  var listeners = this.listeners('end');
  if (fn) listeners.push(fn);
  for (var i = 0, len = listeners.length; i < len; i++) {
    var ret = listeners[i](null, css);
    if (ret) css = ret;
  }
  if (!fn) return css;
}
```
- example usage
```shell
...
      function compile() {
debug('read %s', cssPath);
fs.readFile(stylusPath, 'utf8', function(err, str){
  if (err) return error(err);
  var style = options.compile(str, stylusPath);
  var paths = style.options._imports = [];
  imports[stylusPath] = null;
  style.render(function(err, css){
    if (err) return next(err);
    debug('render %s', stylusPath);
    imports[stylusPath] = paths;
    mkdirp(dirname(cssPath), parseInt('0700', 8), function(err){
      if (err) return error(err);
      fs.writeFile(cssPath, css, 'utf8', next);
    });
...
```

#### <a name="apidoc.element.stylus.renderer.prototype.set"></a>[function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>set (key, val)](#apidoc.element.stylus.renderer.prototype.set)
- description and source-code
```javascript
set = function (key, val){
  this.options[key] = val;
  return this;
}
```
- example usage
```shell
...
* set the 'compress' option, or define additional functions.
*
* By default the compile function simply sets the 'filename'
* and renders the CSS.
*
*      function compile(str, path) {
*        return stylus(str)
*          .set('filename', path)
*          .set('compress', true);
*      }
*
* Pass the middleware to Connect, grabbing .styl files from this directory
* and saving .css files to _./public_. Also supplying our custom 'compile' function.
*
* Following that we have a 'static()' layer setup to serve the .css
...
```

#### <a name="apidoc.element.stylus.renderer.prototype.use"></a>[function <span class="apidocSignatureSpan">stylus.renderer.prototype.</span>use (fn)](#apidoc.element.stylus.renderer.prototype.use)
- description and source-code
```javascript
use = function (fn){
  fn.call(this, this);
  return this;
}
```
- example usage
```shell
...
 *
 *      app.middleware({
 *          src: __dirname
 *        , dest: __dirname + '/public'
 *        , compile: compile
 *      })
 *
 *      app.use(connect.static(__dirname + '/public'));
 *
 * @param {Object} options
 * @return {Function}
 * @api public
 */

module.exports = function(options){
...
```



# <a name="apidoc.module.stylus.selector_parser"></a>[module stylus.selector_parser](#apidoc.module.stylus.selector_parser)

#### <a name="apidoc.element.stylus.selector_parser.selector_parser"></a>[function <span class="apidocSignatureSpan">stylus.</span>selector_parser (str, stack, parts)](#apidoc.element.stylus.selector_parser.selector_parser)
- description and source-code
```javascript
function SelectorParser(str, stack, parts) {
  this.str = str;
  this.stack = stack || [];
  this.parts = parts || [];
  this.pos = 0;
  this.level = 2;
  this.nested = true;
  this.ignore = false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.selector_parser.prototype"></a>[module stylus.selector_parser.prototype](#apidoc.module.stylus.selector_parser.prototype)

#### <a name="apidoc.element.stylus.selector_parser.prototype.advance"></a>[function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>advance ()](#apidoc.element.stylus.selector_parser.prototype.advance)
- description and source-code
```javascript
advance = function () {
  return this.root()
    || this.relative()
    || this.initial()
    || this.escaped()
    || this.parent()
    || this.partial()
    || this.char();
}
```
- example usage
```shell
...
 * @param {Number} n
 * @return {Object}
 * @api private
 */

lookahead: function(n){
  var fetch = n - this.stash.length;
  while (fetch-- > 0) this.stash.push(this.advance());
  return this.stash[--n];
},

/**
 * Consume the given 'len'.
 *
 * @param {Number|Array} len
...
```

#### <a name="apidoc.element.stylus.selector_parser.prototype.char"></a>[function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>char ()](#apidoc.element.stylus.selector_parser.prototype.char)
- description and source-code
```javascript
char = function () {
  var char = this.str[0];
  this.skip(1);
  return char;
}
```
- example usage
```shell
...
SelectorParser.prototype.advance = function() {
  return this.root()
    || this.relative()
    || this.initial()
    || this.escaped()
    || this.parent()
    || this.partial()
    || this.char();
};

/**
 * '/'
 */

SelectorParser.prototype.root = function() {
...
```

#### <a name="apidoc.element.stylus.selector_parser.prototype.escaped"></a>[function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>escaped ()](#apidoc.element.stylus.selector_parser.prototype.escaped)
- description and source-code
```javascript
escaped = function () {
  if ('\\' == this.str[0]) {
    var char = this.str[1];
    if ('&' == char || '^' == char) {
      this.skip(2);
      return char;
    }
  }
}
```
- example usage
```shell
...
, tok = this.eos()
|| this.null()
|| this.sep()
|| this.keyword()
|| this.urlchars()
|| this.comment()
|| this.newline()
|| this.escaped()
|| this.important()
|| this.literal()
|| this.anonFunc()
|| this.atrule()
|| this.function()
|| this.brace()
|| this.paren()
...
```

#### <a name="apidoc.element.stylus.selector_parser.prototype.initial"></a>[function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>initial ()](#apidoc.element.stylus.selector_parser.prototype.initial)
- description and source-code
```javascript
initial = function () {
  if (!this.pos && '~' == this.str[0] && '/' == this.str[1]) {
    this.nested = false;
    this.skip(2);
    return this.stack[0];
  }
}
```
- example usage
```shell
...
 * @return {String}
 * @api private
 */

SelectorParser.prototype.advance = function() {
  return this.root()
    || this.relative()
    || this.initial()
    || this.escaped()
    || this.parent()
    || this.partial()
    || this.char();
};

/**
...
```

#### <a name="apidoc.element.stylus.selector_parser.prototype.number"></a>[function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>number ()](#apidoc.element.stylus.selector_parser.prototype.number)
- description and source-code
```javascript
number = function () {
  var i =  0, ret = '';
  if ('-' == this.str[i])
    ret += this.str[i++];

  while (this.str.charCodeAt(i) >= 48
    && this.str.charCodeAt(i) <= 57)
    ret += this.str[i++];

  if (ret) {
    this.skip(i);
    return Number(ret);
  }
}
```
- example usage
```shell
...
};

/**
 * number ('..' number)?
 */

SelectorParser.prototype.range = function() {
var start = this.number()
  , ret;

if ('..' == this.str.slice(0, 2)) {
  this.skip(2);
  var end = this.number()
    , len = this.parts.length;
...
```

#### <a name="apidoc.element.stylus.selector_parser.prototype.parent"></a>[function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>parent ()](#apidoc.element.stylus.selector_parser.prototype.parent)
- description and source-code
```javascript
parent = function () {
  if ('&' == this.str[0]) {
    this.nested = false;

    if (!this.pos && (!this.stack.length || this.raw)) {
      var i = 0;
      while (' ' == this.str[++i]) ;
      if (~COMBINATORS.indexOf(this.str[i])) {
        this.skip(i + 1);
        return;
      }
    }

    this.skip(1);
    if (!this.raw)
      return this.stack[this.stack.length - 1];
  }
}
```
- example usage
```shell
...
*/

SelectorParser.prototype.advance = function() {
 return this.root()
   || this.relative()
   || this.initial()
   || this.escaped()
   || this.parent()
   || this.partial()
   || this.char();
};

/**
* '/'
*/
...
```

#### <a name="apidoc.element.stylus.selector_parser.prototype.parse"></a>[function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>parse ()](#apidoc.element.stylus.selector_parser.prototype.parse)
- description and source-code
```javascript
parse = function () {
  var val = '';
  while (this.str.length) {
    val += this.advance() || '';
    if (this.ignore) {
      val = '';
      break;
    }
  }
  return { val: val.trimRight(), nested: this.nested };
}
```
- example usage
```shell
...
.set('linenos', options.linenos)
.set('sourcemap', options.sourcemap);
  };

  // Middleware
  return function stylus(req, res, next){
    if ('GET' != req.method && 'HEAD' != req.method) return next();
    var path = url.parse(req.url).pathname;
    if (/\.css$/.test(path)) {

if (typeof dest == 'string') {
  // check for dest-path overlap
  var overlap = compare(dest, path).length;
  if ('/' == path.charAt(0)) overlap++;
  path = path.slice(overlap);
...
```

#### <a name="apidoc.element.stylus.selector_parser.prototype.partial"></a>[function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>partial ()](#apidoc.element.stylus.selector_parser.prototype.partial)
- description and source-code
```javascript
partial = function () {
  if ('^' == this.str[0] && '[' == this.str[1]) {
    this.skip(2);
    this.skipSpaces();
    var ret = this.range();
    this.skipSpaces();
    if (']' != this.str[0]) return '^[';
    this.nested = false;
    this.skip(1);
    if (ret) {
      return ret;
    } else {
      this.ignore = true;
    }
  }
}
```
- example usage
```shell
...

SelectorParser.prototype.advance = function() {
 return this.root()
   || this.relative()
   || this.initial()
   || this.escaped()
   || this.parent()
   || this.partial()
   || this.char();
};

/**
* '/'
*/
...
```

#### <a name="apidoc.element.stylus.selector_parser.prototype.range"></a>[function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>range ()](#apidoc.element.stylus.selector_parser.prototype.range)
- description and source-code
```javascript
range = function () {
  var start = this.number()
    , ret;

  if ('..' == this.str.slice(0, 2)) {
    this.skip(2);
    var end = this.number()
      , len = this.parts.length;

    if (start < 0) start = len + start - 1;
    if (end < 0) end = len + end - 1;

    if (start > end) {
      var tmp = start;
      start = end;
      end = tmp;
    }

    if (end < len - 1) {
      ret = this.parts.slice(start, end + 1).map(function(part) {
        var selector = new SelectorParser(part, this.stack, this.parts);
        selector.raw = true;
        return selector.parse();
      }, this).map(function(selector) {
        return (selector.nested ? ' ' : '') + selector.val;
      }).join('').trim();
    }
  } else {
    ret = this.stack[
      start < 0 ? this.stack.length + start - 1 : start
    ];
  }

  if (ret) {
    return ret;
  } else {
    this.ignore = true;
  }
}
```
- example usage
```shell
...
 * '^[' range ']'
 */

SelectorParser.prototype.partial = function() {
if ('^' == this.str[0] && '[' == this.str[1]) {
  this.skip(2);
  this.skipSpaces();
  var ret = this.range();
  this.skipSpaces();
  if (']' != this.str[0]) return '^[';
  this.nested = false;
  this.skip(1);
  if (ret) {
    return ret;
  } else {
...
```

#### <a name="apidoc.element.stylus.selector_parser.prototype.relative"></a>[function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>relative (multi)](#apidoc.element.stylus.selector_parser.prototype.relative)
- description and source-code
```javascript
relative = function (multi) {
  if ((!this.pos || multi) && '../' == this.str.slice(0, 3)) {
    this.nested = false;
    this.skip(3);
    while (this.relative(true)) this.level++;
    if (!this.raw) {
      var ret = this.stack[this.stack.length - this.level];
      if (ret) {
        return ret;
      } else {
        this.ignore = true;
      }
    }
  }
}
```
- example usage
```shell
...
 *
 * @return {String}
 * @api private
 */

SelectorParser.prototype.advance = function() {
  return this.root()
    || this.relative()
    || this.initial()
    || this.escaped()
    || this.parent()
    || this.partial()
    || this.char();
};
...
```

#### <a name="apidoc.element.stylus.selector_parser.prototype.root"></a>[function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>root ()](#apidoc.element.stylus.selector_parser.prototype.root)
- description and source-code
```javascript
root = function () {
  if (!this.pos && '/' == this.str[0]
    && 'deep' != this.str.slice(1, 5)) {
    this.nested = false;
    this.skip(1);
  }
}
```
- example usage
```shell
...
 * Fetch next token.
 *
 * @return {String}
 * @api private
 */

SelectorParser.prototype.advance = function() {
  return this.root()
    || this.relative()
    || this.initial()
    || this.escaped()
    || this.parent()
    || this.partial()
    || this.char();
};
...
```

#### <a name="apidoc.element.stylus.selector_parser.prototype.skip"></a>[function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>skip (len)](#apidoc.element.stylus.selector_parser.prototype.skip)
- description and source-code
```javascript
skip = function (len) {
  this.str = this.str.substr(len);
  this.pos += len;
}
```
- example usage
```shell
...
 * url char
 */

urlchars: function() {
  var captures;
  if (!this.isURL) return;
  if (captures = /^[\/:@.;?&=*!,<>#%0-9]+/.exec(this.str)) {
    this.skip(captures);
    return new Token('literal', new nodes.Literal(captures[0]));
  }
},

/**
 * ';' [ \t]*
 */
...
```

#### <a name="apidoc.element.stylus.selector_parser.prototype.skipSpaces"></a>[function <span class="apidocSignatureSpan">stylus.selector_parser.prototype.</span>skipSpaces ()](#apidoc.element.stylus.selector_parser.prototype.skipSpaces)
- description and source-code
```javascript
skipSpaces = function () {
  while (' ' == this.str[0]) this.skip(1);
}
```
- example usage
```shell
...
/**
 * '^[' range ']'
 */

SelectorParser.prototype.partial = function() {
if ('^' == this.str[0] && '[' == this.str[1]) {
  this.skip(2);
  this.skipSpaces();
  var ret = this.range();
  this.skipSpaces();
  if (']' != this.str[0]) return '^[';
  this.nested = false;
  this.skip(1);
  if (ret) {
    return ret;
...
```



# <a name="apidoc.module.stylus.stack"></a>[module stylus.stack](#apidoc.module.stylus.stack)

#### <a name="apidoc.element.stylus.stack.stack"></a>[function <span class="apidocSignatureSpan">stylus.</span>stack ()](#apidoc.element.stylus.stack.stack)
- description and source-code
```javascript
function Stack() {
  Array.apply(this, arguments);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.stack.prototype"></a>[module stylus.stack.prototype](#apidoc.module.stylus.stack.prototype)

#### <a name="apidoc.element.stylus.stack.prototype.getBlockFrame"></a>[function <span class="apidocSignatureSpan">stylus.stack.prototype.</span>getBlockFrame (block)](#apidoc.element.stylus.stack.prototype.getBlockFrame)
- description and source-code
```javascript
getBlockFrame = function (block){
  for (var i = 0; i < this.length; ++i) {
    if (block == this[i].block) {
      return this[i];
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.stack.prototype.inspect"></a>[function <span class="apidocSignatureSpan">stylus.stack.prototype.</span>inspect ()](#apidoc.element.stylus.stack.prototype.inspect)
- description and source-code
```javascript
inspect = function (){
  return this.reverse().map(function(frame){
    return frame.inspect();
  }).join('\n');
}
```
- example usage
```shell
...
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
 * Lookahead 'n' tokens.
...
```

#### <a name="apidoc.element.stylus.stack.prototype.lookup"></a>[function <span class="apidocSignatureSpan">stylus.stack.prototype.</span>lookup (name)](#apidoc.element.stylus.stack.prototype.lookup)
- description and source-code
```javascript
lookup = function (name){
  var block = this.currentFrame.block
    , val
    , ret;

  do {
    var frame = this.getBlockFrame(block);
    if (frame && (val = frame.lookup(name))) {
      return val;
    }
  } while (block = block.parent);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.stack.prototype.push"></a>[function <span class="apidocSignatureSpan">stylus.stack.prototype.</span>push (frame)](#apidoc.element.stylus.stack.prototype.push)
- description and source-code
```javascript
push = function (frame){
  frame.stack = this;
  frame.parent = this.currentFrame;
  return [].push.apply(this, arguments);
}
```
- example usage
```shell
...
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
 * Lookahead 'n' tokens.
...
```

#### <a name="apidoc.element.stylus.stack.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.stack.prototype.</span>toString ()](#apidoc.element.stylus.stack.prototype.toString)
- description and source-code
```javascript
toString = function (){
  var block
    , node
    , buf = []
    , location
    , len = this.length;

  while (len--) {
    block = this[len].block;
    if (node = block.node) {
      location = '(' + node.filename + ':' + (node.lineno + 1) + ':' + node.column + ')';
      switch (node.nodeName) {
        case 'function':
          buf.push('    at ' + node.name + '() ' + location);
          break;
        case 'group':
          buf.push('    at "' + node.nodes[0].val + '" ' + location);
          break;
      }
    }
  }

  return buf.join('\n');
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.token"></a>[module stylus.token](#apidoc.module.stylus.token)

#### <a name="apidoc.element.stylus.token.token"></a>[function <span class="apidocSignatureSpan">stylus.</span>token (type, val)](#apidoc.element.stylus.token.token)
- description and source-code
```javascript
function Token(type, val) {
  this.type = type;
  this.val = val;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.stylus.token.prototype"></a>[module stylus.token.prototype](#apidoc.module.stylus.token.prototype)

#### <a name="apidoc.element.stylus.token.prototype.inspect"></a>[function <span class="apidocSignatureSpan">stylus.token.prototype.</span>inspect ()](#apidoc.element.stylus.token.prototype.inspect)
- description and source-code
```javascript
inspect = function (){
  var val = ' ' + inspect(this.val);
  return '[Token:' + this.lineno + ':' + this.column + ' '
    + '\x1b[32m' + this.type + '\x1b[0m'
    + '\x1b[33m' + (this.val ? val : '') + '\x1b[0m'
    + ']';
}
```
- example usage
```shell
...
 */

inspect: function(){
  var tok
    , tmp = this.str
    , buf = [];
  while ('eos' != (tok = this.next()).type) {
    buf.push(tok.inspect());
  }
  this.str = tmp;
  return buf.concat(tok.inspect()).join('\n');
},

/**
 * Lookahead 'n' tokens.
...
```

#### <a name="apidoc.element.stylus.token.prototype.toString"></a>[function <span class="apidocSignatureSpan">stylus.token.prototype.</span>toString ()](#apidoc.element.stylus.token.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
}
```
- example usage
```shell
...
 * @return {String}
 * @api public
 */

Token.prototype.toString = function(){
  return (undefined === this.val
    ? this.type
    : this.val).toString();
};
...
```



# <a name="apidoc.module.stylus.utils"></a>[module stylus.utils](#apidoc.module.stylus.utils)

#### <a name="apidoc.element.stylus.utils.absolute"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>absolute (path)](#apidoc.element.stylus.utils.absolute)
- description and source-code
```javascript
function isAbsolute(path) {
  assertPath(path);
  return path.length > 0 && path.charCodeAt(0) === 47/*/*/;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.utils.assertColor"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>assertColor (node, param)](#apidoc.element.stylus.utils.assertColor)
- description and source-code
```javascript
assertColor = function (node, param){
  exports.assertPresent(node, param);
  switch (node.nodeName) {
    case 'rgba':
    case 'hsla':
      return;
    default:
      var actual = node.nodeName
        , msg = 'expected rgba or hsla, but got ' + actual + ':' + node;
      throw new Error('TypeError: ' + msg);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.utils.assertPresent"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>assertPresent (node, name)](#apidoc.element.stylus.utils.assertPresent)
- description and source-code
```javascript
assertPresent = function (node, name){
  if (node) return;
  if (name) throw new Error('"' + name + '" argument required');
  throw new Error('argument missing');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.utils.assertString"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>assertString (node, param)](#apidoc.element.stylus.utils.assertString)
- description and source-code
```javascript
assertString = function (node, param){
  exports.assertPresent(node, param);
  switch (node.nodeName) {
    case 'string':
    case 'ident':
    case 'literal':
      return;
    default:
      var actual = node.nodeName
        , msg = 'expected string, ident or literal, but got ' + actual + ':' + node;
      throw new Error('TypeError: ' + msg);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.utils.assertType"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>assertType (node, type, param)](#apidoc.element.stylus.utils.assertType)
- description and source-code
```javascript
assertType = function (node, type, param){
  exports.assertPresent(node, param);
  if (node.nodeName == type) return;
  var actual = node.nodeName
    , msg = 'expected '
      + (param ? '"' + param + '" to be a ' :  '')
      + type + ', but got '
      + actual + ':' + node;
  throw new Error('TypeError: ' + msg);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.utils.coerce"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>coerce (val, raw)](#apidoc.element.stylus.utils.coerce)
- description and source-code
```javascript
coerce = function (val, raw){
  switch (typeof val) {
    case 'function':
      return val;
    case 'string':
      return new nodes.String(val);
    case 'boolean':
      return new nodes.Boolean(val);
    case 'number':
      return new nodes.Unit(val);
    default:
      if (null == val) return nodes.null;
      if (Array.isArray(val)) return exports.coerceArray(val, raw);
      if (val.nodeName) return val;
      return exports.coerceObject(val, raw);
  }
}
```
- example usage
```shell
...
 * @param {String} name
 * @param {Function|Node} fn
 * @return {Renderer} for chaining
 * @api public
 */

Renderer.prototype.define = function(name, fn, raw){
fn = utils.coerce(fn, raw);

if (fn.nodeName) {
  this.options.globals[name] = fn;
  return this;
}

// function
...
```

#### <a name="apidoc.element.stylus.utils.coerceArray"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>coerceArray (val, raw)](#apidoc.element.stylus.utils.coerceArray)
- description and source-code
```javascript
coerceArray = function (val, raw){
  var expr = new nodes.Expression;
  val.forEach(function(val){
    expr.push(exports.coerce(val, raw));
  });
  return expr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.utils.coerceObject"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>coerceObject (obj, raw)](#apidoc.element.stylus.utils.coerceObject)
- description and source-code
```javascript
coerceObject = function (obj, raw){
  var node = raw ? new nodes.Object : new nodes.Expression
    , val;

  for (var key in obj) {
    val = exports.coerce(obj[key], raw);
    key = new nodes.Ident(key);
    if (raw) {
      node.set(key, val);
    } else {
      node.push(exports.coerceArray([key, val]));
    }
  }

  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.utils.compileSelectors"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>compileSelectors (arr, leaveHidden)](#apidoc.element.stylus.utils.compileSelectors)
- description and source-code
```javascript
compileSelectors = function (arr, leaveHidden){
  var selectors = []
    , Parser = require('./selector-parser')
    , indent = (this.indent || '')
    , buf = [];

  function parse(selector, buf) {
    var parts = [selector.val]
      , str = new Parser(parts[0], parents, parts).parse().val
      , parents = [];

    if (buf.length) {
      for (var i = 0, len = buf.length; i < len; ++i) {
        parts.push(buf[i]);
        parents.push(str);
        var child = new Parser(buf[i], parents, parts).parse();

        if (child.nested) {
          str += ' ' + child.val;
        } else {
          str = child.val;
        }
      }
    }
    return str.trim();
  }

  function compile(arr, i) {
    if (i) {
      arr[i].forEach(function(selector){
        if (!leaveHidden && selector.isPlaceholder) return;
        if (selector.inherits) {
          buf.unshift(selector.val);
          compile(arr, i - 1);
          buf.shift();
        } else {
          selectors.push(indent + parse(selector, buf));
        }
      });
    } else {
      arr[0].forEach(function(selector){
        if (!leaveHidden && selector.isPlaceholder) return;
        var str = parse(selector, buf);
        if (str) selectors.push(indent + str);
      });
    }
  }

  compile(arr, arr.length - 1);

  // Return the list with unique selectors only
  return exports.uniq(selectors);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.utils.find"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>find (path, paths, ignore)](#apidoc.element.stylus.utils.find)
- description and source-code
```javascript
find = function (path, paths, ignore) {
  var lookup
    , found
    , i = paths.length;

  // Absolute
  if (exports.absolute(path)) {
    if ((found = glob.sync(path)).length) {
      return found;
    }
  }

  // Relative
  while (i--) {
    lookup = join(paths[i], path);
    if (ignore == lookup) continue;
    if ((found = glob.sync(lookup)).length) {
      return found;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.utils.formatException"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>formatException (err, options)](#apidoc.element.stylus.utils.formatException)
- description and source-code
```javascript
formatException = function (err, options){
  var lineno = options.lineno
    , column = options.column
    , filename = options.filename
    , str = options.input
    , context = options.context || 8
    , context = context / 2
    , lines = ('\n' + str).split('\n')
    , start = Math.max(lineno - context, 1)
    , end = Math.min(lines.length, lineno + context)
    , pad = end.toString().length;

  var context = lines.slice(start, end).map(function(line, i){
    var curr = i + start;
    return '   '
      + Array(pad - curr.toString().length + 1).join(' ')
      + curr
      + '| '
      + line
      + (curr == lineno
        ? '\n' + Array(curr.toString().length + 5 + column).join('-') + '^'
        : '');
  }).join('\n');

  err.message = filename
    + ':' + lineno
    + ':' + column
    + '\n' + context
    + '\n\n' + err.message + '\n'
    + (err.stylusStack ? err.stylusStack + '\n' : '');

  // Don't show JS stack trace for Stylus errors
  if (err.fromStylus) err.stack = 'Error: ' + err.message;

  return err;
}
```
- example usage
```shell
...
  if (this.options.sourcemap) this.sourcemap = compiler.map.toJSON();
} catch (err) {
  var options = {};
  options.input = err.input || this.str;
  options.filename = err.filename || this.options.filename;
  options.lineno = err.lineno || parser.lexer.lineno;
  options.column = err.column || parser.lexer.column;
  if (!fn) throw utils.formatException(err, options);
  return fn(utils.formatException(err, options));
}

// fire 'end' event
var listeners = this.listeners('end');
if (fn) listeners.push(fn);
for (var i = 0, len = listeners.length; i < len; i++) {
...
```

#### <a name="apidoc.element.stylus.utils.lookup"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>lookup (path, paths, ignore)](#apidoc.element.stylus.utils.lookup)
- description and source-code
```javascript
lookup = function (path, paths, ignore){
  var lookup
    , i = paths.length;

  // Absolute
  if (exports.absolute(path)) {
    try {
      fs.statSync(path);
      return path;
    } catch (err) {
      // Ignore, continue on
      // to trying relative lookup.
      // Needed for url(/images/foo.png)
      // for example
    }
  }

  // Relative
  while (i--) {
    try {
      lookup = join(paths[i], path);
      if (ignore == lookup) continue;
      fs.statSync(lookup);
      return lookup;
    } catch (err) {
      // Ignore
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.utils.lookupIndex"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>lookupIndex (name, paths, filename)](#apidoc.element.stylus.utils.lookupIndex)
- description and source-code
```javascript
lookupIndex = function (name, paths, filename){
  // foo/index.styl
  var found = exports.find(join(name, 'index.styl'), paths, filename);
  if (!found) {
    // foo/foo.styl
    found = exports.find(join(name, basename(name).replace(/\.styl/i, '') + '.styl'), paths, filename);
  }
  if (!found && !~name.indexOf('node_modules')) {
    // node_modules/foo/.. or node_modules/foo.styl/..
    found = lookupPackage(join('node_modules', name));
  }
  return found;

  function lookupPackage(dir) {
    var pkg = exports.lookup(join(dir, 'package.json'), paths, filename);
    if (!pkg) {
      return /\.styl$/i.test(dir) ? exports.lookupIndex(dir, paths, filename) : lookupPackage(dir + '.styl');
    }
    var main = require(relative(__dirname, pkg)).main;
    if (main) {
      found = exports.find(join(dir, main), paths, filename);
    } else {
      found = exports.lookupIndex(dir, paths, filename);
    }
    return found;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.utils.merge"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>merge (a, b, deep)](#apidoc.element.stylus.utils.merge)
- description and source-code
```javascript
merge = function (a, b, deep) {
  for (var k in b) {
    if (deep && a[k]) {
      var nodeA = exports.unwrap(a[k]).first
        , nodeB = exports.unwrap(b[k]).first;

      if ('object' == nodeA.nodeName && 'object' == nodeB.nodeName) {
        a[k].first.vals = exports.merge(nodeA.vals, nodeB.vals, deep);
      } else {
        a[k] = b[k];
      }
    } else {
      a[k] = b[k];
    }
  }
  return a;
}
```
- example usage
```shell
...
 *
 * @param {String} [filename]
 * @return {Array}
 * @api public
 */

Renderer.prototype.deps = function(filename){
var opts = utils.merge({ cache: false }, this.options);
if (filename) opts.filename = filename;

var DepsResolver = require('./visitor/deps-resolver')
  , parser = new Parser(this.str, opts);

try {
  nodes.filename = opts.filename;
...
```

#### <a name="apidoc.element.stylus.utils.params"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>params (fn)](#apidoc.element.stylus.utils.params)
- description and source-code
```javascript
params = function (fn){
  return fn
    .toString()
    .match(/\(([^)]*)\)/)[1].split(/ *, */);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.utils.parseString"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>parseString (str)](#apidoc.element.stylus.utils.parseString)
- description and source-code
```javascript
parseString = function (str){
  var Parser = require('./parser')
    , parser
    , ret;

  try {
    parser = new Parser(str);
    parser.state.push('expression');
    ret = new nodes.Expression();
    ret.nodes = parser.parse().nodes;
  } catch (e) {
    ret = new nodes.Literal(str);
  }
  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.utils.uniq"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>uniq (arr)](#apidoc.element.stylus.utils.uniq)
- description and source-code
```javascript
uniq = function (arr){
  var obj = {}
    , ret = [];

  for (var i = 0, len = arr.length; i < len; ++i) {
    if (arr[i] in obj) continue;

    obj[arr[i]] = true;
    ret.push(arr[i]);
  }
  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.stylus.utils.unwrap"></a>[function <span class="apidocSignatureSpan">stylus.utils.</span>unwrap (expr)](#apidoc.element.stylus.utils.unwrap)
- description and source-code
```javascript
unwrap = function (expr){
  // explicitly preserve the expression
  if (expr.preserve) return expr;
  if ('arguments' != expr.nodeName && 'expression' != expr.nodeName) return expr;
  if (1 != expr.nodes.length) return expr;
  if ('arguments' != expr.nodes[0].nodeName && 'expression' != expr.nodes[0].nodeName) return expr;
  return exports.unwrap(expr.nodes[0]);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
