
***
>*Important notes*:
* This is not a scientific work, it is just an aggregation and regurgitation of different sources of information. Meaning output of this book is mainly due to efforts of others as indicated in references.
* This is a rolling set of writings, meaning information will be added on a regular basis. There is no end.
* Any corrections and/or additions are encouraged.
***

# Chapter 1 - Motivation

Learning a new discipline is easier if we can apply [analogy-based learning](https://link.springer.com/referenceworkentry/10.1007/978-1-4419-1428-6_11#:~:text=Learning%20by%20analogy%20is%20a,linguistic%20competence%2C%20divergent%20thinking).
Coming from a computational background and trying to decipher research papers of the form: ["Metformin treatment of diverse Caenorhabditis species reveals the importance of genetic background in longevity"](https://onlinelibrary.wiley.com/doi/10.1111/acel.13488) has proven to be hard.

What is Metformin? What is Caenorhabditis? Is that the optimal model? What is a model in the first place? What is the genetic role in longevity? etc.
To navigate this space, one needs to start from [first principles](https://en.wikipedia.org/wiki/First_principle#:~:text=A%20first%20principle%20is%20a,to%20as%20postulates%20by%20Kantians.) of biology.

Here I set out to do following things:

* Define the basic biology terms needed to convey longevity information from first principles.
* Frame research directions in longevity space in terms of computation.


Biology is complex. So are computers. Can we find a mapping between software related terms and the biology related terms? 

Like this:

 Biology | Software | 
------- | -------- | 
[gene](https://en.wikipedia.org/wiki/Gene)  ->   | [library](https://en.wikipedia.org/wiki/Library_(computing)) ||
[genome](https://en.wikipedia.org/wiki/Genome)  ->   | [bytecode](https://en.wikipedia.org/wiki/Bytecode) |
[translation](https://en.wikipedia.org/wiki/Translation_(biology))  ->   | [disassembly](https://en.wikipedia.org/wiki/Disassembler) |
[protein](https://en.wikipedia.org/wiki/Protein)  ->   | [function](https://en.wikipedia.org/wiki/Function_(computer_science)) |
[protein secondary structure](https://en.wikipedia.org/wiki/Protein_secondary_structure)  ->   | [basic blocks](https://en.wikipedia.org/wiki/Basic_block) |
[quaternary structure](https://en.wikipedia.org/wiki/Protein_quaternary_structure)  ->   | [compiled function with inlining](https://en.wikipedia.org/wiki/Inline_expansion) ||
[protein structure prediction](https://en.wikipedia.org/wiki/Protein_structure_prediction)  ->   | [library identification](https://www.hex-rays.com/products/ida/tech/flirt/in_depth/)
[genome analysis](https://en.wikipedia.org/wiki/Genomics#Genome_analysis)  ->   | [static analysis](https://en.wikipedia.org/wiki/Static_program_analysis) |
[molecular dynamics](https://en.wikipedia.org/wiki/Molecular_dynamics)  ->   | [dynamic analysis](https://en.wikipedia.org/wiki/Dynamic_program_analysis) |
[nucleotide](https://en.wikipedia.org/wiki/Nucleotide)  ->   | [byte](https://en.wikipedia.org/wiki/Byte)

While not a perfect mapping it serves a purpose: 
> All of the problems that are going to be faced in biology domain could be tackled with already proposed solutions in software domain.

But why care?

## Biology is just an iteration cycle

We care because solving aging entails solving biology. And solving biology means finding a better iteration cycle: 

![biology_iterations](https://i.ibb.co/PWmtWWp/biology-debugging.jpg")

1. **Observe Phenotype** means observing the effect of the intervention on everything that can be measured. Besides the external changes of the organism, internal measuraments such as [biomarkers](https://en.wikipedia.org/wiki/Biomarker) are also relevent. 
2. **Update the model** means using the observational information to enhance your (computational) understanding of the particular biological part. One example for that can be a computer simulation of particular molecular pathway. Other one could be using animal models that are most similiar to what we are trying to tackle in humans. Using this model we can then make educated therapeutic suggestions.
3. **Suggest therapeutic intervention** means utilizing the previous information in order to make an intervention that will hopefully result in more favorable observations in step 1.

Problem is, biological iteration cycles take a lot of time. As I am writting this, the formatted Markdown text is being rendered on adjecent window. The ("software") iteration cycle is fast, since I can observe all the changes in almost real time. Hence I can adjust accordingly in timely fashion. 

*We need an biological alternative of real time rendering.*




## What gets measured gets simulated

In order to achieve the biological alternative of real time rendering, we face complications on several levels:

1. **Oversimplification of biology.** Example: [Apoptosis pathway](https://en.wikipedia.org/wiki/Apoptosis). Left is the oversimplified understanding. Right is the actual one. Hope is that the data will give us insight in unexplored biological mechanisms.
<a href="https://ibb.co/W0yX9R0"><img src="https://i.ibb.co/cwF95sw/biology-complexity.png" alt="biology-complexity" border="0"></a>
2. **Capturing data.** In order to simulate biology we need to comprehensively capture the information on each cellular level. 
3. **Accurate models.** Both in terms of animal and computational models we are only approximating of what should happen in humans.
4. etc.


## Why longevity?

That its a problem and that rarely a young person experiences age related diseases like Alzheimer and Parkinsons is clear.

Whats more interesting is that we have been trying to [solve this problem](https://www.amazon.com/dp/B00SHPD0N4/ref=dp-kindle-redirect?_encoding=UTF8&btkr=1) for thousands of years. And still fail.


> *But what is the problem definition ?*


**Prolonged health span, not necessaraly life span.**

I like to think of the longevity problem as a multi-objective optimization.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/J5Vx6DF/longevity-mo.jpg" alt="longevity-mo" border="0"></a>

We have two variables. X is the the health span and Y is the life span.
Usually our health span peaks around 50 (or even sooner depending on the definition) and we proceed with life (span). What the actuall goal with longevity should be (or maybe not if you read some research papers) is to first optimize for the X variable as we are optimizing for the Y. Not the other way around. With this objective in mind we can aim for long, healthy life space. Not necesseraly solely life span for the sake of it. 

> “Aging, quite simply, is a loss of information”, Dr. David Sinclair

If one peels through the layers of aging problems and rephrase these challenges in terms of information and data, one can see that aging can be tackled computationally with AI.

[The Science-Technology of growing young](amazon.com/Science-Technology-Growing-Young-Breakthroughs/dp/1950665879) outlined the *The Near Horizon of Longevity and The Far Horizon of Longevity*. We will focus on the former, with brief input to the latter at the end.

# The Near Horizon of Longevity
One of the root causes of understanding complex systems is the fallacy of the correlation implies causation.

Let’s take one of the prominent longevity theories, telomere shortening. The short version is that the telomeres, repetitive nucleotide sequences associated with proteins that lie on both ends of our chromosomes, directly impact longevity – to be precise, the length of telomeres. Scientists observed that shorter-telomere mice lived shorter and vice versa. We rushed to confirm this theory to humans, and ambiguity happened: Even though there were promises, excess telomerase was also linked with cancer. So which one is it, is the telomeres length cause of longevity, or is the length of the telomeres the effect of longevity. We need more data to prove it!

Sergey Young outlined in the third chapter four leading breakthroughs that will have a significant impact on longevity. Here is our (AI) take on them.

## The genetic engineering breakthrough.

The Human Genome Project was finished in 2003, and it successfully sequenced the entire human genome. Meaning we had the information of the whole twenty-five thousand individual genes. Gene sequence allows us to predict many hereditary diseases, the probability of getting cancer, and many other unknowns where we still did not determine the cause and effect relationship. You may be wondering now, given that our genes do not change much from birth, what are other implications of gene sequencing. Our epigenome, the system of chemical modifications around our genes that determines how our genes are expressed, does.Furthermore, according to longevity scientists, the biological age of your epigenome, not your actual age, seems far more critical. **Why is this important for ML?** Horvath clocks (or any other aging clocks for that matter), biological age measuring solutions enable measuring of “aging score” and effectively measuring the chemical activity within the epigenome. All this sums up that now we simulate longevity experiments and observe the effects in a human cell long before this human dies. [Deep learning can be used to improve the Horvath clock accuracy](https://epigenie.com/the-epigenetic-clock-from-deep-space-to-deep-learning/). Another enabler is the price. The price to perform genome sequencing has come down to a couple of hours and hundreds of dollars. The problem (opportunity) is that the size of the data is enormous. One genome contains three billion nucleotide base pairs. The chance to analyze this and make a subsequent inference is considerable. Change just one letter (one nucleotide) in the genome, and one can cause severe side effects. One concrete example of understanding our genome and the effect genes cause is the so-called gene therapy. It works by effectively focussing on genetic modifications of cells to produce a therapeutic effect. You may have heard of the CAR T-cell therapy. A cancer treatment therapy based on gene therapy where patients own immune system T cells are modified to fight specific types of cancer. Machine learning can be used to [improve the manufacturing process of CAR T-cells](https://www.isct-cytotherapy.org/article/S1465-3249(19)30527-4/fulltext).


## The regenerative medicine breakthrough.

Aging wears down the bodily systems and functions. Achieving longevity does not only mean counting up the years but making the years count. For that, we need technologies that can repair these functions. One of those technologies is stem cell therapies. It has been talked about for years, but what has been emerging and further enhancing this subfield is, you guessed it, AI. Ways AI can aid multitude, with a formal overview of tackling different parts of stem cell technology with AI available [here](https://www.eurekaselect.com/186710/article).


## The health-care hardware breakthrough.

Out of all potential breakthroughs, this one holds the most sway. Yearly, out of the 60 million lives lost, we can contribute more than half of that to reversible diseases if caught early. The problem is if we are not monitoring frequently and granularly enough to react in time. We are posing our current approaches as “reactive” and not “proactive.” If we can get this data early and accurately enough, we will diagnose the condition at hand. This brings us to one of the essential principles in AI. **It’s the data that’s the differentiator, not the machine learning algorithms.** If you can gather the quality (labeled) data, the algorithms operating upon this data are not that important. And yes, current wearables are very constrained in function. But this is changing fast, and look at this recent Nature publication. We can measure deep tissue processes without invasive surgery. He who owns the data owns the AI.


## The health data intelligence breakthrough.
Justifiably the seismic shift underpinning the Longevity Revolution is the amount of and quality of data coming in and from these devices. But another vital aspect that is the practice of **precision medicine.** It involves customizing health diagnostics to individual characteristics. And for this we are getting more and more publicly available data, like [here](https://www.biorxiv.org/content/10.1101/2022.05.01.489928v2). **Here is the problem: Privacy issues.** For the machine learning algorithms to operate on the data, one needs to access them first. Sending this data to a server where the diagnostic computation will be performed is a problem.


There are two straightforward solutions: **on-edge machine learning and differential privacy**. The first aspect leverages the fact that our current devices (not only phones) have become exceedingly powerful. They can perform a computation reserved for personal computers or computing clusters just a couple of years ago. The computer used to send the first man to the moon is now weaker than the current phones. This implies that the expensive machine learning calculations can be offloaded to phones and smaller medical devices – obviously, not all components, but just the ones that need the personalized data. For example, one company can train the model offline, meaning on the servers, and then send the model to the patient’s devices to make the inference on the device. Avoiding the privacy problems as a whole. The second paradigm is that of differential privacy. The gist of it is that these are the standard machine learning algorithms with carefully “injected” noise, which mask the data and mathematically guarantee privacy. The data will never be seen, and the algorithms can still extract patterns (make the diagnosis) on this noisy data. This is nothing new; these kinds of algorithms are precisely what Google and Apple use when they process our private data. Or at least they claim they use.

**NOTE:** Privacy discussion and its solutions will be even more critical as we move towards the **internet of bodies (IoB)**. All of the sensors that measure our data are paired between themselves and other people’s data. Since collective intelligence is more significant than single, this step will be essential to get better AI. But managing it will introduce security challenges on its own. Two solutions of which we proposed above.

All this abundance of data is intertwined with better diagnostics. Novel, non-invasive, cheap, and highly effective diagnostic methods:

1. **Liquid biopsy**. Enables examination of bodily fluids like urine, saliva, spinal fluid, or blood to find traces of diseases, examine DNA or RNA. All while we are non-invasive and cheap. The fact that we can extract a lot of information from a single drop of blood opens many doors for diagnosis. As we understand and further analyze, e.g., blood data, we can make better machine learning algorithms. Some companies are already doing this, where they have built in a sense a diagnostic recommender system based on your personal blood information. **Data?** [liqDB](https://academic.oup.com/HTTPHandlers/Sigma/LoginHandler.ashx?error=login_required&state=e0a3ab4a-3fe0-4de1-823e-6176eaa5093fredirecturl%3Dhttpszazjzjacademiczwoupzwcomzjnarzjarticlezj47zjD1zjD113zj5144140) is a small-RNAseq knowledge discovery database for liquid biopsy studies. **What could you do with it?** With this and plenty of other liquid biopsy databases, labels indicate different diseases based purely on bodily fluids measurements. There is an opportunity to expand this to other, not labeled diseases and see if accurate inference can be performed.

2. **Genetic diagnostics.** In the genetic engineering breakthrough, I defined one potential improvement of the Horvath clocks. Still, the reality is companies and research are abundant trying to make actionable insights from the genome. One exciting application is customizing your diet to your genetic makeup. The real challenge, in this case, is not the ML algorithms but creating the data to help make a correct inference. **Data and ML Application?** As mentioned in the 1. The genetic engineering breakthrough. But the applications and databases are vast. A comprehensive summary can be found [here](https://genomemedicine.biomedcentral.com/articles/10.1186/s13073-019-0689-8).

3. **Epigenome diagnostics.** Epigenome may prove more critical in early disease diagnosis than the genome. Epigenetic changes, changes in the chemical compounds and processes that regulate gene expression, can be used to find diseases much earlier than the genetic approach. And are far more accurate in predicting these diseases. **Data?** [Epigenetic Tools](https://epigenie.com/epigenetic-tools-and-databases/) **What could you do with it?** From supervised to unsupervised to RL, the extent of possible application is vast. An interesting example of unsupervised learning was done [here](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0176562). They profiled a high-resolution comparative genomic hybridization (aCGH) and RNA sequencing (RNA-seq) to analyze chromosomal alterations and dysregulated gene expression in tumor specimens of patients with fibrolamellar hepatocellular carcinoma. It is a mouthful, just showcasing that these types of AI applications can not be done without a multidisciplinary approach.

4. **Microbiome diagnostics.** The fact is, the digestive tract hosts more microorganisms than the number of cells in our entire body. But the more interesting fact is that the combination and performing actions of these microorganisms are different for every individual. And these unique combinations, it turns out, are a good indicator of certain diseases. The microbiome is very closely linked to health and longevity. The problem is how do we crunch the data? Again blindly applying the ML on whatever is available out there in regards to microbiome will not work. True enablers here will curate datasets, paired with domain knowledge of clinical experts and only then applying AI to get the superior inference. **Data?** [HMP](https://commonfund.nih.gov/hmp/databases) Database human microbiome project. **What could you do with it?** An extensive review of methods can be found [here](https://www.frontiersin.org/articles/10.3389/fmicb.2021.634511/full). They are taking just one example of applying deep learning, [DeepARG](https://microbiomejournal.biomedcentral.com/articles/10.1186/s40168-018-0401-z) networks trained to predict antibiotic resistance genes (ARGs) from metagenomic data.

Details on these diagnostics and more are found in subsequent chapters.

# The Far Horizon of Longevity

Two main enablers outlined here were **quantum computing and artificial general intelligence**. I did not analyze this part to a greater extent because there is a high probability we would speculate. Technological advances are only apparent in hindsight. And AI had its [winters](https://en.wikipedia.org/wiki/AI_winter). We will instead try to dissect the current state of this technology and what can be applied.

Even though there is a lot of hype around the execution speed that quantum computing brings, this is not (currently) true for all of the computational problems. 

**Where can QC offer the advantage today?**

> **Big enough combinatorics problems.**

What do I mean by that, take a simple known example. Ball counting from a jar. By randomly selecting the balls whats the probability that certain order will be selected.
![](https://ae01.alicdn.com/kf/HTB1XxK1N4naK1RjSZFBq6AW7VXaw/50pcs-5-Colors-Plastic-Balls-Children-Addition-and-Subtraction-Counting-Ball-Primary-Mathematics-Solver-Tools-Math.jpg_Q90.jpg_.webp)

Ofcourse this might seam easy but a lot of real world problems can be posed as combinatorial problems. For example [traveling salesman](https://en.wikipedia.org/wiki/Travelling_salesman_problem).
But now all combinatorical problem are suitable for QC.



Depending on the steps that need to be executed, quantum computing might be slower than the traditional computing paradigm. Take, for example, quantum machine learning. Google developed a [method](https://ai.googleblog.com/2021/06/quantum-machine-learning-and-power-of.html) to evaluate the suitability of applying quantum machine learning given the data at hand. And the conclusion is following:

> *Moreover, a key takeaway from these results is that although we showed datasets where a quantum computer has an advantage, classical learning methods were still the best approach for many quantum problems.*

It is important to note that the execution speed is not the only selling point of quantum computing. Quantum inspired algorithms are offering the ability to pair classical with quantum theory and achieve better results. Check J. Miguel Arrazola, et.al. “Quantum-inspired algorithms in practice,”

Currently, there are companies like AWS offering quantum computing services like Braket, and given the fact, there is an ample space of molecules to be parsed, computational needs are enormous. Hence there is no surprise that there is research in [applying quantum machine learning](https://pubs.acs.org/doi/10.1021/acs.jcim.1c00166) to drug discovery space. The maturity is still coming of age, and there is a lot of potential in classical computing to be exploited.

To talk about the state of **artificial general intelligence (AGI)**, we first have to define it. AGI “should devise a solution to any task through observation, research, and application of past experiences.” While there are different approaches to achieving AGI, and even [reputable sources](https://www.nature.com/articles/s41599-020-0494-4) claiming this will not happen, the current consensus to at least get closer to AGI is applying reinforcement learning. Even a DeepMind publication is claiming this is the case, called [“Reward is enough”](https://www.sciencedirect.com/science/article/pii/S0004370221000862) since the basic premise of this ML domain is training an agent to perform particular action purely by observing the environment and then incentivizing him to perform desirable action rewarding him. **What can we currently do?** For most of the cases RL is simply not feasible. While there is a lot of research being done, the number of real-world applications is limited. Reasons are multitude, and it is extensively summarized in this [article](https://www.alexirpan.com/2018/02/14/rl-hard.html). This is not to say that it can not be done, and there are already people [applying this](https://advances.sciencemag.org/content/4/7/eaap7885) in the drug discovery space, but the scalability and the production level maturity will be a question.

![](https://miro.medium.com/max/450/1*7pYlUXIXWIjHwnPmibcbCw.jpeg)

From https://www.alexirpan.com/2018/02/14/rl-hard.html