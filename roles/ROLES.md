# Roles cards

These are the roles you can play. You need at least one C-level and one staff-level card.

The data format is a simple JSON with the structure:

{
    "title": "Staff",
    "description": "Normal staff employee. You may not take resources from the company pile.",
    "role: "STAFF"
}

{
    "title": "Middle Manager",
    "description": "You may decide on a lot of things on your own and use money from the company pile to spend and distribute - within limits.",
    "role: "MANAGEMENT"
}

{
    "title": "CISO",
    "description": "You are accountable for the company's security posture. You may use money from the company pile to spend and distribute. Your decisions can be overruled by the CEO.",
    "role: "CLEVEL"
}

{
    "title": "CTO",
    "description": "You are accountable for technical strategy of the company. You may use money from the company pile to spend and distribute. Your decisions can be overruled by the CEO.",
    "role: "CLEVEL"
}

{
    "title": "CEO",
    "description": "You are accountable for the company. Period. You may use money from the company pile to spend and distribute. No one can overrule your decisions, yet people can decide to leave.",
    "role: "CLEVEL"
}