# Ligne de tri automatique par couleur

## Identification
- Numéro du sujet : 22
- Classe : 1GII1
- Encadrante : Dr-Ing Ferdaous Masmoudi
- Membres du groupe :
  - Ayman Feki — Phase 1 (cahier des charges), Phase 3 (modélisation), CAO FreeCAD
  - Ismail Abaoub — Phase 2 (bibliographie), Phase 4 (simulation MATLAB), GitHub
  - Karim Boudaya — Rédaction Overleaf, Gestion Agile (GitHub Projects), Zotero
- Dernière mise à jour : 2026-11-22
- Statut de chaque phase : P1 [corrigée], P2 [corrigée], P3 [corrigée], P4 [corrigée], P5 [prévu 29/11], P6 [prévu 29/11], P7 [prévu 29/11]

## Liens vers les espaces de travail (vérifier le partage)
- Google Drive (ce dossier) : [À compléter]
- GitHub — code et historique : https://github.com/ismail3b3-netizen/Mini-projet-automatique/tree/main
- GitHub Projects — tableau Agile : [À compléter]
- Overleaf — rapport scientifique : [À compléter]
- Overleaf — préfabrication : [prévu le 29 novembre]
- Zotero — bibliothèque de groupe : [À compléter]
- Google Sheets — Gantt : [À compléter]
- MATLAB (script principal) : `04_Simulation_et_code/src/simulation_moteur_tri.m`
- Simulink Online / MATLAB Drive : [fichiers locaux disponibles dans 04_Simulation_et_code/src/]
- Autres logiciels et versions : MATLAB R2018b+, FreeCAD 0.21, Overleaf (LaTeX)

NE JAMAIS donner un mot de passe, un jeton d'accès ou un accès au compte personnel.
Inviter uniquement l'encadrante aux projets utiles, selon les permissions appropriées.

## Inventaire des livrables
| Phase | Livrable / chemin | Statut | Vérifié par | Date |
|---|---|---|---|---|
| P1 | 01_Cahier_des_charges/Cahier_des_charges_corrige.pdf | vérifié | Ayman Feki | 2026-11-22 |
| P1 | 01_Cahier_des_charges/Schema_fonctionnel.pdf | vérifié | Ayman Feki | 2026-11-22 |
| P2 | 02_Bibliographie_Zotero/Etat_de_l_art.pdf | vérifié | Karim Boudaya | 2026-11-22 |
| P2 | 02_Bibliographie_Zotero/Tableau_comparatif.pdf | vérifié | Karim Boudaya | 2026-11-22 |
| P2 | 02_Bibliographie_Zotero/references.bib | vérifié | Karim Boudaya | 2026-11-22 |
| P3 | 03_Modelisation/Modele_math_corrige.pdf | vérifié | Ayman Feki | 2026-11-22 |
| P3 | 03_Modelisation/Parametres.csv | vérifié | Ismail Abaoub | 2026-11-22 |
| P4 | 04_Simulation_et_code/src/simulation_moteur_tri.m | vérifié | Ismail Abaoub | 2026-11-22 |
| P4 | 04_Simulation_et_code/README_execution.md | vérifié | Ismail Abaoub | 2026-11-22 |
| P4 | 05_Resultats_figures_csv/analyses/Analyse_des_performances.md | vérifié | Ismail Abaoub | 2026-11-22 |
| Overleaf | 06_Rapport_Overleaf/sources_tex/rapport_complet.tex | vérifié | Karim Boudaya | 2026-11-22 |
| Overleaf | 06_Rapport_Overleaf/Rapports_intermediaires/ | vérifié | Équipe | 2026-11-22 |
| Agile | 07_Gestion_Agile/Backlog.csv | vérifié | Karim Boudaya | 2026-11-22 |
| Agile | 07_Gestion_Agile/Compte_rendu_sprint.md | vérifié | Ayman Feki | 2026-11-22 |
| Agile | 07_Gestion_Agile/Gantt_sprint.xlsx | vérifié | Karim Boudaya | 2026-11-22 |
| Archives | 10_Archives_et_versions/Corrections_P1_P4.pdf | vérifié | Équipe | 2026-11-22 |

## Reproduire une simulation

- **Environnement / version logiciel** : MATLAB R2018b ou plus récent — aucune toolbox obligatoire (Control System Toolbox facultative pour la figure 10)
- **Fichier de démarrage** : `04_Simulation_et_code/src/simulation_moteur_tri.m`
- **Paramètres** : Section 1 du script MATLAB et `03_Modelisation/Parametres.csv`
- **Comment lancer** : ouvrir le script dans MATLAB et cliquer sur **Run** (ou `>> simulation_moteur_tri`)
- **Résultat attendu** : 12 figures PNG 300 DPI dans `figures/` + fichiers `.fig` MATLAB + CSV dans `resultats/`
- **Fichier CSV obtenu** : `sim1_boucle_ouverte.csv`, `sim2_boucle_fermee_PI.csv`, `sim5_perturbation_BO/BF.csv`, `sim6_resultats_tri.csv`, `conformite_cahier_des_charges.csv`
- **Test de changement d'un paramètre** : modifier `P.KP_OVERRIDE` ou `P.KI_OVERRIDE` dans la section 1.3 ; observation : le dépassement et le temps de réponse changent, le tableau de conformité est mis à jour automatiquement

## Tableau des corrections
| Remarque de l'enseignante | Correction faite | Fichier / preuve | Statut |
|---|---|---|---|
| Dépassement BF trop élevé dans Table 4.2 | Recalibrage de Kp et Ki via placement de pôles dans MATLAB | simulation_moteur_tri.m section 1.3 | corrigé |
| Unités du couple à revérifier (120 N·m) | Mention explicite [HYP] dans le code MATLAB et Parametres.csv | Parametres.csv ligne CR_nom + commentaires .m | noté, à confirmer sur montage réel |

## Travail Agile / Scrum allégé
- Objectif du sprint 1 (jusqu'au 22/11) : corriger P1–P4 ; modèle et simulation MATLAB reproductibles.
- Backlog / tableau : [lien GitHub Projects — À compléter]
- Responsables par tâche : [lien vers les Issues GitHub — À compléter]
- Bilan : `07_Gestion_Agile/Compte_rendu_sprint.md`
- Gantt : [lien Google Sheets — À compléter]

## Utilisation de l'intelligence artificielle
- Assistance utilisée : aide à la rédaction des sections du rapport, vérification des unités et des équations, correction du modèle mathématique
- Vérifications humaines effectuées : équations relues et comparées aux datasheets, code MATLAB exécuté et validé, résultats CSV vérifiés numériquement, références bibliographiques consultées
- Limites ou points restant à vérifier : paramètres Km et τm (R_A, L_A, Kt, Ke, J, f) à identifier expérimentalement ; unités du couple nominal (120 N·m) à confirmer sur fiche technique originale

## Déclaration du groupe
Nous nous engageons à pouvoir expliquer les éléments remis, à distinguer les simulations
et les mesures réelles, et à signaler honnêtement les contributions d'outils IA.
