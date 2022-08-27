---
theme: default
highlighter: shiki
lineNumbers: false
info: |
  # Rectify the pronunciations of Chinese children.
---

<h1 class="-mt-32">How to rectify the pronunciations of Chinese children.</h1>

<div class="text-3xl">Use the <b>Mandarin</b> as the standard.</div>

<div class="abs-bl mx-14 my-12 flex">
  <div class="ml-1 mr-48 flex flex-col text-left">
    <div class="text-2xl"><b>Group 1</b></div>
    <div class="text-2xl">August 27th, 2022</div>
  </div>
  <div class="ml-64 flex flex-col text-left">
    <div class="text-2xl">Dongze Wu</div>
    <div class="text-2xl">Dannong Xu</div>
    <div class="text-2xl">Buxiao Chu</div>
    <div class="text-2xl">Siwei Zhang</div>
  </div>
</div>


---

# Introduction
<div></div>

Target group:

Chinese younger students (under 11 years-old)

<br/>

Kindergarten Students (3-6 years-old) : 

Single words, short phrases & sentences

<br/>

Grade 1-3 Students (7-10 years-old) : 

Harder words, complex phrases, longer sentences

---

# Input

Recording from students:
- For the word test, children need to read each word independently. Each word will be a single record.
- For the sentence test, each record will include a whole sentence.  

---

# Output

The **mistake** that the machine finds in the recording:
- Words: just pronunciation
- Phrases/Sentences: also pitch, intonation, interval time span
- The consultant pronunciation record  in sound form
- The accuracy rate of the whole text and some key words 

---

# Dataset

<div></div>

Use the models trained by Chinese language database to generate the right pronunciation of the reading materials according to the context.

<br/>

> AIShell-1: An Open-Source Mandarin Speech Corpus and A Speech Recognition Baseline

![aishell1.png](/aishell1.png)

---

| **Themes**                    | Applied                                                      |
| ----------------------------- | ------------------------------------------------------------ |
| Models (wk2)                  | Train classifiers for each heteronym under different contexts. |
| Educational data mining (wk3) | Record the time length when students read texts to evaluate their proficiency. |
| content generation (wk4)      | Train networks to generate the right pronunciation of heteronyms in Chinese through the contexts. |
| Embedded experiments (wk5)    | Determine which learning method is the most helpful.  |
| Evaluation (wk6)              | Compare the advantage between our machine tutor and real people. |


<style>
.slidev-layout td {
  font-size: 1.6rem;
}
</style>

---

# Example

<div></div>

**Reading:** Automated Generation of Example Contexts for Helping Children Learn Vocabulary

**Contexts:** Pronunciation Constraint

<br/>

Use the **contexts** to train neural networks as **classifiers** for each heteronym.

These **classifiers** could be used to sign the pronunciations of unfamiliar articles

E.g. 路上的**行**人 This pronunces xíng and means 'walking'

银**行**  This pronunces háng and means 'agency'.

---

# Example

<img src="/network.ppm" alt="network" style="zoom: 45%;" />

<br/>

Input: **Context** / Output: **Pronunciation**

Characters have different **weights**

The **closer** characters & **notional** words should be more important

E.g. 元宵节入夜，灯会上**走动**的行人逐渐增多

---

# Reference

<br/>

- [Hui Bu, Jiayu Du, Xingyu Na, Bengu Wu, Hao Zheng. AIShell-1: An Open-Source Mandarin Speech Corpus and A Speech Recognition Baseline. Oriental COCOSDA 2017.](http://openslr.elda.org/33/)
  
- Liu, L., Mostow, J., & Aist, G. (2009, September 3-5). Automated Generation of Example Contexts for Helping Children Learn Vocabulary. Second ISCA Workshop on Speech and Language Technology in Education (SLaTE), Wroxall Abbey Estate, Warwickshire, England.

