# Aegisub_CorrectPonct
Script de correction de ponctuation typographique en Lua pour Aegisub

	 CorrectPonct
	 Copyright (C) 2014-2016 LeSaint

	 To contact me (bug report / evol) : LeSaint_Fansub {at} hotmail {dot} fr
	 This program is free software: you can redistribute it and/or modify
	 it under the terms of the GNU General Public License as published by
	 the Free Software Foundation, either version 3 of the License, or
	 (at your option) any later version.

	 This program is distributed in the hope that it will be useful,
	 but WITHOUT ANY WARRANTY; without even the implied warranty of
	 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
	 GNU General Public License for more details.

	 You should have received a copy of the GNU General Public License
	 along with this program.  If not, see <http://www.gnu.org/licenses/>.

Ce script, � utiliser sur le logiciel Aegisub permet de corriger la ponctuation typographique de sous-titres fran�ais.
Le script g�re les commentaires (lignes commentaires, ou tags) ce qui permet de garder la mise en forme, si pr�sente.
Il corrige les probl�mes d'espaces double, d'espaces autour de ponctuation, de guillemets, g�re certains caract�res ou motifs "sp�ciaux" comme le point de suspension, les acronymes.
Voyez la release note pour plus de d�tails, et testez-le !

Release Note:
v1.7
- effet de bord avec des espaces autour de \N sur une correction en 1.6

v1.6
- correction d'espaces restant avant un \N lors d'ex�cutions successives du script
- mauvais espaces autour de guillemets si entour� d'apostrophe.
- probl�me d'espace avant points de suspension dans certains cas (notamment si les points de suspension suivent directement des guillemets)
- correction pour �viter d'avoir plusieurs fois le tag "{ErrGuillemets}" en d�but de ligne si le script est lanc� plusieurs fois. 
  (Pour rappel, cette erreur n'apparait que si les guillemets initiaux sont des guillemets droits (non fran�ais))

v1.5
- prise en charge de l'espace ins�cable fine (utilis�e pour le point virgule, le point d'exclamation, le point d'interrogation), avec espace ins�cable pour les deux-point et les guillemets

v1.4
- correction pour prise en charge nouvelle version aegisub (� partir de 3.1)

v1.3
- espace ins�cable autour des guillemets fran�ais si utilisation de l'espace ins�cable demand�

v1.2
- Prise en charge des nombres d�cimaux (pas d'espace apr�s . ou , si c'est un s�parateur d�cimal)
- Prise en compte des symboles mon�taires ($, �, � et � pris en charge)
- Prise en compte des acronymes (compos�s d'un ensemble de lettres majuscules, chacune suivie d'un point, comme "A.C.M.E") (id�e de Fenounet)
- Remplacement des doubles apostrophes (droites ou non) comme des guillemets. (id�e de Fenounet)

v1.1
- Correction de bug : Lors d'un texte contenant "\N(", le \ devant le N �tait dupliqu� � chaque ex�cution. (Merci Jikan ^^)

v1.0beta2 :
- Ajout du choix des points de suspension, de l'utilisation des espaces ins�cables et du type d'apostrophe