# Oopsies cards

These cards reflect the current state of your company's security posture. They may have minimal impact or a bigger one. They will also cost more or less resources to be fixed.

The card does need a specified target. The target is the part of your company which will be evaluated when an incident happens. The example below will be evaluated whenever your
log server had an incident.

The data format is a simple JSON with the structure:

{
    "title": "Information Leakage",
    "description": "Your logs contain personal information.",
    "incidentTarget": ["logserver"], 
    "fix": 1 - 3 resources,
}

{
    "title": "Credit Card Data",
    "description": "You store credit card numbers, cardholder names and checksum together in clear text in your database.",
    "incidentTarget": ["database, backup"], 
    "fix": 3 - 18 resources,
}

{
    "title": "Secret Leakage to API Client Cloud",
    "description": "You find that people use the cloud backup to store their API client's requests - and they contain secrets like confidential API keys!",
    "incidentTarget": ["services, backup"],
    "fix": 3 - 9 resources,
}

{
    "title": "DDOS Self-Attack",
    "description": "Your services are suddenly not responding anymore... Until you figure out that this is caused by your own actions. You've been basically ddossing yourself!",
    "incidentTarget": ["services, database"],
    "fix": 3 - 9 resources,
}

{
    "title": "Secret Leakage to Version Control System",
    "description": "Not again - you committed a secret to your version control system. Sigh.",
    "incidentTarget": ["version-control-system"],
    "fix": 3 - 12 resources,
}

{
    "title": "Container images are not scanned",
    "description": "An engineer reports an issue with an image used to build a container. The engineer suggests to integrate a container image scanner into your pipeline.",
    "incidentTarget": ["image selection"]
    "fix": 2-6 resources
}

{
    "title": "Dependeny Mirror",
    "description": "You do not mirror external build dependencies. Engineers point out the risks of broken build caused by missing dependencies and also the security risks in accidentially use non-reviewed depnendecies",
    "incidentTarget: ["build", "production", "development"]
    "fix": 1 - 3 resources
}

{
    "title": "User rights in Local Storage",
    "description": "Your shiny webapp stores a matrix of user rights in the users browser. The user can edit this rights and can gain privileges",
    "incidentTarget: ["webserver", "frontend", "data integrity"]
    "fix": 3 - 12 resources
}