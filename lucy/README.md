# Lucy

Lucy, a CLI companion for competitive programming on AtCoder and Codeforces, frees you from tedious
tasks. It automatically fetches sample tests, sets up directories, and lets you test your code with
just a few commands, streamlining your workflow and letting you focus on writing brilliant
solutions.

## Support Languages
- [x] C++
- [ ] Python

## Supported Platforms
- [x] AtCoder
- [ ] Codeforces

## Featues
- [x] Fetch Sample Test Cases
- [x] Fetch Hidden Test Cases (after the contest 🤪)
- [x] Test Solution
- [x] Setup Snippets
- [ ] Submit Solution
- [ ] What else? 🤔

## Installation
```
pip install lucy01
```

## Environment Variables
- `LUCY_HOME`

    Specify home directory for `lucy`.

- `DROPBOX_TOKEN`

    Dropbox developer access token with `sharing.read` permission. It can be generated at
    [DBX Platform for Developers](https://www.dropbox.com/developers). This is necessary to fetch
    hidden AtCoder test cases releaved after the contest has ended. All AtCoder test cases may be
    found [here](https://www.dropbox.com/sh/nx3tnilzqz7df8a/AAAYlTq2tiEHl5hsESw6-yfLa?dl=0).

## Getting Started
1. Set the environment variable `$LUCY_HOME` as preferred. By default, it uses the `~/.lucy`.
2. Get help!
    ```
    lucy --help
    ```
    Check out the [documentation]().

## Directory Structure
```
$LUCY_HOME
├── .vscode
│   └── cp.code-snippets*
├── AtCoder
│   └── {ARC177}
│       ├──{A}
│       │   ├── main
│       │   ├── tests
│       │   │   ├── in
│       │   │   │   ├── {00.txt}
│       │   │   │   └── ...
│       │   │   └── out
│       │   │       ├── {00.txt}
│       │   │       └── ...
│       │   └── main.cpp
│       └──...
├── Codeforces
└── common*
    ├── base.cpp*
    ├── structures
    │   ├── grid.cpp
    │   └── ...
    └── ...
```

- Lucy organizes your competitive programming workspace with a clear directory structure. Besides folders for specific contests and their solutions with `tests`, a key element is the `common` directory. This folder stores reusable code snippets `(*.cpp)`. These snippets can be easily inserted into your solution files using filename prefixes thanks to the `cp.code-snippets` file in the `.vscode` folder. This file, automatically generated with `lucy update-snippets`,  facilitates code completion within Visual Studio Code.

  [Using Snippets](https://github.com/kid-116/CP/assets/75692643/3636b6f1-ad58-4bd7-8cb1-2c700f8a5b72)
