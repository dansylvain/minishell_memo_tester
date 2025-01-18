# minishell_memo_tester


## Introduction
Ce dossier contient un testeur de mémoire pour le projet Minishell. Il est conçu pour détecter les fuites de mémoire dans le code du Minishell.

## Installation
Pour utiliser ce testeur, clonez directement ce dossier à la racine du projet Minishell.

## Exécution
Pour exécuter le testeur, placez-vous dans le dossier du testeur et exécutez le script memory_check.sh en passant un fichier de commandes en argument. Par exemple :

```bash
./memory_check.sh commandes.txt
```

Vous pouvez personnaliser les fichiers de commandes pour tester les commandes que vous souhaitez.

## Résultats
Si des fuites de mémoire sont détectées, la sortie de Valgrind sera affichée sur la sortie standard. Il est important de vérifier que les fonctions responsables des fuites évoquées dans la sortie Valgrind ne sont pas ignorées.

## Attention
Malgré le fait que la plupart des fuites inhérentes à des fonctions du type cat, ls, grep, etc. sont ignorées, certaines fuites ne sont pas ignorées. Il est donc important de vérifier que les fonctions responsables des fuites évoquées dans la sortie Valgrind ne sont pas compromettantes.

## Sortie Valgrind
Lorsqu'une fuite provoque des fuites "definitely lost", la sortie de Valgrind sera en rouge.

## Exemple d'utilisation
Pour tester les commandes contenues dans le fichier commandes.txt, exécutez la commande suivante :

```bash
./memory_check.sh commandes.txt
```

Si des fuites de mémoire sont détectées, la sortie de Valgrind sera affichée sur la sortie standard.