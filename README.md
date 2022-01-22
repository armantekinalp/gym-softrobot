<div align="center">

<h1> Soft-Robot Control Environment (gym-softrobot) </h1>
  <a href="https://github.com/skim0119/gym-softrobot/blob/main/LICENSE"><img src="https://img.shields.io/apm/l/atomic-design-ui.svg?style=flat"></a>
  <a href="https://github.com/skim0119/gym-softrobot"><img src="https://img.shields.io/github/release/skim0119/gym-softrobot.svg?style=flat"></a>
  <img src="https://github.com/skim0119/gym-softrobot/actions/workflows/main.yml/badge.svg?style=flat">
</div>

The environment is designed to leverage reinforcement learning methods into soft-robotics control.
Our inspiration is from slender-body living creatures, such as octopus or snake.
The code is based on [PyElastica](https://github.com/GazzolaLab/PyElastica), an open-source physics simulation for slender structure.
We intend this package to be easy-to-install and fully compatible to [OpenAI Gym](https://github.com/openai/gym).

> The package is under development, in Pre-Alpha phase. We are planning to complete the initial set of environment by the end of January 2022.

Requirements:
- Python 3.8+
- OpenAI Gym 0.21.0
- PyElastica 0.2+
- Matplotlib (optional for display rendering and plotting)	
- POVray (optional for 3D rendering)

Please use this bibtex to cite in your publications:

```
@misc{gym_softrobot,
  author = {Chia-Hsien Shih, Seung Hyun Kim, Mattia Gazzola},
  title = {Soft Robotics Environment for OpenAI Gym},
  year = {2022},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/skim0119/gym-softrobot}},
}
```

## Installation

```bash
pip install gym-softrobot
```

To test the installation, we provide few debugging script.
The environment can be tested using the following command.

```bash
python -m gym_softrobot.debug.make     # Make environment and run 10 steps
python -m gym_softrobot.debug.registry # Print gym-softrobot environment
```

We use [POVray](https://wiki.povray.org/content/HowTo:Install_POV) python wrapper [Vapory](https://github.com/Zulko/vapory) to visualize the motion in 3D.
POVray is not a requirement to run the environment, but it is necessary to use `env.render()` function as typical gym environment.

If you would like to test `POVray` with `gym-softrobot`, use
```bash
python -m gym_softrobot.debug.render  # Render 10 frames using vapory
```

## Reinforcement Learning Example

We tested the environment using [Stable Baselines3](https://github.com/DLR-RM/stable-baselines3) for centralized control.
More advanced algorithms are still under development.

If you have your own algorithm that you would like to test out, you are welcome to reach out to us.

## Environment Design

## Included Environments

### Octopus[Multi-arm control]

- `OctoFlat-v0` [Pre-Alpha]
- `OctoArmSingle-v0` [Pre-Alpha]
- `OctoReach-v0` [Working in Process]
- `OctoSwim-v0` [Working in Process]
- `OctoHunt-v0` [Working in Process]

### Snake

- `ContinuumSnake-v0` [Pre-Alpha]

### Simple Control

## Contribution

We are currently developing the package internally.

## Author

![GitHub Contributors Image][badge-Contributors-image]

<!-- -->
[badge-CI]: https://github.com/skim0119/gym-softrobot/actions/workflows/main.yml/badge.svg
[badge-Contributors-image]: https://contrib.rocks/image?repo=skim0119/gym-softrobot
