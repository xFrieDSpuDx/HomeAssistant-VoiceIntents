# HomeAssistant-VoiceIntents
A location to keep voice intents for Home Assistant
Two folders are required to get these voice intents working.
custom_sentences
custom_sentences_response

Place both folder in the config director of Home Assistant

Create the custom sentences.
Inside custom_sentences create a folder for the language of the sentences. In my case this is English so create a folder called "en"
Create all new sentence yaml files inside "en"

Create the custom sentenses response
Insude custom_sentences_response create a folder for the language of the sentense responses. In my case this is English so create a folder called "en"
Create all new sentense response yaml files inside "en"

Have Home Assistant recognise the response files
In configuration.yaml add the lines:
intent_script:
  !include_dir_merge_named /config/custom_sentences_response/en/

The language folder will depend which language you chose at the start
