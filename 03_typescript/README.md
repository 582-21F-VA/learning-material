# TypeScript

There are those who will say terrible things about JavaScript. Many of
these things are true. JavaScript is ridiculously liberal in what it
allows. The idea behind this design was that it would make programming
in JavaScript easier for beginners. In actuality, it mostly makes
finding problems in your programs harder because the system will not
point them out to you.

For this reason, TypeScript is generally preferred over JavaScript for
large-scale projects. TypeScript is a syntactic superset of JavaScript
that adds static type checking, which is the process of verifying type
errors before a program is run. In JavaScript, calling a function with
an argument of an incorrect type (say, a string instead of a number)
will throw an error only when that function is executed by the browser.
In TypeScript, the error will appear in your text editor, making it
easier for you to fix it.

TypeScript makes code easier to read, understand, and debug. That is why
we will be using it in this course. Do not worry, however, for almost
everything you will learn in TypeScript can be transfered to JavaScript.
In a sense, you are learning two languages for the price of one. Apart
from their type system, they are functionnaly identical. In fact, any
valid JavaScript code is also valid TypeScript code.

> [!Note]\
> The lecture notes will refer explicitely to TypeScript when a concept
> or feature is not transferable to JavaScript.

## Installation

The main downside of TypeScript is that it you cannot execute TypeScript
code in the browser like you can with JavaScript. A TypeScript program
must be _compiled_ (or translated) into JavaScript before it can run in
a web browser.

This step is not necessary when you run your program from the
command-line in an environment that natively support TypeScript, such as
Deno. However, if you intend on running your code in a web browser, you
must use the TypeScript compiler beforehand to translate your program
into JavaScript.

The simplest way to install the TypeScript compiler is to use a package
manager. [Scoop] is recommended for those on Windows, and [Homebrew] for
those on Mac. On Linux, it depends on your distribution.

Windows :

```sh
scoop install nodejs
npm install -g typescript
```

Mac :

```sh
brew install typescript
```

[Scoop]: https://scoop.sh
[Homebrew]: https://brew.sh

## Usage

To compile a TypeScript program into JavaScript, run the following
command from the root of your project:

```sh
tsc -w
```

The `-w` flag tells the compiler to watch all your TypeScript files, and
translate them to JavaScript when one changes. You only need to execute
this command once at the start of your working session.

The TypeScript compiler can be more or less strict depending on how it
is configured. You will find a `tsconfig.json` file in this directory
which includes the settings we will use in this course. When you use the
TypeScript compiler, ake sure to include a copy of the file at the root
of your program.
