# Documentation for Sri Lanka Elections Commission Software

The Elections Commission is an elections-as-a-service organization, with the people and government of Sri Lanka being their primary customer. Currently, the EC is operating only with that customer but the long term objective of the software is to make it possible to operate any election with varying rules for the electors, candidates, voting technology, results process and so on. 

Give the current priorities, getting the software to that level is not the immediate task (as of November 2018).

This repository contains various documents for the software starting with design docs to user level docs.

## Terminology

* Elector - a person eligible to vote
* Voter - someone who votes in an election

## Functionality

The functionality of elections software can be categorized into 3 distinct phases: Pre-election, during an election and post-election. 

| Pre-election Period | During Election     | Post-election Period |
| ---                 | ---                 | ---                  |
| Register electors   | Create an election  |  Publish analytics   |
| Address complaints  | Manage election operations |  Address complaints  |
|                     | Nominate candidates |                      |
|                     | Run voting process  |                      |
|                     | Count votes         |                      |
|                     | Publish results     |                      |
|                     | Address complaints  |                      |

More information about each of these items will be included in various subsystem documents.

## Architecture

See the ![architecture directory](architecture/) for more information.