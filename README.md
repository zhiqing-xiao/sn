The repo is for editors only. Readers should go to https://zhiqingxiao.github.io/rl-book/en2022

# Errata

(It is being updated.)

- Section 2.5.1, Second Paragraph:  "checked" -> "checks"

=====

- Abbreviation: "Deep Q Newtork" -> "Deep Q Network"

- Code 2-4 ~ Code 2-6, URL: The same as the URL of Code 2-3.

I am also considering that we may remove all URLs, since the URLs are also maintained in GitHub repo. But let us deal with this in a consistent way.

- Code 3-6, URL: the same as the URL of Code 3-5
- Code 5-6, Code: Please take care of the line change here:

Change
```
        self.qs = [np.zeros((env.observation_space.n, env.action_space.n)) for _
in range(2)]
```
to
```
        self.qs = [np.zeros((env.observation_space.n, env.action_space.n))
                for _ in range(2)]
```

- Section 6.4.1, after Algo. 6-8, the item of "Proportional priority", change subscript $t$ to $i$ (7 in total). Change $\delta_t=U_t-q(\mathsfit{S}_t,\mathsfit{A}_t;\mathbf{w})$ to $\delta_i=U_i-q(\mathsfit{S}_i,\mathsfit{A}_i;\mathbf{w})$.
Change $\delta_t=U_t-v(\mathsfit{S}_t;\mathbf{w})$ to $\delta_i=U_i-v(\mathsfit{S}_i;\mathbf{w})$.

- Algo. 10-1, Caption: "Soft Q Learning" -> "SQL"
- Code 11-2, URL: Remove duplicated backslash.
- Section 12.6.2, Heading: "The game Pong" -> "The Game Pong"
- Code 13-4, URL: the same as URL of Code 13-3.
- Code 15-3, URL: the same as URL of Code 15-4.
- Code 16-1 ~ Code 16-3, URL: `Tiger-v0_CloseForm.py` -> `Tiger-v0_CloseForm.ipynb`
- Code 16-4 ~ Code 16-5, URL: `Tiger-v0_Planning.py` -> `Tiger-v0_Planning_demo.ipynb`
