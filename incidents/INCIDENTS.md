# Incident cards

This folder holds incident cards describing security incidents which have happened at the company.
Depending on your current "oopsies" they may or may not have an impact on the company. The impact may vary,
e.g. loss of revenue due to loss of reputation, pay a fee or be put out of business, be charged and go to jail and lose the game.

The data format is a simple JSON with the structure:

{
    "title": "Website Defaced",
    "description": "Someone used your website to propagate hate speech",
    "condition": "Unpatched frontend vulnerability",
    "result: "Lose 25% revenue for the next 5 rounds"
}

{
    "title": "DDOS Attack",
    "description": "Your services are not responding anymore - seems someone is targeting them to keep them down!",
    "condition": "No DDOS mitigation in place",
    "result: "Lose 50% revenue for the next 3 rounds"
}

{
    "title": "Vulnerable Image",
    "description": "One of your teams picked an OS image that contained a backdoor - and now people are mining bitcoins on your system.",
    "condition": "No guardrails for image selection",
    "result: "Lose 30% revenue for the next 3 rounds"
}

{
    "title": "Poisoned Dependency",
    "description": "You always pull build dependencies from a public mirror - someone replaces the dependcy with one with a backdoor and breaks in",
    "condition": "no dependency mirror",
    "result: "Lose 30% revenue for the next 3 rounds"
}