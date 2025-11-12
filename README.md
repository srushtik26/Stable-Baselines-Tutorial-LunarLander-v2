# 🧠 Stable Baselines Tutorial — LunarLander-v2 🚀

## 📘 Overview
This tutorial demonstrates how to train, evaluate, and deploy a reinforcement learning agent using **Stable Baselines** — a popular framework built on top of **TensorFlow 1.x** for training RL models.  
The environment used is **LunarLander-v2** from **OpenAI Gym**, where the goal is to safely land a spacecraft on the landing pad using thrusters.

## 🧩 Algorithms & Techniques
- **ACER (Actor-Critic with Experience Replay)** — a policy gradient algorithm that combines off-policy learning with a replay buffer for stable training.
- **OpenAI Gym** environment simulation.
- **Model evaluation** using Stable Baselines’ built-in `evaluate_policy`.

## ⚙️ Requirements
Install dependencies with:
```bash
pip install tensorflow==1.15.0 tensorflow-gpu==1.15.0 stable_baselines gym box2d-py --user
```

**Dependencies**
- `tensorflow==1.15.0`
- `stable_baselines`
- `gym`
- `box2d-py`

## 🧱 Project Structure
```
Stable Baselines Tutorial.ipynb
```

Contains:
1. **Installation and Imports**
2. **Random Policy Testing**
3. **Model Building & Training (ACER)**
4. **Evaluation**
5. **Model Saving and Reloading**

## 🚀 How to Run
1. Clone or download this repository.
2. Open the Jupyter Notebook:
   ```bash
   jupyter notebook "Stable Baselines Tutorial.ipynb"
   ```
3. Run all cells sequentially to:
   - Initialize the environment.
   - Train the ACER model for 100,000 timesteps.
   - Evaluate the trained policy.
   - Visualize the agent landing in the environment.

## 📊 Results
- The trained agent learns to control the lander and achieves increasing reward scores across episodes.
- Saved model: `ACER_model.zip`
- You can reload and test the model anytime:
  ```python
  model = ACER.load("ACER_model", env=env)
  ```

## 💡 Key Learnings
- How to implement reinforcement learning with Stable Baselines.
- Using **DummyVecEnv** for vectorized environments.
- Saving, loading, and evaluating trained agents.

## 📚 References
- [Stable Baselines Documentation](https://stable-baselines.readthedocs.io/)
- [OpenAI Gym Environments](https://www.gymlibrary.dev/)
- [ACER Paper (DeepMind, 2017)](https://arxiv.org/abs/1611.01224)
