# tree-sitter-mql5

[![CI](https://github.com/mskelton/tree-sitter-mql5/actions/workflows/ci.yml/badge.svg)](https://github.com/mskelton/tree-sitter-mql5/actions/workflows/ci.yml)

MQL5言語のためのtree-sitterパーサーです。

## 概要

このプロジェクトは [tree-sitter-cpp](https://github.com/tree-sitter/tree-sitter-cpp) を拡張し、MQL5の構文をサポートします。

## 使い方

```javascript
const Parser = require('tree-sitter');
const MQL5 = require('tree-sitter-mql5');

const parser = new Parser();
parser.setLanguage(MQL5);

const sourceCode = `
int OnInit()
{
  Print("Hello, world!");
  return(INIT_SUCCEEDED);
}
`;

const tree = parser.parse(sourceCode);
console.log(tree.rootNode.toString());
```
