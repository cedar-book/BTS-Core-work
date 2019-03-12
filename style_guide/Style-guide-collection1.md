
# Coding Standard / Guide -- Collection <1>

> These might be helpful information when you think about the coding style for BitShares



### Standardization is Important

It helps if the standard annoys everyone in some way so everyone feels they are on the same playing field. The proposal here has evolved over many projects, many companies, and literally a total of many weeks spent arguing. It is no particular person's style and is certainly open to local amendments.

#### Good Points 

When a project tries to adhere to common standards a few good things happen:

- Programmers can go into any code and figure out what's going on.
- New people can get up to speed quickly.
- People new to C++ are spared the need to develop a personal style and defend it to the death.
- People new to C++ are spared making the same mistakes over and over again.
- People make fewer mistakes in consistent environments.
- Programmers have a common enemy 

#### Bad Points

- The standard is usually stupid because it was made by someone who doesn't understand C++.
- The standard is usually stupid because it's not what I do.
- Standards reduce creativity.
- Standards are unnecessary as long as people are consistent.
- Standards enforce too much structure.
- People ignore standards anyway.
- Standards can be used as a reason for NIH (not invented here) because the new/borrowed code won't follow the standard. 

### Discussion

The experience of many projects leads to the conclusion that using coding standards makes the project go smoother. Are standards necessary for success? Of course not. But they help, and we need all the help we can get! Be honest, most arguments against a particular standard come from the ego. Few decisions in a reasonable standard really can be said to be technically deficient, just matters of taste. So be flexible, control the ego a bit, and remember any project is fundamentally a team effort.

***

## Standards Enforcement

First, any serious concerns about the standard should be brought up and worked out within the group. Maybe the standard is not quite appropriate for your situation. It may have overlooked important issues or maybe someone in power vehemently disagrees with certain issues 

In any case, once finalized hopefully people will play the adult and understand that this standard is reasonable, and has been found reasonable by many other programmers, and therefore is worthy of being followed even with personal reservations.

Failing willing cooperation it can be made a requirement that this standard must be followed to pass a code inspection.

Failing that the only solution is a massive tickling party on the offending party. 

*************

### Other Coding Style Guidelines 

- Put Your Name On Your Code
- Class Member Variables Use Snake Case Notation
- Class Functions Use Camel-Hump Notation
- Column Width
   - A column of code should be no greater than xx-xx characters wide. Limiting the column width is motivated by wanting to see more than one column on the screen and avoiding wrap-around in a text editor. Seeing code side-by-side is really useful, especially in C++ where much of coding is done on a class implementation and it's nice to see the class definition simultaneously. Most editors with a C++ mode will automatically elegantly indent a single line of code broken up over more
then one line. In Emacs you can set the fill column width in your .emacs file with:

- Code Indentation Two Spaces
- Close Braces Should Be On Their Own Line
- Open Braces - When They Should Be On Their Own Line
- Commenting Class Functions
- Class Interface Organization
- Class Names - Short and Unique
- Function Return Statements Use Parentheses

*****


