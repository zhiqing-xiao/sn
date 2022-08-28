

- Section 2.1.4, paragraph 5: change from 【 For episodic tasks, let $R_t=0$ for $t>T$. The discount factor of episodic tasks is usually $\gamma \in \left(0,1\right]$. We will use this unified notation throughout the book. 】 to 【 For episodic tasks, let $R_t=0$ for $t>T$. In fact, the discount factor of an episodic task can also be $<1$. Consequently, discount factor of an episodic task is usually $\gamma \in \left(0,1\right]$, while discount factor of a sequential task is usually $\gamma \in \left(0,1\right)$. We will use this unified notation throughout the book. 】(The first and last sentense remain unchanged. The middle sentense is extended. Previous statement is misleading.)

- Section 2.3.2: An item start with 【Use state-action distribution at time $t$ to back up the state-action distribution at time $t+1$:】, in the proof, first parentheses, change 【 $\mathsf{s}' in \mathcal{S}$ 】 to 【 $\mathsf{s} in \mathcal{S}$ 】. (remove the ' on $\mathsf{s}$.)

- Section 2.3.4, Paragraph 2: Change 【 many statistics can be represented using the  notation of expected over distribution.】 to 【many statistics can be represented using the  notation of expected over discounted distribution.】 Add a word "discounted".

- Section 2.4.3, the first item group, the first item: Change 【Therefore, $\pi_\ast < \pi'$, which conflicts】to 【Therefore, $\pi_\ast \prec \pi'$, which conflicts】.

- Section 3.1, the paragraph after "Interdisciplinary Reference 3-2", the formula after the line "Therefore". Please take care whether there are extra period ".". (There may be or may not be, I am not sure.)

- Section 4.1.2, the paragraph before Algo. 4-5: Change 【Step 2.5.3】 to 【Step 2.5.2】  (three times in this paragraph).

- Section 6.2.1, Interdisciplinary Reference 6-1, the third paragraph, change 【(Zhiqing, 2018)】 to 【(Xiao, 2018)】.

- Section 8.2.2, Algo. 8-3. Please help check the format consistency (especially the intent) between Step 3.1 and Step 3.2.

- Section 13.3: In a line between two formula, change 【Due to the selection method of `$\mathsf{A}_t$`,】 to 【Due to the selection method of `$\mathsf{A}_{\kappa,t}$`,】 (add things to the subscript.)

- Section 16.1.2, the paragraph starts with "The way to use differential values to calculate average reward is", change 【$r_\pi$】  to 【`$\bar{r}_\pi$`】 (4 occurances in total). The first equation group will become 【 `${{\bar r}_\pi } = \sum\limits_\mathsf{a} {\pi \left( {\mathsf{a}|\mathsf{s}} \right)\sum\limits_{\mathsf{s'}} {p\left( {\mathsf{s'}|\mathsf{s},\mathsf{a}} \right)} \left[ {r\left( {\mathsf{s},\mathsf{a},\mathsf{s'}} \right) - {{\tilde v}_\pi }\left( \mathsf{s} \right) + {{\tilde v}_\pi }\left( {\mathsf{s'}} \right)} \right]} , & \mathsf{s} \in {\cal S}, {{\bar r}_\pi } = \sum\limits_{\mathsf{s'},r} {p\left( {\mathsf{s'},r|\mathsf{s},\mathsf{a}} \right)\sum\limits_{\mathsf{a'}} {\pi \left( {\mathsf{a'}|\mathsf{s'}} \right)\left[ {r - {{\tilde q}_\pi }\left( {\mathsf{s},\mathsf{a}} \right) + {{\tilde q}_\pi }\left( {\mathsf{s'},\mathsf{a'}} \right)} \right]} } , & \mathsf{s} \in {\cal S},\mathsf{a} \in {\cal A}$`.】 The second equation group will change from 【`${\tilde v_\pi }\left( \mathsf{s} \right) = \sum\limits_\mathsf{a} {\pi \left( {\mathsf{a}|\mathsf{s}} \right)\sum\limits_{\mathsf{s'}} {p\left( {\mathsf{s'}|\mathsf{s},\mathsf{a}} \right)} \left[ {r\left( {\mathsf{s},\mathsf{a},\mathsf{s'}} \right) - {r_\pi } + {{\tilde v}_\pi }\left( {\mathsf{s'}} \right)} \right]} ,\quad \mathsf{s} \in {\cal S}$`】to【`${\tilde v_\pi }\left( \mathsf{s} \right) = \sum\limits_\mathsf{a} {\pi \left( {\mathsf{a}|\mathsf{s}} \right)\sum\limits_{\mathsf{s'}} {p\left( {\mathsf{s'}|\mathsf{s},\mathsf{a}} \right)} \left[ {r\left( {\mathsf{s},\mathsf{a},\mathsf{s'}} \right) - {\bar{r}_\pi } + {{\tilde v}_\pi }\left( {\mathsf{s'}} \right)} \right]} ,\quad \mathsf{s} \in {\cal S}$`】. The third equation group will change from 【`${\tilde q_\pi }\left( {\mathsf{s},\mathsf{a}} \right) = \sum\limits_{\mathsf{s'},r} {p\left( {\mathsf{s'},r|\mathsf{s},\mathsf{a}} \right)\sum\limits_{\mathsf{a'}} {\pi \left( {\mathsf{a'}|\mathsf{s'}} \right)\left( {r - {r_\pi } + {{\tilde q}_\pi }\left( {\mathsf{s'},\mathsf{a'}} \right)} \right)} } ,\quad \mathsf{s} \in {\cal S},\mathsf{a} \in {\cal A}$`】 to【`${\tilde q_\pi }\left( {\mathsf{s},\mathsf{a}} \right) = \sum\limits_{\mathsf{s'},r} {p\left( {\mathsf{s'},r|\mathsf{s},\mathsf{a}} \right)\sum\limits_{\mathsf{a'}} {\pi \left( {\mathsf{a'}|\mathsf{s'}} \right)\left( {r - {\bar{r}_\pi } + {{\tilde q}_\pi }\left( {\mathsf{s'},\mathsf{a'}} \right)} \right)} } ,\quad \mathsf{s} \in {\cal S},\mathsf{a} \in {\cal A}$`】.


----

The repo is for editors only. Readers should go to https://zhiqingxiao.github.io/rl-book/en2022
