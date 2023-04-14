Update on 2023-04-01:

- Math Notation, Other notation, first entry. Delete 【; partial oder of policy】

- Math Notation, Other notation, add another entry after first entry: 【 $\prec$, $\preceq$  partial order of policy】. The LaTeX codes are `\prec` and `\preceq`.

- Section 2.2.3, Algo. 2-1, Inputs: 

_From:_

dynamics $p$, policy $\pi$ and its values $v_\pi$ and action values $q_\pi$.

_To:_

policy $\pi$ and its action values $q_\pi$.

- Section 2.3.2, 2nd entry group, the 1st entry, first block math, rightmost part, Change 【 $\mathsfit{s'}\in\mathcal{S}$ 】 to 【 $\mathsfit{s}\in\mathcal{S}$ 】.

_From:_【 $\rho_\pi\left(\mathsfit{s}\right)=p_{\mathsfit{S}_0}\left(\mathsfit{s}\right)+ ..., \quad \mathsfit{s}'\in\mathcal{S}$ 】

_To:_【 $\rho_\pi\left(\mathsfit{s}\right)=p_{\mathsfit{S}_0}\left(\mathsfit{s}\right)+ ..., \quad \mathsfit{s}\in\mathcal{S}$ 】

- Section 2.3.2, 2nd entry group, the 2st entry, first block math, the smaller letter under the summation symbol $\Sigma$, Change 【 $\mathsfit{s}'\in\mathcal{S}$ 】 to 【 $\mathsfit{s}'\in\mathcal{S},\mathsfit{a}'\in\mathcal{A}$ 】.

_From:_

$\rho_\pi\left(\mathsfit{s},\mathsfit{a}\right)=p_{0,\pi}\left(\mathsfit{s},\mathsfit{a}\right)+\sum\limits_{\mathsfit{s}'\in\mathcal{S}}{\gamma{p_\pi}\left(\mathsfit{s},\mathsfit{a}\mid\mathsfit{s}',\mathsfit{a}'\right)\rho_\pi\left(\mathsfit{s}',\mathsfit{a}'\right)}$

_To:_

$\rho_\pi\left(\mathsfit{s},\mathsfit{a}\right)=p_{0,\pi}\left(\mathsfit{s},\mathsfit{a}\right)+\sum\limits_{\mathsfit{s}'\in\mathcal{S},\mathsfit{a}'\in\mathcal{A}}{\gamma{p_\pi}\left(\mathsfit{s},\mathsfit{a}\mid\mathsfit{s}',\mathsfit{a}'\right)\rho_\pi\left(\mathsfit{s}',\mathsfit{a}'\right)}$

- Section 2.4.3, delete a paragraph and following two entries: Delete 【

The relationship among the optimal values also has vector representations:

- The relationship that uses optimal state value at time $t+1$ to back up the optimal state value at time $t$:

$v_\ast\left(\mathsfit{s}\right)=r_\ast\left(\mathsfit{s}\right)+\gamma ... $

can be written as

$\mathbf{v}_\ast=...$

where ....

- The relationship that uses optimal action value at time $t+1$ to back up the optimal state value at time $t$:

$q_\ast\left(\mathsfit{s},\mathsfit{a}\right)=r\left(\mathsfit{s},\mathsfit{a}\right)+\gamma ... $

can be written as

$\mathbf{q}_\ast=...$

where .... is an $\left|\mathcal{S}\right|\left|\mathcal{A}\right|\times\left|\mathcal{S}\right|\left|\mathcal{A}\right|$ matrix.

】

- Section 2.4.3, Search "Case I": Change【 $\lt q_\ast\left(\text{full},\text{eat}\right)$ 】to 【 $\lt q_\ast\left(\text{full},\text{feed}\right)$ 】. (That is, change "eat" to "feed".)

- Section 2.4.3, Search "Case I" (the same entry as the above), inline math: Change 【 $v_\ast\left(\text{hungry}\right)=q_\ast\left(\text{hungry},\text{feed}\right)=$ 】to 【 $q_\ast\left(\text{hungry},\text{feed}\right)=$ 】.
Change 【 $q_\ast\left(\text{hungry},\text{ignore}\right)=$ 】 to 【 $v_\ast\left(\text{hungry}\right)=q_\ast\left(\text{hungry},\text{ignore}\right)=$ 】.
Change 【 $q_\ast\left(\text{full},\text{feed}\right)=$ 】 to 【 $v_\ast\left(\text{full}\right)=q_\ast\left(\text{full},\text{feed}\right)=$ 】.
Change 【 $v_\ast\left(\text{full}\right)=q_\ast\left(\text{full},\text{ignore}\right)=$ 】to 【 $q_\ast\left(\text{full},\text{ignore}\right)=$ 】.

- Section 2.4.3, Search "Case II": Change 【 $v_\ast\left(\text{hungry}\right)=q_\ast\left(\text{hungry},\text{eat}\right)=$ 】to 【 $v_\ast\left(\text{hungry}\right)=q_\ast\left(\text{hungry},\text{feed}\right)=$ 】. (That is, change "eat" to "feed".)

- Section 2.4.4, immediately after "Interdisciplinary Reference", just before the body text "Section 2.4.3 told us that", add two new paragraphs (outside the Interdisciplinary reference): 【

The reason why these programmings can find the optimal policy is as follows: We have known the equivalency between the discounted visitation frequency and the policy. Therefore, every feasible solution in the duel programming will meet the conditions for visitation frequencies so it corresponds to a policy, and every policy corresponds to a feasible solution in dual programming. Therefore, the dual programming can search over all policies and find the policy that obtains the optimal expected discounted return. Due to strong duality, the primary programming can find the values that obtains the optimal expected discounted return too.

People tend to use the primary programming, rather than the duel programming. The reasons are as follows: First, the optimal value is unique, but the optimal policies may not unique. Second, we can further change the primary programming such that it does not depend on the initial state distribution, while the duel programming always requires the knowledge of initial state distribution. Next, let us see how to make primary programming no longer dependent on the initial state distribution.

】

- Section 2.4.4, the example near the end of this subsection. There are two set of block math, in total they have six subscript $\pi$, and all six $\pi$ should be changed to $\ast$ . That is, two 【 $v_\pi$ 】 should be changed to 【 $v_\ast$ 】, and four 【 $q_\pi$ 】 should be changed to 【 $q_\ast$ 】. (Previously we have changed all "not eat" to "ignore".)

- Section 10.1.3, 2nd paragraph, the line after the block math. Change from 【the two policy satisfies】 to 【the two policies satisfy】.

----

Update on 2023-03-30:

- Section 2.1.2, the first bullet group, 1st entry:

_From:_

$p_{\mathsfit{S}_0}:\mathcal{S}\rightarrow\left[0,1\right]$

_To:_

$p_{\mathsfit{S}_0}$

- Section 2.1.2, the first bullet group, 2nd entry:

_From:_

$p:\mathcal{S}^+\times\mathcal{R}\times\mathcal{S}\times\mathcal{A}\rightarrow\left[0,1\right]$

_To:_

$p$

- Section 2.1.3, first paragraph:

_From:_

$\pi:\mathcal{S}\times\mathcal{A}\rightarrow\left[0,1\right]$

_To:_

$\pi$

- Section 2.4.4, near the end of this subsection, there is an "Example". In the last inline equation of this example, there is an equation set consisting of four equations. Two of them have "not eat". Both "not eat" should be changed to "ignore".

_From:_

$q_\ast\left(\text{hungry},\text{not eat}\right)=\frac{6}{11}$

_To:_

$q_\ast\left(\text{hungry},\text{ignore}\right)=\frac{6}{11}$


_From:_

$q_\ast\left(\text{full},\text{not eat}\right)=\frac{21}{11}$

_To:_

$q_\ast\left(\text{full},\text{ignore}\right)=\frac{21}{11}$

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
