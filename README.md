# Personal Assistant

Designed to live on my website to be a fun replacement for resumes.
Also designed as a playground for unique chatbot intents.

# Todo
1. Fix deny + goodbye story. Make sure to ask yes / no question and end it at that -utter_goodbye.
2. Release 1 based on working chat front end tool
3. Publish git on 

# Future
Add work specific intents (Mojo, accenture, lbi/digitas/digitaslbi)
Add hobby/tell me about varun / fun fact
* tell_me_more: tell me about varun (fun fact)
  - utter_hobby

# Persona design
[fun, cool, owl]
Have my owl in an animated version? The icon. This is after release.

# Notes
Need ```pip install rasa[convert]``` to test ConveRTT Tokenizer and Featurizer, in a new branch and will test using

``` $ rasa test nlu --config config.yml config_conveRTT.yml --nlu data/nlu.md --runs 3 --percentages 0 25 50 70 90 ```

# Pipeline examples

rasa visualize
rasa data validate --fail-on-warnings --max-history <max_history>
rasa train
rasa test rasa test --fail-on-prediction-errors
Test Action Code
pip install -U rasa-x --extra-index-url https://pypi.rasa.com/simple

