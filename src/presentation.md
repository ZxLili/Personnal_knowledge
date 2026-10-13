<style>
  details.admonition-navy {
    background: #0d1b2a;                      /* Fond bleu nuit très sombre */
    border: 1px solid #1b263b;                /* Bordure discrète */
    border-left: 4px solid #38bdf8;           /* Accentuation bleu glacier / cyan */
    border-radius: 8px;
    padding: 0.85rem 1.15rem;
    margin: 1.25rem 0;
    box-shadow: 0 4px 12px rgba(10, 25, 47, 0.4);
    font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    transition: all 0.2s ease-in-out;
  }

  details.admonition-navy summary {
    font-weight: 600;
    font-size: 1.9rm;
    color: #c2c2c2; 
    cursor: pointer;
    user-select: none;
    outline: none;
    display: list-item;
    list-style-position: outside;
    margin-left: 2.3rem;
  }

  details.admonition-navy summary:hover {
    color: #38bdf8;                           /* Éclaircissement cyan au survol */
  }

  .admonition-subtitle {
    font-size: 1.5rem;
    font-weight: 400;
    color: #64748b;                           /* Gris ardoise atténué */
    margin-top: 0.55rem;
  }

  details.admonition-navy[open] summary {
    margin-bottom: 0.85rem;
    padding-bottom: 0.65rem;
    border-bottom: 1px solid rgba(255, 255, 255, 0.08); /* Séparateur subtil */
  }

  details.admonition-navy .admonition-content {
    color: #94a3b8;                           /* Gris ardoise clair, très lisible */
    line-height: 1.6;
    /* font-size: 1rem; */
  }

  details.admonition-navy .admonition-content code {
    background: #1b263b;
    color: #7dd3fc;
    padding: 0.2rem 0.4rem;
    border-radius: 4px;
    font-size: 0.88em;
  }
</style>

<div class="hidden">
Au dessus on retrouve le style des boite qui sont deroulante.
Sous ce commentaire on retrouve le contenue de la page elle meme
</div>

# Lili ZHENG

> [!NOTE]
> Cette page va etre une page de presentation sur moi et mes projet, il a pour but d'ennumerer tout les projets/TPs interressant

## Parcours

Master SAR / SESI \_\_\_ 2024-2026
:

Licence Informatique \_\_\_ 2021-2024
:

Prepa PCSI - PSI \_\_\_ 2020-2021
: Mathématique (Philippe Doumal)
: Physique
: Chimie
: [SI] Science de l'ingenieur
: Anglais
: Philosophie

Bac S - SVT \_\_\_ 2017 - 2020
: Mathematique (Mme Dumail)
: Math Spé
: Histoire-Geographie
: SVT
: Sport
: Physique Chimie (Vidal-Cross)
: Francais / Philosophie (Emmanuelle Carlin)

## Projets

<details class="admonition-navy">
        <summary> 
        Modelisation Formelle et Verification d'une architecture multiprocesseur à mémoire partagée
        <div class="admonition-subtitle"> 
        oct 2025 - fev 2026
        </div>
        </summary>

Conception, modélisation formelle et vérification matérielle d'une plateforme multiprocesseur à mémoire partagée (3 cœurs, hiérarchie de caches L1 privés et bus partagé avec arbitrage).

Architecture & Protocoles Matériels : Modélisation d'une interconnexion par bus multiplexé (SPI) régi par un arbitre garantissant l'accès exclusif et séquentiel à la mémoire centrale.

Cohérence de Cache (Snooping) & Hiérarchie Mémoire : Implémentation de caches L1 avec politique d'écriture write-through et mécanisme d'espionnage de bus (Snoop-based cache coherence) pour invalider/mettre à jour les copies locales lors des écritures concurrentes.

Synchronisation Matérielle & Verrous : Extension de l'architecture pour intégrer des variables non cachables en mémoire dédiées à la gestion de verrous matériels (exclusion mutuelle et protection des sections critiques multi-cœurs).

Vérification Formelle (Model Checking) : Modélisation sous NuSMV ; formalisation et validation rigoureuse des propriétés de sûreté (safety) et de vivacité (liveness) via la logique temporelle (LTL / CTL) pour garantir l'absence d'interblocage (deadlock) et la cohérence stricte des données.

Compétences
: NuSMV
: Verification Formelle
: Protocole de cache L1
: Protocole de d'arbitrage d'acces au bus
: Interface de Bus

</details>

<details class="admonition-navy">
        <summary> 
        Optimisation d'un programme d'un systeme à N corp
        <div class="admonition-subtitle"> 
        déc. 2025 – févr. 2026
        </div>
        </summary>

Ce projet aussi appelé "Move ur Body".

Conception, implémentation et optimisation avancée d'un simulateur de problème à N corps en C++ et CUDA, explorant les limites matérielles du calcul intensif (HPC) sur le cluster Dalek (Ryzen 9 7945HX & NVIDIA RTX 4090).
(Description du cluster : https://dalek.proj.lip6.fr/ )

Réalisations & Résultats clés :

- Accélération CPU (Speedup ×254) : Réorganisation mémoire en SoA (Structure of Arrays), vectorisation SIMD (AVX2/AVX-512 via wrapper MIPP avec FMA et rsqrt) et parallélisation multithread OpenMP, atteignant 1,52 TFlops.
- Accélération GPU & Optimisation Mémoire : Développement de kernels CUDA hautement optimisés par tiling en mémoire partagée (shared memory), minimisant les accès à la mémoire globale et atteignant 36,8 TFlops sur 500 000 corps (~92 % de la limite théorique de la RTX 4090).
- Calcul Hétérogène & Distribué : Exploration de modèles hybrides CPU+GPU et distribution multi-nœuds/multi-GPU avec MPI (analyse des goulots d’étranglement PCIe, synchronisation MPI_Allgather et latence réseau).
- Progression globale des performances de 6 GFlops à 36,8 TFlops (gain de plus de 6 100×).

Compétences
: C/Cpp
: Parallelisation (MPI, thread, IPC...)
: Mipp / AVX512f
: Cuda
: ssh
: script de test (bash, make)
: optimisation ( deroulage de boucle, pipelining, calcul, specifique aux processeurs, vectorisation, gcc -O2 -O3 -O0 -O1)

</details>

<details class="admonition-navy">
        <summary> 
        Conception et implémentation d’une centrale de commande numérique DCC (Digital Command Control)  National Model Railroad Association sur FPGA
        <div class="admonition-subtitle"> 
        mars 2025 – mai 2025
        </div>
        </summary>

        https://www.nmra.org/index-nmra-standards-and-recommended-practices

Développement d’un système embarqué destiné au pilotage de trains miniatures via le protocole DCC.

Le projet s’est articulé en deux volets principaux (co-design HW/SW):

🔹 Conception matérielle (VHDL / FPGA Basys3)

Élaboration de modules dédiés : diviseur d’horloge, générateurs de bits, machine à états, registre DCC et temporisation

Génération continue et synchronisée de trames DCC conformes au protocole

Simulation, synthèse et validation sur FPGA avec analyse à l’oscilloscope

🔹 Intégration logicielle (MicroBlaze / AXI / Vitis)

Création d’une IP personnalisée pour la communication via bus AXI

Développement d’une interface de contrôle utilisateur (boutons, interrupteurs)

Implémentation d’un programme en C pour la transmission des commandes DCC et le pilotage en temps réel des locomotives

Résultats :
Respect des contraintes temps réel, conception VHDL modulaire, communication fiable entre matériel et logiciel, validation complète sur matériel physique.

Compétences
: C/Cpp
: carte Basys3 - FPGA Xilinx (Artix7)
: Vivado/Vitis
: Firmware
: BSP
: Automate Moore/Mealy
: simulation pre, post synthèse
: debuggage oscilloscope
: HDL (VHDL)
: SOPC (Microblaze-0 & AXI4-Lite)
: definition architecture
: developpement plateforme materiel et logiciel

</details>

<details class="admonition-navy">
        <summary> 
        Extension d'un système de fichiers — Block-sharing File System (Linux Kernel 6.5.7)
        <div class="admonition-subtitle"> 
        avr. 2025 – mai 2025
        </div>
        </summary>

Développement d’un module noyau Linux visant à améliorer l’efficacité du système de fichiers OuicheFS en introduisant un mécanisme de partage de blocs (block slicing) pour réduire le gaspillage d’espace lors de la gestion de nombreux petits fichiers.

Principales réalisations :

Refonte des fonctions read et write pour un accès direct au disque sans page cache (sb_bread, mark_buffer_dirty, sync_dirty_buffer).

Conception d’une nouvelle structure de stockage : blocs découpés en tranches (slices) avec métadonnées intégrées.

Implémentation d’un système sysfs exposant les statistiques du système de fichiers (blocs libres, efficacité, etc.).

Développement d’une commande ioctl pour l’inspection et le débogage des tranches en mémoire.

Gestion complète du cycle de vie des petits fichiers (écriture, lecture, suppression, libération des tranches).

Extension du support aux fichiers de toute taille avec bascule automatique entre stockage en tranches et stockage classique.

Étude des performances et comparaison avec l’implémentation standard du VFS.

Objectif atteint : réduction significative de la fragmentation interne et optimisation de l’utilisation de l’espace disque, tout en respectant les contraintes du noyau Linux et de la couche VFS.

Compétence
: C (Kernel)
: Qemu
: Git
: Systemes de fichiers
: Module Linux
: Bash
: optimisation de l'occupation des fichiers en disque
: Linux

</details>

<details class="admonition-navy">
        <summary> 
        Shell & Systèmes de fichier
        <div class="admonition-subtitle"> 
        janv 2025 - mai 2026
        </div>
        </summary>
KO6 est un système d’exploitation conçu à des fins pédagogiques. Initialement réduit à son socle minimal, le projet avait pour objectif de franchir une étape clé : concevoir et intégrer une interface en ligne de commande (shell) ainsi qu’un système de fichiers persistant, permettant une interaction directe et complète avec le système.
https://github.com/franckwajsburt/ko6

Pour concrétiser cela, nous avons développé :

Un shell interactif : doté d’un parseur et d'un analyseur syntaxique conçus à l'aide de Flex et Bison, intégrant plusieurs commandes internes (builtins) indispensables telles que cd, ls, mkdir ou encore exec.

Une couche de stockage et un système de fichiers : reposant sur la modélisation d’un disque virtuel, nous avons implémenté un système de fichiers inspiré des architectures classiques de type ext3/ext4 (gestion des métadonnées, blocs de données, répertoires et structures d'indexation).

Cette extension permet à KO6 de passer d’un simple noyau rudimentaire à un environnement fonctionnel capable d’exécuter des programmes et de gérer l'arborescence des données.

Compétence
: C
: Bash
: Bison (grammaire) & Flex (logique)
: Git & Github
: Systeme de fichier (ext4)
: Qemu
: Linux

</details>

<details class="admonition-navy">
    <summary> 
    Conception & Analyse d’Arbres Cartésiens et Treaps
    <div class="admonition-subtitle"> 
    nov 2024 - janv 2026
    </div>
    </summary>

Dans le cadre du module d'Algorithmique Avancée & Complexité, conception et analyse complète d'une structure de données hybride : les Arbres Cartésiens (combinant les propriétés des Arbres Binaires de Recherche et des Tas / Heaps).

Principales réalisations :

- Conception & Implémentation : Développement des structures de nœuds et d'arbres, ainsi que des algorithmes clés (recherche, insertion et suppression optimisées par rotations d'arbres en $O(\log n)$ en moyenne).
- Treap & Équilibre probabiliste : Implémentation d'arbres cartésiens aléatoires avec génération stochastique des priorités pour garantir l'auto-équilibrage et éviter les dégénérescences classiques des ABR.
- Benchmark & Analyse expérimentale : Évaluation des performances sur de grands volumes de données, analyse de la profondeur moyenne, de la résistance aux cas limites et de l'impact des collisions.
- Preuve théorique : Démonstration formelle de la profondeur moyenne en $O(\log n)$ via des variables indicatrices et l'analyse probabiliste (inspirée de Quicksort).

**Avis:**  
C'est très avancé pour l'analyse, il faut etre a l'aise avec les proba, c'est un peu mon point faible mais après ca rien de vraiment compliqué, c'est de la formalité.

Compétence
: Algorithme Las-Vegas & Monte Carlo
: optimisation
: Java
: Théorie des Graphes
: Classe de Complexité probabiliste
: Algoritmie probabiliste

</details>

<details class="admonition-navy">
    <summary> 
   Conception d’un processeur ARM simplifié (VLSI)
    <div class="admonition-subtitle"> 
    sept 2024 – janv 2025
    </div>
    </summary>
Dans ce projet, nous avons conçu un processeur RISC-V simplifié pipeline 4 étages, en suivant une approche modulaire, orientée bas niveau et entièrement codée en VHDL. L’objectif était de maîtriser l’architecture interne d’un processeur tout en assurant sa fonctionnalité par simulation, test et intégration complète.

Composants et étapes clés du projet :
Étages du pipeline : IFetch, Decode, Execute (EXE), Memory (MEM), chacun développé et simulé individuellement

Modules principaux :
ALU (Arithmetic Logic Unit) avec gestion complète des flags (Zero, Carry, Overflow…)
Shifter multi-opérations (LSL, LSR, ASR, ROR, RRX)

FSM (Machine à états finis) pour la synchronisation des instructions

Registre Banc et FIFO pour le contrôle et le flux de données
Caches ICache/DCache pour améliorer la latence
Testbenchs unitaires et globaux pour validation fonctionnelle

Intégration finale :
Les différents blocs ont été assemblés pour former un processeur fonctionnel capable d’exécuter des instructions arithmétiques, logiques, de branchement, et de mémoire, avec un contrôle fin du pipeline et une gestion correcte des conflits et interruptions.

Compétences développées :
: RISC-V
: Modelisation par des automate Mealy/Moore
: Pipeline materiel
: VHDL
: GHDL/Gtkwave
: Description flot de controle, comportemental et structurel
: Conception et simulation VHDL (GHDL, GTKWave)
: Architecture de processeur RISC
: Pipeline, FIFO, synchronisation, testbench structuré

</details>

<details class="admonition-navy">
    <summary> 
    Projet Ile - Proie predateur
    <div class="admonition-subtitle"> 
    sept 2024 – janv 2025
    </div>
    </summary>

https://github.com/LHinode/projet-ile  
(La personne a changer de nom pour pas que je retrouve le projet or c'est moi qui a fait le projet de a-z, un peu culotté, faire ce genre de chose mesquin à la place de me dire ce que j'ai fait, ya des gens doué de parole et puis ya ça)

Réalisation d'un jeu 3D isométrique avec python à l'aide de la bibliothèque pygame.
Implémentation d'une simulation proie prédateur, ajout d'un joueur qui interagie avec l'environnement.
Le jeux contiens un mécanisme de scoring et de plusieurs animation.

Le but de ce projet était de pratiquer la gestion de projet, en utilisant la méthode scrum et la rédaction de rapport et documentation.

Competence:
: python
: pygame
: Programmation orienté objets
: creation d'icon
: animation d'ondelette de vague
: menu de lancement nyancat
: rapport, suivie, methode Scrum

 </details>
