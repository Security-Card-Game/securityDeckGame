# Event cards

This folder holds event cards which are have no direct impact on the security part of the company.
However, they may have impact on revenue or other things, e.g. one CTO is not available or something else.

The data format is a simple JSON with the structure:

{
    "title": "Normal Day",
    "description": "Relax, just a normal day.",
    "action: "Nothing happens"
}

{
    "title": "New Hire",
    "description": "Your company hired a new person who now needs to get onboarded.",
    "action: "Increase the next resource costs for a fix by 1."
}

{
    "title": "Security Training",
    "description": "You've just received a really valuable training! Your awareness increased, you know what needs doing and how to fix issues - you still need to get resources to do so.",
    "action: "Decrease the next resource costs for a fix by 2."
}

{
    "title": "Dependency License Change",
    "description": "One of your key dependencies suddenly changes their license so you cannot use it anymore in a legal manner and have to rewrite your solutions.",
    "action: "Increase the next resource costs for a fix by 5."
}

{
    "title": "Bug Bounty",
    "description": "You have a bug bounty program running. One security researcher submitted a valid finding that needs to get fixed.",
    "action: "Increase the next resource costs for a fix by 3."
}