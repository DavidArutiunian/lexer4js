# Lexer4JS

[![npm](https://img.shields.io/npm/dt/lexer4js.svg)](https://www.npmjs.com/package/lexer4js)
[![npm version](https://badge.fury.io/js/lexer4js.svg)](https://badge.fury.io/js/lexer4js)
[![David](https://img.shields.io/david/DavidArutiunian/lexer4js.svg)](https://github.com/DavidArutiunian/lexer4js)
[![npm bundle size (minified + gzip)](https://img.shields.io/bundlephobia/minzip/lexer4js.svg)](https://www.npmjs.com/package/lexer4js)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat)](https://github.com/prettier/prettier)
![Snyk Vulnerabilities for GitHub Repo](https://img.shields.io/snyk/vulnerabilities/github/DavidArutiunian/lexer4js.svg)
![GitHub top language](https://img.shields.io/github/languages/top/DavidArutiunian/lexer4js.svg)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/DavidArutiunian/lexer4js.svg)
![GitHub last commit](https://img.shields.io/github/last-commit/DavidArutiunian/lexer4js.svg)
[![TLOC](https://tokei.rs/b1/github/DavidArutiunian/lexer4js)](https://github.com/DavidArutiunian/lexer4js)
![Node.js CI](https://github.com/DavidArutiunian/lexer4js/workflows/Node.js%20CI/badge.svg)
![CodeQL](https://github.com/DavidArutiunian/lexer4js/workflows/CodeQL/badge.svg)

## 🚀 Using lexer

Pass the source code to the `tokenize(source)` method like this

```js
import { Lexer } from "lexer4js";

const source = fs.readFileSync("source.txt", "utf8");

const lexer = new Lexer();
const tokens = lexer.tokenize(source);
```

You would get list of tokens. Calling `.toString()` method of `Token` will result in such output

```js
tokens.forEach((token) => console.log(token.toString()));
```

```
CLASS 'class' [L1:0]
IDENTIFIER 'Foo' [L1:6]
OPENING_CURLY_BRACE '{' [L1:10]
PRIVATE 'private' [L2:4]
DOUBLE 'double' [L2:12]
IDENTIFIER 'big' [L2:19]
ASSIGNMENT '=' [L2:23]
SCIENTIFIC_LITERAL '3.2e+23' [L2:25]
SEMICOLON ';' [L2:32]
PRIVATE 'private' [L3:4]
DOUBLE 'double' [L3:12]
IDENTIFIER 'small' [L3:19]
ASSIGNMENT '=' [L3:25]
SUBTRACTION '-' [L3:27]
SCIENTIFIC_LITERAL '4.70e-9' [L3:28]
SEMICOLON ';' [L3:35]
PRIVATE 'private' [L5:4]
IDENTIFIER 'String' [L5:12]
IDENTIFIER 'message' [L5:19]
ASSIGNMENT '=' [L5:27]
STRING_LITERAL '"FooBarBaz"' [L5:29]
SEMICOLON ';' [L5:40]
PRIVATE 'private' [L6:4]
IDENTIFIER 'char' [L6:12]
IDENTIFIER 'newline' [L6:17]
ASSIGNMENT '=' [L6:25]
CHAR_LITERAL ''\n'' [L6:27]
SEMICOLON ';' [L6:31]
PRIVATE 'private' [L8:4]
INT 'int' [L8:12]
IDENTIFIER 'hex' [L8:16]
ASSIGNMENT '=' [L8:20]
HEX_LITERAL '0x0A0B0C' [L8:22]
SEMICOLON ';' [L8:30]
PRIVATE 'private' [L9:4]
INT 'int' [L9:12]
IDENTIFIER 'octal' [L9:16]
ASSIGNMENT '=' [L9:22]
OCTAL_LITERAL '0737' [L9:24]
SEMICOLON ';' [L9:28]
PRIVATE 'private' [L10:4]
INT 'int' [L10:12]
IDENTIFIER 'binary' [L10:16]
ASSIGNMENT '=' [L10:23]
BINARY_LITERAL '0b01001001110' [L10:25]
SEMICOLON ';' [L10:38]
PRIVATE 'private' [L12:4]
BOOLEAN 'boolean' [L12:12]
IDENTIFIER 'flag' [L12:20]
ASSIGNMENT '=' [L12:25]
FALSE 'false' [L12:27]
SEMICOLON ';' [L12:32]
PRIVATE 'private' [L14:4]
IDENTIFIER 'String' [L14:12]
IDENTIFIER 'multiline' [L14:19]
ASSIGNMENT '=' [L14:29]
MULTILINE_STRING_LITERAL '"""
        Hello, World!
        Who I am?
    """' [L14:31]
SEMICOLON ';' [L17:7]
PUBLIC 'public' [L23:4]
VOID 'void' [L23:11]
IDENTIFIER 'main' [L23:16]
OPENING_BRACE '(' [L23:20]
IDENTIFIER 'String' [L23:21]
OPENING_SQUARE_BRACE '[' [L23:27]
CLOSING_SQUARE_BRACE ']' [L23:28]
IDENTIFIER 'args' [L23:30]
CLOSING_BRACE ')' [L23:34]
OPENING_CURLY_BRACE '{' [L23:36]
INT 'int' [L24:8]
IDENTIFIER 'size' [L24:12]
ASSIGNMENT '=' [L24:17]
INT_LITERAL '3' [L24:19]
SEMICOLON ';' [L24:20]
INT 'int' [L25:8]
OPENING_SQUARE_BRACE '[' [L25:12]
IDENTIFIER 'size' [L25:13]
CLOSING_SQUARE_BRACE ']' [L25:17]
IDENTIFIER 'array' [L25:19]
ASSIGNMENT '=' [L25:25]
OPENING_CURLY_BRACE '{' [L25:27]
INT_LITERAL '1' [L25:29]
COMMA ',' [L25:30]
INT_LITERAL '2' [L25:32]
COMMA ',' [L25:33]
INT_LITERAL '3' [L25:35]
CLOSING_CURLY_BRACE '}' [L25:37]
SEMICOLON ';' [L25:38]
INT 'int' [L26:8]
IDENTIFIER 'index' [L26:12]
ASSIGNMENT '=' [L26:18]
INT_LITERAL '0' [L26:20]
SEMICOLON ';' [L26:21]
FLOAT 'float' [L27:8]
IDENTIFIER 'e' [L27:14]
ASSIGNMENT '=' [L27:16]
DOUBLE_LITERAL '2.73' [L27:18]
SEMICOLON ';' [L27:22]
WHILE 'while' [L28:8]
OPENING_BRACE '(' [L28:14]
IDENTIFIER 'index' [L28:15]
NOT_EQUALS '!=' [L28:21]
INT_LITERAL '0' [L28:24]
CLOSING_BRACE ')' [L28:25]
OPENING_CURLY_BRACE '{' [L28:27]
IDENTIFIER 'index' [L29:12]
ASSIGNMENT '=' [L29:18]
IDENTIFIER 'index' [L29:20]
SUBTRACTION '-' [L29:26]
INT_LITERAL '1' [L29:28]
SEMICOLON ';' [L29:29]
IDENTIFIER 'var' [L30:12]
IDENTIFIER 'coefficient' [L30:16]
ASSIGNMENT '=' [L30:28]
IDENTIFIER 'big' [L30:30]
MULTIPLICATION '*' [L30:34]
IDENTIFIER 'small' [L30:36]
DIVISION '/' [L30:42]
IDENTIFIER 'hex' [L30:44]
SEMICOLON ';' [L30:47]
IDENTIFIER 'println' [L31:12]
OPENING_BRACE '(' [L31:19]
IDENTIFIER 'message' [L31:20]
COMMA ',' [L31:27]
IDENTIFIER 'array' [L31:29]
OPENING_SQUARE_BRACE '[' [L31:34]
IDENTIFIER 'index' [L31:35]
CLOSING_SQUARE_BRACE ']' [L31:40]
MULTIPLICATION '*' [L31:42]
IDENTIFIER 'coefficient' [L31:44]
COMMA ',' [L31:55]
IDENTIFIER 'newline' [L31:57]
CLOSING_BRACE ')' [L31:64]
SEMICOLON ';' [L31:65]
CLOSING_CURLY_BRACE '}' [L32:8]
FOR 'for' [L33:8]
OPENING_BRACE '(' [L33:12]
IDENTIFIER 'var' [L33:13]
IDENTIFIER 'num' [L33:17]
COLON ':' [L33:21]
IDENTIFIER 'array' [L33:23]
CLOSING_BRACE ')' [L33:28]
OPENING_CURLY_BRACE '{' [L33:30]
IDENTIFIER 'var' [L34:12]
IDENTIFIER 'coefficient' [L34:16]
ASSIGNMENT '=' [L34:28]
IDENTIFIER 'big' [L34:30]
MULTIPLICATION '*' [L34:34]
IDENTIFIER 'small' [L34:36]
DIVISION '/' [L34:42]
IDENTIFIER 'hex' [L34:44]
SEMICOLON ';' [L34:47]
IDENTIFIER 'println' [L35:12]
OPENING_BRACE '(' [L35:19]
IDENTIFIER 'message' [L35:20]
COMMA ',' [L35:27]
IDENTIFIER 'num' [L35:29]
MULTIPLICATION '*' [L35:33]
IDENTIFIER 'coefficient' [L35:35]
COMMA ',' [L35:46]
IDENTIFIER 'newline' [L35:48]
CLOSING_BRACE ')' [L35:55]
SEMICOLON ';' [L35:56]
CLOSING_CURLY_BRACE '}' [L36:8]
IDENTIFIER 'var' [L37:8]
IDENTIFIER 'secret' [L37:12]
ASSIGNMENT '=' [L37:19]
IDENTIFIER 'hex' [L37:21]
XOR '^' [L37:25]
IDENTIFIER 'octal' [L37:27]
XOR '^' [L37:33]
IDENTIFIER 'binary' [L37:35]
SEMICOLON ';' [L37:41]
IDENTIFIER 'println' [L38:8]
OPENING_BRACE '(' [L38:15]
IDENTIFIER 'secret' [L38:16]
CLOSING_BRACE ')' [L38:22]
SEMICOLON ';' [L38:23]
CLOSING_CURLY_BRACE '}' [L39:4]
CLOSING_CURLY_BRACE '}' [L40:0]
```
