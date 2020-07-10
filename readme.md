# Zettelkasten
This is my dedicated and opinionated Zettelkasten, forked/modified from [foambubble/foam](https://github.com/foambubble/foam).

![](_images/2020-07-08-14-22-07.png)

_Information vs. Knowledge (by @gapingvoid)_

## concepts
Zettelkasten is German for “slip-box”. It originates from German sociologist Niklas Luhmann.

- Some key ideas in a literature note are converted into a permanent note
- Connections made via relevant notes and #topic tags
- [ ] add other concept practices as features on [roadmap](https://foambubble.github.io/foam/roadmap) is completed

---
## organization

### template
```
title of some research or notes
    - literature note
    - tags: #data #recon #intelligence #riots #covid19 #Boltzmann (if permanent note)
    - source: [[source]] or url://
    
    - simplified intro stating purpose, interest, topic of discussion
        - metadata
    
    - relevant notes
    
    - summary
    
    - [[linkageToAnotherZettel]]
        - metadata
references
```

### types
All types of documents, topics or notes qualify to be a '`zettel`', some are detailed below.

### literature note
Every book, document, article, whitepaper, research I read will be added as a literature note, with some metadata:

- a tag for the `#literature note`
- a source (title, URL, etc)
- author and|or field of research or domain

### permanent note
To create a permanent note, surround the string in `[[ ]]` brackets, with some metadata:

- a tag for the `#permanent note`
- topic tags like `#awesome`, `#python`, `#infra`
- source link to literature being read
- Relevant permanent notes and a short explanation of how it is relevant
- Summary of the idea in prose
- backlinking
  - this linkage is like Wiki Links, to link pages together using annotations

### todo
Keeping track of loose-tasks or ideas for the project. This `- [ ]` can be added anywhere you need a checkbox.
- [ ] if you need a checkbox like this
