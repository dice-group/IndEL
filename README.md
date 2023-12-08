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


## Experiments
IndEL was used to evaluate cutting-edge EL systems in multilingual settings using [the GERBIL framework](https://github.com/dice-group/gerbil).
The EL systems included [Babelfy](http://babelfy.org/), [DBpedia Spotlight](https://www.dbpedia-spotlight.org/), [MAG](https://github.com/dice-group/AGDISTIS), and [WAT](https://sobigdata.d4science.org/web/tagme/wat-api).
Steps to perform the evaluation can be found [here](https://github.com/dice-group/gerbil/wiki/How-to-setup-GERBIL).
Evaluation results are as follows.
|Metrics         |Babelfy   |DBpedia Spotlight|MAG     |WAT        |
|----------------|----------|-----------------|--------|-----------|
|General Domain  						   |	
|Precision       |0.7278    |0.6746           |0.4265  |0.6121     |
|Recall          |0.3719    |0.3575           |0.4166  |*0.5551*   |
|F1              |0.4923    |0.4673           |0.4215  |*0.5822*   |
|----------------|----------|-----------------|--------|-----------|
|Specific Domain  						   |	
|Precision       |0.8 	    |*0.8471*         |0.1523  |0.7681     |
|Recall          |0.4696    |0.6731           |0.1508  |*0.7468*   |
|F1              |0.5918    |0.7501           |0.1515  |*0.7573*   |

### Another Evaluation with MAG
To further investigate the impact of how Indonesian entities are presented in Wikidata on the EL systems' performance, another evaluation was performed by employing MAG, targeting the identification of NIL entities within both the general and specific domains. 
The evaluation results are distinguished into linked and Not in Lexicon (NIL) entities as follows.
|Domain          |Total Entities|Linked Entities|NIL Entities|
|----------------|--------------|---------------|------------|
|General Domain  |4767          |3163		|1604        |
|Specific Domain |2453          |1930 		|523         |


## Contact
If you have any questions or feedbacks, feel free to contact us at ria.hari.gusmita@uni-paderborn.de or ria.gusmita@uinjkt.ac.id
