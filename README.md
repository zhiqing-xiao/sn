Update on 2023-03-27:

- Section 2.4.3. Change a 【 $\pi$ 】 in subscript is to 【 $\ast$ 】:

_From:_

The relationship that uses optimal action value at time $t+1$ to back up the optimal action value at time $t$:
$q_\ast\left(\mathsfit{s},\mathsfit{a}\right)=r\left(\mathsfit{s},\mathsfit{a}\right)+\gamma\sum\limits_{\mathsfit{s'},\mathsfit{a'}}{p_\ast\left(\mathsfit{s'},\mathsfit{a'}|\mathsfit{s},\mathsfit{a}\right)q_\pi\left(\mathsfit{s'},\mathsfit{a'}\right)},\quad \mathsfit{s}\in\mathcal{S},\mathsfit{a}\in\mathcal{A}$

_To:_

The relationship that uses optimal action value at time $t+1$ to back up the optimal action value at time $t$:
$q_\ast\left(\mathsfit{s},\mathsfit{a}\right)=r\left(\mathsfit{s},\mathsfit{a}\right)+\gamma\sum\limits_{\mathsfit{s'},\mathsfit{a'}}{p_\ast\left(\mathsfit{s'},\mathsfit{a'}|\mathsfit{s},\mathsfit{a}\right)q_\ast\left(\mathsfit{s'},\mathsfit{a'}\right)},\quad \mathsfit{s}\in\mathcal{S},\mathsfit{a}\in\mathcal{A}$



----

Errata on the Interdisciplinary Reference 4-2 in Section 4.1.1 has been sent via email on 2023-03-19.

----

- Preface, Features, 2nd Item Group, Item 4: Change 【PyTorch 1】 to 【PyTorch 1&2】.
- Section 2.4.3, in the example, the paragraph starting with "Case II", the sentense "The condition can be simplied to $\gamma\ge\frac{1-4\alpha}{1-\alpha}$ and $\gamma<\frac{1-4\beta}{1-\alpha}$". Change 【 $\gamma<\frac{1-4\beta}{1-\alpha}$  】 to 【 $\gamma\ge\frac{1-4\beta}{1-\alpha}$  】.
- Section 5.7.3, Problem 5-8: (The author assigned the style incorrectedly. Please notice the paragraph format.)
- Section 6.5.3, Paragraph 5: Change 【PyTorch 1】 to 【PyTorch 1&2】 (two occurances).
- Section 6.7.1, Problem 6-1: Remove the answer 【[A]】.
- Section 6.7.2, before Problem 6.5: Remove the line in Chinese.
- Section 12.4, Paragraph 1: Change 【They conducted】 to 【They conduct】.
- Section 15.5, correct the numbering of heading.
- Section 15.6, correct the numbering of heading.
- Section 16.2, bullet, entry 1: Change 【 $G_t=\int_{t}^{T}\gamma^{\tau-t}dR_\tau+G_T$ 】 to 【 $G_t=\int_{t}^{T}\gamma^{\tau-t}dR_\tau+\gamma^{T-t}G_T$ 】.

----

An updated Word has been emailed on 2022-09-26.

The content of Word sent on 2022-09-18 shared exactly the same contents as that sent on 2022-09-26.

----

The repo is for editors only. Readers should go to https://zhiqingxiao.github.io/rl-book/en2022
