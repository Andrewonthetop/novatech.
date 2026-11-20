# TP final Git - NovaTech
Nolan Tellier

## Mission 5 
Git n'a pas fusionner automatique car les deux branches on du modifier la meme ligne du meme fichiers differament , il ne savais donc pas quelle version garder  donc j'ai choisie de garder novatech l'innovation au quotidien 


## Mission 6 
1. Identifiant court du premier commit : b7d162e
2. Commit de l'ajout de la page Contact : d0f2c58 (ajout de contact)
3. Nombre de commits : 9
4. Commande pour afficher l'historique en graphique : git log --oneline --graph --all

Commande utilisée pour examiner un commit de la fonctionnalité Contact : git show d0f2c58

## Mission 7
j'ai corrige le message avec git commit --amend, ca remplace le dernier commit au lieu d'en refaire un autre donc y'a qu'un seul commit

## Mission 8
j'ai fait git restore index.html pour remettre le fichier comme au dernier commit, puis git status pour verifier que c'etait propre

## Mission 9
j'ai utilise git reset --mixed HEAD~1
ca enleve le commit mais la modif reste dans le fichier, parce que mixed touche pas aux fichiers
avec git reset --hard HEAD~1 la modif aurait ete supprimee aussi

## Mission 10
j'ai utilise git revert HEAD
ca cree un nouveau commit qui annule l'ancien, le commit "Ajout promotion" reste dans l'historique
c'est different de reset car reset supprime le commit, et si les autres l'ont deja recupere ca pose probleme

## Mission 11
j'ai fait git stash -u pour mettre equipe.html de cote (le -u car c'etait un nouveau fichier), j'ai fait la correction et le commit, puis git stash pop pour recuperer mon travail

## Mission 12
j'ai cree un .gitignore avec *.log, cache/, .env et .vscode/ et j'ai verifie avec git status qu'ils apparaissent plus

## Questions finales
1. zone de travail = les fichiers que je modifie, staging = ce que j'ai ajoute avec git add, historique = les commits
2. pour pas casser main pendant qu'on developpe, on fusionne quand c'est fini
3. quand 2 branches modifient la meme ligne, on choisit la bonne version, on enleve les marqueurs puis git add et git commit
4. reset supprime le commit (en local seulement), revert le garde et cree un commit qui l'annule (pour un commit partage)
5. quand on doit changer de tache en urgence sans faire un commit pas fini
6. HEAD c'est le commit ou on est actuellement
7. HEAD~2 c'est 2 commits avant HEAD
8. le local c'est sur mon pc, le distant c'est sur github, on envoie avec git push
9. c'est plus facile de comprendre l'historique et d'annuler une seule modif si besoin
10. parce que certains fichiers sont temporaires (logs, cache) ou contiennent des mots de passe (.env)
