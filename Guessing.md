```mermaid
flowchart TD
    Start([Start Game]) --> RandomNum[Generate Random Number]
    RandomNum --> Input[Ask User for a Guess]
    Input --> Validate{Is input valid?}
    Validate -->|No| Error[Show Error Message] --> Input
    Validate -->|Yes| Compare{Is Guess Correct?}
    Compare -->|Yes| Correct[Show 'Correct' Message] --> End([End Game])
    Compare -->|No| Feedback{Is Guess Too High or Too Low?}
    Feedback -->|Too High| High[Show 'Too High' Message] --> Input
    Feedback -->|Too Low| Low[Show 'Too Low' Message] --> Input