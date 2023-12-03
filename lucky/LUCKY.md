# Lucky cards

This folder holds lucky (joker) cards which may prevent or lessen the impact of an incident, or may allow to save resources fixing an oopsie.

The data format is a simple JSON with the structure:

{
    "title": "Awesome Employee",
    "description": "You just got lucky, you hired a really skillful person",
    "result: "Reduce the resource costs for a fix by 2. Then discard this card."
}

{
"title": "None Of Our Business",
"description": "The vulnerability reported simply does not apply to you, the dependency version is not in use, the configuration settings are fine, the related piece had been removed already. Lucky you!",
"result: "Reduce the resource costs for a fix by 5. Then discard this card."
}