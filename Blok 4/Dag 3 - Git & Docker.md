Kahoot quiz over git -> opsturen voor 10 uur naar email Nico

### git switch vs git checkout:
Met checkout kan je switchen, maar ook werk wat je lokaal hebt staan ongedaan maken.
git checkout -- features/ziekenhuis.md
Hetzelfde als git restore .
Dit checkout is oud en is een soort bug waar het voor 2 verschillende functionaliteiten zorgt.

### Git merge strategieen:
Git merge --squash branchname
git commit voordeel: lineaire geschiedenis en vaak netter.

Git commit

git tag v1.0 -> create new tag
git tag -> lijst met tags

### States of Tracking
untracked (nadat je een file toevoegt)
unmodified (na git commit) (zie je niet met git status)
modified (na het wijzigen van een file)
staged (als je git add .)

git diff:
zien wat je hebt toegevoegd.

git reset:
undo your code changes, om een fout op te lossen.
git reset hashcode
