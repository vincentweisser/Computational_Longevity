# Chapter 3 - Hallmarks and agng clocks


Contents of this chapter are:

* Hallmarks of aging and how tackle them computationally.
* New hallmarks of aging and how tackle them computationally.
* Aging clocks, causality and the future of evaluating biological age.


![](https://nintil.com/images/2020-01-05-longevity/image-20200117094655213.png)

Inspired by the seminal paper in cancer research, the [hallmarks of cancer](https://www.cell.com/fulltext/S0092-8674(11)00127-9), there has been a similiar attempt for aging.

 [Seminal paper](https://pubmed.ncbi.nlm.nih.gov/23746838/) defined the nine (then extended to 10) main “causes” of our decline, the ten horsemen of an internal apocalypse. The question I wanted to answer is:

> *Can we frame these problems/horsemen computationally in terms of machine learning and then try to solve them?*



1. **Genomic instability**: DNA doesn’t always replicate according to plan. Typically, these errors in gene expression get caught and corrected, but not always. Over time, these misfires build up, causing our body to wear down — meaning genetic instability leads to genetic damage leads to a limit on lifespan. Think of it as a broken copy machine, except, instead of producing unreadable pages, our broken genetic copier produces diseases like cancer, muscular dystrophy and ALS. **Data?** [HumCFS](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-018-5330-5): a database of fragile sites in human chromosomes. **What could you do with it?** Identify other fragile chromosomes sites AND link them to other diseases based on atom/chemical level properties.


1. **Telomere Attrition**: At the heart of a cell, DNA is packed into threadlike structures called chromosomes. Chromosomes are capped by telomeres which act like barriers — like bumpers on a car — designed to protect the core of the chromosome. But as DNA replicates, telomeres get shorter and at a critical level, the cell stops dividing, and we become more prone to disease and death. It has been shown that if one can increase or reduce the shrinkage of telomere on mice, longevity increases. **Data?** [Telomerase Database](http://telomerase.asu.edu/) **What could you do with it?** [Telomerase can be used as a target in anti-cancer therapy](https://pubmed.ncbi.nlm.nih.gov/28218725/). What this essentially means is one can find computationally (in-silico) inhibitors that hinder the shrinkage of telomerase. Doing this which we know has positive side effects for longevity.

1. **Epigenetic Alterations**: Nature impacts nurture. Over the course of a lifetime, environmental toxins can change how our genes express, sometimes for the worst. Exposure to carcinogens in the environment can silence the gene that suppresses tumors for example. But also the other way around, we can silence the gene that is responsible for cancer. **Data?** [dbEM](https://www.nature.com/articles/srep19340) and [GenAge](https://genomics.senescence.info/genes/index.html): A database of epigenetic modifiers curated from cancerous and normal genomes. **What could you do with it?** Epigenetic proteins (modifiers) are targets in cancer. With this database we get not only the protein but also genomic information pertaining to mutational status, copy number variation and expression level of epigenetic proteins in tumor samples. This enables explorationof other protein that were not classified as epigenetic, based upon their genomic information. **How to utilise GenAge?** There are tools and companies out there that allow for a complete measurement of one genes. ML models could be built that recommend actions based on certain gene structure.

1. **Loss of Proteostasis**: Inside a cell, proteins run the show. They transport materials, send signals, switch processes on and off, and provide structural support. But proteins become less effective over time, so the body recycles them. Unfortunately, as we age, we can lose this ability. The trash collector goes on strike and we suffer a toxic buildup of proteins that can, for example, lead to diseases such as Alzheimer’s. **Data?** [AlphaFold](https://alphafold.ebi.ac.uk/): Protein Structure Database. **What could you do with it?** Proteins that become terminally misfolded, or are no longer functionally required, they must be degraded to avoid damaging effects of their continued presence, predicting these proteins for shapes that we do not know could be essential in targeting their degradation. Which is exactly what we have achieved with Celeris (using a different approach)

1. **Nutrient Sensing Goes Awry**: The human body relies on over forty different nutrients to stay healthy. For everything to work perfectly, cells need to be able to recognize and process each of these. But this ability breaks down as we get older. For example, one reason people gain weight as they age is that our cells can no longer properly digest fat and carbohydrates. And one reason we die is that this impacts the insulin and IGF-1 pathway and can result in diabetes. **Data?** [Nutrient Sensing Mechanisms and Pathways](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4313349/). **What could you do with it?** [GenDR Database of Dietary Restriction-Related Genes](https://genomics.senescence.info/diet/). Not a direct ML approach but utilising [advancements in wearables and mobile sensors](https://pubs.acs.org/doi/10.1021/acssensors.1c00553) to get a more granular and personalised data on nutrition intake based on your current metabolic state could have huge impact. One can easily imagine getting measuraments on nutrient sensing of different (cancer) cells in the body and then depending on that information adjusting the nutrient intake such that the desired effect on cells is achieved. For example death of cancer cells. Extending this to genes one can use the GenDR Database of Dietary Restriction-Related Genes

1. **Mitochondrial Dysfunction**: Mitochondria are power plants. By converting oxygen and food into energy, they provide the basic fuel for our cells. But performance declines over time. The result is free radicals, a damaging form of oxygen that mangles DNA and proteins and leads to many of the chronic illnesses associated with aging. **Data?** [MSeqDR](https://mseqdr.org/mitobox.php) Mitochondrial Genomic Tools and Databases **What could you do with it?** With this currated list of databses one could combine measurements of Oxygen consumption ratio (OCR), maximal oxygen consumption and mitochondrial reserve capacity and their respective proteins. Beeing especially interested [in proteins that are targets in certain diseases](https://academic.oup.com/nar/article/47/D1/D1225/5162470?login=false), one could then have clear indicator with wearables or other measurement devices wether some disease is going to be triggered.

1. **Cellular Senescence**: As cells undergo stress, they occasionally become “senescent”, both losing their ability to divide and becoming resistant to death. These “zombie cells” can’t be removed from the body. They build up over time, infect neighboring cells, and ultimately create a zombie apocalypse of inflammatory debilitation. **Data?** [CellAge](https://genomics.senescence.info/cells/) Database of Cell Senescence Genes **What could you do with it?** Based on our personal gene makeup we could have model that recommend altering of genes associated with cellular senescence. Instead of altering [one can do further analysis of what action](https://pubmed.ncbi.nlm.nih.gov/32264951/) is needed for the genes involved in the sensescence.

1. **Stem Cell Exhaustion**: As we age, our supply of stem cells plummets, in certain cases by a ten thousand fold decline. Worse, the ones we do manage to hang on to become far less active. This means that the body’s internal tissue and organ repair system loses its ability to do its job. Now we already know that stem cells help and there are therapies out there for them. But how can AI make this even better? **Data?** [Stemformatics](https://academic.oup.com/nar/advance-articles?login=false): visualize and download curated stem cell data **What could you do with it?** A curated list of potenital AI applications in stem cell research can be found [here](https://www.eurekaselect.com/article/110522). One crucial application in designing stem cell therapies for central nervous system (CNS) diseases is differentiation of neural stem cells (NSCs) into neurons. Differentiation is complex and not yet clearly established, especially at the early stage. Novel [nature](https://www.nature.com/articles/s41467-021-22758-0) publication shows that deep learning could extract minutiae from large-scale datasets, and present a deep neural network model for predictable reliable identification of NSCs fate.

1. **Altered Inter Cellular Communication**: For the body to function properly, cells need to communicate. This happens constantly, with messages flowing through our bloodstream, immune system and endocrine system. Over time, signals get crossed. Some cells become unresponsive, others become inflammation-producing zombie cells. This inflammation blocks further communication. Once this happens, messages can’t get through and the immune system can’t find pathogens. **Data?** [PanglaoDB](https://panglaodb.se/): is a database for the scientific community interested in exploration of single cell RNA sequencing experiments from mouse and human. **What could you do with it?** Developing a ML tool that can quantitatively infer and analyze intercellular communication would be useful because increases and decreses in signal between cells could be indicative of changes in the organism and other action should be taken. Novel nature publication develops such tool. [CellChats](https://www.nature.com/articles/s41467-021-21246-9).

1. **Protein crosslinking**: This is a phenomenon where multiple separate proteins become bonded together by a sugar molecule in a process called glycation. Depending upon where this occurs, it tends to correlate with different signs of aging — wrinkles, arteriosclerosis, cataracts, and kidney failure, to name a few.

**Data?** [ProXL](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4977572/) (Protein Cross-Linking Database): A Platform for Analysis, Visualization, and Sharing Protein Cross-Linking Mass Spectrometry Data. **What could you do with it?** Developing an ML to identify where this bondage/linkage occurs and what kind of damage it will cause. If labeled data is hard to obtain, clustering techniques can be used to analyze already known bonding regions and try to abstract from there.

> **But they are not enough**

[JPM argues](https://pubmed.ncbi.nlm.nih.gov/34271186/), that the proposed hallmarks are not causative and explanatory enough of the true complexity of the underlying processes.

> *"In this context, the scheme is 
akin to a folding screen bearing a hallmarks of aging diagram that blocks 
the view of the true state of undress of the field. Shivering behind the 
screen is the ailing damage maintenance paradigm. We argue that as a 
field we must look and move beyond the hallmarks to understand the 
process of aging. Only by doing so can paradigms be formulated that 
possess sufficient explanatory power to enable treatments for human 
aging to be developed."*


It comes back to one of the fallacy I outlined: **Oversimplification of biology.**

So what can be done? Taking the table underneath as insight, one could quantify every possible biomarker. Determine which are statistically significant and try to map novel theory (hallmark) that could causative explanation of this multifactorial complex process we call aging.

The American Federation for Aging Research (AFAR) recommends the following criteria for biomarkers of aging:

1) It must predict a person’s physiological, cognitive, and physical function in an age-related way, independently of chronological age.

2) It must be testable and not harmful to test subjects (for example a blood test or an imaging technique); it must also be technically simple to perform, and it must be accurate and reproducibly without the need for specialized equipment or techniques.

3) It should work in laboratory animals as well as humans since preliminary testing is always done in nonhuman subjects.

Check [here](https://link.springer.com/article/10.1007/s11912-020-00977-w/tables/2) for additional details: 

![](https://i.postimg.cc/Yq4CNqVz/hallmark.jpg)

Another important reference for the biomarkers of aging is the [following](https://www.frontiersin.org/articles/10.3389/fgene.2021.686320/full). The rc-score displays how often a potential biomarker was referred to in reviews, based on the above-described NCBI-PubMed queries. 

Then effort score was added for each potential biomarker. Following values were considered:

• A low e-score (-) describes a potential biomarker which is easy to sample, to handle and to process (usually automated fast and reliable measurements are available from known sources). For example, blood counts from venous blood qualify, since such blood can be sampled easily, the plasma/serum can be stored at room temperature (up to 3 h for many analytes) or in a standard freezer (≥3 month for most analytes) and be processed by equipment that is regularly available in a standard diagnostic/clinical unit or research laboratory. The costs are low to moderate (≤10 €).

• A moderate e-score (–) is assigned if one step (sampling, handling, or processing) is associated with substantial extra effort for routine laboratories. This includes sampling under special conditions, a requirement for prompt sample handling, or the need for elaborate validation.

• A high e-score (—) implies elaborate sampling (e.g., biopsy, lumbar puncture, etc.), handling (e.g., storage in liquid nitrogen) and/or processing (e.g., non-routine nucleotide or protein sequencing). The financial costs are usually high.

![](https://www.frontiersin.org/files/Articles/686320/fgene-12-686320-HTML/image_m/fgene-12-686320-t001.jpg)

Again the relevance of these biomarkers is that they could be utilized not only to elucidate new theories and hallmarks computationally but also construct [aging clocks](https://www.technologyreview.com/2022/04/15/1050019/aging-clocks/).



## New hallmarks of aging

As the research progresses new theories started to emerge that aim to extend the current hallmarks.

### Extracellular matrix (ECM) and its connection to longevity

The extracellular matrix (ECM) is a network of proteins and other molecules that support, surround, and give structure to cells and tissues in the body. The ECM helps cells attach to and communicate with nearby cells, and plays an important role in cell growth, movement, and other functions. This three-dimensional network provides physical structure to the body and serves as a substrate for cells to live and grow. Cells often modify the components of the ECM, such as osteoclasts and osteoblasts, which degrade and lay down bone ECM, respectively.

Changes to the ECM are often overlooked as a cause of aging, but they can drastically impact cell behavior. Studies have shown that ECM characteristics such as stiffness and chemical composition can affect cell behaviors including proliferation rate, secretome, differentiation, and cellular maintenance. There is growing consensus that ECM-related changes, particularly matrix stiffening, should be considered on a similar level to the other hallmarks of aging.

"Accumulation of damage to the ECM drives cellular aging and disease progression. Collagen fragmentation, collagen glycation, collagen crosslinking, and aggregation of proteins in the extracellular space affect ECM integrity to accelerate agin." From [The Matrisome during Aging and Longevity](https://www.karger.com/Article/FullText/504295)

![](https://www.researchgate.net/profile/Abdelaziz-Ghanemi/publication/340352699/figure/fig1/AS:875550012895237@1585758798873/Example-of-extracellular-matrix-ECM-implications-The-extracellular-matrix-is-involved.png)

## New hallmarks of ageing: a 2022 Copenhagen ageing meeting summary

After almost a decade, we have gotten a [formal update](https://www.aging-us.com/article/204248/text) on potential novel hallmarks of aging. Here is the list:

1. Autophagy
2. Inflammation
3. Microbiome disturbance
4. Altered mechanical properties
5. Splicing dysregulation

![](https://www.aging-us.com/article/204248/figure/f1/hero)

*Now our goal is same as for the original hallmarks. We want to describe them briefly, comment the data for them and then pose some question that can be answered computationally.*


### 1. Autophagy 

![](https://images.theconversation.com/files/436311/original/file-20211208-188518-1fyp5pw.png?ixlib=rb-1.1.0&q=45&auto=format&w=754&h=448&fit=crop&dpr=1)

Senescence and autophagy are essential cellular processes that play a role in aging. Senescent cells are damaged cells that stop dividing and secrete cytokines and chemokines that can cause inflammation in neighboring cells. This can lead to tissue damage and promote cancer. Autophagy, on the other hand, is the process by which cells break down and recycle damaged components. This can help repair and prevent damage to cells. Interventions that target pathways involved in aging often upregulate autophagy. Some drugs can also promote autophagy, which can help alleviate the hallmarks of aging.

**What are some interesting computational research questions concerning autophagy?**

If we accept that the molecular damage is confounding variable in aging process, then getting rid of damaged objects would aid in tackling the problem.

**Autophagy measuring and prediction through biomarkers:**

- Tsuboyama, Kotaro, et al. "The ATG conjugation systems are important for degradation of the inner autophagosomal membrane.„ - **gives evidence of a direct correlation between LC3-II and p62 and autophagy level**
- Bobillo Lobato, Joaquin, Maria Jiménez Hidalgo, and Luis M. Jiménez Jiménez. "Biomarkers in lysosomal storage diseases.“ --- **links potential biomarkers.**


Both together give the ability to model the autophagy (flux) levels insilico.

So the approach would look something like this:

<a href="https://ibb.co/h20my03"><img src="https://i.ibb.co/6DQWmQj/autophagy.jpg" alt="autophagy" border="0"></a>

And the potential input features, that were quantified when taking biomarkers, would be:

- Globotriaosylceramide (Gb3)
- Glucosylceramide
- Galactosylceramide
- Dermatan sulfate
- Heparan sulfate
- Hyaluronic acid
- Glycogen
- Free cholesterol
- Calbindin D
- Myostatin
- Chitotriosidase
- HbA1c
- Glucose level
- Lipofuscin [Molecular damage in aging Gladyshev et.al]
- Acidification [Molecular damage in aging Gladyshev et.al]
- enzymatic activity  [Molecular damage in aging Gladyshev et.al]
- Lysosomal-associated membrane protein expression [Molecular damage in aging Gladyshev et.al]


Alternative computational question for autophagy would be: 

> What are some drugs that exhibit the same [mode of action](https://www.emcdda.europa.eu/document-library/computer-aided-silico-approaches-mode-action-analysis-and-safety-assessment-ostarine-and-4-methylamphetamine_en) as example underneath.

Screening huge libraries of compounds, like [ZINC](https://paperswithcode.com/dataset/zinc) and after finding the same mode of action, perform [lead optimization](https://medium.com/@medicilon2004/effective-use-of-in-silico-tools-in-lead-optimization-62fd2cd3de55) might produce interesting candidates.

![](https://nintil.com/images/2020-01-05-longevity/image-20200116074340112.png)

### 2. Inflammation

![](https://www.mypathologyreport.ca/wp-content/uploads/2021/12/inflammatory-cells.jpg)

Cellular senescence is a state in which cells stop dividing and enter a state of arrested growth. This is a natural protective mechanism that prevents damaged or potentially harmful cells from reproducing and potentially becoming cancerous. However, when a large number of senescent cells accumulate in the body, they can release harmful factors known as the senescence-associated secretory phenotype (SASP) that can lead to chronic inflammation and tissue damage.


Inflammation is a response to perceived threats in the body, such as pathogens or tissue damage. While this response is beneficial in the short term, chronic inflammation, or "inflammaging," can cause tissue damage and increase the risk of developing diseases such as cancer. This type of inflammation can be triggered by factors such as the accumulation of senescent cells and unhealthy lifestyles, such as overeating.


Final interesting research question, that one could pursue, is elucidating the combined effect of most of these hallmarks. Askin the questions of the type

## Aging clocks, causality and the future of evaluating biological age.

Deep neural networks (DNNs) can be used to extract useful features from large sets of biomarkers available through common blood testing. For example, Putin et al. (2016) trained an ensemble of DNNs on biochemical parameters from 62,419 individuals and achieved impressive performance in the prediction of chronological age (R2 = 0.8). More interestingly, this approach allowed for feature extraction and identified albumin, glucose, alkaline phosphatase, urea, and erythrocytes as the most promising markers for predicting human chronological age (Putin et al., 2016). This exercise demonstrates the data mining potential of these new methods, even in well-investigated areas like biomarkers.

Feature selection is a critical and actionable area when considering the potential application of -omics sciences. While large-scale omics data are essential for providing insights into the aging phenotype, a selected number of actionable elements must be identified in order to enable intervention strategies. Galkin et al. (2020) also used deep learning (DL) to predict chronological age, but trained their algorithms on the taxonomic profiling of human gut microbiomes. This is a strategic choice, considering the growing importance of the microbiota and, in turn, nutrition for wellbeing and health.


One of the most important obstacles is waiting for human biology to confirm certain longevity intervention. What if we can simulate this?

Sure one potential solution are the animal models that we outline in chapter 4. But sometimes these animal models do not translate well to human outcomes. But can we do that computationally?

Aging clocks seem to predict true biological state (age). Great overview can be found [here](https://www.technologyreview.com/2022/04/15/1050019/aging-clocks/).

The most important aspect is the input data/biomarkers that are informative in infering the biological information.

* [The Epigenetic Clock](https://epigenie.com/the-epigenetic-clock-from-deep-space-to-deep-learning/)
* [DeepMAge: A Methylation Aging Clock Developed with Deep Learning](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8279523/)
* [Deep Aging Clocks](https://www.cell.com/trends/pharmacological-sciences/fulltext/S0165-6147(19)30114-2)
* etc

It still remains to be seen wether this will be enough to infer goodnes of a certain intervention. It would be great if this could be used as a clinical target proxy to pass the FDA trials. Time will tell.