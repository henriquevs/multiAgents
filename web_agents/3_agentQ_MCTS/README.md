# AgentQ and MCTS: Overview

## Limitations to Existing Frameworks

1. **Reliability and Trust**
2. **Decision Making Errors**
3. **Plan Divergence and Looping**

## Steps for the Agent

1. **Plan**
2. **Reasoning** (a significant portion of issues come from this step)  
   - AgentQ addresses this issue
3. **Environmental Action**
4. **Explanation**

## AgentQ Components

1. **Monte Carlo Tree Search (MCTS)**
2. **Self-critique Mechanism and Process Supervision**
3. **Direct Preference Optimization (DPO)**  
   - Reinforcement learning algorithm that improves based on the current experience

## MCTS ( explores possibilities )

1. **Search Methodology** for backtracking and exploring
2. **Exploitation**: Try to find the best path to explore
3. **Future Reward Explanation**: When reaching the leaf node, it gives an estimate of what we can expect
4. **Back Propagation**: After the future reward estimate, MCTS reviews all the nodes (bottom-up approach)  
   - This tells the algorithm "hey, this path led to these results, so update your knowledge accordingly"
   - These steps repeat many times

## Self-critique ( evaluate options )

- Uses an LLM critique to give feedback and improve reasoning

## DPO ( learn )

- Reinforcement Learning with Human Feedback (RLHF)
- Refines preference and learns from both successful and failed trajectories
