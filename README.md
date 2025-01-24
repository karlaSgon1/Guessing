# Guessing Gaming

```mermaid
%%{
  init: {
    'theme': 'base',
    'themeVariables': {
      'primaryColor': '#D6EAF8',
      'primaryTextColor': '#EC7063',
      'primaryBorderColor': '#AED6F1',
      'lineColor': '#D7BDE2',
      'secondaryColor': '#F5B7B1',
      'tertiaryColor': '#B03A2E'
    }
  }
}%%


flowchart TD
    Start((start))--> A 
    A((Computer Randomly Chooses number, <br> range between 1-20))--> B{Person gives #}
    B --> |Correct!| C{You won! Play again?}
    C --> A
    B -->|Incorrect! <br> Number is too low| D{Guess again!, <br>Another guess}
    B -->|Incorrect! <br> Number is too high| D
    B -->|Error! <br>Not a number!| D
    B -->|Number not in range!| D
    D -->|Incorrect! <br> Number too high!| E{Last Chance! <br> Player gives one more guess}
    D -->|Incorrect! <br> Number too low!| E
    D -->|Error! <br> Not a number!| E
    D -->|Number not in range!| E
    E -->|Correct! You won! Play again?| A
    E -->|Incorrect! You lost, Computer Won| A
    D -->|Correct!| G{Play again?}
    G --> A
```


The flow chart describes the three tries the player gets to guess the correct number. The computer randomly picks a number between 1 and 20. The player then has 3 tries to guess the number chosen by the computer. 

If a number is lower than the chosen number, it will display "Incorrect! Number is too low!". If the number is higher than the chosen number it will display, "Incorrect!, Number is too high!". If the player inputs anything other than a number, it will display "Error! Not a number!". 

Finally, if the player inputs the correct number, the game will loop back to the start where a new number will be chosen by the computer. 
