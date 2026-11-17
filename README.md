# PostTrain_RSI
RL(with RL_RSI) -> self distillation -> SFT -> RL

## self distillation
- Create several roles: data-miner\Judge\Rewritter\Manager, with the current checkpoint.
- Create a share database: store knowledge from now on. Every roles can access the share database.
- Data-miner: search for prompt and generate trajectory
- Judge: Judge whether the generated trajectory is correct or wrong.
- Rewritter: Rewrite the correct trajectory into a trajectory based on specific preferences, such as a more efficient thought chain.
- Manager: Store the rewrited trajectory into a database(called share knowledge) and use them for SFT.
