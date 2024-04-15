# Redgrim Issues

This repository has the sole purpose of tracking issues and feature requests for the Redgrim project.

When reporting an issue, please provide as much information as possible, including the steps to reproduce the issue and
the related traceback if any.

Screenshots are also welcomed if relevant.

## Template

Try to follow this template, even partially, when creating a new issue:

---
When looking at a very old character, the command doesn't work and the following traceback is raised:

```
Traceback (most recent call last):
  File "/evennia/commands/cmdhandler.py",
line 628, in _run_command
    ret = cmd.func()
          ^^^^^^^^^^
  File "evennia/commands/default/general.py", line 88, in func
    desc = caller.at_look(target)
           ^^^^^^^^^^^^^^^^^^^^^^
  File "redgrim/typeclasses/characters.py", line 310, in at_look
    description = target.return_appearance(self, **kwargs)
                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "redgrim/typeclasses/characters.py", line 387, in return_appearance
    if limb in self.db.custom_limbs_desc:
       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
TypeError: argument of type 'NoneType' is not iterable
```

To reproduce the issue:
 - type `look character` in the game
---
## IMPORTANT

Just in case, please **DO NOT** include the complete File path in the traceback.

Remove server related data from the local path and keep only the relevant parts of the traceback.
    
    /xxx/xxx/redgrim/typeclasses/characters.py
    /xxx/xxx/evennia/commands/default/general.py

should become
    
    redgrim/typeclasses/characters.py
    evennia/commands/default/general.py

In the event that the traceback is too long, only include the lowest relevant part or send the traceback on Discord.