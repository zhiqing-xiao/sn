

- Section 2.1.4, paragraph 5: change from 【 For episodic tasks, let $R_t=0$ for $t>T$. The discount factor of episodic tasks is usually $\gamma \in \left(0,1\right]$. We will use this unified notation throughout the book. 】 to 【 For episodic tasks, let $R_t=0$ for $t>T$. In fact, the discount factor of an episodic task can also be $<1$. Consequently, discount factor of an episodic task is usually $\gamma \in \left(0,1\right]$, while discount factor of a sequential task is usually $\gamma \in \left(0,1\right)$. We will use this unified notation throughout the book. 】(The first and last sentense remain unchanged. The middle sentense is extended. Previous statement is misleading.)

- Section 2.3.2: An item start with 【Use state-action distribution at time $t$ to back up the state-action distribution at time $t+1$:】, in the proof, first parentheses, change 【 $\mathsf{s}' in \mathcal{S}$ 】 to 【 $\mathsf{s} in \mathcal{S}$ 】. (remove the ')

- Section 2.3.4, Paragraph 2: Change 【 many statistics can be represented using the  notation of expected over distribution.】 to 【many statistics can be represented using the  notation of expected over discounted distribution.】 Add a word "discounted".

- Section 2.4.3, the first item group, the first item: Change 【Therefore, $\pi_* < \pi'$, which conflicts】to 【Therefore, $\pi_* \preceq \pi'$, which conflicts】.

----

The repo is for editors only. Readers should go to https://zhiqingxiao.github.io/rl-book/en2022
