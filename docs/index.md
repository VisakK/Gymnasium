---
hide-toc: true
firstpage:
lastpage:
---

<center>
    <div class="logo">
        <img src="_static/img/gymnasium-text.png" width="65%" alt="Gymnasium Logo">
    </div>
</center>

<div class="header-text">
    <h2>An API standard for reinforcement learning with a diverse collection of reference environments</h2>
</div>

```{figure} _static/videos/box2d/lunar_lander.gif
   :alt: Lunar Lander
   :width: 500
```

**Gymnasium is a maintained fork of OpenAI’s Gym library.** The Gymnasium interface is simple, pythonic, and capable of representing general RL problems, and has a [compatibility wrapper](content/gym_compatibility) for old Gym environments:

```{code-block} python

import gymnasium as gym
env = gym.make("LunarLander-v2", render_mode="human")
observation, info = env.reset(seed=42)
for _ in range(1000):
   action = env.action_space.sample()  # this is where you would insert your policy
   observation, reward, terminated, truncated, info = env.step(action)

   if terminated or truncated:
      observation, info = env.reset()

env.close()
```

<style>
h2 {
    padding-top: 0;
    padding-bottom: 20px;
    font-size: 28px;
    margin: 0;
    overflow: auto;
}
img{
    vertical-align:bottom;
    padding-bottom: 0;
    padding-top: 0
 }
.logo{
    padding-left: 8%;
    padding-top: 10px
}
@media (min-width: 455px) {
    .header-text{
        text-align: center;
    }
}
@media (max-width: 455px) {
    .header-text{
        text-align: left;
    }
}
</style>

```{toctree}
:hidden:
:caption: Introduction

content/basic_usage
content/gym_compatibility
content/migration-guide
```

```{toctree}
:hidden:
:caption: API

api/env
api/registry
api/spaces
api/wrappers
api/vector
api/utils
api/experimental
```

```{toctree}
:hidden:
:caption: Environments

environments/classic_control
environments/box2d
environments/toy_text
environments/mujoco
environments/atari
environments/third_party_environments
```

```{toctree}
:hidden:
:glob:
:caption: Tutorials

tutorials/**/index
Comet Tutorial <https://www.comet.com/docs/v2/integrations/ml-frameworks/gymnasium/?utm_source=gymnasium&utm_medium=partner&utm_campaign=partner_gymnasium_2023&utm_content=docs_gymnasium>
```

```{toctree}
:hidden:
:caption: Development

Github <https://github.com/Farama-Foundation/Gymnasium>
gymnasium_release_notes/index
gym_release_notes/index
Contribute to the Docs <https://github.com/Farama-Foundation/Gymnasium/blob/main/docs/README.md>
```
