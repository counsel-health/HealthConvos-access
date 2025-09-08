## Dataset Column Information

Here is an example row with sample values from the de-identified dataset, with descriptions for what each column represents.

- `thread_idx`: Integer; unique identifier for each thread
- `messageHistories`: List of de-identified and paraphrased messages within a thread that can be loaded with ast.literal_eval; has a "body" field (containing text) and "sender" field (e.g., "patient", "physician", "system")
- `ordinalMessages`: List of Integers containing the order of each message from messageHistories; e.g., [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]; order is global across `ordinalMessages` and `ordinalNotes` (e.g., if `ordinalMessages[x] == 5`, that means the xth message in the thread is the 6th message overall considering messages and notes)
- `outcomeNotes`: List of strings containing physician-written notes for each thread
- `ordinalNotes`: List of Integers containing the order of each note from outcomeNotes; e.g., [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]; order is global across `ordinalMessages` and `ordinalNotes` (e.g., if - `ordinalNotes[x] == 5`, that means the xth note in the thread is the 6th note overall considering messages and notes)
- `threadCategory`: String containing the category of the thread, with possible values: Acute Care, Chronic Care, Other, Lifestyle/Prevention, General Advice/Info, Behavioral Health, Data Review
- `escalationLabel`: String containing physician-adjudicated label of whether the thread should be escalated to in-person care, with possible values: "Positive", "Negative".
