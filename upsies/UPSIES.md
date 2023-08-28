# Upsies cards

This cards reflect the current state of your companies security. They may hav a minimal impact or a bigger one. They will also cost more or less resources to be fixed.
The card does need a target sepcified. The target is the part of your company which will be evaluated when an incident happens. The example below will be evaluated whenever your
log server had an incident.

The data format is a simple JSON with the structure:

{
    "title": "Information leakage",
    "description": "Your logs contain personal information",
    "incidentTarget": ["logserver"], 
    "fix": 1 - 3 resources,
}

{
    "title": "Credit Card Data",
    "description": "You store credit card numbers, holder names and checksum together in clear text in your database.",
    "incidentTarget": ["database, backup"], 
    "fix": 3 - 18 resources,
}