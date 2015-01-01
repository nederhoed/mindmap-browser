mindmap-browser
===============

A mindmap browser loosely based on Topic Map theory. A mindmap is just one view on some knowledge. What you would want is a web of mindmaps, based on the underlying knowledge.

To realise this, we separate knowledge and visualization. We model the knowledge using a system based on Topic Map theory. Then we browse through the knowledge using a dynamic visualization of parts of the knowledge.

Topic Maps theory offers 3 types of information: Topics, Associations and Occurences. We define knowledge in these terms.

### An example: The Simpson family
Let's model a family and visualize some possible mindmaps for this family. To keep it simple, we will start with Marge, Homer, Bart and Lisa.

Topics: Marge, Homer, Bart, Lisa, Saxophone

Associations: 
* "Marge is married to Homer"
* "Homer is married to Marge"
* "Bart is Lisa's brother"
* "Lisa is Bart's sister"
* "Marge is Lisa's parent"
* "Homer is Lisa's parent"
* "Lisa plays Saxophone"

Occurences:
* https://www.youtube.com/watch?v=OFoW6fa79xA (Lisa playing Saxophone)

Topic types: "cartoon character", "musical instrument"

Association types: (which are topics themselves)
* "is married to"
* "plays musical instrument"
* "is parent of"
* etc.

Occurence types: "video"

Keep in mind that the goal is to make the family browsable. We're not focussing on a reasoning engine. 

## Datamodel

### Topic
* id
* title ("cartoon character")

### Association (one direction)
* id
* tm_type ("is married to")
* agent ("Marge")
* object ("Homer")

### Occurence
* id
* tm_type ("video")
* title ("What Homer thinks of Lisa's saxophone")
* url ("https://www.youtube.com/watch?v=OFoW6fa79xA")

## Related resources
* JSON Topic Maps 1.1 - http://www.cerny-online.com/jtm/1.1/
