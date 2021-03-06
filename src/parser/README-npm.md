# The flow-parser package

This package contains the Flow parser in its compiled-to-JavaScript form.

# What is Flow

See [flowtype.org](http://flowtype.org/). The code for the Flow parser [lives on GitHub](https://github.com/facebook/flow/tree/master/src/parser).

# What is the Flow Parser

The Flow Parser is a JavaScript parser written in OCaml. It produces an AST that conforms to the [ESTree spec](https://github.com/estree/estree) and that mostly matches what [esprima](http://esprima.org/) produces. The Flow Parser can be compiled to native code or can be compiled to JavaScript using [js_of_ocaml](http://ocsigen.org/js_of_ocaml/). This npm package contains the Flow parser compiled to JavaScript.

# Usage

You can use the Flow parser in your browser or in node. To use in node you can just do

```JavaScript
require('flow-parser').parse('1+1');
```

To use in the browser, you can add

```HTML
<script src="flow_parser.js"></script>
```

which will make the `flow` object available to use like so:

```JavaScript
flow.parse('1+1');
```

# bin scripts

* `flowparse` - Pass it a string to parse or a file to parse and it dumps the AST to stdout
* `flowvalidate` - Pass it one or more files and it checks if they parse

