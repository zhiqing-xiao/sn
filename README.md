- Section 1.2, Fig. 1-4, caption: Change 【`https://www.gymlibrary.ml/pages/environments/box2d/bipedal_walker`】 to 【`https://www.gymlibrary.dev/environments/box2d/bipedal_walker/`】
- Section 1.6.2: Paragraph 3: Change 【`env = gym.make('CartPole-v0', new_step_api=True)`】 to 【`env = gym.make('CartPole-v0')`】. (Gym 0.26 released on 8 Sep 2022 removed this parameter.)
- Section 1.6.2: Paragraph 3: Remove 【The parameters `new_step_api` controls the API. This book uses new API, so we set ..... between the old API and new API in the sequel.】
- Section 1.6.2, Paragraph 6: Change 【which returns the initial observation】 to 【which returns an initial observation and an information variable of the type `dict`.】
- Section 1.6.2, Paragraph 8: Change 【For the API with `new_step_api = True`, this】 to 【This】.
- Section 1.6.2, Paragraph 8: Remove 【The old API with `new_step_api = False` only has ... logical-or of `termination` and `truncation`.】.
- Section 1.6.2, Gym Internal 1-5, The second paragraph: Change 【The parameters of the constructor of the class `Wrapper` are the environment object `env` and the parameter `new_step_api` to control the return format of the member function `step()`.】 to 【The parameter of the constructor of the class `Wrapper` is the environment object `env`.】.
- Section 1.6.2, Code 1-5, Codes: Change 【
```
    def step(self, action: ActType) -> Union[tuple[ObsType, float, bool, bool,
            dict], tuple[ObsType, float, bool, dict]]:
        """Steps through the environment with action."""
        from gym.utils.step_api_compatibility import step_api_compatibility
                # avoid circular import
        return step_api_compatibility(self.env.step(action), self.new_step_api)

    def reset(self, **kwargs) -> Union[ObsType, Tuple[ObsType, dict]]:
        """Resets the environment with kwargs."""
        return self.env.reset(**kwargs)

```
】 to 【
```
    def step(self, action: ActType) -> Tuple[ObsType, float, bool, dict]:
        """Steps through the environment with action."""
        return self.env.step(action)

    def reset(self, **kwargs) -> Tuple[ObsType, dict]:
        """Resets the environment with kwargs."""
        return self.env.reset(**kwargs)

```
】
- Section 1.6.2, Gym Internal 1-6, The first paragraph: Change 【the function `step()` returns `truncation` (new API) or `done` (old API) as `True`. The member `function step()` calls the function `step_api_compatibility()`, which converts the return to the new return format (5 return values) when `new_step_api = True`. and converts return format to the old return format (4 return values) when `new_step_api = False`.】 to 【the function `step()` returns `truncation` (new API) or `done` (old API) as `True`.】
- Section 1.6.2, Code 1-6, Codes, Line 2: Remove the line 【`from gym.utils.step_api_compatibility import step_api_compatibility`】
- Section 1.6.2, Code 1-6, Codes: Change 【
```
    def __init__(self, env: gym.Env, max_episode_steps: Optional[int]=None,
            new_step_api: bool=False):
        super().__init__(env, new_step_api)
        if max_episode_steps is None and self.env.spec is not None:
            max_episode_steps = env.spec.max_episode_steps
        if self.env.spec is not None:
            self.env.spec.max_episode_steps = max_episode_steps
        self._max_episode_steps = max_episode_steps
        self._elapsed_steps = None

    def step(self, action):
        """Steps through the environment and if the number of steps elapsed
        exceeds ``max_episode_steps`` then truncate."""
        observation, reward, terminated, truncated, info = \
                step_api_compatibility(self.env.step(action), True)
        self._elapsed_steps += 1

        if self._elapsed_steps >= self._max_episode_steps:
            truncated = True

        return step_api_compatibility((observation, reward, terminated,
                truncated, info), self.new_step_api)

```
】 to 【
```
    def __init__(self, env: gym.Env, max_episode_steps: Optional[int]=None):
        super().__init__(env)
        if max_episode_steps is None and self.env.spec is not None:
            max_episode_steps = env.spec.max_episode_steps
        if self.env.spec is not None:
            self.env.spec.max_episode_steps = max_episode_steps
        self._max_episode_steps = max_episode_steps
        self._elapsed_steps = None

    def step(self, action):
        """Steps through the environment and if the number of steps elapsed
        exceeds ``max_episode_steps`` then truncate."""
        observation, reward, terminated, truncated, info = self.env.step(action)
        self._elapsed_steps += 1
        if self._elapsed_steps >= self._max_episode_steps:
            truncated = True
        return observation, reward, terminated, truncated, info
```
】
- Section 1.6.3, Code 1-7, Codes, Line 2: Remove 【`, new_step_api=True`】.
- Section 1.6.3, Code 1-9, Codes, Line 2: Change 【`observation = env.reset(seed=seed)`】 to 【`observation, _ = env.reset(seed=seed)`】.
- Section 1.6.3, Code 1-11, Codes, Line 2: Remove 【`, new_step_api=True`】.
- Section 2.1.4, paragraph 5: change from 【 For episodic tasks, let $R_t=0$ for $t>T$. The discount factor of episodic tasks is usually $\gamma \in \left(0,1\right]$. We will use this unified notation throughout the book. 】 to 【 For episodic tasks, let $R_t=0$ for $t>T$. In fact, the discount factor of an episodic task can also be $<1$. Consequently, discount factor of an episodic task is usually $\gamma \in \left(0,1\right]$, while discount factor of a sequential task is usually $\gamma \in \left(0,1\right)$. We will use this unified notation throughout the book. 】(The first and last sentense remain unchanged. The middle sentense is extended. Previous statement is misleading.)
- Section 2.3.2: An item start with 【Use state-action distribution at time $t$ to back up the state-action distribution at time $t+1$:】, in the proof, first parentheses, change 【 $\mathsfit{s}' \in \mathcal{S}$ 】 to 【 $\mathsfit{s} \in \mathcal{S}$ 】. (remove the ' on $\mathsfit{s}$.)
- Section 2.3.4, Paragraph 2: Change 【 many statistics can be represented using the  notation of expected over distribution.】 to 【many statistics can be represented using the  notation of expected over discounted distribution.】 Add a word "discounted".
- Section 2.4.3, the first item group, the first item: Change 【Therefore, $\pi_\ast<\pi'$, which conflicts】to 【Therefore, $\pi_\ast\prec\pi'$, which conflicts】. （change the compare sign)
- Section 2.5.1, Code 2-3, Codes, Line 3: Remove 【`, new_step_api=True`】
- Section 3.1, the paragraph after "Interdisciplinary Reference 3-2", the formula after the line "Therefore". Please take care whether there are extra period ".". (There may be or may not be, I am not sure.)
- Section 3.5.1, Code 3-1, Codes, Line 5: Remove 【`, new_step_api=True`】
- Section 3.5.1, Code 3-2, Codes, Line 3: Change 【`observation = env.reset()`】 to 【`observation, _ = env.reset()`】.
- Section 4.1.2, the paragraph before Algo. 4-5: Change 【Step 2.5.3】 to 【Step 2.5.2】  (three times in this paragraph).
- Section 4.3.1, Code 4-2, Codes, Line 5: Change 【`observation = env.reset()`】 to 【`observation, _ = env.reset()`】.
- Section 4.3.2, Code 4-3, Codes, Line 7: Change 【`observation = env.reset()`】 to 【`observation, _ = env.reset()`】.
- Section 4.3.3, Code 4-6, Codes, Line 8: Change 【`observation = env.reset()`】 to 【`observation, _ = env.reset()`】.
- Section 4.3.4, Code 4-7, Codes, Line 8: Change 【`observation = env.reset()`】 to 【`observation, _ = env.reset()`】.
- Section 4.3.5, Code 4-8, Codes, Line 10: Change 【`observation = env.reset()`】 to 【`observation, _ = env.reset()`】.
- Section 5.5.1, Code 5-1, Codes, Line 2: Change 【`state = env.reset()`】 to 【`state, _ = env.reset()`】.
- Section 6.2.1, Interdisciplinary Reference 6-1, the third paragraph, change 【(Zhiqing, 2018)】 to 【(Xiao, 2018)】.
- Section 6.5.1, Code 6-1, Codes, Line 2: Remove 【`, new_step_api=True`】
- Section 6.5.1, Code 6-2, Codes, Line 2: Change 【`observation = env.reset()`】 to 【`observation, _ = env.reset()`】.
- Section 8.2.2, Algo. 8-3. Please help check the format consistency (especially the intent) between Step 3.1 and Step 3.2.
- Section 12.6.1, Fig. 12-1, caption: Change 【`https://www.gymlibrary.ml/pages/environments/atari/`】 to 【`https://www.gymlibrary.dev/environments/atari/complete_list/`】
- Section 12.6.3, Code 12-3, Codes, Line 3: Remove the line 【from gym.utils.step_api_compatibility import step_api_compatibility】
- Section 12.6.3, Code 12-3, Codes, Change 【
```
    def __init__(self, env: gym.Env, num_stack: int, lz4_compress: bool = False,
        new_step_api: bool = False):
        super().__init__(env, new_step_api)
```
】 to 【
```
    def __init__(self, env: gym.Env, num_stack: int, lz4_compress: bool = False):
        super().__init__(env)
```
】

- Section 12.6.3, Code 12-3, Codes, Change 【
```
    def step(self, action):
        observation, reward, terminated, truncated, info = \
                step_api_compatibility(self.env.step(action), True)
        self.frames.append(observation)
        return step_api_compatibility((self.observation(None), reward,
                terminated, truncated, info), self.new_step_api)
```
】 to 【
```
    def step(self, action):
        observation, reward, terminated, truncated, info = self.env.step(action)
        self.frames.append(observation)
        return self.observation(None), reward, terminated, truncated, info
```
】

- Section 12.6.3, Code 12-4, Codes, Line 1: Remove 【`, new_step_api=True`】.
- Section 13.3: In a line between two formula, change 【Due to the selection method of $\mathsfit{A}_t$ ,】 to 【Due to the selection method of ` $\mathsfit{A}_{\kappa,t}$ `,】 (add " $\kappa,$ " to the subscript . GitHub has some render issue here.)
- Section 13.4.1, Code 13.1, Codes, Line 8: Change 【`rand(n)`】 to 【`random(n)`】.
- Section 13.4.1, Code 13.1, Codes, Line 10: Remove 【`return_info=False, `】.
- Section 13.4.1, Code 13.1, Codes, Line 12: Change 【`return np.empty(0, dtype=float)`】 to 【`return np.empty(0, dtype=float), {}`】.
- Section 14.3.1, Code 14.5, Codes, Line 1: Change 【`return_info=False`】 to  【`return_info=True`】.
- Section 14.3.2, Code 14-7, Codes, Line 2: Change 【`observation, winner = env.reset(), 0`】 to 【`observation, _ = env.reset()`】.
- Section 14.3.3, Code 14-7, Codes, Line 3: Change 【`termination, truncation = False, False`】 to 【`winner, termination, truncation = 0, False, False`】.
- Section 15.2, the first paragraph, there is an inline equation may have additional "," at the right side.
- Section 15.4.1, Code 15-2, Codes, Line 4: Change 【`observation = env.reset()`】 to 【`observation, _ = env.reset()`】.
- Section 15.4.1, Paragraph 4, Code block 2, Line 1: Remove 【`, new_step_api=True`】
- Section 16.1.2, first paragraph, change 【its average reward $r_\pi$.】 to 【its average reward $\bar{r}_\pi$.】 .
- Section 16.1.2, first bullet item: change 【 $r_\pi$ 】 to 【 $\bar{r}_\pi$ 】(two occurances, the first one is in the end of the inline equation, the second one is at the end of this point.)
- Section 16.1.2, the paragraph starts with "The way to use differential values to calculate average reward is", change 【 $r_\pi$ 】  to 【 $\bar{r}_\pi$ 】 (4 occurances in total). The first equation group will become 【 ` ${{\bar r}_\pi } = \sum\limits_\mathsfit{a} {\pi \left( {\mathsfit{a}|\mathsfit{s}} \right)\sum\limits_{\mathsfit{s'}} {p\left( {\mathsfit{s'}|\mathsfit{s},\mathsfit{a}} \right)} \left[ {r\left( {\mathsfit{s},\mathsfit{a},\mathsfit{s'}} \right) - {{\tilde v}_\pi }\left( \mathsfit{s} \right) + {{\tilde v}_\pi }\left( {\mathsfit{s'}} \right)} \right]} , & \mathsfit{s} \in {\cal S}, {{\bar r}_\pi } = \sum\limits_{\mathsfit{s'},r} {p\left( {\mathsfit{s'},r|\mathsfit{s},\mathsfit{a}} \right)\sum\limits_{\mathsfit{a'}} {\pi \left( {\mathsfit{a'}|\mathsfit{s'}} \right)\left[ {r - {{\tilde q}_\pi }\left( {\mathsfit{s},\mathsfit{a}} \right) + {{\tilde q}_\pi }\left( {\mathsfit{s'},\mathsfit{a'}} \right)} \right]} } , & \mathsfit{s} \in {\cal S},\mathsfit{a} \in {\cal A}$` .】 The second equation group will change from 【`${\tilde v_\pi }\left( \mathsfit{s} \right) = \sum\limits_\mathsfit{a} {\pi \left( {\mathsfit{a}|\mathsfit{s}} \right)\sum\limits_{\mathsfit{s'}} {p\left( {\mathsfit{s'}|\mathsfit{s},\mathsfit{a}} \right)} \left[ {r\left( {\mathsfit{s},\mathsfit{a},\mathsfit{s'}} \right) - {r_\pi } + {{\tilde v}_\pi }\left( {\mathsfit{s'}} \right)} \right]} ,\quad \mathsfit{s} \in {\cal S}$`】to【`${\tilde v_\pi }\left( \mathsfit{s} \right) = \sum\limits_\mathsfit{a} {\pi \left( {\mathsfit{a}|\mathsfit{s}} \right)\sum\limits_{\mathsfit{s'}} {p\left( {\mathsfit{s'}|\mathsfit{s},\mathsfit{a}} \right)} \left[ {r\left( {\mathsfit{s},\mathsfit{a},\mathsfit{s'}} \right) - {\bar{r}_\pi } + {{\tilde v}_\pi }\left( {\mathsfit{s'}} \right)} \right]} ,\quad \mathsfit{s} \in {\cal S}$`】. The third equation group will change from 【`${\tilde q_\pi }\left( {\mathsfit{s},\mathsfit{a}} \right) = \sum\limits_{\mathsfit{s'},r} {p\left( {\mathsfit{s'},r|\mathsfit{s},\mathsfit{a}} \right)\sum\limits_{\mathsfit{a'}} {\pi \left( {\mathsfit{a'}|\mathsfit{s'}} \right)\left( {r - {r_\pi } + {{\tilde q}_\pi }\left( {\mathsfit{s'},\mathsfit{a'}} \right)} \right)} } ,\quad \mathsfit{s} \in {\cal S},\mathsfit{a} \in {\cal A}$`】 to【`${\tilde q_\pi }\left( {\mathsfit{s},\mathsfit{a}} \right) = \sum\limits_{\mathsfit{s'},r} {p\left( {\mathsfit{s'},r|\mathsfit{s},\mathsfit{a}} \right)\sum\limits_{\mathsfit{a'}} {\pi \left( {\mathsfit{a'}|\mathsfit{s'}} \right)\left( {r - {\bar{r}_\pi } + {{\tilde q}_\pi }\left( {\mathsfit{s'},\mathsfit{a'}} \right)} \right)} } ,\quad \mathsfit{s} \in {\cal S},\mathsfit{a} \in {\cal A}$`】.
- Section 16.6.2, the paragraph before Code 16-2: change 【Another is `TigerEnv1000-v0`, which mimics the sequential case by setting the maximum steps of the episode to a very large number 1000.】to 【Another is `TigerEnv200-v0`, which mimics the sequential case by setting the maximum steps of the episode to a very large number 200.】 (Change two 1000 to 200.)
- Section 16.6, Code 16.1, Codes, Line 15: Remove 【`return_info=False, `】.
- Section 16.6, Code 16.1, Codes, Line 18: Change 【`return Observation.START`】 to 【`return Observation.START, {}`】.
- Section 16.7, bullet points #4, change 【 $r_\pi$ 】 to 【 $\bar{r}_\pi$ 】.

----

The repo is for editors only. Readers should go to https://zhiqingxiao.github.io/rl-book/en2022
