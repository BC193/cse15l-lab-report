# CSE 15L Lab Report 3

## Table of Contents
- Command: ```grep```
- Command Line Options

## Command: ```grep```
> grep stands for global regular expression print

- Used to redirect and search files for specific stings
- Uses search patterns to filter through files

## Command Line Options
### Part 1: "-l"
> the -l command allows us to find a file with any specific string


``` 
Input:

grep -r -l "Lucayans" written_2

Output:
written_2/travel_guides/berlitz2/Bahamas-History.txt
```

> This looks for a file with the word Lucayans in the directory written_2. It is helpful to allow us to find where a particular word is found.


``` 
Input:

grep -r -l "definitive" written_2 

Output:
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
```

> This looks for a file with the word definitive in the directory written_2. It allows for us to find a particular file when there are too many files to manually go through.

### Part 2: "-r"
> the -r command makes grep recursive


``` 
Input:

grep -r  "Lucayans" written_2

Output:
The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently 
passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera 
the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies 
of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As 
for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and 
die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```

> This looks for the text that includes the word Lucayans and it will return the entire file. When we need to find the word and its context the -r allows us to look through multiple files that search a wider scope. 


``` 
Input:

grep -r "definitive" written_2

Output:
In the little Vanier Park by the Burrard Bridge, you’ll find two interesting little museums and the MacMillan Planetarium.
The Centennial Museum is devoted to local history and anthropology. The Maritime Museum traces the history of the Pacific 
port. Its showpiece is the Saint-Roch. This proud ship of the Royal Canadian Mounted Police, sailed clear around the North 
American continent via the Panama Canal and the Arctic Ocean, to plot a definitive Northwest Passage and hunt German 
U-boats on the way.
```

> This looks for the text that includes the word definitive and it will return the entire file. Looks into more files and a wider search. 

### Part 3: "-c"
> the -c command allows us to find the total number of lines that are included on the 


``` 
Input:

grep -c written_2 *.txt

Output:
236
```

> This finds the total number of txt files in the directory written_2. Useful in potentially finding the total number of files a test will have to go through.


``` 
Input:

grep -c written_2 *.java

Output:
DocSearchServer.java:1
Server.java:0
TestDocSearch.java:3
```

> This through all the .java files in written_2 in order to find the total lines in each file. The wider scope of file search allows for helpful information regarding the files we are navigating. 

### Part 4: "-n"
> the -n command allows us to find the line in a specific file where a string is found. It can help with combing the data and provide more direct links to information in bigger files. 


``` 
Input:

grep -r -n "Lucayans" written_2  

Output:
written_2/travel_guides/berlitz2/Bahamas-History.txt:6:Centuries before the arrival of Columbus, a peaceful Amerindian 
people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled 
up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. 
Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and 
the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly 
called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas 
for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks 
before sailing towards Cuba.

written_2/travel_guides/berlitz2/Bahamas-History.txt:7:The Spaniards never bothered to settle in the Bahamas, but 
the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from 
the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot 
now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the 
long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of 
them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on 
farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```

> This looks for the line numbers where the word Lucayans is contained. It can provide more context and allows us to go and physically refer to the line a command or sentence is located. 


``` 
Input:

grep -n "definitive" written_2 

Output:
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt:393:In the little Vanier Park by the Burrard Bridge, you’ll 
find two interesting little museums and the MacMillan Planetarium. The Centennial Museum is devoted to local 
history and anthropology. The Maritime Museum traces the history of the Pacific port. Its showpiece is the 
Saint-Roch. This proud ship of the Royal Canadian Mounted Police, sailed clear around the North American continent 
via the Panama Canal and the Arctic Ocean, to plot a definitive Northwest Passage and hunt German U-boats on the way.
```

> This looks for the line numbers where the word definitive is contained 
