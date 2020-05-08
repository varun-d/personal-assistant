# Personal Assistant

Designed to live on my website to be a fun replacement for resumes.
Also designed as a playground for unique chatbot intents.

# Todo
Experiment with custom model, duplicate config.yml and test it. #results: ConveRTT works slighly better.
Train it with more data!

Add contact
Add work specific intents (Mojo, accenture, lbi/digitas/digitaslbi)
Add hobby/tell me about varun / fun fact
* tell_me_more: tell me about varun (fun fact)
  - utter_hobby


# Intent simulations
* greet
  - utter_greet (Hoot! How are you {name}? This is Owlo, Varun's personal assistant.)
  - utter_menu (You can ask me about: <a. button: Varun's work experience> <b. button: his education> <c. button: contact him>)
* workexperience
  - utter_work1 (Varun has been working at Accenture since 2 years. /n Prior to that he founded Nameless Co. in 2016.)
  - utter_needmore (Would you like to know more?)
* affirm
  - utter_work2 (In 2015, Varun was Head of Digital Strategy at Mojo Group where he introduced new UX and digital pitching protocols. /n Prior to that, he worked in Digital Analytics at DigitasLBi.)
  - utter_linkedin (Just like you expect, he has a linked in too at <LinkedinID>))
* deny
  - utter_altmenu (That's a hoot! If you like, you can ask me about: )

* education
  - utter_edu1 (Back in 2008, Varun graduated with a BEng in Electronics and Instrumentation)
* affirm
  - utter_edu2 ()
  - utter_linkedin (Just like you expect, he has a linked in too at <LinkedinID>))
* deny
  - utter_altmenu (That's a hoot! If you like, you can ask me about: )

c. book an appointment



# Chitchat collection
* menu
  - utter_menu

* goodbye
  - utter_bye (It was a hoot talking to you!)

* joke
  - utter_joke (Why are owls so good at math? They excel at owlgebra.)
  (What kind of gang violence is common among owls? A drive by hooting.)
  (What did the owl’s valentine say? You are hootiful.)
  (What do you call a smartass bird of prey? A know it owl.)
  (Why doesn’t an owl study for a test? They prefer to wing it.)

* whomadeyou
  - utter_mademe (Varun didn't want to be owl by himself, so he created me @_@)

 * notunderstand
  - utter_learning (It doesn't look like anything to me. Sorry, still learning.)
  - utter_altmenu (That's a hoot! If you like, you can ask me about:)

* bot_challenge
  - utter_iamabot


# Owlo design
Have my owl in an animated version

# Notes
Need ```pip install rasa[convert]``` to test ConveRTT Tokenizer and Featurizer, in a new branch and will test using

``` $ rasa test nlu --config config.yml config_conveRTT.yml --nlu data/nlu.md --runs 3 --percentages 0 25 50 70 90 ```
rasa visualize

# Pipeline

rasa data validate --fail-on-warnings --max-history <max_history>
rasa train
rasa test rasa test --fail-on-prediction-errors
Test Action Code
