# Data Challenge

Emerging science requires data collection to support the research and development of advanced methodologies. In the educational field, conceptual frameworks such as Learning Analytics (LA) or Intelligent Tutoring System (ITS) also require data. Prior studies demonstrated the efficiency of academic data, for example, risk student prediction and learning strategies unveiling. However, a publicly available data set was lacking for benchmarking these experiments. To contribute to educational science and technology research and development, we conducted a programming course series two years ago and collected 160 students' learning data. The data set includes two well-designed learning systems and measurements of two well-defined learning strategies: Self-regulated Learning (SRL) and Strategy Inventory for Language Learning (SILL). Then we summarized this data set as a Learning Behavior and Learning Strategies data set (LBLS-160) in this study; here, 160 indicates a total of 160 students. Compared to the prior studies, the LBLS data set is focused on students' book reading behaviors, code programming behaviors, and measurement results on students' learning strategies. Additionally, to demonstrate the usability and availability of the LBLS data set, we conducted a simple risk student prediction task, which is in line with the challenge of cross-course testing accuracy. Furthermore, to facilitate the development of educational science, this study summarized three data challenges for the LBLS data set.

## Folder Structure

```
    .
    ├── ...
    ├── data                    
    │   ├── br.csv              # Students' BookRoll activities (learning behavior)
    │   ├── score.csv           # Students' final score
    │   ├── sill.csv            # Students' Strategy Inventory for Language Learning (SILL) measurement results
    │   ├── srl_motivation.csv  # Students' Self-regulated Learning (SRL) measurement results
    │   ├── viscode.csv         # Students' VisCode activities (learning behavior)
    ├── example.ipynb           # An example to train a prediction model, then evaluate its performance                    
    ├── 000_BookRoll PCA.png    # PCA analysis results on BookRoll, generated by example.ipynb
    ├── 000_SILL PCA.png        # PCA analysis results on SILL measurement, generated by example.ipynb
    ├── 000_VisCode PCA.png     # PCA analysis results on VisCode, generated by example.ipynb
```

## Data Formats

### Students' BookRoll activities (learning behavior)

| Feature   | Description |
|---------  |-------------|
| userid    | Anonymized student userid, eg: b1dfc5c6ec04d46d1823c5fa972ad320   |
| ADD BOOKMARK          | Added a bookmark to current page. |
| ADD MARKER            | Added a marker to current page. |
| ADD MEMO              | Added a memo to current page. |
| ADD_HW_MEMO           | Added a handwrite memo to current page. |
| BOOKMARK_JUMP         | Jump to a specific page with a bookmark. |
| CHANGE MEMO           | Modify the content of an existing memo on current page. |
| CLEAR_HW_MEMO         | Clear the content of an existing handwrite memo on current page. |
| CLOSE                 | Closed the book. |
| CLOSE_RECOMMENDATION  | Deleted an exist bookmark in the e-book.|
| DELETE BOOKMARK       | Deleted a bookmark on current page. |
| DELETE MARKER         | Deleted a marker on current page. |
| DELETE_MEMO           | Deleted a memo on current page. |
| GETIT                 | Press the smiley face icon to indicate the understanding on current page. |
| MEMO_JUMP             | Select a note to jump to the specific page. |
| NEXT                  | Went to the next page. |
| NOTGETIT              | Press the crying face icon to indicate the misunderstanding on current page.|
| OPEN                  | Opened the book. |
| OPEN_RECOMMENDATION   | |
| PAGE_JUMP             | Jumped to a particular page. |
| PREV                  | Went to the previous page. |
| REGIST CONTENTS       | |
| SEARCH                | Searched for something within the e-book. |
| SEARCH_JUMP           | Jumped to a page from the search results. |
| UNDO_HW_MEMO          | Undo the last action of handwriting. |

### Students' final score

| Feature   | Description |
|---------  |-------------|
| userid    | Anonymized student userid, eg: b1dfc5c6ec04d46d1823c5fa972ad320   |
| score     | Students' final score, less than 60 indicated failed on this course. |
| class     | Students' class identity. |

### Students' Strategy Inventory for Language Learning (SILL) measurement results

| Feature   | Description |
|---------  |-------------|
|userid     | Anonymized student userid, eg: b1dfc5c6ec04d46d1823c5fa972ad320. |
|s_1         | (Memory) I think of relationships between what I already know and new things I learn in programming language. |
|s_2         | (Memory) I use Syntax or Lexical which just learned in my code, so I can remember them. |
|s_3         | (Memory) I connect the diagram or logic of a new programming skill to help remember them. |
|s_4         | (Memory) I remember a new Syntax or Lexical by making a diagram which the function might be used. |
|s_5         | (Memory) I use textbooks or dictionary to remember Syntax or Lexical which I just learned. |
|s_6         | (Memory) I physically implement a function by Syntax or Lexical which I just learned. |
|s_7         | (Memory) I review code often. |
|s_8         | (Memory) I remember new Syntax or Lexical by remembering their location on the page. |
|s_9         | (Cogntive) I practice coding often. |
|s_10        | (Cogntive) I try to code like an open-source contributor. |
|s_11        | (Cogntive) I pratice to design code structure. |
|s_12        | (Cogntive) I implement a founction in different code structure. |
|s_13        | (Cogntive) I refer example code in open-source community. |
|s_14        | (Cogntive) I code for pleasure. |
|s_15        | (Cogntive) I code for solving the problems encountered in life. |
|s_16        | (Cogntive) I first skim code structure (function name, variable name, calls) then go back to simulate execution carefully. |
|s_17        | (Cogntive) I run units to understand a complex code or new Syntax or Lexical. |
|s_18        | (Cogntive) I try to find patterns in code. |
|s_19        | (Cogntive) I find the meaning of a code by dividing it into units. |
|s_20        | (Cogntive) I try not to avoid to read comments in code. |
|s_21        | (Cogntive) I make summaries, notes when I interpret code. |
|s_22        | (Compensation) To understand unfamiliar Syntax or Lexical, I make guesses. |
|s_23        | (Compensation) I use other functions or methods when I forget the direct one. |
|s_24        | (Compensation) I make up new functions if I do not know the right ones. |
|s_25        | (Compensation) I can read a code without using textbooks or dictionary. |
|s_26        | (Compensation) I try to guess what the meaning of unfamiliar Syntax or Lexical. |
|s_27        | (Compensation) If I can' t think of a Method or Class, I implement one instead. |
|s_28        | (Metacognitive) I try to guess what the other person will design in assignment. |
|s_29        | (Metacognitive) I notice my weakness of programming skills and use that information to help me do better. |
|s_30        | (Metacognitive) I pay attention when someone is explaining a concept on programming. |
|s_31        | (Metacognitive) I try to fine out how to be a better programmer. |
|s_32        | (Metacognitive) I plan my schedule so I will have enough time to study programming. |
|s_33        | (Metacognitive) I look for people I can talk to in programming. |
|s_34        | (Metacognitive) I look for opportunities to read as much as possible in codes. |
|s_35        | (Metacognitive) I have clear goals for improving my programming skills. |
|s_36        | (Metacognitive) I think about my progress in learning programming. |
|s_37        | (Affective) I try to relax whenever I feel afraid of coding. |
|s_38        | (Affective) I encourage myself to code even when I am afraid of making a mistake. |
|s_39        | (Affective) I give myself a reward or treat when I do well in programming assignment. |
|s_40        | (Affective) I notice if I am tense or nervous when I am coding a programming. |
|s_41        | (Affective) I write down my feelings in a language learning diary. |
|s_42        | (Affective) I talk to someone else about how I feel when I am learning programming. |
|s_43        | (Social) If I do not understand something in programming, I ask question in opensource communities. |
|s_44        | (Social) I ask contributers in opensource communities to review my code. |
|s_45        | (Social) I join opensource communities. |
|s_46        | (Social) I ask for help from opensource communities. |
|s_47        | (Social) I ask questions. |
|s_48        | (Social) I try to kearn about the style of coding. |

###  Students' Self-regulated Learning (SRL) measurement results

### Students' VisCode activities (learning behavior)

| Feature   | Description |
|---------  |-------------|
| userid            | Anonymized student userid, eg: b1dfc5c6ec04d46d1823c5fa972ad320   |
| code_length       | Nunber of lines of code (LOC) coded in this semester. | 
| code_copy         | Number of times a student copy codes. | 
| code_execution    | Number of times a student execute codes. |
| code_paste        | Number of times a student paste codes. |
| code_speed        | Average input digits per minutes. |
| notebook_open     | Number of times a student open coding environment. |
| tree_open         | Number of times a student open a foder looking for a code. | 
| AttributeError    | Raised when attribute reference or assignment fails. |
| ConversionError   | Failed to convert value(s) to axis units. |
| FileExistsError   | Raised when trying to create a file or directory which already exists. |
| FileNotFoundError | Raised when a file or directory is requested but doesn’t exist. |
| IndentationError  | Base class for syntax errors related to incorrect indentation. |
| IndexError        | Raised when a sequence subscript is out of range. |
| JSONDecodeError   | Raised if the given JSON document is not valid. |
| KeyError          | Raised when a mapping (dictionary) key is not found in the set of existing keys. |
| KeyboardInterrupt | Raised when the user hits the interrupt key (normally Control-C or Delete). |
| LookupError       | The base class for the exceptions that are raised when a key or index used on a mapping or sequence is invalid: IndexError, KeyError. |
| ModuleNotFoundError   | A subclass of ImportError which is raised by import when a module could not be located. |
| NameError         | Raised when a local or global name is not found. |
| OperationalError  | Exception raised for errors that are related to the database’s operation, and not necessarily under the control of the programmer. |
| SyntaxError       | Raised when the parser encounters a syntax error. |
| TabError          | Raised when indentation contains an inconsistent use of tabs and spaces. |
| TypeError         | Raised when an operation or function is applied to an object of inappropriate type. |
| UnboundLocalError | Raised when a reference is made to a local variable in a function or method, but no value has been bound to that variable. |
| UnicodeDecodeError | Raised when a Unicode-related error occurs during decoding. |
| ValueError        | Raised when an operation or function receives an argument that has the right type but an inappropriate value, and the situation is not described by a more precise exception such as IndexError. |
| ZeroDivisionError | Raised when the second argument of a division or modulo operation is zero. |

https://docs.python.org/3/library/exceptions.html

https://docs.python.org/3/library/json.html

https://github.com/matplotlib/matplotlib/blob/cd9d371cd473b286310845ada9e5a3e786630e1a/lib/matplotlib/units.py#L52

https://docs.python.org/3/library/sqlite3.html#sqlite3.OperationalError