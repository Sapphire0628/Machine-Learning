# Stanford RNA 3D Folding: Machine Learning Approaches to Predict RNA Structure

## Project Overview
This project aims to apply machine learning techniques to predict the 3D structure of RNA (ribonucleic acid) molecules. RNA molecules play important roles in various biological processes, from transferring genetic information to catalyzing biochemical reactions. Understanding the 3D structure of RNA is essential to reveal its functions and interactions. Traditional wet lab methods can be time-consuming and costly, so computational prediction methods offer an efficient alternative.

Our project participated in the Stanford RNA 3D Folding competition, which requires predicting the 3D coordinates of RNA from its nucleotide sequence. We adopted an integrated approach that combines traditional machine learning algorithms, statistical methods, and geometric considerations to build a prediction model.

## Data Analysis and Feature Extraction (EDA)

### Data Structure
Our dataset includes:
- Training sequences and labels: RNA sequences and corresponding 3D coordinates used for model training
- Validation sequences and labels: used to adjust model parameters and evaluate performance
- Test sequences: sequences for which we need to predict 3D coordinates

### Sequence Analysis
During the data exploration phase, we conducted extensive analysis of RNA sequences, including:
1. **Sequence length distribution**: Analyze the length variation of RNA sequences in different datasets
2. **Nucleotide composition**: Calculate the distribution of four nucleotides: A, C, G, and U
3. **GC content analysis**: Measure the ratio of G and C nucleotides in the sequence, which has an important impact on RNA structure
4. **Position-specific nucleotide distribution**: Analyze the nucleotide preference at different positions in the sequence

### Structural analysis
We visualized and analyzed the 3D structure of RNA:
1. **Coordinate range analysis**: Understand the distribution characteristics of coordinates in each dimension
2. **Structural similarity comparison**: Analyze the differences between different structural variants of the same RNA molecule
3. **Nucleotide position and spatial relationship**: explore the relationship between adjacent nucleotides in the sequence and adjacent nucleotides in space

## Methodology

Our method includes the following core components:

### 1. Feature Engineering
- **Sequence features**: features extracted from nucleotide sequences, such as mononucleotide and dinucleotide frequencies
- **Structural features**: secondary structure information predicted using tools such as ViennaRNA and forgi
- **Energy features**: various energy parameters calculated to reflect the stability of RNA molecules

### 2. Graphical modeling method
We adopted a graph-based approach to capture long-range interactions in RNA structure:
- Establish an interaction network between nucleotides
- Identify possible structural elements (such as stem loops, pseudoknots, etc.)
- Simulate physical constraints on RNA folding

### 3. Machine learning model integration
We developed a multi-model integration system, including:
- Random forest-based sequence-structure mapping model
- Structural optimization model, applying RNA-specific physical constraints
- Quality assessment model for selecting the best structure from multiple candidate structures

### 4. Structure generation and purification
- Generate multiple candidate structures for each RNA sequence
- Rank the structures using the quality assessment model
- Select the best five structures as the final submission

## Results and Evaluation

### Model Performance
Our method shows good performance on the validation data:
- Successfully captures the overall topology of most RNA molecules
- For small and medium-sized RNA molecules (length < 100 nucleotides), the prediction accuracy is high
- For more complex RNA structures (such as those containing pseudoknots), the prediction is more challenging

### Visual Comparison
By visually comparing the true structure with the predicted structure, we found that:
- The predicted structure is able to preserve the main structural features (such as the overall shape of the backbone)
- The prediction of local structural details (such as the precise position of loops and stems) is more difficult

### Evaluation Metrics
We used a variety of metrics to evaluate the quality of structure prediction:
- Distance MAE (Mean Absolute Error): Measures the mean absolute error between the predicted coordinates and the true coordinates
- Coordinate RMSE (Root Mean Square Error): Evaluates the root mean square of the prediction error
- Structural Similarity: Similarity score based on structural superposition
- TM-score (Template Modeling score): measures the similarity between the predicted structure and the true structure, ranging from 0.0 to 1.0, with higher values ​​indicating more similar structures

## Future work

In the future, we plan to make further improvements in the following areas:

1. Integrate deep learning methods to improve prediction accuracy

2. Improve modeling of long-range interactions

3. Incorporate molecular dynamics simulations into the structure refinement process

4. Enhance prediction capabilities for larger RNA molecules

## Resources
- [Project presentation file](PPT.pdf)
- [Source code analysis](sourceCode.ipynb)

## Team members
- WANG Zhixuan
- CHAN Yuk Yee