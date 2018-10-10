# README

Nrf1 proteomics repository

Brendon Smith

[br3ndonland](https://github.com/br3ndonland)

[![code license](https://img.shields.io/badge/code%20license-MIT-blue.svg?longCache=true&style=for-the-badge)](https://choosealicense.com/)

Code in this repository is MIT-licensed.

[![prose license](https://img.shields.io/badge/prose%20license-CC--BY--4.0%20-blue.svg?longCache=true&style=for-the-badge)](https://creativecommons.org/licenses/by/4.0/)

Prose in this repository is provided with a CC-BY-4.0 license, which is commonly used for open-access scientific publications. If you use the prose in this repository for your own work, please **attribute me** and **explain what you changed**.

## Table of Contents <!-- omit in toc -->

- [Reproducibility](#reproducibility)
  - [Comments](#comments)
  - [Practices](#practices)
  - [Resources](#resources)
- [Scientific background](#scientific-background)
- [Supplementary data](#supplementary-data)
- [Data analysis](#data-analysis)
  - [Jupyter Notebook](#jupyter-notebook)
- [Results](#results)

## Reproducibility

### Comments

Science is an incredible tool for learning about the world. We use theory and experiment to generate new knowledge. In science, reproducibility occurs when different scientists do the same experiment and get results that agree. **Our current scientific practices do not promote or reward reproducibility**. As a result, the scientific community is experiencing a **reproducibility crisis**, in which the discoveries that we publish can't be reproduced by multiple labs, or even repeated within the same lab by the same person, in some instances. This is not authentic knowledge.

The reproducibility crisis is troubling. During my postdoc in a large molecular biology lab, I saw the reproducibility crisis unfold, both in the scientific literature and among my colleagues. Even more striking than the crisis itself was the lack of an insightful solution.

**Documentation is the *sine qua non* of reproducibility.** How can we hope to reproduce experiments if we don't know how they were done? Documentation must start at the beginning, with reproducible data analysis being preceded by reproducible experimental practices. No statistical adjustment can make up for lack of detailed metadata collected at the time the experiment is performed. Clear, annotated raw data should be provided, and data analyses should clearly describe each action taken from raw data to final analysis.

This repository is a practical example of reproducible scientific data analysis. I have attempted to provide, to the greatest extent possible, a complete documentation of the methods that led to the results presented. It's not perfect. The information is not complete, as I worked with others who don't care about documenting their work. Some aspects of the experiment didn't work well, but that's the point. Experiments don't usually turn out exactly according to plan. **By carefully documenting the experiment, and sharing the results openly, I can understand what went wrong, and how to move forward in the most efficient way. That's how science should be.**

It might seem strange to my scientific colleagues, who are mostly focused on career advancement and personal aggrandizement, that I would take so much time to analyze preliminary data from a pilot study like this. **It's not just about the end result. If we want to address the reproducibility crisis, we need to focus on the process.**

### Practices

To promote reproducible scientific work:

- Comprehensively **document** experiments and analyses.
- Format code files as **computational narratives** mixing prose and code with a tool like Jupyter Notebook.
- **Version control code** with Git and share code on a website like GitHub.
- Create a **reproducible cloud computing environment** using a tool like Binder.

### Resources

- NPR correspondent Richard Harris sums up the reproducibility crisis in his book Rigor Mortis.
  - [Rigor Mortis: How Sloppy Science Creates Worthless Cures, Crushes Hope, and Wastes Billions, by Richard Harris](http://a.co/5uQDILy)
  - [Retraction Watch interview with Rigor Mortis author Richard Harris](https://retractionwatch.com/2017/04/04/failure-essential-part-science-qa-author-new-book-reproducibility/)
  - [Recorded livestream discussion at NYU](https://livestream.com/accounts/17645697/events/7229448/videos/153465413)
- The surgeon and writer Atul Gawande wrote a book about his research, in which he found that distributing a checklist (protocol) to surgical team members reduced patient deaths by half. If world-class surgeons can benefit from improved protocols, scientists certainly can also.
  - [The Checklist Manifesto, by Atul Gawande](http://a.co/0SjWYmN)
  - Haynes, AB et al. A surgical safety checklist to reduce morbidity and mortality in a global population. *NEJM* 360:491–499 (2009). DOI: [10.1056/NEJMsa0810119](https://doi.org/10.1056/NEJMsa0810119)
- The scientific journal *eLife* is a leader in reproducible data analysis and publishing. I particularly enjoy the [eLife Labs blog](https://elifesciences.org/labs). The Editor-in-Chief, Nobel laureate Randy Schekman, has written about the [reproducibility crisis](https://elifesciences.org/articles/31697) and the [damaging effects of luxury journals](http://www.theguardian.com/commentisfree/2013/dec/09/how-journals-nature-science-cell-damage-science). Naomi Penfold, Innovation Officer at eLife, has made me aware of many of the [tools below](#tools).
- These papers provide general discussions of reproducibility:
  - Barba LA. The hard road to reproducibility. *Science* 354:142 (2016). DOI: [10.1126/science.354.6308.142](https://doi.org/10.1126/science.354.6308.142)
  - Loscalzo J. Irreproducible experimental results: Causes, (mis)interpretations, and consequences. *Circulation* 125:1211–1214 (2012). DOI: [10.1161/circulationaha.112.098244](https://doi.org/10.1161/circulationaha.112.098244)
  - Morrison SJ. Time to do something about reproducibility. *eLife* 3:1–4 (2014). DOI: [10.7554/eLife.03981](https://doi.org/10.7554/eLife.03981)
  - Sarewitz D. The pressure to publish pushes down quality. *Nature* 533:147 (2016). DOI: [10.1038/533147a](https://doi.org/10.1038/533147a)
- This *Cell Reports* commentary is a valuable example of the importance of documentation for experimental reproducibility.
  - Hines WC, Su Y, Kuhn I, Polyak K, Bissell MJ. Sorting out the FACS: A devil in the details. *Cell Rep.* 6:779–781 (2014). DOI: [10.1016/j.celrep.2014.02.021](https://doi.org/10.1016/j.celrep.2014.02.021)
- Research reagents and materials, including antibodies, cell lines, and mice, appear to contribute substantially to lack of reproducibility.
  - Baker M. Reproducibility crisis: Blame it on the antibodies. *Nature* 521:274–276 (2015). DOI: [10.1038/521274a](https://doi.org/10.1038/521274a)
  - Couzin-Frankel J. When mice mislead. *Science* 342:922–925 (2013). DOI: [10.1126/science.342.6161.922](https://doi.org/10.1126/science.342.6161.922)
  - Ioannidis JPA. Extrapolating from animals to humans. *Sci. Transl. Med.* 4:151ps15 (2012). DOI:  [10.1126/scitranslmed.3004631](https://doi.org/10.1126/scitranslmed.3004631)
  - Lorsch JR, Collins FS, Lippincott-Schwartz J. Fixing problems with cell lines: Technologies and policies can improve authentication. *Science* 346:1452–1453 (2014). DOI: [10.1126/science.1259110](https://doi.org/10.1126/science.1259110)
  - Martin B, Ji S, Maudsley S, Mattson MP. 'Control' laboratory rodents are metabolically morbid: Why it matters. *PNAS* 107:6127–6133 (2010). DOI: [10.1073/pnas.0912955107](https://doi.org/10.1073/pnas.0912955107)
- *Nature* ironically reports on the reproducibility crisis, while continuing to publishing trendy irreproducible articles weekly.
  - Baker M. 1,500 scientists lift the lid on reproducibility. *Nature* 533:452–454 (2016). DOI: [10.1038/533452a](https://doi.org/10.1038/533452a)
  - Shen H. Interactive notebooks: Sharing the code. *Nature* 515:151–2 (2014). DOI: [10.1038/515151a](https://doi.org/10.1038/515151a)
- The citation style used above is my own custom style that I used in my [dissertation](http://hdl.handle.net/2142/72961). It combines aspects of the Nature and BioMed Central (BMC) styles. The style is informative, concise, and light on punctuation and formatting.

#### Tools

- [Binder](https://mybinder.org/) turns GitHub repositories into reproducible computing environments. It uses code and dependency files to create [Docker](https://www.docker.com/) images that run in web browsers. **Binder is a potentially great feature, but my experience so far is that it's extremely slow, and not properly loading additional R packages.**
- [Gigantum](http://gigantum.io/): Research project management and collaboration system. It version-controls your research materials, allows them to be easily shared and published, and bundles everything to run reproducibly in the cloud.
- [Greene Integrative Genomics Laboratory at Penn](http://www.greenelab.com/): Bioinformatics lab that prioritizes transparent and computationally reproducible research. They developed a pipeline for continuous analysis of research data (see [Nature Biotechnology paper](https://www.nature.com/articles/nbt.3780), [GitHub](https://greenelab.github.io/continuous_analysis/) and [eLife Labs blog post](https://elifesciences.org/labs/e623676c/reproducibility-automated)), and published an [open, collaborative review article](https://greenelab.github.io/deep-review/) and an [analysis of Sci-Hub](https://elifesciences.org/articles/32822). Check out their [GitHub](https://github.com/greenelab/).
- [Hypothesis](https://web.hypothes.is/): Open annotations on the web.
- Jupyter Notebook:
  - See below
  - Somers J. "[The scientific paper is obsolete](https://www.theatlantic.com/science/archive/2018/04/the-scientific-paper-is-obsolete/556676/)." *The Atlantic*, 20180405
- [Open Science Framework](https://cos.io/our-products/open-science-framework/): Research project management and collaboration system. Integrates many other software tools and forms of data.
- [Protocols.io](https://www.protocols.io/): Open access repository for creation and sharing of scientific protocols.
- [ScienceFair](http://sciencefair-app.com/): Decentralized p2p science literature client. See the [eLife Labs blog post](https://elifesciences.org/labs/88b45406/sciencefair-a-new-desktop-science-library) about ScienceFair.
- [sciNote](https://scinote.net/): Free electronic lab notebook.
- [Stencila](https://stenci.la/): Open document suite that can be used to write and run code in a computationally reproducible way. I recently attended an eLife webinar about Stencila. eLife is [considering](https://elifesciences.org/for-the-press/e6038800/elife-supports-development-of-open-technology-stack-for-publishing-reproducible-manuscripts-online) Stencila as part of a "Reproducible Document Stack" to generate their manuscripts.
- [We-Sci](http://www.we-sci.com/): Tool to ensure proper attribution for scientific work.
- [Whole Tale](http://wholetale.org/): Research project management system.
- [Zenodo](https://zenodo.org/): Repository for digital materials to be permanently archived and stored with DOI versioning.

[(Back to top)](#top)

#### Workshops

- [Data Carpentry](http://www.datacarpentry.org/), which is sponsored by [NumFOCUS](https://www.numfocus.org/), has a [Reproducible Science Curriculum](https://github.com/Reproducible-Science-Curriculum) and holds workshops on reproducible data analysis in Python and R.
- The Harvard [Institute for Applied Computational Science (IACS)](https://iacs.seas.harvard.edu/) provides free resources to the scientific computing community, such as the annual [Computefest](https://computefest.seas.harvard.edu/). See *EDA.ipynb* and *grammarofdata.ipynb* from [Computefest 2018](https://github.com/Harvard-IACS/computefest2018-pandas) for info on reproducible Exploratory Data Analysis (EDA) workflows.
- Vincent Carey (Harvard Medical School, Brigham & Women's Hospital) provided helpful [resources](https://github.com/vjcitn/Repro2017) for reproducible data analyses associated with his Repro2017 Harvard Catalyst talk.

[(Back to top)](#top)

## Scientific background

This is a summary report of an experiment I performed during my postdoc. The goal of this experiment was to identify a [molecular](https://www.khanacademy.org/science/biology/macromolecules) complex associated with Nrf1, a protein our research group was studying. Nrf1 is also abbreviated NFE2L1, and should not be confused with Nuclear Respiratory Factor 1.

We began studying Nrf1 because it resides in a [cellular organelle](https://youtu.be/URUJD5NEXC8) called the Endoplasmic Reticulum (ER). We study the ER and its roles in [metabolism](http://learn.genetics.utah.edu/content/metabolism/). We found that Nrf1 mediates the cellular response to cholesterol, and that it seemed to do this separately from its known function as a genetic transcription factor in the nucleus. Cholesterol metabolism occurs at the ER, and is very important in the liver, where cholesterol is metabolized and prepared for excretion.

We hypothesize that a group of other proteins interacts with Nrf1 to mediate its response to cholesterol at the ER. We used proteomics to test our hypothesis, which identifies all possible proteins in a sample with a technique called mass spectrometry.

I incorporated practices for reproducible scientific experimentation and data analysis throughout the project.

[(Back to top)](#top)

## Supplementary data

Supplementary data files, including the electronic lab notebook, protocols, datasheets and information on materials used, raw data, other data analyses, slides, and images, are available in the *[data-supplementary](data-supplementary)* sub-directory of this repository.

[Git-LFS](https://git-lfs.github.com/) was used to manage supplementary files.

```sh
$ brew install git-lfs
$ git lfs install
$ cd path/to/repo
$ touch .gitattributes
$ git lfs track "*.docx" "*.pdf" "*.pptx" "*.xlsx" "*.zip"
Tracking "*.docx"
Tracking "*.pdf"
Tracking "*.pptx"
Tracking "*.xlsx"
Tracking "*.zip"
$ git add .gitattributes
$ git commit -m "Initialize Git LFS"
$ git add --all
$ git commit
$ git push origin master
$ git lfs push origin master
```

## Data analysis

### Jupyter Notebook

- Data analysis was performed with the [Python](https://www.python.org/) 3 computing language in a [Jupyter Notebook](http://jupyter.org) computational narrative.
- Jupyter Notebook **combines prose and code** to promote construction of **reproducible computational narratives** that configure the computing environment and precisely describe each step in the data analysis. When code from a reproducible computational narrative is run on another computer, there is a high probability that the same result will be obtained. Reproducibility.
- [JupyterLab](http://jupyterlab.readthedocs.io/en/latest/) can be used to run Jupyter Notebook files.
- [Binder](https://mybinder.org/) can run Jupyter Notebooks in the cloud.
- Google provides a cloud-based Jupyter Notebook environment called [Colaboratory](https://colab.research.google.com). At the time of this writing, it only supports Python.

## Results

![Volcano plot from R analysis comparing proteins in cholesterol-fed vs chow-fed liver](img/r-proteomics-nrf1-volcano.png)

Complement C1q proteins A, B, C (green dots in the plot above) were identified as potentially interacting with Nrf1 in the setting of liver cholesterol accumulation. The experiment did have notable limitations, which prompted us to refine our methods and continue with further experiments.

[(Back to top)](#top)