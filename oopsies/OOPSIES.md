# Oopsies cards

These cards reflect the current state of your company's security posture. They may have minimal impact or a bigger one. They will also cost more or less resources to be fixed.

The card does need a specified target. The target is the part of your company which will be evaluated when an incident happens. The example below will be evaluated whenever your
log server had an incident.

The data format is a simple JSON with the structure:

{
    "title": "Information Leakage",
    "description": "Your logs contain personal information",
    "incidentTarget": ["logserver"], 
    "fix": 1 - 3 resources,
}

{
    "title": "Credit Card Data",
    "description": "You store credit card numbers, cardholder names and checksum together in clear text in your database.",
    "incidentTarget": ["database, backup"], 
    "fix": 3 - 18 resources,
}