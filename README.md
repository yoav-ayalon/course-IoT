# course-IoT

This project implements distributed algorithms for multi-agent coordination in a simulated environment. The algorithms included are:

- **DSA (Distributed Stochastic Algorithm)**: Implemented with different change probabilities (LOW, MEDIUM, HIGH).
- **MGM (Maximum Gain Messaging)**: Standard MGM and MGM-2 (matching with k partners).

## Project Structure

- `main.py`: Entry point. Runs experiments and plots results.
- `config.py`: Configuration parameters for the environment and algorithms.
- `enviroment_class.py`: Simulation environment setup.
- `graph_class.py`: Graph and agent network creation.
- `agent_class.py`: Agent logic and messaging.
- `post_office.py`: Message delivery system.
- `algorithms/`: Contains algorithm implementations:
  - `base_algorithm.py`: Abstract base class.
  - `dsa_c_algorithm.py`: DSA implementation.
  - `mgm_algorithm.py`: MGM and MGM-2 implementation.

## How to Use

1. **Install requirements** (if needed, e.g. `matplotlib`, `networkx`):
   ```sh
   pip install matplotlib networkx

2. **Run the main script**
    python main.py

    This will execute all algorithms on different graph settings, average the results over multiple runs, and plot the cost per iteration for each algorithm.

## Algorithms
- **DSA_C:** Agents change their assignments based on a probability and local cost improvement.
- **MGM-K:** Agents propose changes to up to k neighbors, negotiate, and commit if mutual gain is achieved.
    
## Output
    Plots showing the performance (cost over iterations) of each algorithm under different graph densities and domains.