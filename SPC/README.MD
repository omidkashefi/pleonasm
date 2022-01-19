
The Semantic Pleonasm Corpus (SPC) dataset is stored in ```SPC.json```.
- Each line contains a JSON object representing a single annotated sentence.
- Read the file line by line, parsing each line into a separate dictionary (e.g. ```dict``` in python)

Here is the format for a single annotated sentence (all on one line):
``` json
{
    "before": "This is the part of the sentence before the pair of potentially redundant words",
    "after": "This is the part of the sentence after the pair of potentially redundant words",
    "first": "first_redun_word",
    "second": "second_redun_word",
    "consensus": "neither|both|first_word|second_word",
    "annotations": {
        "worker_id_1": {
            "delete": "...",
            "certainty": "Certain|Somewhat certain|Uncertain",
            "explanation": "{...}"
        },
        "worker_id_2": {
            "delete": "...",
            "certainty": "Certain|Somewhat certain|Uncertain",
            "explanation": "{...}"
        },
        "worker_id_3": {
            "delete": "...",
            "certainty": "Certain|Somewhat certain|Uncertain",
            "explanation": "{...}"
        },
        "worker_id_4_maybe": {
            "delete": "...",
            "certainty": "Certain|Somewhat certain|Uncertain",
            "explanation": "{...}"
        }
    }
}
```
``` shell
Counts:
    1,283 sentences where consensus is to delete neither word
    1,720 sentences where consensus is to delete a single word
       16 sentences where consensus is to delete both words
    -----
    3,019 sentences total
```
