## Matters Of Interest

### 0. Navigation

- [Back](https://github.com/xiang-lim)
- [About](#1-about-top)
- [Experimental Ideas](#2-experimental-ideas-top)
- [Projects](#3-projects-top)

---

### 1. About [[top]](#0-Navigation)

A repository to catalog all experimental ideas and projects.

All projects/repositories will follow this project's license unless otherwise
stated in the project/repository itself.
---

### 2. Experimental Ideas [[top]](#0-Navigation)

---

### 3. Projects [[top]](#0-Navigation)

<details>
<summary> 1. Symmetry</summary> <blockquote>

Project Link: [Symmetry](https://github.com/xiang-lim/Symmetry)
<details>
<summary>Overview</summary>

A project to find patterns in terraform files which can be used to create templates of cloud resource configurations

</details>
<details>
<summary>Limitations</summary> <blockquote>
<details>
<summary>Overall</summary>

- A naive approach to tackle code clustering patterns.
- Bad design to persist data

</details>
<details>
<summary>Data pre-processing section</summary>

**Problem:**

~~~
Using Regex
- to handle the splitting of code block
- to remove tags
- to remove source field and having to manually map to AWS resources
~~~

**Reason for improvements:**

~~~
Having to manually set up the pre-processing to parse a data in specific ways so that the clusters of code can be determined
~~~

</details>
<details><summary>Data Processing and Machine Learning section</summary>

**Problem:**

~~~
Machine Learning Model
   - Heavily relies on data to be cleansed and processed
   - Unable to differentiate that certain fields are meant to be dissimilar

Data provided
   - Transform code of blocks into numpy array by determining the sequences of code blocks that match
~~~

**Reason for improvements:**

~~~
Data has been reduced to an array of numbers without weight (importance) and context.
Certain blocks of code have the same configurations but referenced arns/endpoints might be different.

Another issue is that some code blocks are fields that references other resources.
This becomes a limitation as `Symmetry` cannot determine the template for such resources.
~~~

</details>
</blockquote></details>

<details><summary>Learnt</summary>

**Gains**

~~~
- Able to cleanse and segment code blocks
- Utilise TF-IDF and Sequence Matcher
- Able to parse code blocks into numpy array
- Visualize clusters using scipy
- Automate calculation of elbow method to optimize KMeans Cluster
- Label similar clusters of code blocks
~~~

</details>

<details><summary>Next Step</summary>

**Ideas:**

~~~
Experimental Idea `Symmetric`: 
Ideate a way to have unsupervised learning that is able to grasp the underlying rules when processing the data.
~~~

~~~
Project `Tetraform`:
Create a terraform language generator to effectively create group of resources from a configuration file
~~~

</details>
</blockquote>
</details>