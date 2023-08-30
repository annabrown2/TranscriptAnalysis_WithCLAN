# Step 3: Running the MOR Command 
The MOR command is essential for morphosyntactical analysis and extracting many useful language markers. 
It is recommended you read [CLAN manual:Part3](https://doi.org/10.21415/T5B97X) to fully understand how the morphosyntactical analysis works.   

#### This protocol contains 
1. How to identify all the words not recognised by CLAN.
2. Causes of unrecognised entries.
3. Using CHstring to fix multiple errors.
4. Adding words to MOR lexicon. 
5. Running the final MOR command on all files. 

## Check for unrecognised words 
The MOR XB command needs to be run to generate a list of lexical items that are not recognised. 
```
MOR +xb +t*MOT *.cha
```
+ use the switch `+t` to specify if you want it to run on a single ID tier
+ The command generates an output window that tells you it made a file with all the words not recognised in the lexical directory.
  + It is usually named after the first transcript in the file directory with extension .ulx.cex
+ Triple click the output line to bring up the list of unrecognised lexical items. 

## Causes of unrecognised entries.

### Error: It is misspelled.  
+ If you have doubts about the spellings of certain words, you can look in the 0allwords.cdc file (MOR > eng > 0allwords.cdc). The words there are listed in alphabetical order.
+ **Important note**: CLAN only accepts the American spelling of words, not UK English spelling. Either change the spelling using CHSTRING or add UK spelling to the lexcial dictionary  
+ **Solution:** Fix each instance to correct spelling in the CHAT file *unless* misspelling repeatedly occurs then use CHSTRING command (see below)

### Error: It's a non-word or filler word. 
+ An ampersand should precede the word ‘&’ to block look up through MOR.
+ Four forms are using the ampersand.  
  + Nonwords just take the '&' alone, e.g. `&gaga`.
  + Incomplete words should be transcribed as &+text, e.g. `&+sn` for the beginning of snake.
  + Filler words should be transcribed as '&-' e.g. `&-uh`.
+ **Solution:**  Recode incomplete and non-words, but check the context and make sure it's not a dialectal form or anything else less common. 
 
### Error: The word should have been transcribed with a special form marker, as in bobo@o or bo^bo@o for onomatopoeia.  
+ It is impossible to list all possible onomatopoeic forms in the MOR lexicon.
+ So the @o marker solves this problem by telling MOR how to treat the form.
+ This approach will be needed for other special forms, such as babbling '@b', word play '@wp'.
+ **Solution:** Change any onomatopoeia using @o marker, babbling with '@b' marker and wordplay with '@wp' marker

### Error: The word was transcribed in “eye-dialect” to represent phonological reductions. 
+ E.g. ‘’cause’ ‘gonna’
+ When this is done, there are two basic ways to allow MOR to achieve the correct lookup.
+ either use parentheses or [: text] replacement method.

**Words where phonemes have been dropped should be coded as…**
```
*MOT: I want (a)nother 
*MOT: but if you tell (th)em 
*MOT: but like I only do it (be)cause
```
**Words where phonemes have been contracted should be coded as…**
```
*MOT:	I wanna [: want to] go 
*MOT: I’m gonna [: going to] go 
*MOT: do ya [:do you]
```

### Error: No capital letter for a proper noun e.g. someone's name. 
+ You should treat the word as a proper noun by capitalizing the first letter. 
+ **Solution:** Capitalise the first letter of the pronoun.
 
### Error: The stem is in the lexicon, but the inflected form is not recognized.  
+ In this case, it is possible that one of the analytic rules of MOR is not working.  

### Error: The stem or word is missing from MOR.  
+ In that case, we shall create a file called something like 0add.cut in the /lex folder of the MOR grammar (see below).

## Using CHSTRING to fix repeated errors 
+ If an error occurs repeatedly across transcripts for example a spelling mistake or dialectal form then it will be easier to fix the error using CHSTRING command

### Make one change at a time 
+ Sometimes you need to change just one word, or string, in a file(s).
+ These changes can be put directly on the command line following the +s option.
+ e.g., if you wanted to mark all usages of the word moo in a file as an onomatopeia, enter this into the command window
```
CHSTRING +s"moo" "moo@o"
```
### Making multiple changes
1. Create a CHAT file and save it as 'changes.cut'
2. Save the file in 'lib' folder of your CLAN applications folder (e.g. on mac applications>Clanc>lib)
3. Within the file, record the change in the format of "old string" "new string"
  *e.g. To change the misspelling of 'preschool' to 'pre_school' it should be in Changes.cut as `"preschool" "pre_school"`
5. Each new line in the changes.cut will be a different change
6. Once the file is complete enter this code into the commands window
```
CHSTRING +c +1 *.cha
```
## Adding words to the MOR lexicon 
MOR contains an extensive dictionary but it won't have every word. If none of the options above apply then it may be necessary to add the words to the MOR lexicon. 

1. Create a file called 0addmorewords.cut
2. Save the file in the /lex folder of the MOR grammar files on your computer
3. Within the file code each word under the following format `STEM {[scat WORD CLASS CODE]}`
  *e.g. when adding the word ‘chocoholic’. It would be added into the file as… `Chocoholic {[scat n]}`

## Once there are no unrecognised lexicon entries run MOR 
For full information about how the MOR command works consult [CLAN manual:Part3](https://doi.org/10.21415/T5B97X)  

Run the final MOR code 
```
MOR *.cha
```
+ use the switch `+t` to run MOR on select ID tiers 




