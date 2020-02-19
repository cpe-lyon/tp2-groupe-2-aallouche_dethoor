# Compte rendu TP2

## Exercice 1

1. Les commandes tapées par l'utilisateur sont dans :  
  * **usr/bin**
  * **usr/local/sbin**
  * **usr/local/bin**
  * **usr/sbin**
  * **usr/games**
  
 2. On utilise comme argumment **$HOME**. La variable $HOME contient le chemin absolu vers le répertoire personnel de l'utilisateur connecté.
 
 3.  
* la variable **LANG  détermine la langue que les logiciels utilisent pour communiquer avec l'utilisateur. 
 * La variable **$PWD contient le chemin absolu vers le répertoire courant (permet de savoir où on est dans l'arborescence).
 * La variable **$OLDPWD contient le chemin absolu vers le répertoire courant précédent (permet de savoir d'où on vient).
 * **$SHELL indique l'interpréteur shell utilisé par défaut
 
 4. 
 **MY_VAR=2**
 
 5. 
 La commande **bash** affiche un nouveau bash. Toutes les variables locales sont supprimées mais les variables d'environnements sont conservées.
 
 6.
 Nous pouvons  créer une variable d'environnement pour le shell en cours avec la commande : **export MY_VAR= /etc/appli**. Lorsque j'execute la commande **bash** les variables locales sont supprimées mais pas les variables d'environnement, ce qu'est **MY_VAR**.
 
 7.
 **NOMS='AALLOUCHE DETHOOR'**. Pour afficher et verifier la valeur de la variable **NOMS**, j'execute **echo $NOM** 
 
8.
La commande pour afficher "Bonjour a vous deux, binome1 binome 2" est : **echo "Bonjour a vous deux, $NOMS "**

9. 
**unset** est la commande qui supprime la variable rentrée en parametre. Alors que si on donne aucune valeur a une variable, elle est tout de meme crée. Elle n'aura juste aucune valeur, mais sera quand meme présente.

10.
Pour afficher "$HOME=*chemin*" j'execute echo "\$HOME=$HOME"

### Programmation Bash ###
Apres avoir créer le dossier script dans le repertoire personnel, il faut renseigner le chemin dans le PATH pour pouvoir executer les programmes contenus dans ce dossier peut importe ou nous sommes dans l'arborescence. La commande est : **export PATH=$PATH:/home/ahmedaall/script**
 
 
 
 
 ## Exercice 2
 
 ```bash
 jaune='\e[1;33m'
neutre='\e[0;m'
pass="linux"
echo -e "${jaune}Entrez votre password de test${neutre}"
read -s passtest

if  [ $passtest == $pass ]
then
        echo "Mot de passe correct"
else
        echo "Mot de passe incorrect"
fi
 
 ```
 
 ## Exercice 3
 
 ```bash
 #? /bin/bash

function is_number()
{
        re='^[+-]?[0-9]+([.][0-9]+)?$'
        if ! [[ $1 =~ $re ]] ; then
                return 1
        else
                return 0
        fi
}

is_number $1

if [ $? == 0 ]
then
        echo "c'est bien un nombre réél"
else
        echo "erreur"
fi
 ```
