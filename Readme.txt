1) d�compresser les deux dossiers (libs et MenuNavigationMyscript) dans un dossier

2) Ouvrez avec android SDK le projet MenuNavigationMyscript

3) Ex�cutez le projet 

(si cela ne marche pas � cause du certificat, recr�ez un nouveau certificat : 
l'id de ce certificat est le nom du package dans androidManifest.xml)




Dans ce projet avec les onglets :

1) Je n'ai pas r�ussi � mettre plusieurs onglets avec plusieurs widgets de MyScript 
(c'est � cause de probl�mes concurrents : 2 widgets ne peuvent pas s'�x�cuter sur la m�me thread. Il faudrait donc g�rer cela autrement)

2) Aller dans l'onglet "Exercices" afin de consulter les diff�rents exercices

3) Pour changer d'exercice, appuyer sur changer : on g�n�re un exercice diff�rent al�atoire

4) Tous les champs commen�ant par @ sont des "Android annotations". Tu peux chercher sur google ou sur le document qui est sur le drive 
(Serge tah� - Introduction � la programmation de Tablettes android....)