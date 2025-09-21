---
title: "semARTagger: A Human–AI Collaborative Tool for Semantic Metadata Enrichment in Art Historical Archives"
layout: post
date: 2025-09-19 16:05
image: 
headerImage: false
tag:
- markdown
- elements
star: true
category: project
projects: true
author: "Marianiki Zafeiraki"
description: "semARTagger: A Human–AI Collaborative Tool for Semantic Metadata Enrichment in Art Historical Archives"
--- 

## semARTagger: A Human–AI Collaborative Tool for Semantic Metadata Enrichment in Art Historical Archives

![*semARTagger* Interface](assets/images/semartagger.jpg "The semARTagger interface")

This thesis introduces *semARTagger*, a multilingual, human-in-the-loop annotation pipeline and browser-based interface developed to enhance semantic metadata enrichment in digitized art historical collections, relying exclusively on textual information. The project focuses on the Exhibitions of Living Masters, a series of 19th-century Dutch art exhibition catalogs, exploring how artworks can be meaningfully and effectively annotated when visual data is not available. At the core of the pipeline lies a combination of multilingual embeddings (LaBSE), multi-label classification techniques, Named Entity Recognition (NER), and hierarchical concept expansion using the Art & Architecture Thesaurus (AAT). This integration allows the system to assign both English and Dutch tags to each artwork title, creating a semantic framework for historical records that are often minimally described. The project also includes a custom-built interface developed in Streamlit—a lightweight Python-based solution for interactive applications—which enables art historians, curators, and researchers to upload their data, view the pipeline’s predictions, edit tags, and export their annotated datasets. By incorporating human expertise in the workflow, the tool supports meaningful human–AI collaboration in annotation and metadata curation tasks. 

The system is evaluated through qualitative expert feedback and usage testing, highlighting both its strengths and the limitations and underscoring the broader capabilities but also the domain experts’ perception of AI-based methods in digital art history (DAH) metadata practices. Ultimately, *semARTagger* contributes an adaptive solution for semantic metadata enrichment in low-resource, multilingual cultural heritage contexts and reinforces the discourse around designing accessible, interoperable and collaborative frameworks that align with domain values and support sustainable knowledge infrastructure in the digital humanities. 

### Methodology

The system was built in two main layers: a tagging pipeline and a user interface.  

For the pipeline, the foundation was a training dataset provided by the RKD, containing over 99,000 artwork–tag pairs in Dutch and English. This dataset was cleaned, consolidated, and transformed into a format suitable for machine learning. Artwork titles were encoded using LaBSE multilingual embeddings, which capture semantic meaning across more than 100 languages. On top of these embeddings, a multi-label classifier was trained to predict relevant tags for each artwork. To capture entities like places and names, Named Entity Recognition (NER) was added, while the predictions were enriched and standardized using the AAT. The use of this controlled vocabulary ensured that tags were not only relevant but also interoperable with other cultural heritage databases.  

The second layer was the *semARTagger* interface, built with Streamlit. This browser-based tool connects directly to the pipeline and was designed for curators and researchers to interact with the system. Users can upload catalog data, view automatically generated tags, compare them with AAT terms, make corrections, and export the enriched dataset. The interface was designed to be lightweight, intuitive, and transparent, so that experts remain in control of the annotation process while benefiting from the efficiency of automation.  

Together, the pipeline and the interface created a complete workflow: from raw artwork titles to enriched, bilingual metadata that is consistent with controlled vocabularies and ready to be integrated into research or cataloging environments.  

---

### Evaluation  

The system was evaluated through a user study with curators and metadata specialists at the RKD. Participants tested *semARTagger* in real annotation tasks and provided feedback on usability, accuracy, and interpretability.  

The study revealed that users valued the time saved by automated suggestions, while also emphasizing the importance of being able to control, edit, and refine the results. Their insights shaped interface refinements, highlighting the role of human expertise in validating AI-driven tagging.  

---

### Key Takeaways

- **Successful Metadata Enrichment:** The pipeline generated meaningful Dutch and English semantic tags for historical artworks based solely on their titles.  

- **Standardization Through AAT:** By relying on a controlled vocabulary, the system ensured semantic consistency and interoperability across collections.  

- **Improved Efficiency:** Compared to manual tagging, the system reduced the time and effort required while still preserving expert oversight.  

- **Usability:** User studies confirmed that *semARTagger* was intuitive, transparent, and adaptable to curatorial workflows.  

- **Positive Perception of AI:** Experts appreciated the tool as a supportive assistant rather than a replacement, noting improved trust when they could see, edit, and correct the AI’s output.  

- **Scalable Solution:** The separation of pipeline and interface ensures the system can be retrained and extended for other collections and low-resource, multilingual datasets.
  
---

This project was created by Maria Elpiniki Zafeiraki as part of an *Embedded Research Project* at the RKD – Nederlands Instituut voor Kunstgeschiedenis (Netherlands Institute for Art History) and the *MA Thesis* course, supervised by Dr. Houda Lamqaddam, for the Master's in Cultural Data and AI at the University of Amsterdam.  

It was also showcased as a poster during the Posters Presentation at *Celebrating 10 Years of Digital Humanities at KU Leuven*.

This work is my own, and I hold the rights to it. You are welcome to cite it.  

For access to the original manuscript please refer to University of Amsterdam's thesis repository, [*Scripties*](https://scripties.uba.uva.nl/search?id=c13645749). 
For the project’s code and additional technical details, please see the [GitHub repository](https://github.com/marnikzaf/semARTagger).

For any questions or ideas to further develop this research, please **[contact me](mailto:marnikzaf@gmail.com)**.

