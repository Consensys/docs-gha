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

## Testing Vale Here

This heading should trigger warning for non-compliance with sentence case. Metamask should upset 
Vale too.

## ToDo

### Linea

1. We seem to be using proper noun for Coordinator but not for prover
2. Proper Linea Voyage

### General
2. Will links be false positives, e.g. Can linting for " CLI" work to avoid false positives for links?
3. Can we use reject [here to prevent links being put in this format, is it covered another way?

### Testing

Removed this from Vale ini to try and just get Microsoft working

# Style.Rule = {YES, NO} to enable or disable a specific rule
Microsoft.Contractions = warning

Microsoft.GeneralURL = NO

# Microsoft.Acronyms is replaced by Consensys list
Microsoft.Acronyms = NO

# Microsoft.Avoid is not relevant
Microsoft.Avoid = NO

Microsoft.Headings = YES

write-good.Weasel = NO

proselint.Hyperbole = warning