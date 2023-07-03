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
git reset HEAD~1 (vanaf je HEAD 1 commit terug)

git revert:
de betere reset

### .gitignore
Je wilt in je source control geen build output hebben staan.
Oplossing is door .gitignore file toe te voegen.
Gebruik github.com/github/gitignore

.gitkeep file:
Om lege folders toe te voegen aan git


### switch naar een vroegere commit
git switch --detach hashcode
Hierna moet je een branch maken, anders verlies je je werk als je aanpassingen doet.