Zhiqing has removed errata entries that have been corrected in the PDF attached on 2023-11-16 email. Zhiqing thanks for editors' efforts that resolve most of previous issues, as well as update Section 4.1.1 and Section 15.2 according to Word files.

----

Update on 2023-11-1X

- **(Feedback based on the PDF 2023-11-16.)** Section 1.6.2, Section 11.3.1: When codes are immediately followed by "Online Contents", could you please add a new blank line without background color, so that the two blocks can be apart visually?

- Chapter 2, Body Text, the first line: Change 【the most famous, the most classical, and most important】 to 【the most famous, most classical, and most important】. That is, remove the second "the".

- **(Feedback based on the PDF 2023-11-16.)** Section 3.5, the Author Query "AU1": Let me explain it: I meant that, the "quotation marks" in codes needs to be straight quotation marks, rather than left quotation marks or right quotation marks. Example: `"`. You can either use single quotation marks (i.e. `'`) or double quotation marks (i.e. `"`), but please be consistent within the whole paragraph.

- **(Feedback based on the PDF 2023-11-16.)** Section 4.1.1, Fig. 4-1. I noticed that this figure is rasterized rather than vectorized. It should be vectorized. Please repaste. (Please tell me if you want me to email the source of figure again.)

- **(Feedback based on the PDF 2023-11-16.)** Section 4.1.1, 2nd paragraph: Change 【the estimate of values based on the first $c$ samples is ...】 to 【the estimate of values based on the first $c$ samples is $\bar{g}_c=\frac{1}{c}\sum\nolimits_{i=1}^c{g_i}$ .】 The inline latex codes are `$\bar{g}_c=\frac{1}{c}\sum\nolimits_{i=1}^c{g_i}$`. There should not be any new line changes around the equation.

- Section 4.1.1, Interdisciplinary Reference 4.2, Search "Taking the expectation on the condition of", the block math after this line: Change 【 $=-2{\alpha_k}\left(X_{k-1}-x_\ast\right)f\left(X_{k-1}\right)+\alpha_k^2\mathrm{E}\left[\left|{F{{\left(X_{k-1}\right)}^2}}\right|\mid{X_{k-1}}\right]$ 】 to 【 $=-2{\alpha_k}\left(X_{k-1}-x_\ast\right)f\left(X_{k-1}\right)+\alpha_k^2\mathrm{E}\left[\left|{F{{\left(X_{k-1}\right)}}}\right|^2\mid{X_{k-1}}\right]$ 】

- Section 7.1.2, Search "Therefore, we get the recursive expression from", and there is a one-line block math, and then there is a line "Therefore,", and then there are a multi-line block math. In this multi-line block math, the line before "...", change the last entry from 【 

$\gamma^2{\mathrm{E}_{\pi\left(\boldsymbol\uptheta\right)}}\left[\nabla{v_{\pi\left(\boldsymbol\uptheta\right)}}\left(\mathsfit{S}_1\right)
\right]$

】 to 【

$\gamma^2{\mathrm{E}_{\pi\left(\boldsymbol\uptheta\right)}}\left[\nabla{v_{\pi\left(\boldsymbol\uptheta\right)}}\left(\mathsfit{S}_2\right)
\right]$

】. That is, change the subscript from 【1】 to 【2】. (Please notice that only the term that starts with 【$\gamma^2$】 needs to be changed.

- **(Feedback based on the PDF 2023-11-16.)** TOC, Section 15.1.1: The math symbol $f$ should be italic. (C.f. Other heading texts with math: Section 5.4.1, 5.4.2, 13.2.2.)


----

Update on 2023-10-XX

- Section 2.4.1. The second bullet point. Block math. Change 【 $p_\ast\left(\mathsfit{s'},\mathsfit{a'}|\mathsfit{s},\mathsfit{a}\right)=\sum\limits_{\mathsfit{a'}}{\pi_\ast\left(\mathsfit{a'}\mid\mathsfit{s'} \right)\sum\limits_\mathsfit{a}{p\left(\mathsfit{s'}\mid\mathsfit{s},\mathsfit{a}\right)}},\quad\mathsfit{s}\in\mathcal{S},\mathsfit{a}\in\mathcal{A}\left(\mathsfit{s}\right),\mathsfit{s'}\in\mathcal{S},\mathsfit{a}\in\mathcal{A}\left(\mathsfit{s'}\right)$ 】 to 【 $p_\ast\left({\mathsfit{s'},\mathsfit{a'}\mid\mathsfit{s},\mathsfit{a}}\right)=\pi_\ast\left(\mathsfit{a'}\mid\mathsfit{s'}\right)p\left( \mathsfit{s'}\mid\mathsfit{s},\mathsfit{a}\right),\quad\mathsfit{s}\in\mathcal{S},\mathsfit{a}\in\mathcal{A}\left(\mathsfit{s}\right),\mathsfit{s'}\in\mathcal{S},\mathsfit{a'}\in\mathcal{A}\left(\mathsfit{s'}\right)$ 】. That is, remove two summation signs, and add a prime at the last $\mathsfit{a}$.

Update on 2023-09-XX

- Section 2.1.4, the last but one paragraph, the last line, change 【 $\sum\limits_{\tau=1}^{+\infty}{\gamma^\tau R_{\left(t+1\right)+\tau+1}}$  】 to 【 $\sum\limits_{\tau=0}^{+\infty}{\gamma^\tau R_{\left(t+1\right)+\tau+1}}$ 】. That is, change 【1】 to 【0】. (one occurrence in total.)


**Update 2023-11-18** ~~Update on 2023-05-XX:~~

- Section 16.6.1, 3rd paragraph, ~~Change 【`sequential`】 to 【`episodic`】. Three cases in total. After the change, the paragraph be alike: 【Code 16.1 implements the environment. The constructor of the class `TigerEnv` has a parameter `episodic`. We can deploy an episodic task by setting `episodic` as True, and deploy a sequential task by setting `episodic` to `False`.】~~ **I noticed that, the first edit also incorrectedly remove the code format. Please edit it back. That is, change** 【The constructor of the class `TigerEnv` has a parameter episodic.】 **to** 【The constructor of the class `TigerEnv` has a parameter `episodic`.】.

**Update 2023-11-18** ~~Update on 2023-04-27:~~

- Please search the whole book: Change 【discounted factor】to 【discount factor】. ~~(Section 2.6, 4.3.2, 6.4.1, 8.2.1, 8.2.2, 8.2.3, 8.4.3, 8.5, 9.2, 9.3.1, 16.6.1, Tables of Codes):~~ **Parameters of Algo. 6.8, Table of codes: Code 16.3 (You can also search the PDF to identify the occurrences)**

- Section 6.7.1, Problem 6-1: ~~Remove the answer 【[A]】.~~  **I did not mean to remove the choice A. I meant to remove the "answer" that had been incorrectly pasted after the choices, with all three choices unchanged. Please help add the choice A back. The choices of problem 6.1 should be:**

  A. Stochastic gradient descent does NOT use bootstrapping.

  B. Semi-gradient descent does NOT use bootstrapping.

  C. Semi-gradient descent with eligibility trace does NOT use bootstrapping.


----

The repo is for editors only. Readers should go to https://zhiqingxiao.github.io/rl-book/en2023
