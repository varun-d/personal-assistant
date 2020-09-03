# Personal Assistant

Designed to live on my website to be a fun replacement for resumes.
Also designed as a playground for unique chatbot intents.

# Todo
1. Fix deny + goodbye story. Make sure to ask yes / no question and end it at that -utter_goodbye.
2. Release 1 based on working chat front end tool
3. Publish git on
4. Add, two statistical test intents on it.
	Create Sqlite DB, table and add a data field on it. data_list, data_source (flat)
	Check DB, and other.

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
pip install -U rasa-x --extra-index-url https://pypi.rasa.com/simple


# Common commands examples

rasa visualize
rasa data validate --fail-on-warnings --max-history <max_history>
rasa train
rasa test rasa test --fail-on-prediction-errors
// Then run any action method tests

# Devops pipeline
rasa data validate --fail-on-warnings --max-history 5
rasa train
rasa test --fail-on-prediction-errors

// In case great changes to nlu have been made! rasa test nlu --cross-validation

# Future: Add DB feature
import sqlite3
from sqlite3 import Error


def create_connection(db_file):
    """ create a database connection to a SQLite database """
    conn = None
    try:
        conn = sqlite3.connect(db_file)
        print(sqlite3.version)
    except Error as e:
        print(e)
    finally:
        if conn:
            conn.close()


if __name__ == '__main__':
    create_connection(r"C:\sqlite\db\pythonsqlite.db")