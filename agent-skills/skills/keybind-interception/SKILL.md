---
name: keybind-interception
description: Map keyboard shortcuts across the user's apps, identify conflicts and actual usage, and guide fixes through recommended multiple-choice decisions.
---

# keybind interception

1. Inventory installed and running apps, OS shortcuts, remappers, and tools inside terminals or editors. Collect available effective bindings, overrides, and contexts from config, exports, menus, and authoritative docs. Record coverage and anything still unknown.
2. Use available recent activity and stated preferences to identify the apps and shortcuts the user uses. Mark observed use, user-confirmed use, and unknown use separately. Missing activity leaves use unknown.
3. Build one map with shortcut, action, app or layer, context, usage, conflicting binding, recommended fix, and source. Trace which layer receives the key first. Shared keys conflict when their active contexts overlap.
4. Present a recommended setup based on that map. Use the host's multiple-choice question tool to resolve choices, with the recommendation first. Each question names the competing actions and explains what each choice changes. Batch independent choices. Ask about important usage gaps the same way.
5. Apply the selected fixes in the config that owns each binding, reload as needed, and verify automatically where possible. Keep unrelated bindings and useful fallbacks. Request a physical key check only when needed, using multiple-choice outcomes such as works, wrong action, or no action.
6. Update the map as decisions land. Continue until every identified conflict is fixed, intentionally kept, dropped, or blocked with a specific reason. Report any verification still pending.
