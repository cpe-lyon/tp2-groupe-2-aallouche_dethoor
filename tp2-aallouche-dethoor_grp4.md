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
 


 
 
 
 
 ## Exercice 2
 
 ```bash
 jaune='\e[1;33m'
neutre='\e[0;m'
pass="linux"
echo -e "${jaune}Entrez votre password de test${neutre}"
read passtest

if  [ $passtest == $pass ]
then
        echo "Mot de passe correct"
else
        echo "Mot de passe incorrect"
fi
 
 ...
 
