# Deno

Originally, JavaScript was meant to run in the web browser. This is
still the case today. Unlike other programming languages, most
JavaScript programs are not executed from the command-line. Rather, it
is the web browser's responsibility to interpret the source code.

Since 2010, several other runtime environments have become available.
Instead of limiting JavaScript to the browser, platforms such as Node,
Deno, and Bun allow access to the entire operating system, thus enabling
JavaScript programs to be executed from the command-line.

Since this course focuses on client-side programming, one might assume
that all our programs will target the browser. While that is mostly
true, it is sometimes useful — especially at the beggining — to run
programs in a simpler environment. When that is necessary, we will use
[Deno] (pronounced "dino" like "dinosaur").

The creators of Deno are the same as those of Node, the first JavaScript
runtime environment outside the web browser. Although Node is more
popular today, Deno is used in this course because it can run TypeScript
natively, and includes all the tooling necessary for writing a program:
formater, linter, test framework, etc. Moreover, unlike Node, Deno uses
the same standardized interfaces as web browsers, which means that, with
few exceptions, a program can be executed both in a web browser and with
Deno.

[Deno]: https://deno.com

## Installation

The simplest way to install Deno is to use a package manager. [Scoop] is
recommended for those on Windows, and [Homebrew] for those on Mac. On
Linux, it depends on your distribution.

Windows :

```sh
scoop install deno
```

Mac :

```sh
brew install deno
```

[Scoop]: https://scoop.sh
[Homebrew]: https://brew.sh

## Usage

To run a TypeScript program with Deno, execute the following command in
your terminal:

```sh
deno run --check <filename>
```

The `--check` flag tells Deno to type check your code.

You may also add the `--watch` flag if you want Deno to run your code
everytime you save.

```sh
deno run --check --watch <filename>
```

## Configuration file

Most programming tools allows the use of configuration files to
customize how they work. These files may be in different formats: JSON,
TOML, YAML, to name a few.

In Deno's case, the configuration file is named `deno.json`. Adding this
file at the root of your project allows you to configure how Deno
formats the source code, how strict is the type checker, which warnings
to display, and so on.

To make sure a program's source code is consistant, team members use the
same settings, and so share the same configuration file. You will find
included in this directory the `deno.json` file to use for this course.
Make sure to include a copy in every projects.
