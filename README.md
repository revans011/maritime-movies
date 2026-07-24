# Introduction
This maritime movie catalogue is designed to be used with AI.

It uses a NoSQL / Semi-Structured data framework, which are approaches for storing and organizing data that do not require the rigid table structure used in relational databases. 

NoSQL originally meant “No SQL,” but is now more commonly interpreted as “Not Only SQL,” reflecting the idea that these databases complement rather than replace traditional relational databases. NoSQL databases are designed to handle flexible schemas, large-scale data, high-speed access, distributed computing environments, and complex or evolving data structures that may not fit neatly into fixed tables. 

The JSON format was used for this movie database. Although it is meant to be uploaded to a chatbot and then queried, it can easily converted to a .CSV file using python, and then uploaded into a spreadsheet. 


# Data structure
Each json entry is of the form presented in this example:

```json
{
"id": "action-in-the-north-atlantic-1943",
  "title": "Action in the North Atlantic",
  "original_title": "Action in the North Atlantic",
  "year": 1943,
  "release_date": "1943-05-21",
  "release_date_notes": null,
  "film_type": "Feature film",
  "runtime_minutes": 126,
  "countries": [
    "United States of America"
  ],
  "languages": [
    "German",
    "English"
  ],
  "studios": [
    "Warner Bros.",
    "Warner Bros. Pictures"
  ],
  "directors": [
    "Lloyd Bacon",
    "Byron Haskin",
    "Raoul Walsh"
  ],
  "writers": [
    "John Howard Lawson",
    "Guy Gilpatric",
    "A.I. Bezzerides",
    "W.R. Burnett"
  ],
  "cast": [
    {
      "actor": "Humphrey Bogart",
      "character": "Lieutenant Joe Rossi",
      "original_text": "Humphrey Bogart as Lieutenant Joe Rossi"
    },
    {
      "actor": "Raymond Massey",
      "character": "Captain Steve Jarvis",
      "original_text": "Raymond Massey as Captain Steve Jarvis"
    },
    {
      "actor": "Alan Hale",
      "character": "Boats O'Hara",
      "original_text": "Alan Hale as Boats O'Hara"
    },
    {
      "actor": "Julie Bishop",
      "character": "Pearl O'Neill",
      "original_text": "Julie Bishop as Pearl O'Neill"
    },
    {
      "actor": "Ruth Gordon",
      "character": "Mrs. Sarah Jarvis",
      "original_text": "Ruth Gordon as Mrs. Sarah Jarvis"
    },
    {
      "actor": "Sam Levene",
      "character": "Abel 'Chips' Abrams",
      "original_text": "Sam Levene as Abel 'Chips' Abrams"
    },
    {
      "actor": "Dane Clark",
      "character": "Johnnie Pulaski",
      "original_text": "Dane Clark as Johnnie Pulaski"
    },
    {
      "actor": "Peter Whitney",
      "character": "Whitey Lara",
      "original_text": "Peter Whitney as Whitey Lara"
    },
    {
      "actor": "Dick Hogan",
      "character": "Cadet Ezra Parker",
      "original_text": "Dick Hogan as Cadet Ezra Parker"
    },
    {
      "actor": "Virginia Christine",
      "character": "Pebbles",
      "original_text": "Virginia Christine as Pebbles"
    },
    {
      "actor": "Louis Adlon",
      "character": "German Ensign (uncredited)",
      "original_text": "Louis Adlon as German Ensign (uncredited)"
    },
    {
      "actor": "Iris Adrian",
      "character": "Jenny O'Hara (uncredited)",
      "original_text": "Iris Adrian as Jenny O'Hara (uncredited)"
    },
    {
      "actor": "Frank Alten",
      "character": "German (uncredited)",
      "original_text": "Frank Alten as German (uncredited)"
    },
    {
      "actor": "Kirk Alyn",
      "character": "Brazilian Gun Captain (uncredited)",
      "original_text": "Kirk Alyn as Brazilian Gun Captain (uncredited)"
    },
    {
      "actor": "C.E. Anderson",
      "character": "Bearded Lieutenant Commander (uncredited)",
      "original_text": "C.E. Anderson as Bearded Lieutenant Commander (uncredited)"
    },
    {
      "actor": "Tod Andrews",
      "character": "Ahearn (uncredited)",
      "original_text": "Tod Andrews as Ahearn (uncredited)"
    }
  ],
  "genres": [
    "Drama",
    "War"
  ],
  "historical_periods": [
    "World War II",
    "Contemporary period"
  ],
  "historical_figures": [],
  "maritime_categories": [
    "Maritime disaster",
    "Submarine operations"
  ],
  "maritime_topics": [],
  "vessels": [],
  "bodies_of_water": [],
  "ports_and_locations": [],
  "maritime_occupations": [],
  "based_on": {
    "type": null,
    "title": null,
    "author": null
  },
  "music": {
    "composers": [],
    "songs_or_themes": [],
    "notes": [
      "Composed by Adolph Deutsch"
    ]
  },
  "awards": [
    {
      "organization": null,
      "ceremony": null,
      "year": null,
      "category": null,
      "recipient": null,
      "result": "Nominated",
      "original_text": "Nominated for Best Writing (Original Story) at the Academy Awards"
    }
  ],
  "watch_links": [
    {
      "url": "https://youtu.be/b30JSlrbpxw?si=PHc1LssQ2DeY8jR0",
      "platform": null,
      "notes": null
    }
  ],
  "maritime_connections": "A World War II film that follows voyage of a liberty ship as they carry supplies from Halifax to Murmansk while facing attacks from German U-boats and planes.",
  "reflection": "This is a promotional movie trying to show that merchant seamen were just as much \"men\" as naval seamen, without disparaging naval seamen. The story itself was good, and the early scene with the sinking of the tanker a useful way of bonding the merchant crew who join together for the next trip like a band of brothers. I'm surprised the writing was nominated for an award, because it was full of tropes. The \"walk inland until someone asks what an oar is\" was old even then, I think. On the other hand, the movie had details that might be overlooked by contemporary set designers and directors, such as towing spars in fog to prevent collisions, and the Russian plane signalling \"V\" for victory by revving his engine in Morse code for \"V.\" ([At 2:04](https://youtu.be/1mx4c0edHiM?si=SVRbTffx4_KthJqp))",
  "review_notes": []
  }
```


# Usage and Idea for prompts

Upload the maritime_films.json into your chatbot. 

## Casual Queries

1. List all the submarine films in the database.
2. Which films are from the 1940s?
3. What films did John Ford direct?
4. Who are the most frequently appearing actors across the database?
5. What studios produced the most maritime films?

## Analytical Queries

1. Organize the films by maritime subgenre (submarine warfare, naval battle, merchant marine,
   sailing/age of sail, etc.) and list the titles under each category.
2. Give me a chronological tour of the database by decade, identifying one or two representative
   or standout films from each era and noting how the maritime themes evolved over time.
3. Which films deal with the tension between individual survival and collective duty at sea?
4. Are there patterns in which studios or directors returned repeatedly to maritime themes?
5. How does the representation of the enemy change across the World War II films in the database —
   from early wartime productions to postwar retrospectives?

# Adding movies

## Method One

The approach is to edit the maritime-films.json file to establish your own maritime movies database. 
1. Clone this repository or simply download the .json file.
3. Open the .json file in a text editor
4. Paste the new record at the bottom of the file (don't forget the preceding comma), using this template:

```json
{
  "id": "[String: e.g., film-title-year]",
  "title": "[String]",
  "original_title": "[String or null]",
  "year": [Integer],
  "release_date": "[String: YYYY-MM-DD or null]",
  "release_date_notes": "[String or null]",
  "film_type": "[String]",
  "runtime_minutes": [Integer or null],
  "countries": [
    "[String]"
  ],
  "languages": [
    "[String]"
  ],
  "studios": [
    "[String]"
  ],
  "directors": [
    "[String]"
  ],
  "writers": [
    "[String]"
  ],
  "cast": [
    {
      "actor": "[String or null]",
      "character": "[String or null]",
      "original_text": "[String]"
    }
  ],
  "genres": [
    "[String]"
  ],
  "historical_periods": [
    "[String]"
  ],
  "historical_figures": [
    "[String]"
  ],
  "maritime_categories": [
    "[String]"
  ],
  "maritime_topics": [
    "[String]"
  ],
  "vessels": [
    {
      "name": "[String or null]",
      "type": "[String or null]",
      "fictional": [Boolean or null],
      "original_text": "[String or null]"
    }
  ],
  "bodies_of_water": [
    "[String]"
  ],
  "ports_and_locations": [
    "[String]"
  ],
  "maritime_occupations": [
    "[String]"
  ],
  "based_on": {
    "type": "[String or null]",
    "title": "[String or null]",
    "author": "[String or null]"
  },
  "music": {
    "composers": [
      "[String]"
    ],
    "songs_or_themes": [
      "[String]"
    ],
    "notes": [
      "[String]"
    ]
  },
  "awards": [
    {
      "organization": "[String or null]",
      "ceremony": "[String or null]",
      "year": [Integer or null],
      "category": "[String or null]",
      "recipient": "[String or null]",
      "result": "[String or null]",
      "original_text": "[String]"
    }
  ],
  "watch_links": [
    {
      "url": "[String: URL]",
      "platform": "[String or null]",
      "notes": "[String or null]"
    }
  ],
  "maritime_connections": "[String or null]",
  "reflection": "[String or null]",
  "review_notes": [
    "[String]"
  ]
}
```

## Method Two

The approach is to lot AI edit the maritime-films.json file. 
1. Clone this repository or simply download the .json file.
2. Upload the maritime-films.json file into a chatbot and then paste the blank template into a chatbot along with the name of the movie and have it fill in the key values, then double check them. AI can often writes insightful reflections but it is better to add some of you own thoughts. 
3. Have AI merge your completed template and the maritime-films.json
