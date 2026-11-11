---
name: keybind-interception
description: Trace keyboard shortcuts that trigger the wrong action or never reach the intended app. Use to diagnose and resolve one shortcut or audit a set of bindings.
---

# keybind interception

1. List each shortcut in scope, the focused app and mode, what it does now, and what the user wants it to do. For an audit, inventory the active bindings in the apps and layers in scope. Ask about desired behavior only where it changes the fix.
2. Reproduce one shortcut and trace it from the keyboard to the intended action. Check OS shortcuts, remappers, host apps such as terminals or editors, multiplexers or remote sessions, and the target app's active mode as applicable. Read effective bindings and their config sources. A config file or default by itself does not prove what is active.
3. Find the first layer that consumes or rewrites the key. Compare with a working shortcut or bypass one layer at a time. For terminal apps, check the bytes or key event the child receives and whether the target can decode that modifier. A host unbind and a target binding can both be necessary.
4. Make the smallest authorized edit in the source that owns the binding. Preserve unrelated shortcuts and existing fallbacks. Reload the affected layer or start a fresh target session if needed.
5. Test the original shortcut in the original context and verify the intended action plus any displaced shortcut the user wants to keep. A successful config parse only proves the file loads. If a physical keypress is needed, give the user one exact check and ask what happened.

Keep going through the list until each shortcut works, the user chooses to keep or drop it, or a specific blocker needs their input. Report the outcome per shortcut and identify what still needs a live check.
