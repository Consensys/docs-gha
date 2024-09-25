# Vale

[Vale](https://vale.sh/docs/) is currently WIP for use locally and as GH action. 

## Get started with Vale

https://passo.uno/posts/first-steps-with-the-vale-prose-linter/ provides a decent quickstart (but 
get [install from main docs](https://vale.sh/docs/vale-cli/installation/)).


## Vale commands

Grab the to-date version of a style package referenced in the vale.ini with:

```bash
vale sync
```

> Microsoft is sourced from https://github.com/errata-ai/Microsoft

To run Vale against all relevant files in repo, use:

```bash
vale .
```

Or pass Vale the path to the file you want to lint, e.g. lint this file with:

```bash
vale README.md
```

> For help with Regex expression building use [Regex101](https://regex101.com).

Vale is currently wip. The Vale resources and project-word resources from several sites will
be compiled to this one sot.

## Vale and Yaml?

If API specs are managed as YAML files, need to test whether Vale can handle linting YAMLs.

## ToDo

### Incorporate project-words.txt from repos
[x] Besu
[x] Teku

### Overrides

Attempted to overcome false positives with:

1. /styles/ignore which references the Consensys-common/ignore.txt text file 
2. With styles/Consensys/ProjectWords.yml which is a dummy extend of "existence" to allow use of an exceptions
list





