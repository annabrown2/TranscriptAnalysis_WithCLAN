# Step 1: Convert existing transcript to a CHAT file 
This Protocol outlines how to convert the transcribed speech samples so that they follow CHAT transcription guidelines and can be analysed in CLAN. 

## How to use this protocol: 
+ Follow the steps in chronological order.  
+ Anything written within quotation marks (e.g. “&=Laughs”) must be written exactly as it appears, including correct capitalization.  

## Setting up the Transcript 
Watch a useful tutorial for this step here: https://talkbank.org/screencasts/template.mp4 

1. Go to  ‘Clan > File > New…’ to open a blank CHAT file.
2. Save the new CHAT file. 
3. All Transcripts must begin with the following header tiers.
  
```
@Begin
@Languages:	eng
@Participants:	PAR Participant, MOT Mother, INV Investigator
@Options:
@ID:	eng|change_corpus_later|MOT|||||Mother|||
@ID:	eng|change_corpus_later|INV|||||Investigator|||
@Media:	(FILE NAME HERE), audio unlinked
@Transcriber:(YOUR NAME HERE)

```
*In this example our transcripts consisted of a mother being interviewed about her children, therefore we have used ID headers for Mother and Investigator. For all ID headers available in CLAN consult the manual.*

4. Add the filename to the media tier (excluding file extension). 
5. Add your name to the transcriber header tier.
6. Once you have entered this information, click on tiers on the top menu bar and then on update. The participants' codes should appear in the tier list.
7. Underneath the transcriber header tier enter the existing transcript.
   
*Note:* 
+ Don’t end header tiers with a punctuation mark. 
+ Each colon on a header tier needs to be followed by a tab.
  
## Change participants code 
*Speaker labels must follow the code as specified in the ID header tier.*
+ e.g. for lines of mothers speech the line would begin with `*MOT:  `  
+ All lines of speech must begin with the same format. 
+ CLAN also has strict guidelines about punctuation and spaces for participant codes. There can be no space after the colon, just a tab space.

## Recode identifiable information
*To anonymise your transcripts, you can recode any identifiable information.*
+ Use code `www` followed by a marker `[% Identifiable Information]`
+ e.g. 'This is Family ID 1234' becomes 'This is Family ID www [% Family ID].'

## Recode pauses 
*There may be long breaks in the transcript currently recorded e.g. [pause 00:03:45 - 00:03:50], these need to be removed from the transcript or recoded depending on length.* 
#### If pause is on its own line in the transcript…
+ Add “%act:[tab space]” followed by the pause timemark. 
    e.g. `%act:	[pause 00:03:45 - 00:03:50]`
#### If pause is within a speech line… 
+ Delete current pause tag and change to `(..)` for a long pause or `(.)` for a short pause.

## Recode any other markers 
*Any other nonverbal or additional information included within transcripts must be recoded. Examples of how to recode some of these instances are listed below.*

#### If the marker is for speech that couldn’t be transcribed… 
e.g. unclear, inaudible or an interruption.  
1. delete full unclear marker and replace with `xxx`
2. After the utterance delimiter (the full stop) add postcode `[+ PI]` 

#### If the marker is for non-verbal behaviour… 
e.g. laughs, coughs, sighs. 
1. mark the non verbal information with the &= marker
2. e.g. laughs becomes `&=laughs`

#### If the marker is providing context to the transcript…
e.g. information about what is happening during the speech. 
1. add “%act:(followed by a tab space)”
2. The marking on an interruption would become `%act:	[Interruption 00:17:20-00:17:40]`

#### This is not an exhaustive list of all markers. For more information, consult CLAN manual part 1. 

## Make sure all the utterance delimeters are correct
+ CHAT guidelines means all utterances/lines of speech have to end with a full stop.
+ No other punctuation (except ? or !) can end a line of speech.
+ These punctuation marks can also not occur within a line of speech, only at the end.

#### If the line of speech was interuppted 
1. If the line of speech was incomplete or interrupted, mark with `+...`
2. If the speech is then continued after the interruption, mark the next line of speech `+,`
  e.g.,
    *MOT:  I can't remember exactly +...
    *INV:  That's okay.
    *MOT:  +, but it was around July.

## Add an end and save the transcript. 
*Once other steps have been completed, add an end marker to the transcript.*
1. On the final line add `@End`
2. Save the transcript. 



   

   
