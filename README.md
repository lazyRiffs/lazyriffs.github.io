
# Table of Contents

1.  [Lux Notes](#orgdb6f240)
    1.  [Components](#org8b012a6)
        1.  [Headers](#orgd364e6b)
        2.  [Raw text](#org9dc6add)
        3.  [Links](#org7a2b9e2)
    2.  [File Types](#orgb3a6448)


<a id="orgdb6f240"></a>

# Lux Notes

Lux Notes is a system for organizing information. It is an attempt to capture chunks of information in a modular way that can be composed as needed.

The basic structure is:

1.  There is one root directory per project
2.  The root directory contains a .lxn directory (for lux-notes), akin to the .git directory
3.  The .lxn directory contains an index of the whole project.
4.  There can be nested .lxn directories within the root to make more specific modifications to a given subdirectory


<a id="org8b012a6"></a>

## Components

There are three components available in a notefile:

1.  Headers
2.  Raw text
3.  Links


<a id="orgd364e6b"></a>

### Headers

A header marks a discrete information container. The value of the header is the name for that container.

Additionally, a header can have "Properties" associated to it. These properties are key-value pairs. Any header that has the line-kind-name triplet is considered a proper Note and will get its own file.


<a id="org9dc6add"></a>

### Raw text

The majority of notes are simple raw text. There's nothing special here. The first flavor to be added will be the '[time] [\(|%|&] [value]' structure which denotes a journal entry. (Any timestamped entry is considered a journal entry.) (I'm still up in the air on whether I really want to complicate that leader-separator character by allowing '\)' or '%' or '&' &#x2013; like, that could mean something if I wanted, but I have no real use at the moment.


<a id="org7a2b9e2"></a>

### Links

Links are how Lux Notes achieves multidimensional, modular text editing. A link creates an entry in the current directories .index file, with meaningful information. The simplest link is an href-style hyperlink that takes you to another file, like any old anchor tag on the web.

You can also use links for various other purposes, to be defined as I build this out better.

In essence, a link is more than a pointer to another file. Lux Notes Links add a layer of indirection in a third file, the common entry in the .index files in the source and target directories. If the link is to another file within the exact same directory, then there are two entries in the index file.


<a id="orgb3a6448"></a>

## File Types

There are several file types available. In the general abstract, each chunk of information exists as its own interconnected, multidimensional node in the context of its semantic web. But in practice, we need to store these ethereal nodes of information in physical disk space as a file. So, a file is a representation of some abstract chunk of information that is embedded within a given semantic web.

The file types are:

1.  Single note
    1.  This type of file is one note with the root, level-1 header as the name of the entire note. There are no embedded notes here. But you can have any variety of links in your note.
2.  Multi Note
    1.  This type of file has multiple notes within it. It can either be or not be a proper note itself.
    2.  If it is no more than an arrangement of other notes, then it is a Multi Note (Pure) and if it is a note itself with linked notes contained inside of it, then it is a Multi Note (mixed)
3.  Index Note
    1.  This type of file is a special Muti Note (pure) that is used to describe a group of notes.

Note: #3 is just an idea, and I have no idea what that actually means. Just that I like the idea of having one special type of Multi Note I guess.

