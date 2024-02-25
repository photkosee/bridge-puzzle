# Bridge Puzzle
> Note that the code here is not the complete version of the project. The complete code could only be published after 2025 due to UNSW policy.
Please contact me to review the complete version of the code in person.

### Specification

This project is based on a popular puzzle, variously known as "Hashiwokakero", "Hashi" or "Bridges". You will need to write a program to solve this puzzle, and provide a brief description of the algorithm and data structures you have used. The input to your program will be a rectangular array of numbers and dots, for example:
<pre>
.1...6...7....4.4.2.
..4.2..2...3.8...6.2
.....2..............
5.c.7..a.a..5.6..8.5
.............2......
...5...9.a..8.b.8.4.
4.5................3
....2..4..1.5...2...
.2.7.4...7.2..5...3.
............4..3.1.2
</pre>
Each number represents an "island", while the dots represent the empty space (water) between the islands. Numbers larger than 9 are indicated by 'a' (10), 'b' (11) or 'c' (12). The aim is to connect all the islands with a network of bridges, satisfying these rules:
- All bridges must run horizontally or vertically
- Bridges are not allowed to cross each other, or other islands
- There can be no more than three bridges connecting any pair of islands
- The total number of bridges connected to each island must be equal to the number on the island
<br>
For example, after reading the 10-line input above, your program should produce this output:<br>
<pre>
 1---6EEE7====4=4=2 
  4-2" 2 " 3E8EEE6 2
  # |2 " "   "   # "
5EcE7EEaEa==5"6EE8=5
" #    " #  #2#    |
" #5===9Ea--8=bE8E4|
4=5#   " #  " # " |3
   #2==4 #1-5 # 2 |"
 2=7=4===7=2" 5===3"
            4==3-1 2
</pre>
<br>
Note that single bridges are indicated by the characters '-' or '|', pairs of bridges by '=' or '"' and triples by 'E' or '#', depending on whether they run horizontally or vertically. Water between bridges and islands is indicated by space characters ' '.
In some cases, there may be many solutions, in which case your program should only print one solution. More details about the puzzle can be found on this Wikipedia page. Note, however, that our version allows up to 3 bridges instead of 2; also, we do not insist that the entire graph be connected.
Tools
An executable file called bridgen is provided in the tools directory which can be used to generate sample data of any specified size (type bridgen -help for details). Another executable called bridgecheck is also provided, to help you test the validity of your solutions (see FAQ for details).
Questions
At the top of your code, in a block of comments, you must provide a brief answer (one or two paragraphs) to this Question:
Briefly describe how your program works, including any algorithms and data structures employed, and explain any design decisions you made along the way.
