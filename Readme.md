Purpose
=======

This module allows groups of users to edit own tags, and thus, creation of sophisticated
hierarchies of content using core taxonomy module and its field API integration. In other
words, this "nodifies" taxonomy terms. The module use only core taxonomy api and core
widgets (user autocomplete), no jquery additions.

Permissions added:
- Edit own terms in {vocabulary}
- Delete own terms in {vocabulary}
- Choose only own terms (global setting)

Schema:
- Table with tid/vid/uid (filled with uid 1 on install)

Todo:
- Choose only own terms for specified {vocabulary}
- hook_user_delete()
- massive change author (action/vbo)

Example usage:
Forget about book and node hierarchy modules. You want to create a website for poem
writers. Poem (an article) can be assigned to one of the pre-created poembooks (taxonomy).
The user may add own poembooks, and edit only own if granted. With FieldAPI integrated to
core taxonomy, you can create sophisticated poembooks, containing cover picture, ISBN
numbers etc. and assign poems to different poembooks (i.e. you want to create a selection
of already published poems in poembooks). You may restrict that users can assign poems to
only own or all poembooks.

Drawbacks:
The taxonomy terms are not treated the same as node/users/files. This means that you
cannot create revisions of terms (err... maybe other module would do that!) 
Maybe in D8 they will be first class citizens too.
