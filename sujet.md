# Practical Session #1: Introduction

1. Find in news sources a general public article reporting the discovery of a software bug. Describe the bug. If possible, say whether the bug is local or global and describe the failure that manifested its presence. Explain the repercussions of the bug for clients/consumers and the company or entity behind the faulty program. Speculate whether, in your opinion, testing the right scenario would have helped to discover the fault.

https://gizmodo.com/alaska-airlines-talk-strikes-software-bug-cybersecurity-1850150052?utm_source=YPL
Salon l'article, le bug aurait causé le tailstrike de 2 avions d'Alaksa Airlines dans la même matiné du dimanche 27 février 2023.
Le bug a affecté le système utilisé pour mesurer le poids et l'équilibre de l'appareil, empêchant le pilote de calculer avec précision la poussé que les moteurs seront capable de fournir et à quelle vitesse l'avion décollera. En l'occurence le poids de l'avion avait été sous estimé. Il s'agit d'un bug global puisque le système affecté était incapable de sa tâche correctement. 

Le défaut s'est manifesté lorsque les pilotes de deux vols d'Alaska Airlines ont remarqué des divergences dans les données de poids et d'équilibre, ce qui les a empêchés de décoller. En conséquence les 2 avions ont été immobilisés, et les passagers de ces vols ont subi des retards et des annulations, entraînant des inconvénients et ayant potentiellement un impact sur leurs plans de voyage. Pour la compagnie aérienne, les conséquences comprennent des pertes financières en raison de vols annulés et des pertes de revenus potentielles en raison de clients mécontents. Cela pourrait également endommager la réputation de la compagnie aérienne.

Le bug était causé par une mise à jour du logicel, ce problème aurai pu être évité si le fournisseur du logiciel avait testé correctement la nouvelle version notamment en vérifiant que les résultats fournis étaient les même que la version précedement.

---

2. Apache Commons projects are known for the quality of their code and development practices. They use dedicated issue tracking systems to discuss and follow the evolution of bugs and new features. The following link https://issues.apache.org/jira/projects/COLLECTIONS/issues/COLLECTIONS-794?filter=doneissues points to the issues considered as solved for the Apache Commons Collections project. Among those issues find one that corresponds to a bug that has been solved. Classify the bug as local or global. Explain the bug and the solution. Did the contributors of the project add new tests to ensure that the bug is detected if it reappears in the future?

COLLECTIONS-830, bug global

Le bug affectait la méthode CollectionUtils.filter() dans le projet Apache Commons Collections. La méthode ne fonctionnait pas correctement avec les collections non synchronisées, provoquant des erreurs de concurrence et des exceptions.

Les contributeurs du projet ont résolu le bug en apportant des modifications à la méthode CollectionUtils.filter() pour qu'elle fonctionne correctement avec les collections non synchronisées. Ils ont également ajouté des vérifications de concurrence pour éviter les exceptions.

Les contributeurs du projet ont ajouté de nouveaux tests pour s'assurer que la méthode CollectionUtils.filter() fonctionne correctement avec les collections non synchronisées. Les tests ont été ajoutés au cadre de test existant et vérifient que la méthode fonctionne correctement dans différentes situations, notamment avec des collections contenant des éléments null. Les nouveaux tests garantissent que le bogue a été résolu de manière fiable et qu'il ne réapparaîtra pas dans le futur.

---

3. Netflix is famous, among other things we love, for the popularization of *Chaos Engineering*, a fault-tolerance verification technique. The company has implemented protocols to test their entire system in production by simulating faults such as a server shutdown. During these experiments they evaluate the system's capabilities of delivering content under different conditions. The technique was described in [a paper](https://arxiv.org/ftp/arxiv/papers/1702/1702.05843.pdf) published in 2016. Read the paper and briefly explain what are the concrete experiments they perform, what are the requirements for these experiments, what are the variables they observe and what are the main results they obtained. Is Netflix the only company performing these experiments? Speculate how these experiments could be carried in other organizations in terms of the kind of experiment that could be performed and the system variables to observe during the experiments.



---

4. [WebAssembly](https://webassembly.org/) has become the fourth official language supported by web browsers. The language was born from a joint effort of the major players in the Web. Its creators presented their design decisions and the formal specification in [a scientific paper](https://people.mpi-sws.org/~rossberg/papers/Haas,%20Rossberg,%20Schuff,%20Titzer,%20Gohman,%20Wagner,%20Zakai,%20Bastien,%20Holman%20-%20Bringing%20the%20Web%20up%20to%20Speed%20with%20WebAssembly.pdf) published in 2018. The goal of the language is to be a low level, safe and portable compilation target for the Web and other embedding environments. The authors say that it is the first industrial strength language designed with formal semantics from the start. This evidences the feasibility of constructive approaches in this area. Read the paper and explain what are the main advantages of having a formal specification for WebAssembly. In your opinion, does this mean that WebAssembly implementations should not be tested? 

5.  Shortly after the appearance of WebAssembly another paper proposed a mechanized specification of the language using Isabelle. The paper can be consulted here: https://www.cl.cam.ac.uk/~caw77/papers/mechanising-and-verifying-the-webassembly-specification.pdf. This mechanized specification complements the first formalization attempt from the paper. According to the author of this second paper, what are the main advantages of the mechanized specification? Did it help improving the original formal specification of the language? What other artifacts were derived from this mechanized specification? How did the author verify the specification? Does this new specification removes the need for testing?

## Answers
