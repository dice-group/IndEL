# IndEL
IndEL is the first Indonesian Entity Linking (EL) benchmark dataset for general and specific domains.
It was manually created where the labeling process performed using a semantic annotation platform, [INCEpTION](https://inception-project.github.io/). 
There are two Indonesian NER benchmark datasets utilized for entity extraction, i.e. [NER UI](https://github.com/indolem/indolem/tree/main/ner/data/nerui) and [IndQNER](https://github.com/dice-group/IndQNER/tree/main/datasets). NER UI contains entities in a general domain, and IndQNER provides entities in a specific domain, i.e. the Indonesian Translation of the Quran.
The dataset contains:
|Domain          |Sentences|Tokens|Linked Entities|
|----------------|---------|------|---------------|
|General Domain  |2114     |44833 |4767		  |
|Specific Domain |2621     |61816 |2453           |

## Annotation Stage
There were six annotators who contributed to the annotation process. They are students of Informatics Engineering and Quran and Tafseer departments at the State Islamic University Syarif Hidayatullah Jakarta. 
1. Anggita Maharani Gumay Putri
2. Azmi Muchtar
3. Muhammad Destamal Junas
4. Muhammad Rifqi Setiabudi
5. Naufaldi Hafidhigbal
6. Rosyidatul Liulinnuha 

## Evaluation
We evaluated the annotation quality of IndEL by employing the MAG approach, a well-established multilingual entity linking method. The evaluation results are distinguished into linked and Not in Lexicon (NIL) entities as follows.
|Domain          |Total Entities|Linked Entities|NIL Entities|
|----------------|--------------|---------------|------------|
|General Domain  |4767          |3163		|1604        |
|Specific Domain |2453          |1930 		|523         |


## Contact
If you have any questions or feedbacks, feel free to contact us at ria.hari.gusmita@uni-paderborn.de or ria.gusmita@uinjkt.ac.id
