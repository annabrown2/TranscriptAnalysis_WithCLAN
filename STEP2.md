# STEP 2: Checking CHAT files for Errors
This Protocol outlines how to check files for remaining errors and make sure all CHAT guidelines are followed. 

## How to use this protocol: 
+ Follow the steps in chronological order.  
+ Anything written within quotation marks (e.g. “&=Laughs”) must be written exactly as it appears including correct capitalization.

## Preparing CLAN and File Storage
### Install MOR grammar library 
This installs the grammar library for English, a group of folders containing a library of every word that CLAN recognises and its grammatical information. 
1. To install this library, go to file > Get MOR grammar > and select eng
2. This library will then install on your desktop and appear in MOR lib in the commands window. 

### Create Working and Output Files 
Create a file directory that you will use to organise your CHAT files. 
1. Create a folder on your desktop named ‘Work’.
2. Open commands window in CLAN (window > commands)
3. Make sure your working and output folders are both set to your 'Work' folder

## Run the FIXIT command 
This command ensures that there is only one sentence (utterance) per line of speech. 
It will break up any lines of speech that contain more than one sentence. 
```
FIXIT +1 *.cha
```
`FIXIT` is the command 
`+1` is the switch that means it will overwrite the existing file 
`*.cha` means it will run on all CHAT files in your working directory 

#### In the event of an error 
+ Any errors will appear in the output window.
+ Triple-click on the line that details which file contains the error.
+ The relevant CHAT file will load and navigate to the error.
+ Fix the error (normally by manually assigning a speaker to the line of speech)

## Run the LOWCASE command 
The command ensures there isn’t a capital letter at the start of a line of speech. 
Only pronouns can begin with a capital letter

```
LOWCASE +1 *.cha
```
`LOWCASE` is the command 
`+1` is the switch that means it will overwrite the existing file 
`*.cha` means it will run on all CHAT files in your working directory 

## Run the DELIM command 
The command makes sure that there is an utterance delimeter at the end of every utterance. 
```
DELIM +1 +t* *.cha
```
`DELIM` is the command 
`+1` is the switch that means it will overwrite the existing file 
`+t*` is the switch that make sure it runs on all dependent tiers
`*.cha` means it will run on all CHAT files in your working directory 

## Check for remaining Errors 
CLAN has a built-in check function. This can be run using the `CHECK` command in the commands window or manually checking each file. 
I would recommend checking each file manually 

1. Open the CHAT file, and move cursor to the start of the file.
2. Press esc+L and this will check the file for errors
3. CLAN will navigate to the error and list the error below.
4. Use the common errors guide to fix the error.
5. Repeat the process until CLAN says ‘Success! No Errors Found!’ 





 

