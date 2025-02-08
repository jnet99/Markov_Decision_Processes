# Markov_Decision_Processes

## Objective
This project implements the **Value Iteration Algorithm** to solve Markov Decision Processes (MDPs) for grid-based environments. The algorithm computes the optimal utility values and policies for each state in the environment.

## Code Structure

### `value_iteration_main.py`:
- Sets the environment file, non-terminal reward (`ntr`), discount factor (`gamma`), and number of iterations (`K`).
- Calls the `value_iteration` function with the specified inputs.

### `value_iteration.py`:
- **Environment Loading**: Reads the environment file and identifies terminal states, non-terminal states, and blocked states.
- **Utility Initialization**: Initializes utility values for all states to 0 (except blocked states, which are set to `None`).
- **Value Iteration**:
  - Iterates `K` times to update utility values using the Bellman equation.
  - Considers transition probabilities (`p_intended` and `p_adjacent`) for intended and adjacent actions.
- **Policy Extraction**: Computes the optimal policy for each state based on the final utility values.
- **Output**:
  - Prints the utility values for all states in a grid format.
  - Prints the optimal policy for all states in a grid format.
 
  ## Key Features
- Supports grid-based environments with terminal, non-terminal, and blocked states.
- Configurable parameters:
  - `non_terminal_reward`: Reward for non-terminal states.
  - `gamma`: Discount factor for future rewards.
  - `K`: Number of iterations for value iteration.
- Uses transition probabilities for intended and adjacent actions.
- Handles blocked states and terminal states appropriately.

## Testing and Results
- Tested on `environment1.txt` and `environment2.txt` with the following configurations:
  1. **`environment2.txt`, `ntr=-0.04`, `gamma=1`, `K=20`**:
     - Output: Utility values and optimal policy.
  2. **`environment2.txt`, `ntr=-0.04`, `gamma=0.9`, `K=20`**:
     - Output: Utility values and optimal policy.
- Results were consistent with expected performance ranges.

## Example Output
![value_iteration_2_ 98](https://github.com/user-attachments/assets/0b802325-d374-4835-b51d-ff32ace7ba99)

