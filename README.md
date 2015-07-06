# Sprintify

This script turn your trello cards which represent you story cards with user stories into sprint cards.

## How it Works

The script assumes that your trello card is in a particular format. The description of the card should be in the following form:

```

User Story Title (Points for Story)
---

- Bulleted list of acceptance criteria
- More criteria
- More criteria

Another User Story Title (Points for Story)
---

- Acceptance Criteria
- More criteria
- More criteria

```

The card must be in the above form or weird things may happen. 

When the script is run, the title of the user story is covertered into the title of a sprint card with the acceptance criteria turned into a checklist.

## Installation

To install, clone this repository and run

```
$ bundle install
```



## Usage

In order to use your script you must have the proper API keys. The script will read your api keys from the environment, the following variables must be present for the script to run.

- `DEV_KEY` - represents the developers public key
- `MEMEBER_KEY` - represents the members key

More information about these keys can be found in the gem that make it all possible, [Ruby Trello](https://github.com/jeremytregunna/ruby-trello)

Then run the script using

```
$ ./sprintify
```

and follow the steps as prompted to have you story cards changed into sprint cards.

## Caveats

- Make sure the correct format is in the description of the story cards
- Any dashes in the description (-) will be stripped out so avoid using them unless the represent a markdown bullet point


## Special Thanks

Special thanks to [Jeremy Tregunna](https://github.com/jeremytregunna) for developing the [Ruby Trello](https://github.com/jeremytregunna/ruby-trello) gem which made this super easy.

