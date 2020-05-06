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
  - utter_linkedin

## no: greet -> work
* workexperience
  - utter_work1
  - utter_needmore
* deny
  - utter_altmenu

## yes: greet -> education
* education
  - utter_edu1
  - utter_linkedin
  - utter_altmenu

## say goodbye
* goodbye
  - utter_goodbye

## bot challenge
* bot_challenge
  - utter_iamabot
