## 
[<p align="center">
  <strong>[STAGE DE MEMOIRE DE MASTER 1 : ANALYSE BIOINFORMATIQUE DES DONNEES DE SEQUENCAGE SHOTGUN](titre) </strong>
</p> 

 <img width="414" height="122" alt="image" src="https://github.com/user-attachments/assets/0ea6c372-5c49-4cb4-9afa-5731d155801b" />  |<img align="right" width="250" height="103" alt="image" src="https://github.com/user-attachments/assets/6198ae93-0de2-43a4-8a68-aa808c83b899" />   

      
<p align="center">
  <strong>EQUIPE 1 Culturomics</strong>
</p> EQUIPE CULTUROMICS    

Culture bacterienne                |  Extraction ADN
:------------------------------:|:-------------------------:
<img align="left" width="420" height="353" alt="Image" src="https://github.com/user-attachments/assets/002d21a4-f70e-44fd-bb4f-4b96e2884d04" />                |   <img align="right" width="500" height="300" alt="Image" src="https://github.com/user-attachments/assets/ff3a5b98-1ae5-45d4-9696-b099728895ca" />
<img src="https://github.com/Joseph7e/HCGS-Genomics-Tutorial/blob/master/fragmentation3.png?raw=true" width="800">   


## [🔵Description : ](description)    
Cette étude portant sur le microbiote chez enfants atteints de malnutrition aigue sévère a pour but de faire la caractérisation du génome d'*Escherichia marmotae*  grâce au séqence du génome entier(le whole génome sequencing, WGS) et la culture sélective sur Mac Conkey (MC) sur des échantillons de selles provenants d'enfants atteints de malnutrition aiguë sévère en République Démocratique du Congo (RDC). Cette bactérie Gram négative de la famille des *Enterobacteriaceae* est souvent confondue à *E. coli* du fait de sa promiximité génomique et ne présentant que 10% de différence sur l'ensemble de son génome. De plus, des études récentes ont montrés une certaine résistance aux antibiotiques notamment àla famille des betalactamines mais égalemment des cas de septiémie chez l'homme.

**📌Objecif :** L'objectif de cette étude est d'isoler cette bactérie en culture pour pouvoir caractériser son génome grâce à l'analyse bioinformatique.  

 **📍Echantillons** :
 Nos échantillons ont été selectionnées sur la base d'un précédent shotgun qui a montré une fréquence élevée en *Escherichia coli*, *Escherichia marmotae* et *Escherichia fergusonii*.      

 Sur cette repository, nous avons chargé l'ensemble des fichiers et scripts nécessaires pour analyser ces données.
## [__TABLE DES MATIERES__](Table)   
*  [__Contrôle qualité__](contrôle)
   * fastqc  
*  [__Correction des reads__](correction)
   * Trimmomatic v.0.39
*  [__Assemblage__](assemblage)
   * spades
*  [__Annotation du génome__](annotation)
   * prokka
*  [__Recherche de gène(s) et/ou de plasmide(s) de virulence__](virulence)
   * Abricate
   * VFDB
   * Plasmidfinder
*  [__pangenome__](pan)
   * roary
*  [__Average Nucleotidique identity__](average)
   * FastANI
*  [__Typage des souches d'*Escherichia*__](typage)
   * mlst
*  [__Construire d'arbre phylogénétique__](tree)
   * IQtree
   * MEGA v.11
 


**1) Création des environnements conda**
````
conda create -n amr -c bioconda -c conda-forge -y
conda create -n busco -c bioconda -c conda-forge -y
conda create -n abricate -c bioconda -c conda-forge -y
conda create -n mlst -c bioconda -c conda-forge -y
````
Explication des paramètres :

  conda create : Permet de créer un environnement conda  
  -n : donne le nom de l'environnement  
  -c : ajoute un channel dans l'environnement  
  -y : répondre "yes" à tout
