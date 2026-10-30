# Skill import examples

Generated dummy repositories for testing skill discovery. No credentials or application configuration are included.

In n8n, select **Create skills → Connect to GitHub**. Paste a scenario's folder URL below. Use the folder URLs, not the repository root: the root combines all scenarios, including a broken manifest.

| Scenario | Folder URL | Expected result |
| --- | --- | --- |
| Groups and skipped files | https://github.com/DeveloperTheExplorer/skill-discovery-preview/tree/main/grouped | Writing and Engineering groups, three selectable skills, four skipped files, an external plugin notice. |
| Broken manifest | https://github.com/DeveloperTheExplorer/skill-discovery-preview/tree/main/fallback | Flat list with a warning, three selectable skills, two blocked rows. |
| Specific subfolder | https://github.com/DeveloperTheExplorer/skill-discovery-preview/tree/main/grouped/plugins/writing/skills/brand-voice | Only brand-voice. No parent group or sibling skills. |
| Cursor custom paths | https://github.com/DeveloperTheExplorer/skill-discovery-preview/tree/main/cursor-custom | editorial is grouped; legacy remains selectable outside the group. |
| Description boundary | https://github.com/DeveloperTheExplorer/skill-discovery-preview/tree/main/long-description | One valid skill with a 1024-character description. |
| External entries only | https://github.com/DeveloperTheExplorer/skill-discovery-preview/tree/main/external-only | An external plugin notice with no selectable local skills. |
| Starter skill | https://github.com/DeveloperTheExplorer/skill-discovery-preview/tree/main/starter | team-writing-guide and one reference file. |

The grouped and fallback examples share skill names. Inspect both pickers before importing, or use separate project scopes to avoid name conflicts.

The external plugin points to a dummy repository. The sample script is inert. n8n should list it as skipped.
