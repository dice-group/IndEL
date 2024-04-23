# IndEL
IndEL is the first Indonesian Entity Linking (EL) benchmark dataset for general and specific domains. It was manually created, and the labeling process was performed using a semantic annotation platform, [INCEpTION](https://inception-project.github.io/). There are two Indonesian NER benchmark datasets utilized for entity extraction, i.e., [NER UI](https://github.com/indolem/indolem/tree/main/ner/data/nerui) and [IndQNER](https://github.com/dice-group/IndQNER/tree/main/datasets). NER UI contains entities in a general domain, and IndQNER provides entities in a specific domain, i.e., the Indonesian Translation of the Quran. IndEL is presented in [NIF format](https://persistence.uni-leipzig.org/nlp2rdf/). The dataset contains:
|Domain          |Sentences|Tokens|Linked Entities|
|----------------|---------|------|---------------|
|General Domain  |2114     |44833 |4765		  |
|Specific Domain |2621     |61816 |2453           |


## Annotation Stage
The manual annotation of IndEL, in both its general and specific domains, was carried out by non-volunteer native speakers. Specifically for the specific domain (pertaining to the Indonesian translation of the Quran), the annotators comprised students in their fourth year of bachelor studies from the Quran and Tafseer department at State Islamic University Syarif Hidayatullah Jakarta. There were six annotators as follows: 
1. Anggita Maharani Gumay Putri
2. Azmi Muchtar
3. Muhammad Destamal Junas
4. Muhammad Rifqi Setiabudi
5. Naufaldi Hafidhigbal
6. Rosyidatul Liulinnuha 


## Experiments
To showcase the utility of IndEL as a benchmark dataset, it was used to evaluate cutting-edge EL systems in multilingual settings using [the GERBIL framework](https://github.com/dice-group/gerbil). The EL systems included [Babelfy](http://babelfy.org/), [DBpedia Spotlight](https://www.dbpedia-spotlight.org/), [MAG](https://github.com/dice-group/AGDISTIS), and [WAT](https://sobigdata.d4science.org/web/tagme/wat-api). Steps to perform the evaluation can be found [here](https://github.com/dice-group/gerbil/wiki/How-to-setup-GERBIL). Evaluation results are as follows:
|Metrics         |Babelfy   |DBpedia Spotlight|MAG     |WAT        |
|----------------|----------|-----------------|--------|-----------|
|General Domain  						   |	
|Precision       |**0.7278**|0.6746           |0.4265  |0.6121     |
|Recall          |0.3719    |0.3575           |0.4166  |**0.5551** |
|F1              |0.4923    |0.4673           |0.4215  |**0.5822** |
|Specific Domain  						   |	
|Precision       |0.8000    |**0.8471**       |0.1523  |0.7681     |
|Recall          |0.4696    |0.6731           |0.1508  |**0.7468** |
|F1              |0.5918    |0.7501           |0.1515  |**0.7573** |

### Another Evaluation with MAG
To further investigate the impact of how Indonesian entities are presented in Wikidata on the EL systems' performance, another evaluation was performed by employing MAG, targeting the identification of NIL entities within both the general and specific domains. The evaluation results are distinguished into linked and Not in Lexicon (NIL) entities as follows:
|Domain          |Total Entities|Linked Entities|NIL Entities|
|----------------|--------------|---------------|------------|
|General Domain  |4767          |3163		|1604        |
|Specific Domain |2453          |1930 		|523         |


## How to Use
We have integrated IndEL into [the GERBIL framework](https://gerbil.aksw.org/gerbil/). This integration facilitates the evaluation of both multilingual and Indonesian-specific EL systems using IndEL.

## Further Development Plan
During the creation of IndEL, we identified that a significant number of entities are missing in the Indonesian Wikidata. This observation highlights the limited range of entries in Indonesian Wikidata, particularly in comparison with its counterparts in other languages. To address this, our improvement plan includes expanding the linkage of entities in IndEL to other knowledge bases, such as DBpedia and YAGO. Additionally, in terms of domain-specific content, our plan is to broaden the scope of the dataset to encompass the complete Indonesian translation of the Quran, extending from the currently included 8 chapters to all 114 chapters.
 
## Contact
If you have any questions or feedbacks, feel free to contact us at ria.hari.gusmita@uni-paderborn.de or ria.gusmita@uinjkt.ac.id
