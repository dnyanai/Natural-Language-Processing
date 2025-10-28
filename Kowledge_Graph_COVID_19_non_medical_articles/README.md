# COVID-19 Knowledge Graph Project

## 🎯 At a Glance

**Project Name**: Knowledge Graph Construction from COVID-19 Non-Medical Articles  
**Domain**: Natural Language Processing, Knowledge Graphs, Information Retrieval  
**Goal**: Transform unstructured text into a queryable knowledge graph


## 📚 Dataset
- **Source**: Kaggle COVID-19 News Articles Dataset
- **Size**: ~200,000 non-medical articles
- **Domains**: Business, Technology, Finance, Automotive, AI, Science, Healthcare, Environment
- **Initial Scope**: Technology and Automotive articles

---
## Project Flowchart:
![Project Workflow](https://github.com/dnyanai/Natural-Language-Processing/blob/main/Kowledge_Graph_COVID_19_non_medical_articles/Imgs/Flowchart.png)

## 🔑 Key Problem Solved

**Challenge**: Information overload during COVID-19 pandemic - scattered non-medical information across 200K+ articles with no way to discover relationships, connect concepts, or perform semantic queries.

**The Gap or improvement opportunity**:
Traditional keyword search and document retrieval methods fall short because they:
- Cannot capture semantic relationships between entities
- Fail to connect information across multiple documents
- Don't reveal hidden patterns and connections
- Provide no mechanism for relationship-based querying

**Solution**: Automated NLP pipeline that extracts entities and relationships from articles, constructs a knowledge graph in Neo4j, and enables visual exploration and semantic querying.

---

## 🛠️ Technical Architecture

### Core Pipeline (5 Stages)

1. **Data Preparation**
   - Filter articles by domain (Tech, Automotive)
   - Clean text (remove URLs, hashtags, special chars)
   - Summarize articles to preserve key content

2. **Triple Extraction** (Dual Approach)
   - **Path I**: Noun-Verb-Noun pattern matching
   - **Path II**: Noun chunk dependency parsing
   - Extract (Subject, Predicate, Object) triples

3. **Validation & Export**
   - Manual quality verification
   - Remove redundancies
   - Generate CSV files (Nodes, Links, Triples)

4. **Graph Database**
   - Import to Neo4j using Cypher
   - Create dynamic relationships with APOC plugin
   - Build queryable knowledge graph

5. **Visualization**
   - NetworkD3 interactive visualizations
   - Neo4j Browser native rendering
   - Force-directed graph layouts

---

## 💻 Technology Stack

| Category | Technologies |
|----------|-------------|
| **NLP Processing** | Python, SpaCy, NLTK, Pandas |
| **Graph Database** | Neo4j, Cypher, APOC Plugin |
| **Visualization** | NetworkD3 (R), D3.js |
| **Data Format** | CSV, JSON, Graph format |

---

## 📊 Project Components

### Jupyter Notebooks
1. `EDA___Attempts.ipynb` - Data exploration and experimentation
2. `Text_Summarization.ipynb` - Article condensation pipeline
3. `Path_I_Noun_Verb_Noun.ipynb` - NVN triple extraction
4. `Path_II_Noun_Chunks.ipynb` - Enhanced chunk-based extraction
5. `NetworkD3_R.ipynb` - Interactive visualization generation

### Documentation
- `Neo4j_Steps.pdf` - Database setup guide
- `NetworkD3_NounChunks.html` - Interactive graph output

---

## 🎯 Key Features

✅ **Dual Extraction Methods**: Complementary approaches for comprehensive coverage  
✅ **Automatic Summarization**: Reduce article length while preserving meaning  
✅ **Graph Querying**: Cypher-based semantic search  
✅ **Interactive Viz**: Web-based exploration of relationships  
✅ **Scalable Pipeline**: Can extend to full 200K article dataset  

---

## 💡 Real-World Applications

### Research
- Discover hidden connections across articles
- Track pandemic impacts across domains
- Literature review automation

### Policy Making
- Understand cross-sector dependencies
- Identify critical intervention points
- Evidence-based decision support

### Data Science
- Benchmark NLP extraction techniques
- Study graph-based retrieval methods
- Develop domain-specific KG pipelines

---

## 📈 Results & Impact

**Achieved**:
- Extracted thousands of meaningful entity relationships
- Built fully queryable Neo4j knowledge graph
- Created interactive visualization for exploration
- Demonstrated 2 complementary extraction methods
- Enabled semantic search beyond keyword matching

**Advantage over Traditional Methods**:
- Reveals relationships, not just document matches
- Connects information across multiple sources
- Supports complex graph traversal queries
- Visual discovery of patterns

---

## 🔮 Future Directions
1. Scale to full 200K article corpus across all domains
2. Add Named Entity Recognition (NER) for better extraction
3. Temporal analysis of evolving relationships
4. Sentiment dimensions on entity relationships
5. Cross-domain impact analysis
6. REST API for programmatic access
7. ML-based automated triple validation

---

## 📝 Bottom Line

This project demonstrates how NLP and graph databases can transform unstructured pandemic-related text into structured, queryable knowledge - making sense of information overload and enabling insights impossible through traditional search methods.

**Impact**: From 200K scattered articles → Structured knowledge graph → Actionable insights


## 📄 License

This project is for educational and research purposes. 

