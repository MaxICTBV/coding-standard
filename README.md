# 🧑🏼‍🏫 MaxICT Coding Standard

A PHP_CodeSniffer coding standard to be used across MaxICT PHP code bases.


## Installation

To install, run: 

```bash
composer require --dev maxictbv/coding-standard
```

Copy the [`phpcs.xml.dist`](phpcs.xml.dist) file to the root of your project.


## Progressive Application

Most legacy codebases won't play nice with the full coding standard at the
start. Introducing strict typing for example may cause major issues. To avoid
these issues, the following approach can be used. It is a bit tedious, because
unfortunately Codesniffer can only exclude rules (blacklist) and not whitelist:
- Copy the [`phpcs.xml.dist`](phpcs.xml.dist) file to the root of your project.
- Add an [exclusion](https://github.com/squizlabs/PHP_CodeSniffer/wiki/Annotated-Ruleset)
  for every sniff.
- Start removing exclusions one by one until an acceptable set is reached.
- When the codebase improves over time, re-evaluate from time to time if
  more rules can be enabled, and do so if that's the case.
