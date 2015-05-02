# minecraft-data 
[![NPM version](https://badge.fury.io/js/minecraft-data.svg)](http://badge.fury.io/js/minecraft-data) [![Build Status](https://circleci.com/gh/PrismarineJS/minecraft-data.svg?style=shield)](https://circleci.com/gh/PrismarineJS/minecraft-data)

Provide minecraft data for minecraft clients, servers and libraries.

Support minecraft 1.8.3.

## Documentation

 * See [doc/api.md](doc/api.md)
 * See [doc/history.md](doc/history.md)
 * [Documentation generated using the json schemas and docson](http://prismarinejs.github.io/minecraft-data/)
 * [Textual documentation of the recipe format](doc/recipes.md)

## Extractors

Minecraft data provides a few extractors to update the data :

 * bin/wiki_extractor/item_extractor.js extracts items.json from the minecraft wiki
 * bin/wiki_extractor/entities_extractor.js extracts entities.json from the minecraft wiki
 * bin/wiki_extractor/blocks_extractor.js extracts blocks.json from the minecraft wiki
 * manual filling of materials.json : this file is very simple, it is there to make it easier to handle some edge cases
 * manual filling of instruments.json : data coming from http://wiki.vg/Block_Actions
 * bin/wiki_extractor/recipes_extractor.js extracts recipes.json from the minecraft wiki

## Data quality

Minecraft data provides scripts to audit the data, they can be useful to check the data is correct :

 * bin/audit_block_enum.js audits blocks.json : it checks for duplicates names and jumps in ids
 * bin/audit_item_enum.js audits items.json : it checks for duplicates names and jumps in ids
 * bin/audit_recipes.js audits recipes.json : it counts the number of recipes with a shape, without one and with an outShape 
 
Minecraft data also provides json schemas in enums_schemas/ that are used in test/test.js to check the json file are valid relative to these schemas.
These schemas can also be used to understand better how the json files are formatted in order to use it.