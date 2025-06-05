Real-timeSubtitlingforLiveEvents
Introduction:
Real-timesubtitlingprovideslivecaptioningofaudiocontent,enablingaccessibilityfor hearing-impairedaudiencesandimprovingcontentengagement.Thisprojectsimulatesa real-time subtitling system by transcribing pre-recorded audio chunks (.wav files) sequentially, adding timestamps, and generating subtitle text files.

ProblemStatement:
Live events often require real-time subtitles to aid accessibility and comprehension. Creatinganautomatedsystemthat convertslivespeechtotextwithaccuratetiming is challengingduetonoisyenvironments,speechvariations,andprocessingdelays.This project addresses the simulation of real-time subtitling using offline audio files to approximate live transcription.

Objectives:
Theobjectivesofthisprojectare:
●	Totranscribeaudiospeechfrommultiplepre-recorded.wavfilessequentially.
●	Toappendrecognizedtextwithtimestampstoasubtitle file.
●	Tosimulatereal-timebehaviorwithcontrolleddelaysbetweenaudiosegments.
●	Tohandleerrorsgracefullyduringspeechrecognition.
●	Toprovideadownloadablesubtitlefile foruserconvenience.

Methodology:
Themethodologyforthereal-timesubtitlingsysteminvolvesthefollowingsteps:

1.	Uploading andExtractingAudioFiles
The user uploads a ZIP file containing multiple .wav audio files. These files representsegmentedaudiorecordingsfromaliveevent.TheZIPfileisextracted into a specified directory for processing.

2.	LocatingandSortingAudioFiles
Theprogramrecursivelyscanstheextracteddirectorytofindall.wavfiles.These audio files are then sorted by filename to maintain the correct sequence,
 
simulatingaliveaudiostream.

3.	SpeechRecognitionUsing GoogleWebSpeechAPI
Foreach.wavfile,theprogramusestheSpeechRecognitionPythonlibrarywith Google's Web Speech API to transcribe the speech content into text.

4.	TimestampingandSubtitleGeneration
Eachrecognized text segment isappended to asubtitle file along with a timestampindicatingthetimeoftranscription.Thissimulateslivesubtitle captions appearing in real-time.

5.	SimulatingReal-TimeProcessing
Thesystemintroducesadelay(e.g.,1second)betweenprocessingeachaudio segment to imitate real-time subtitling behavior.

6.	ErrorHandling
The system detects and handles errors such as unrecognized speech or API failures.Itlogsappropriatemessagesandcontinuesprocessingsubsequentaudio files.
InputFormat:
AZIPfilecontainingoneormore.wavaudiofilesrepresentingaudiosegmentsto be transcribed.

OutputFormat:
Aplaintextfilenamed'live_subtitles.txt'containingtimestampedsubtitlesinthe following format:
[HH:MM:SS]Transcribedspeechtext
TestingandValidation:
The system was tested with multiple WAV files of varying lengths and speech clarity. Recognitionaccuracywasvalidatedbycomparingtranscribedtexttotheoriginalspeech. Error handling was tested by including noisy and silent audio clips.

Conclusion:
Thisproject demonstratedthefeasibilityofsimulatingreal-timesubtitlingusing pre-recordedaudiofiles.Whilenotasubstitutefortrueliveaudiotranscription,it
provides a foundation for developing accessible captioning tools. Future work could includeintegratingrealmicrophoneinput,improvingrecognitionaccuracy,andadding advanced subtitle formatting.
