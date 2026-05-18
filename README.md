# Cpu-32-Bits-RISC-V-Project-MSL5P-

⚠️ TEXTE CORRIGÉ PAR IA (car mon talent en français est casi nul !)
📝 Note que C'est moi qui ai fait tous les choix de design, 
l'IA a juste corrigé l'orthographe et amélioré la formulation pour mon portfolio.
Le projet, lui, est 100% le mien.

JE Tien a dire que j'ai utiliser le logitiel Antares c'est ici ou j'ai tous fait en numerique

🎯 Le Projet
Mon but est de créer un CPU 32 bits entièrement fait par moi.
Je ne copie personne, je crée tout avec mes propres idées et ma logique.

Depuis longtemps, je m'intéresse au fonctionnement réel des ordinateurs et à l'électronique logique.
Au lieu de juste utiliser des programmes, j'aime comprendre comment une machine fonctionne à l'intérieur.

⚡ ALU — Le commencement
J'ai commencé par l'ALU (Arithmetic Logic Unit), parce que c'était déjà un domaine que je maîtrisais bien.

Vers mes 12 ans, j'avais déjà créé une calculatrice 8 bits entièrement sur Minecraft, construite de zéro uniquement avec de la logique Redstone et des FULL ADDER.
J'avais développé ce projet en environ 3 jours juste par passion.

🧠 Réflexion et conception
Au début, je faisais énormément de schémas sur papier pendant les temps morts en cours.

Je réfléchissais directement à la logique des additions binaires :

1 + 1 = 10
1 + 0 = 1
Je me suis donc dit que quand les deux entrées sont à 1, une retenue devait être créée.

J'ai alors utilisé une porte logique AND pour gérer cette retenue :

1 AND 1 = 1
toutes les autres combinaisons donnent 0
Premier objectif validé ✅

Ensuite, j'ai commencé à imaginer plusieurs versions de mon ADDER directement sur papier.
Je faisais énormément de tests théoriques avant même de construire les circuits.

Mais un problème est rapidement apparu :

beaucoup de mes concepts fonctionnaient sur papier, mais ne convenaient pas aux systèmes industriels ou aux logiciels de simulation utilisant des portes logiques "propres".

Du coup, j'ai décidé d'adapter toute mon ALU à une architecture plus stable et plus réaliste.

🔧 Ajout de sécurités
En travaillant sur mon architecture, j'ai aussi ajouté plusieurs sécurités logiques.

Le but était d'éviter que certaines parties du CPU exécutent des calculs ou changent d'état sans qu'une instruction le demande réellement.

🚀 Le FULL ADDER
Après ça, je suis passé au FULL ADDER.

Le but était maintenant de gérer :

les deux bits d'entrée ;
mais aussi la retenue provenant de l'addition précédente.
C'est ce qui permet ensuite de relier plusieurs additions ensemble pour construire une vraie architecture capable de gérer plusieurs bits.

💀 Le SUB — Le vrai début des problèmes
J'étais super content de mon FULL ADDER.

Mais ensuite je suis passé au SUB… et c'est là que les vrais problèmes ont commencé.

J'avais deux choix :

Solution 1
Utiliser la technique A + (!B) utilisée dans beaucoup de vrais processeurs.
Mais au début, je ne la considérais pas comme totalement fiable.

Solution 2
Créer tout le système de soustraction moi-même de zéro.

Et évidemment… c'est cette solution que j'ai choisie 😭

⚠️ Le FULL SUB — L'enfer
Au début, mon SUB fonctionnait parfaitement.

Le vrai problème est arrivé quand j'ai commencé le FULL SUB, donc la gestion des retenues, des dettes et des emprunts binaires.

Là c'était un enfer.

J'ai essayé énormément de techniques :

sécurités logiques ;
protections ;
nouvelles structures ;
systèmes de contrôle.
🐛 Les deux bugs qui m'ont détruit
Après énormément de travail, je termine enfin mon FULL SUB.

Je teste tout. Tout fonctionne.

J'étais littéralement à deux doigts de crier de joie.

Puis la réalité me rattrape 💀

Premier bug
Dans certains cas négatifs très précis : 0 - 1 + 0 - 0 le système me donnait -3 en décimal. Ce qui était totalement faux.

Deuxième bug
La gestion des emprunts et des dettes binaires n'était pas stable.

Et là… j'étais vraiment proche d'abandonner.

🔥 Le déclic
J'ai fait une pause de 2 jours pour vider ma tête.

Puis un matin, je reviens avec une énorme énergie.

Et là… énorme déclic.

Je reprends toute ma logique du FULL ADDER.

C'est à ce moment-là que mon FULL ADDER V3 stable est né.
Plus expérimental. Vraiment stable.

Ensuite je crée la V2 du SUB avec une technique un peu… barbare 😭

9 XOR
Oui. 9 XOR.

J'étais moi-même en train de rire devant ce que j'avais créé juste pour sécuriser certains cas négatifs.

Malheureusement, j'ai supprimé cette version sans prendre de capture ou de photo. Et aujourd'hui encore je le regrette.

⚡ La vraie solution
Puis j'ai eu un autre déclic.

J'ai retesté la fameuse méthode : A + (-B)

Au début ça ne fonctionnait pas correctement.

Puis j'ai décidé de dupliquer certains modules et de reconstruire la logique autrement.

Et là… tout fonctionne.

C'est aussi à ce moment-là que j'ai compris quelque chose d'important :

la retenue n'était pas seulement une retenue. C'était aussi elle qui indiquait si le système était dans un état négatif ou non.

🚀 Architecture scalable
Une fois ce problème réglé, tout est allé extrêmement vite.

Sous l'effet de la joie, j'ai créé :

mon ALU 4 bits ;
puis 8 bits ;
puis 16 bits ;
en environ 10 minutes.

Parce que dès le début, j'avais pensé toute mon architecture comme un système modulaire et scalable.

Chaque bloc pouvait être réutilisé et agrandi facilement.

Et c'est exactement ce que je voulais depuis le début.

🔌 Câblage de l'ALU — La souffrance
Maintenant que toute la logique ADD/SUB était enfin stable — ce qui m'a quand même pris 5 jours à cause des passages entre la V1, V2 puis V3 — je suis passé à la suite.

Mais pour garder l'histoire dans un ordre logique, je vais expliquer ce qu'il restait encore à faire dans l'ALU.

Il me restait :

un décodeur 3 bits ;
les portes logiques AND, OR et XOR en 32 exemplaires chacune.
Et là… c'était une étape monstrueuse.

Ça m'a pris environ 6 heures de travail quasiment non stop. J'ai littéralement sacrifié une journée entière juste pour cette partie : toute une journée + encore 2 heures le lendemain.

🧠 Le décodeur — Le déclic
Le décodeur, je l'ai fait après. Pas parce que c'était difficile, mais surtout parce que je ne savais pas comment les vrais systèmes faisaient ça proprement.

Et en analysant le fonctionnement, plusieurs trucs ont directement provoqué un énorme déclic dans ma tête.

J'ai compris qu'un décodeur pouvait gérer jusqu'à un certain nombre de bits proprement, et que pour aller plus loin il fallait combiner plusieurs décodeurs ensemble avec une logique spéciale.

Mais ça… ça reviendra plus tard dans l'histoire 😭

🔧 Câblage monstrueux
Du coup je suis revenu sur mon ALU.

Je devais maintenant câbler toutes les portes logiques une par une et ajouter mes propres barrières de sécurité avec des transistors classiques.

Le seul truc que je n'ai pas entièrement créé de zéro : le décodeur classique.

Parce que pour moi, un décodeur simple, c'était surtout du par cœur. Et le par cœur, j'aime pas vraiment ça.

Le seul vrai choix personnel que j'ai fait dans ce décodeur, c'était l'organisation des sorties et la façon de l'intégrer dans mon architecture.

Par contre le décodeur 5 bits, lui je l'ai fait moi-même. Et la première fois que j'ai réfléchi à sa logique, ça m'a vraiment fasciné.

Vous allez voir pourquoi dans la partie sur les registres.

💀 Le calvaire des câbles
Pour cette ALU, j'ai dû câbler une quantité ABSURDE de fils.

Je faisais ça non stop. Des milliers de connexions.

Voici le calcul :

ADD/SUB intégré : 66 entrées
XOR : 64 entrées
AND : 64 entrées
OR : 64 entrées
Ce qui donne :

66 + 64 + 64 + 64 = 258 entrées à relier.

258 connexions. Et ça, c'est seulement une partie de l'ALU 💀

Et évidemment, je devais aussi réfléchir au cable management.

🎨 L'art du câblage
Du coup j'ai choisi le style de câblage que je préfère :

des fils propres, organisés, avec des chemins précis, sans croisements inutiles.

Et honnêtement… à la fin ça devient presque de l'art 😭

Dans mon logiciel, j'essaie toujours d'utiliser le moins de fils possible et d'avoir un rendu visuel propre.

Mais avant ça, j'avais pensé à utiliser des systèmes de bus simplifiés.

Ça aurait été beaucoup plus simple et beaucoup moins fatigant.

Mais j'ai volontairement refusé cette solution.

Je voulais vraiment ressentir ce que ça fait de construire une architecture manuellement, comme un vrai concepteur de circuits.

Du coup j'ai tout relié à la main.

Par contre, pour les sorties finales, j'ai quand même utilisé un vrai bus. Parce que là, ça devenait logique pour l'architecture finale de l'ALU.

🚌 Le bus final
J'ai donc relié tous les bus ensemble — 4 au total — avec des portes OR à 4 entrées afin d'obtenir une seule sortie bus de 32 bits.

Et là… mon ALU était enfin terminée.

Entièrement.

Après tout ce temps, tous les bugs, toutes les versions et tout le câblage… c'était enfin fini.

⚡ Performance
Pour les curieux, cette ALU a une latence d'environ 5370 ns.

Ce qui donne environ 180 kHz.

Et honnêtement, pour ma première ALU entièrement terminée, je trouve ça vraiment correct.

Surtout que dès le début j'avais prévu un objectif de seulement 100 kHz pour mon CPU.

Donc au final, j'étais largement satisfait 😭

🧩 LES REGISTRES — Fun
Puis après… LES REGISTRES 😭

Et étonnamment, cette partie était vraiment fun.

Avec les bascules à relier, les copier-coller, les connexions… c'était presque reposant comparé au reste.

Du coup j'ai utilisé la méthode classique que tout le monde utilise pour les registres.

Et j'ai créé un registre capable de stocker 32 bits.

Puis ensuite, j'ai transformé ce système en un registre capable de stocker 32 nombres de 32 bits grâce à un décodeur 5 bits que j'ai conçu.

🔮 Le décodeur 5 bits — Fascinant
Le système du décodeur 5 bits m'a vraiment fasciné.

Parce qu'il me rappelait une logique que j'avais déjà expérimentée quand j'étais plus petit avec des LEGO et des systèmes modulaires.

Et honnêtement… je kiffais trop réfléchir à ce genre de structure 😭

Du coup celui-là, je l'ai entièrement fait à la main.

🔁 Double bus — La solution
Mais il restait encore un problème :

mon registre pouvait stocker 32 nombres de 32 bits, mais il ne possédait qu'un seul bus d'entrée/sortie.

Et pour mon ALU, ça devenait vite problématique.

Du coup j'ai créé un autre module basé sur ce registre afin de le transformer en système à double bus entrée/sortie.

Et honnêtement, cette partie était plutôt simple.

Beaucoup de copier-coller, du reliage et surtout de l'organisation pour éviter d'envoyer les valeurs deux fois.

Pour les curieux, ce registre a une latence d'environ 3380 ns.

Ce qui reste totalement acceptable pour mon objectif de fréquence.

⏱️ La clock — Contrôle
Et justement en parlant de fréquence :

j'ai finalement utilisé la clock de base du logiciel.

Je n'avais pas vraiment le choix pour une future intégration dans une Tang Nano 9K.

Du coup j'ai surtout travaillé sur le contrôle de cette clock.

J'ai ajouté un transistor P à la sortie afin de pouvoir stopper certaines parties du système.

Comme ça, plus tard, je pourrai aussi réfléchir à de l'économie d'énergie.

📦 La ROM — Spoiler
Le dernier élément sur lequel j'ai commencé à travailler : la ROM.

Mais pour l'instant… elle ne contient quasiment rien 😭

Là je suis surtout en phase d'analyse pour préparer la suite du CPU.

Par contre, même si je comprends comment une ROM fonctionne réellement, je ne peux pas totalement la recréer de zéro dans ce projet.

Il y a deux raisons :

Le logiciel ne possède pas les composants mémoire transistorisés nécessaires.
Je devrai utiliser la ROM native du logiciel pour pouvoir compiler correctement le projet dans la Tang Nano 9K.
⏳ À SUIVRE...
