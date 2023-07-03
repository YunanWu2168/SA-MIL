<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Smooth Attention for Deep Multiple Instance
Learning: Application to CT Intracranial
Hemorrhage Detection</h3>

  <p align="center">
    The codes for the paper accepted in MICCAI 2023.
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#introduction">Introduction</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
  </ol>
</details>



<!-- INTRODUCTION -->
## Introduction

Multiple Instance Learning (MIL) has been widely applied to medical imaging diagnosis, where bag labels are known and instance labels inside bags are unknown. Traditional MIL assumes that instances in each bag are independent samples from a given distribution. However, instances are often spatially or sequentially ordered, and one would expect similar diagnostic importance for neighboring instances. To address this, in this study, we propose a smooth attention deep MIL (SA-DMIL) model. Smoothness is achieved by the introduction of first and second order constraints on the latent function encoding the attention paid to each instance in a bag. The method is applied to the detection of intracranial hemorrhage (ICH) on head CT scans.
The results show that this novel SA-DMIL: (a) achieves better performance than the non-smooth attention MIL at both scan (bag) and slice (instance) levels; (b) learns spatial dependencies between slices; and (c) outperforms current state-of-the-art MIL methods on the same ICH test set.   

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites

This is an example of how to list things you need to use the software and how to install them.
* The codes use Tensorflow and you can download all packages in [requirements.txt](https://github.com/YunanWu2168/SA-MIL/blob/master/requirements.txt).

```
matplotlib==3.7.1

numpy==1.22.4

opencv_contrib_python==4.7.0.72

opencv_python==4.7.0.72

opencv_python_headless==4.7.0.72

pandas==1.5.3

scikit_learn==1.2.2

tensorflow==2.12.0
```

### Installation

1. Pip install [requirements.txt](https://github.com/YunanWu2168/SA-MIL/blob/master/requirements.txt)
   ```sh
   pip install requirements.txt
   ```
2. Open SA-MIL-preprocessing.ipynb - How to process head CTs
3. Open SA-MIL-training.ipynb - Train SA-DMIL
4. Open Non-SA-MIL-training.ipynb - Train Att-MIL
5. Open SA-MIL-testing.ipynb - Test SA-DMIL and Att-MIL
6. Open vis-SA-MIL.ipynb - Visualize at slice level

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Dataset

### Download
The dataset used in this paper can be download via [Kaggle Challenge Dataset](https://www.kaggle.com/competitions/rsna-intracranial-hemorrhage-detection/data)

### CT Slice Image Processing with Windowing 
[SA_MIL_preprocessing.ipynb](https://github.com/YunanWu2168/SA-MIL/blob/master/SA_MIL_preprocessing.ipynb)

<!-- USAGE EXAMPLES -->
## Usage

1. Model training at scan level

  [SA_MIL_training.ipynb](https://github.com/YunanWu2168/SA-MIL/blob/master/SA_MIL_training.ipynb)

  [Non_SA_MIL_training.ipynb](https://github.com/YunanWu2168/SA-MIL/blob/master/Non_SA_MIL_training.ipynb)

2. Model testing at scan level

  [SA_MIL_testing.ipynb](https://github.com/YunanWu2168/SA-MIL/blob/master/Non_SA_MIL_testing.ipynb)

4. Model testing at slice level

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

