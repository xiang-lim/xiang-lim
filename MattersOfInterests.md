## Matters Of Interest

### Navigation

- [Back](https://github.com/xiang-lim)
- [About](#about-top)
- [Experimental Ideas](#experimental-ideas-top)
- [Projects](#projects-top)

---

### About [[top]](#matters-of-interest)

A repository to catalog all experimental ideas and projects.

All projects/repositories will follow this project's license unless otherwise
stated in the project/repository itself.

---

### Experimental Ideas [[top]](#matters-of-interest)

<blockquote>

**Idea 2: BetterScribe**

About:
Understanding how speech to text work

Status: In progress
<details>
<summary>Improvements</summary>

</details>
<details>
<summary>Learnt</summary>

</details>
<details>
<summary>Next step</summary>

</details>
</blockquote>

---

### Projects [[top]](#matters-of-interest)

<blockquote>

**[Project 1: Symmetry](https://github.com/xiang-lim/Symmetry)**

About:
A project to find patterns in terraform files which can be used to create templates of cloud resource configurations

Status:
Completed

<details>
<summary>Improvements</summary> <blockquote>
<details>
<summary>Overall</summary>

- A naive approach to tackle code clustering patterns.
- Bad design to persist data

</details>
<details>
<summary>Data pre-processing section</summary>

**Problem:**

<blockquote>

Using Regex

- to handle the splitting of code block
- to remove tags
- to remove source field and having to manually map to AWS resources

</blockquote>

**Reason for improvements:**

<blockquote>
Having to manually set up the pre-processing to parse a data in specific ways so that the clusters of code can be determined
</blockquote>

</details>
<details><summary>Data Processing and Machine Learning section</summary>

**Problem:**

<blockquote>

Machine Learning Model

- Heavily relies on data to be cleansed and processed
- Unable to differentiate that certain fields are meant to be dissimilar

Data provided

- Transform code of blocks into numpy array by determining the sequences of code blocks that match

</blockquote>

**Reason for improvements:**

<blockquote>

Data has been reduced to an array of numbers without weight (importance) and context.
Certain blocks of code have the same configurations but referenced arns/endpoints might be different.

Another issue is that some code blocks are fields that references other resources.
This becomes a limitation as `Symmetry` cannot determine the template for such resources.
</blockquote>

</details>
</blockquote></details>


<details><summary>Learnt</summary><blockquote>

- Able to cleanse and segment code blocks
- Utilise TF-IDF and Sequence Matcher
- Able to parse code blocks into numpy array
- Visualize clusters using scipy
- Automate calculation of elbow method to optimize KMeans Cluster
- Label similar clusters of code blocks

</blockquote>

</details>

<details><summary>Next Step</summary><blockquote>

Experimental Idea `Symmetric`:

Ideate a way to have unsupervised learning that is able to grasp the underlying rules when processing the data.

Project `Tetraform`:

Create terraform language generator to effectively create group of resources from a configuration file
</blockquote>
</details>
</blockquote>

<blockquote>

**[Project 2: Linart](https://github.com/xiang-lim/Linart)**

About:
A project that converts jpeg images into a line art

Status: Completed
<details>
<summary>Learnt</summary>

1. Depth perception issue: Using an image, it's hard for the computer to determine which sections of the image is more "in front of" the other .
2. Hard to define which point is on the edge and which are enclosed or excluded by the "edge". Perhaps there are other factors needed to be considered to determine the edge.
3. Multi-Processing vs Multi-Threading
     * Multi-Processing: Better for more intense cpu
     * Multi-Threading: Better for IO
4. Experimented with HOG
</details>
<details>
<summary>Next step</summary>

1. Optimize computation and memory use
2. Figure a better way to approximate solution

</details>
</blockquote>

<blockquote>

**Project 3: Tetraform**

About:
A project that aims to create terraform language generator that effectively create group of resources from a
configuration file

Status: Not started
<details>
<summary>Improvements</summary>

</details>
<details>
<summary>Learnt</summary>

</details>
<details>
<summary>Next step</summary>

</details>
</blockquote>