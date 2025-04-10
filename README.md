# Controllable_Koopman

A continuous-time Koopman-based system identification and control framework  
with controllability-aware learning and structure.

## Features

- Continuous-time dynamics (ODE)
- Neural Koopman operator with Neural encoder
- No decoder: original state is embedded in latent
- LQR / MPC rollout on true systems
- Controllability-aware structure and loss, Gramian analysis

## Project Structure
<pre><code>
Controllable_Koopman/
├── configs/              # YAML experiment configs
├── dynamics/             # Continuous-time true system dynamics
├── models/               # Encoder + Koopman operator
├── controllers/          # LQR, MPC, rollout logic
├── utils/                # simulate, dataset generation, visualization
├── training/             # Training & evaluation
├── experiments/          # Entry scripts for train/test/control
└── main.py               # Optional main CLI
</code></pre>

## Example Commands

```bash
python experiments/run_train.py --config configs/pendulum.yaml
python experiments/run_control.py --config configs/pendulum.yaml --controller lqr