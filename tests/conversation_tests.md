#### This file contains tests to evaluate that your bot behaves as expected.
#### If you want to learn more, please see the docs: https://rasa.com/docs/rasa/user-guide/testing-your-assistant/

## greet check
* greet: hey hi
  - utter_greet
  - utter_menu

## yes: greet -> work
* workexperience: tell me about his work experience
  - utter_work1
  - utter_needmore
* affirm: yea
  - utter_work2
  - utter_linkedin
  - utter_altmenu

## no: greet -> work
* workexperience: varuns experience
  - utter_work1
  - utter_needmore
* deny: no that's fine
  - utter_altmenu

## yes: greet -> education
* education: what did he study?
  - utter_edu1
  - utter_linkedin
  - utter_altmenu

## contact
* contact: how do I contact him?
  - utter_contact
  - utter_altmenu

## say goodbye
* goodbye: take care bye
  - utter_goodbye

## bot challenge
* bot_challenge: are you a bot?
  - utter_iamabot
  - utter_altmenu

## joke 
* asked_joke: tell me a joke
  - utter_joke

## insult
* insult: shit bot
  - utter_reprimand
