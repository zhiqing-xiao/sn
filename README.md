Zhiqing has removed errata entries that have been corrected in the PDF attached on 2023-11-16 email.

----

Update on 2023-11-18

- <span style='color: blue;'>Feedback based on the PDF 2023-11-16.</span> Section 3.5, the Author Query "AU1": Let me explain it: I meant that, the "quotation marks" in codes needs to be straight quotation marks, rather than left quotation marks or right quotation marks. Example: `"`. You can either use single quotation marks (i.e. `'`) or double quotation marks (i.e. `"`), but please be consistent within the whole paragraph.

- <span style='color: blue;'>Feedback based on the PDF 2023-11-16.</span> Section 4.1.1, Fig. 4-1. I noticed that this figure is rasterized rather than vectorized. It should be vectorized. Please repaste. (Please tell me if you want me to email the source of figure again.)


----

Update on 2023-10-XX

- Section 2.4.1. The second bullet point. Block math. Change 【 $p_\ast\left(\mathsfit{s'},\mathsfit{a'}|\mathsfit{s},\mathsfit{a}\right)=\sum\limits_{\mathsfit{a'}}{\pi_\ast\left(\mathsfit{a'}\mid\mathsfit{s'} \right)\sum\limits_\mathsfit{a}{p\left(\mathsfit{s'}\mid\mathsfit{s},\mathsfit{a}\right)}},\quad\mathsfit{s}\in\mathcal{S},\mathsfit{a}\in\mathcal{A}\left(\mathsfit{s}\right),\mathsfit{s'}\in\mathcal{S},\mathsfit{a}\in\mathcal{A}\left(\mathsfit{s'}\right)$ 】 to 【 $p_\ast\left({\mathsfit{s'},\mathsfit{a'}\mid\mathsfit{s},\mathsfit{a}}\right)=\pi_\ast\left(\mathsfit{a'}\mid\mathsfit{s'}\right)p\left( \mathsfit{s'}\mid\mathsfit{s},\mathsfit{a}\right),\quad\mathsfit{s}\in\mathcal{S},\mathsfit{a}\in\mathcal{A}\left(\mathsfit{s}\right),\mathsfit{s'}\in\mathcal{S},\mathsfit{a'}\in\mathcal{A}\left(\mathsfit{s'}\right)$ 】. That is, remove two summation signs, and add a prime at the last $\mathsfit{a}$.

Update on 2023-09-XX

- Section 2.1.4, the last but one paragraph, the last line, change 【 $\sum\limits_{\tau=1}^{+\infty}{\gamma^\tau R_{\left(t+1\right)+\tau+1}}$  】 to 【 $\sum\limits_{\tau=0}^{+\infty}{\gamma^\tau R_{\left(t+1\right)+\tau+1}}$ 】. That is, change 【1】 to 【0】. (one occurrence in total.)


<span style='color: grey;'>Update on 2023-05-XX:</span>

- <span style='color: grey;'>Section 16.6.1, 3rd paragraph, Change 【`sequential`】 to 【`episodic`】. Three cases in total. After the change, the paragraph be alike: 【Code 16.1 implements the environment. The constructor of the class `TigerEnv` has a parameter `episodic`. We can deploy an episodic task by setting `episodic` as True, and deploy a sequential task by setting `episodic` to `False`.】</span><span style='color: red;'>【Update 2023-11-18】I noticed that, ,the first edit also incorrectedly remove the code format. Please edit it back. That is, change 【The constructor of the class `TigerEnv` has a paramter episodic.】 to 【The constructor of the class `TigerEnv` has a paramter `episodic`.】. </span>

<span style='color: grey;'>Update on 2023-04-27:</span>

- Please search the whole book: Change 【discounted factor】to 【discount factor】.<span style='color: grey;'> (Section 2.6, 4.3.2, 6.4.1, 8.2.1, 8.2.2, 8.2.3, 8.4.3, 8.5, 9.2, 9.3.1, 16.6.1, Tables of Codes):</span><span style='color: red;'>【Update 2023-11-18】Parameters of Algo. 6.8, Table of codes: Code 16.3 (You can also search the PDF to identify the occurrences)</span>

- <span style='color: grey;'>Section 6.7.1, Problem 6-1: Remove the answer 【[A]】.</span><span style='color: red;'>【Update 2023-11-18】 Section 6.7.1, Problem 6-1: I did not mean to remove the choice A. I meant the remove the "answer" that had been incorrectly pasted after the choices, while keeping all of the three choices. Please help add the choice A back. The choices of question 6.1 should be:</span>

<span style='color: red;'>  A. Stochastic gradient descent does NOT use bootstrapping.</span>

<span style='color: red;'>  B. Semi-gradient descent does NOT use bootstrapping.</span>

<span style='color: red;'>  C. Semi-gradient descent with eligibility trace does NOT use bootstrapping.</span>


----

The repo is for editors only. Readers should go to https://zhiqingxiao.github.io/rl-book/en2023
