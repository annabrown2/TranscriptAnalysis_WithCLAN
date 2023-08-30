# Common Errors in CLAN 
Below is a list of common errors likely to occur when converting text files to CHAT files. 
This is not an exhaustive list and can be regularly updated 

## Errors with Punctuation 
+ Lines of speech have to end with an Utterance Delimiter. Utterance delimiters can only be ‘.’ ‘!’ ‘?’ . 
+ These utterance delimiters cannot occur within a line of speech. 
+ The only code allowed after an utterance delimiter is [+ PI]. 

### Examples of punctuation errors. 
Error | Description | Solution
--- | --- | ---
Item ‘,’ must be followed by SPACE or end-of-line. | A comma has been misplaced or there is no space between the comma and word.  | There needs to be a space between the comma and the word
Redundant utterance delimiter found | There are two utterance delimeters at the end of a sentence OR there is an utterance delimiter at the start of the sentence. | Remove the extra utterance delimiter. 
Symbol is not declared in the depfile | This is because the transcript has a symbol that doesn’t follow any CLAN guidelines. | If its a ‘-’ used in the middle of the line of speech simply delete. If its [+PI] the symbol has been used incorrectly, must be in format of [+ PI] 
Item ‘&’ can not be followed by the next symbol. | An ampersand can not be used as punctuation in a CHAT file only to be used as code (e.g. &=Laughs) | Write out the ‘&’ as ‘and’ 
Item [+ PI] must follow after utterance delimiter | E.g. *MOT:	[+ PI] So now we play a game, that I let him go as far as I can see him. The [+ PI] is in the wrong place, OR the code is written wrong. Sometimes the FIXIT command misplaces the [+ PI] code | Either correct the code or move it onto the correct line of speech. 

## Errors with Speaker Tiers 
+ The start of a line of speech must begin with a speaker tier that is correctly formatted.
+ This should be the Speaker code e.g. ‘*MOT’ followed by a colon ‘:’ followed by a tab space then the speech begins.
+ There can be no space before or after the colon. 

### Examples of speaker tier errors. 
Error | Description | Solution
--- | --- | ---
Tabs should only be used to mark the beginning of lines.|A tab space has been used elsewhere within a line of speech, OR there is no Tabspace after the speaker tier code|Add or remove the tab space as appropriate. 
Ilegal character ‘Space’ found in tier text. If it CA, than add “@options: CA’ |There is a normal space after the tab space. |Delete the space by pressing backspace when the error is highlighted. 
Use TAB character instead of space character after Tier name. |There is just a normal space and no tab space after the speaker code. |Change the space for a tab space. 

*Note:* Sometimes these errors will only affect some lines of speech, but sometimes it might be easier to fix these errors with ‘Find and Replace’ if it occurs on every line of speech. 

## Errors with numbers 
+ Numbers are written out numerically (e.g. 3) rather than alphabetically (e.g. three).
+ CLAN doesn’t allow numbers to be written out numerically so they need to be written out alphabetically (e.g. 3 year old would be rewritten as three year old)
+ Make sure you write it out exactly how it would be spoken e.g. ‘25.5’  would be  ‘twenty-five point five’ or ‘twenty-five and a half’.
+ Watch out for units and symbols, these need to be written out as they would be spoken e.g. ‘15lb’ as ‘fifteen pounds'

TESTING
