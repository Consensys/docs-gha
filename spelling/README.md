# Vale

[Vale](https://vale.sh/docs/) may be used from local copy of this repo and as GH action. 

## Set up Vale

https://passo.uno/posts/first-steps-with-the-vale-prose-linter/ provides a decent quickstart (but 
get [install from main docs](https://vale.sh/docs/vale-cli/installation/)).


## Vale commands for local linting

From the spelling directory (where the vale.ini file is held):

1. {Optional} Grab the to-date version of a style package referenced in the vale.ini with:

```bash
vale sync
```

> Microsoft is sourced from https://github.com/errata-ai/Microsoft

2. 

a) To run Vale against all relevant files in repo, use:

```bash
vale .
```

b) Or pass Vale the path to the file you want to lint, e.g. lint this file with:

```bash
vale README.md
```

## Configure Vale

Vale is highly customizable and the boilerplate styles may not be what you need. To override these with Consensys styles, you will probably update one of 3 locations:
1. [project-words](./styles/config/ignore/Consensys-common/project-words.txt)
> [Ignore files are case insensitive](https://vale.sh/docs/topics/styles/#ignoring-non-dictionary-words), but apply all permutations of the term (all cases).
2. [accept](./styles/config/vocabularies/Consensys-common/accept.txt)
3. [reject](./styles/config/vocabularies/Consensys-common/reject.txt)
> [accept and reject use regex](https://vale.sh/docs/topics/vocab/) there is no need to create the reject case forEach accept nor vice versa.

> For help with Regex expression building use [Regex101](https://regex101.com).

Finally, there are more nuanced Consensys-specific styles such as substitutions, acronym overrides, and other configurations in the [Consensys Style folder](./styles/Consensys).

The [vale.ini](vale.ini) file provides various switches to turn styles on and off and to set what file types are formatted. Furthermore, as part of the GHA, the downstream repos that use this can specify which folders Vale may lint.

## ToDo

## Vale and yaml

Vale may need a parser to handle linting YAMLs (e.g., PyYAML, ruyaml). Then Update the .vale.ini file to include the YAML style guide and specify the file extensions to lint.
 
### Incorporate project-words.txt from repos

WARN -- I need to rethink this, GPT failed to compile these without loosing terms
[x] Besu
[x] Teku
[x] Web3Signer
[x] Linea

? Can Josh compile them all

-- started on Linea when discovered the issue

## Test This

title should trigger
ConsenSys should trigger

Should trigger:
With off brand Metamask 
  ′
  ″
zk-EVM
goerli
Goerli

Shouldn't trigger:

booleans
celo
whitelist


