# LeRobot - Folding Short Pants

**Team:** Steve Saito, Vinai Rachakonda, Maxime Zand, Alejandro Ojeda

**Project Overview:**

Our LeRobot Hackathon project focused on enabling a robot to autonomously fold short pants in half. We approached this challenge in several key steps:

1.  **Leveraging LeRobot Configuration:** We began by utilizing existing LeRobot file structures to streamline the initial configuration of the robot's identification parameters.
2.  **Initial Training with Phosphobot:** We then employed Phosphobot to establish our initial training pipelines and collected three distinct datasets specifically for the task of folding short pants.
3.  **Accelerating Training via Runpod and gr00t:** To overcome potential training bottlenecks with Phosphobot, we concurrently implemented a Runpod GPU instance, leveraging the gr00t framework for significantly faster model training.
4.  **Deploying a Robust Inference Solution on Runpod:** When we encountered instability during inference with Phosphobot, we transitioned to a dedicated Runpod GPU server. This setup allowed us to reliably perform inference using real-time data from both robot cameras and the robot's internal sensors.

**Key Technologies & Resources:**

* **LeRobot:** [https://huggingface.co/lerobot](https://huggingface.co/lerobot)
* **Phosphobot:** [https://pypi.org/project/phosphobot/](https://pypi.org/project/phosphobot/) or [https://robots.phospho.ai/](https://robots.phospho.ai/)
* **Runpod:** [https://www.runpod.io/](https://www.runpod.io/)
* **Datasets:**
    * [https://huggingface.co/datasets/ssaito/example_dataset](https://huggingface.co/datasets/ssaito/example_dataset)
    * [https://huggingface.co/datasets/ssaito/actual25](https://huggingface.co/datasets/ssaito/actual25)
    * [https://huggingface.co/datasets/ssaito/hackathon](https://huggingface.co/datasets/ssaito/hackathon)
* **Test Models:**
    * [https://huggingface.co/phospho-app/actual25-lpho177tyl/tree/main](https://huggingface.co/phospho-app/actual25-lpho177tyl/tree/main)
    * [https://huggingface.co/ssaito/testmodel](https://huggingface.co/ssaito/testmodel)
    * [https://huggingface.co/maxzand/gr00tfoldingrobot](https://huggingface.co/maxzand/gr00tfoldingrobot)
    * [https://huggingface.co/maxzand/gr00t-folding-clothes](https://huggingface.co/maxzand/gr00t-folding-clothes)

**Additional Comments:**

* The initial robot configuration was significantly expedited by the utilization of pre-existing LeRobot file structures.
* The parallel training on a Runpod GPU, powered by the gr00t framework, provided a substantial acceleration in model training compared to the initial Phosphobot-only approach.
* The deployment of a dedicated Runpod GPU server proved critical for achieving stable and reliable inference, effectively handling input from multiple cameras and the robot's sensor data when Phosphobot inference encountered issues.
