## greet
* greet
  - utter_greet
  - utter_menu

## yes: greet -> work
* workexperience
  - utter_work1
  - utter_needmore
* affirm
  - utter_work2
  - utter_menu

## no: greet -> work
* workexperience
  - utter_work1
  - utter_needmore
* deny
  - utter_menu

## yes: greet -> education
* education
  - utter_edu1
  - utter_menu

## contact
* contact
  - utter_contact
  - utter_menu

## say goodbye
* goodbye
  - utter_goodbye

## bot challenge
* bot_challenge
  - utter_iamabot
  - utter_menu

## joke pos
* asked_joke
  - utter_joke
  - utter_wasitgood
* affirm
  - utter_happy
  - utter_menu

## joke neg
* asked_joke
  - utter_joke
  - utter_wasitgood
* deny
  - utter_sad
  - utter_menu

## bad language
* insult
  - utter_reprimand