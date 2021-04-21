# Projet-cripting
#!/bin/bash
 

executegnuplot()
{
	cd ~/MiniProjet
	gnuplot config
}
exlsblk()
{
	yad --text "`lsblk`"
}
afficherlsblk()
{
	yad --text "`cat sauvegarde.txt`"
}
afficherdf()
{
	yad --text "`cat sauvegarde1.txt`"
}
afficherhelp()
{
	echo "	-lblk : affiche les caracteristique hardware des devices  "
	echo "	-ldf :  affiche la liste des block devices "
	echo "	-plot : pour afficher les courbe "
	echo "  -gnuplot : pour afficher les courbes camembert"
	echo "	-s :  pour sauvegarder quelques des resultats retourne par -lblk et -ldf"
	echo "	-m : pour afficher le Menu"
	echo "	-g : pour le Menu graphique avec YAD "
	echo "	-h : pour l'aide" 
}
afficheryadhelp()
{
	yad --text "`afficherhelp`"
}
afficheryadhelp()
{
	yad --text "`afficherhelp`"
}
execlsblk()
{
	lsblk>sauvegarde.txt
	echo "sauvegarde reussi"
	yad --text "sauvegarde reussi"    
}

exec_lsblk_mem()
{
	lsblk>sauvegarde.txt
	echo "cache    efuhfei   hcveiuvc        "
	awk ' /Mem:/ {print $1}' sauvegarde.txt
