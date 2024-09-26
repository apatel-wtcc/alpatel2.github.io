flowchart TD
    Start([Start]) --> GenerateRandomNumber[Generate Random Number]
    GenerateRandomNumber --> GetUserGuess[Get User Guess]
    GetUserGuess --> ValidateInput{Is Input Valid?}
    ValidateInput -->|Yes| CheckGuess[Check Guess]
    ValidateInput -->|No| DisplayError[Display Error Message]
    DisplayError --> GetUserGuess
    CheckGuess -->|Too High| ProvideFeedback[Provide Feedback: Too High]
    CheckGuess -->|Too Low| ProvideFeedback[Provide Feedback: Too Low]
    CheckGuess -->|Correct| Congratulate[Congratulate User]
    ProvideFeedback --> GetUserGuess
    Congratulate --> End([End])