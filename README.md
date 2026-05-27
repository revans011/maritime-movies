# Introduction
This maritime movie catalogue is designed to be used with AI.

It uses a NoSQL / Semi-Structured data framework, which are approaches for storing and organizing data that do not require the rigid table structure used in relational databases. 

NoSQL originally meant “No SQL,” but is now more commonly interpreted as “Not Only SQL,” reflecting the idea that these databases complement rather than replace traditional relational databases. NoSQL databases are designed to handle flexible schemas, large-scale data, high-speed access, distributed computing environments, and complex or evolving data structures that may not fit neatly into fixed tables. 

NoSQL systems generally fall into four categories, with the **document model** being one of the most common forms of semi-structured data storage. In document databases, data are stored as self-contained documents, usually in a JSON-like format, allowing information to be nested and vary from one record to another. For example, a patient record may include an embedded list of clinical visits and measurements within a single document rather than requiring multiple linked tables. 

Document databases are commonly used for clinical records, user profiles, configuration files, and omics metadata. Popular examples include MongoDB and CouchDB. Their primary strengths are schema flexibility, natural handling of nested data, and straightforward integration with JSON-based applications. However, these advantages come with trade-offs, including more difficult joins between records and less rigid enforcement of data integrity compared with traditional relational databases.


## Data structure
Each json entry is of the form

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

### Sub-subsection 1.1.1
More text.

# Usage
Text here.

# Adding movies
The approach is to edit the maritime-movies.json file to establish your own maritime movies database. 
1. Clone this repository or simply download the .json file.
3. Open the .json file in a text editor
4. Paste the new
