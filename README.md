# Introduction
This maritime movie catalogue is designed to be used with AI.

It uses a NoSQL / Semi-Structured data framework, which are approaches for storing and organizing data that do not require the rigid table structure used in relational databases. 

NoSQL originally meant “No SQL,” but is now more commonly interpreted as “Not Only SQL,” reflecting the idea that these databases complement rather than replace traditional relational databases. NoSQL databases are designed to handle flexible schemas, large-scale data, high-speed access, distributed computing environments, and complex or evolving data structures that may not fit neatly into fixed tables. 

The JSON format was used for this movie database. Although it is meant to be uploaded to a chatbot and then queried, it can easily converted to a .CSV file using python, and then uploaded into a spreadsheet. 


# Data structure
Each json entry is of the form presented in this example:

```json
{
    "title": "Action in the North Atlantic",
    "year": 1943,
    "watch_link": "https://youtu.be/b30JSlrbpxw?si=PHc1LssQ2DeY8jR0",
    "release_date": "May 21, 1943",
    "studio": "Warner Bros.",
    "director": "Lloyd Bacon",
    "lead_actors": [
      "Humphrey Bogart as Lieutenant Joe Rossi",
      "Raymond Massey as Captain Steve Jarvis",
      "Alan Hale as Boats O'Hara"
    ],
    "awards": [
      "Nominated for Best Writing (Original Story) at the Academy Awards"
    ],
    "music": [
      "Composed by Adolph Deutsch"
    ],
    "maritime_connections": "A World War II film that follows voyage of a liberty ship as they carry supplies from Halifax to Murmansk while facing attacks from German U-boats and planes.",
    "reflection": "This is a promotional movie trying to show that merchant seamen were just as much \"men\" as naval seamen, without disparaging naval seamen. The story itself was good, and the early scene with the sinking of the tanker a useful way of bonding the merchant crew who join together for the next trip like a band of brothers. I'm surprised the writing was nominated for an award, because it was full of tropes. The \"walk inland until someone asks what an oar is\" was old even then, I think. On the other hand, the movie had details that might be overlooked by contemporary set designers and directors, such as towing spars in fog to prevent collisions, and the Russian plane signalling \"V\" for victory by revving his engine in Morse code for \"V.\" ([At 2:04](https://youtu.be/1mx4c0edHiM?si=SVRbTffx4_KthJqp))"
  }
```


# Usage and Idea for prompts

Upload the maritime-movies-2026-05-21.json into your chatbot. 

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
The approach is to edit the maritime-movies-xxxx-xx-xx.json file to establish your own maritime movies database. 
1. Clone this repository or simply download the .json file.
3. Open the .json file in a text editor
4. Paste the new record at the bottom of the file (don't forget the preceding comma), using this template:

```json
{
    "title": "",
    "year": null,
    "watch_link": "",
    "release_date": "",
    "studio": "",
    "director": "",
    "lead_actors": [],
    "awards": [],
    "music": [],
    "maritime_connections": "",
    "reflection": ""
}
```

Most of the keys in the template record are self explanatory. 
1. The value of the key *maritime_connections* is a few sentences explaining why you believe the film is a maritime film.
2. The key  *reflection* is your thoughts about the film and any interesting facts you might want to include.
3. *year* and *release_date* are essentially the same and are there together as a legacy issue.
4. *music* is whatever is interesting, often the composer or music director.

A trick is to paste the blank template into a chatbot along with the name of the movie and have it fill in the key values, then double check them. AI can often writes insightful reflections but it is better to add some of you own thoughts. 
