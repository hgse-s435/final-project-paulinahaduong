HW for Week 10:
* Analyze your data; run different models and compare them; update your research questions based on your preliminary findings.
* What is your metric for success? Make sure that you think about how you are going to check whether your approach was successful. Are you going to present numbers, visualizations or something else to share your results? What are they going to look like, if your hypothesis was correct?
* Research your topic and find online resources to help you analyze your data (e.g., one datacamp course).


# Project updates
## April 18, 2019 (week 10)
* Read a lot (see some of the annotated bibliography below). Thing I could do: Code for five different types of reflection (Valli): technical, reflection-in and on action, deliberative reflection, personalistic reflection, and critical reflection. Does this apply to learners as well as teachers? Also the Shum (2016) has an interesting looking rubric of reflective writing
* Found this doc particularly helpful: https://github.com/brandomr/document_cluster/blob/master/cluster_analysis_web.ipynb 
* Metric of success...I think i'm just looking for interestingness? Hoping for visualizations (will need to do some descriptive statistics visualizations, I think). 
* Work-wise: had to finish data cleaning from last week (was trying to join two dataframes but on two specific columns of CSVs that were out of order & also of different sizes). Had previously cleaned data using lemmatization, but w/ all of the italian projects & emojis, decided to start over to filter out just for projects with English reflections (tried TextBlob - made too many server requests, and then Spacy --which seemed to give me weird lists that were hard to work with? e.g., \['en']. Ultimately ended up using the Google lang-detect, which gives me a string 'en'. This drops my # of projects down to 3000. Definitely want to do some descriptive stuff for next week (average length of reflection, etc.).
* WORKING IN THIS FILE: Week9-Final-Project-haduong-eng


# Annotated Bibliography

## Q. Liu, S. Zhang, Q. Wang and W. Chen, "Mining Online Discussion Data for Understanding Teachers Reflective Thinking," in IEEE Transactions on Learning Technologies, vol. 11, no. 2, pp. 243-254, 1 April-June 2018. doi: 10.1109/TLT.2017.2708115. https://ieeexplore.ieee.org/document/7934007

Abstract: Teachers' online discussion text data shed light on their reflective thinking. With the growing scale of text data, the traditional way of manual coding, however, has been challenged. In order to process the large-scale unstructured text data, it is necessary to integrate the inductive content analysis method and educational data mining techniques. An inductive content analysis on samples taken from 17,624 posts was implemented and the categories of teachers' reflective thinking were obtained. Based on the results of inductive content analysis, we implemented a single-label text classification algorithm to classify the sample data. Then, we applied the trained classification model on a large-scale and unexplored online discussion text data set and two types of visualizations of the results were provided. By using the categories gained from inductive content analysis to create a radar map, teachers' reflection level was represented. In addition, a cumulative adjacency matrix was created to characterize the evolution of teachers' reflective thinking. This study could partly explain how teachers reflected in online professional learning environments and brought awareness to educational policy makers, teacher training managers, and education researchers.

Notes:
* "The purposes of this research are 1) to explore the categories of teachers reflective thinking and realize the automatic classification of the online discussion data by integrating the inductive content analysis and educational data mining techniques; and 2) to analyze teachers reflective thinking in the online teacher professional development program, including teachers reflection levels and evolution.

* Why online PD? "The way of online profession development provides convenience and flexibility for teachers to participate in learning activities, interact and communicate with colleagues and mentors in ways that would have previously been difficult. Operating blog-based teaching portfolios as an online learning community tool for teachers to discuss, negotiate and reflect on their own understanding of teaching experience, researchers have showed a positive impact of blog-based teaching portfolios on teachers professional development [16]. The online learning community help teachers establish their professional identity, reduce isolation, and enhance their reflective practice [17], [18]. Reflective practice has long been considered as a key activity in quality teacher professional development programs [3]."

* DCLA: "Discourse-centric learning analytics (DCLA) focus on learners discourse to identify patterns of meaningful learning and knowledge construction [30]. DCLA can reveal the presence or absence of the intended knowledge construction processes which can serve as good indicators for tracking and assessing whether the unfolding learning processes are productive or not from the perspective of co-construction of knowledge [31], [32]. The emergence of social constructivist approaches to education also prompts the appearance of applications to analyze the discourse of users within the context of social networks. After defining the domain-specific epistemic frame, epistemic network analysis (ENA) uses the elements of the epistemic frame as the nodes and creates an adjacency matrix to represent the co-occurrences of nodes in each line of chat data [33]. ENA can characterize students discourse and visualize the structure of their epistemic frame. Under the guidance of ENA, we defined the nodes and the co-occurrences of nodes within a discussion data as the connections, and created a cumulative adjacency matrix to characterize the development of teachers reflective thinking."

* research model:
"Phase 1: We developed a data collection tool to collect teacher-generated online discussion data. We obtained 21,388 posts by using the data collection tool over a period of 6 months.

Phase 2: A random sample (2,000 posts) were drawn from the online discussion data set and used for inductive content analysis.

Phase 3: Three experts who had experience with qualitative research and familiarity with pre-existing cod-ing schemes collaborated on the inductive content anal-ysis process. Three experts conducted an inductive content analysis on the random sample of online discussion data set. After phase 3, we obtained the categories used for text classification.

Phase 4: A single-label Nave Bayes Classification algorithm had been implemented to classify the labeled data. Then, we evaluated the performance of the single-label Nave Bayes classification algorithm by comparing it with other commonly used text classification algorithm.

Phase 5: We implemented a large-scale text classification based on the trained classification model. All the online discussion data has been automatically coded.

Phase 6: We visually represented teachers reflection levels after we obtained the results of large-scale text classification. Additionally, we created a cumulative adjacency matrix to characterize the evolution of teachers reflective thinking. Then, the results of text classification and visualization were sent back to the data storage."

* Protecting participants:
"In this study, three steps were taken to protect the gathered data: (1) all participant names were replaced with pseudonyms; (2) we only analyzed the online discussion text data; and (3) we only present the results of data analysis and did not release the original data."

* Types of reflection: technical, reflection-in and on action, deliberative reflection, personalistic reflection, and critical reflection.
"A number of coding schemes for analyzing teachers reflective thinking were development [41]. Van Manen [42] distinguished three levels of reflection. At the first level of reflection, teachers dominant concern was with technical rationality (applying knowledge in order to reach predetermined educational objectives). At the second level, teachers reflection went beyond technical rationality into investigating, questioning and clarifying the end objectives and the assumptions behind teaching activities. At the highest level of reflection, the critical reflection, teachers incorporated moral and ethical questions into their line of thinking. Valli [20] summarized five different types of reflection as follows: technical reflection, reflection-in and on action, deliberative reflection, personalistic reflection, and critical reflection. Among these types of reflection, technical reflection was concerned with the general instruction and management behaviors aspect of classroom teaching, deliberative reflection was concerned with the whole range of teaching (students, curriculum, rules and organization of the classroom, etc.), personalistic reflection was concerned with teachers personal growth and relationships with students, and critical reflection was concerned with the social, moral, and political dimensions of schooling. A typology of reflection which was developed to bridge theory and practice in an effort to teach reflective practice to preservice teachers was proposed and the typology profiles three dimensions of teachers reflective thought: descriptive, comparative, and critical [23]."

* Nave-Bayes algorithm - for every pre-determined category, there are a certain number of words associated with each. (so, if you did the clusters by hand instead of with code, perhaps)

# annotated bib
### Gibson, A., & Kitto, K. (2015, March). Analysing reflective text for learning analytics: An approach using anomaly recontextualisation. In Proceedings of the fifth international conference on learning analytics and knowledge (pp. 275-279). ACM. http://users.on.net/~kirsty.kitto/papers/lak15-gibson_kitto-short-FINAL.pdf
**Abstract**: "Reflective writing is an important learning task to help foster reflective practice, but even when assessed it is rarely analysed or critically reviewed due to its subjective and affective nature. We propose a process for capturing subjective and affective analytics based on the identification and recontextualisation of anomalous features within reflective text. We evaluate 2 human supervised trials of the process, and so demonstrate the potential for an automated Anomaly Recontextualisation process for Learning Analytics."
* "Reflective writing is used by educators to help students
develop the metacognitive capability required for effective
reflective practice, an important dimension of continual improvement in many professions [6, 5, 13]. However, despite
it’s educational value, reflective writing presents challenges.
Firstly, it is difficult to assess [13], and can require a lot
of reading time on the part of the educator. Secondly, the
inherent lack of structure in reflective writing, its personal
style, and variability in quality [6], makes it difficult to treat
in the same way as other more structured written tasks, and
thus an unlikely candidate for computational analysis."
* "Our approach, which we call Anomaly Recontextualisation
(AR), is based on accommodating rather than eliminating
anomalous data. It is fundamentally a 2 step process. Step
1 requires the identification of an anomaly within a given
context. Step 2 involves recontextualising the anomaly such
that it is no longer anomalous within its new context."
* "We extracted a large range of features from the data set
that could be used in our computational analysis. For each
individual reflection we extracted features related to: reflection point, date, word length, word and sentence counts,
parts of speech, word frequencies, and topics. We also extracted features for the group as a whole: Statistical analysis of reflection point, day of week, word lengths, word
and sentence counts. We also collected frequency distributions of words, counts, ratios, and various parts of speech."
* 24 people's reflections  a reflective # on a slider scale

### Ashley N. Castleberry, Nalin Payakachat, Sarah Ashby, Amanda Nolen, Martha Carle, Kathryn K. Neill, and Amy M. Franks (2016). Qualitative Analysis of Written Reflections during a Teaching Certificate Program. American Journal of Pharmaceutical Education: Volume 80, Issue 1, Article 10. https://www.ajpe.org/doi/full/10.5688/ajpe80110
* 132 essays; 2 people independently identified themes; "Twenty-eight themes were identified within 132 essays. Common themes encompassed content delivery, student assessment, personal successes, and challenges encountered. Deep reflection was exhibited, with 48% of essays achieving the highest level of critical reflection. Extent of reflection trended higher from midpoint to final essays, with significant increases in the strengths and feedback areas."
* "By using a constant comparative approach, coders agreed by consensus on every essay to achieve 100% inter-rater reliability. Additional reflective themes also were added based on coder agreement when a new topic was discussed that did not fit into one of the predetermined themes. A third investigator periodically reviewed the coding process and identified themes for verification to enhance agreement between coders. 
* themes & reflections: "Quotations from teaching certificate program participant essays specific to the area of assessment were extracted to illustrate the extent of reflection. An example of nonreflection (level 1) was: “Assessment questions are aimed at evaluating comprehension of stated objectives.” A statement that was consistent with understanding (level 2) was: “There are various characteristics that students display that allow assessment of their abilities.” Reflection was evident in the level 3 statement: “It is easier to see two students evaluate similar patients than it is to see students present two different cases and discern which is more proficient.” Critical reflection (level 4) was evidenced by the statement: “But then I realized that I didn’t know if I was being an effective teacher without an assessment of some type. So I have started incorporating pre- and post-lecture questions to see what the learner gained from the presentation.”

### Shum, S. B., Sándor, Á., Goldsmith, R., Wang, X., Bass, R., & McWilliams, M. (2016, April). Reflecting on reflective writing analytics: Assessment challenges and iterative evaluation of a prototype tool. In Proceedings of the sixth international conference on learning analytics & knowledge (pp. 213-222). ACM. https://www.researchgate.net/publication/328942550_Automatic_Reflective_Writing_Analysis_based_on_Semantic_Concept
* Abstract: "When used effectively, reflective writing tasks can deepen learners' understanding of key concepts, help them critically appraise their developing professional identity, and build qualities for lifelong learning. As such, reflecting writing is attracting substantial interest from universities concerned with experiential learning, reflective practice, and developing a holistic conception of the learner. However, reflective writing is for many students a novel genre to compose in, and tutors may be inexperienced in its assessment. While these conditions set a challenging context for automated solutions, natural language processing may also help address the challenge of providing real time, formative feedback on draft writing. This paper reports progress in designing a writing analytics application, detailing the methodology by which informally expressed rubrics are modelled as formal rhetorical patterns, a capability delivered by a novel web application. This has been through iterative evaluation on an independently human-annotated corpus, showing improvements from the first to second version. We conclude by discussing the reasons why classifying reflective writing has proven complex, and reflect on the design processes enabling work across disciplinary boundaries to develop the prototype to its current state."
	•	https://link.springer.com/article/10.1007/s40593-019-00174-2
	•	https://dl.acm.org/citation.cfm?id=2883951
	•	https://dl.acm.org/citation.cfm?id=2883955
	•	https://eric.ed.gov/?id=EJ1062704
	•	https://www.tandfonline.com/doi/abs/10.1080/07294360.2010.512627
	•	https://onlinelibrary.wiley.com/doi/abs/10.1046/j.1365-2923.2002.01227.x


