These are the commands to be run to produce the results

### Behaviour Cloning

***1/2 Cheeter-v2***
```
python cs285/scripts/run_hw1_behavior_cloning.py --expert_policy_file cs285/policies/experts/HalfCheetah.pkl --env_name HalfCheetah-v2 --exp_name test_bc_ant --n_iter 1 --expert_data cs285/expert_data/expert_data_HalfCheetah-v2.pkl --video_log_freq -1
```

***Humanoid-v2***
```
python cs285/scripts/run_hw1_behavior_cloning.py --expert_policy_file cs285/policies/experts/Humanoid.pkl --env_name Humanoid-v2 --exp_name test_bc_ant --n_iter 1 --expert_data cs285/expert_data/expert_data_Humanoid-v2.pkl --video_log_freq -1
```

> The above two were used in section 1.2, comparing performance of the behavioral cloning agent achieves to achieve at least 30% of the performance of the expert
```bash
python cs285/scripts/run_hw1_behavior_cloning.py --expert_policy_file cs285/policies/experts/Ant.pkl --env_name Ant-v2 --exp_name test_bc_ant --n_iter 1 --expert_data cs285/expert_data/expert_data_Ant-v2.pkl
```


```
python cs285/scripts/run_hw1_behavior_cloning.py --expert_policy_file cs285/policies/experts/Walker2d.pkl --env_name Walker2d-v2 --exp_name test_bc_ant --n_iter 1 --expert_data cs285/expert_data/expert_data_Walker2d-v2.pkl
```

```
python cs285/scripts/run_hw1_behavior_cloning.py --expert_policy_file cs285/policies/experts/Hopper.pkl --env_name Hopper-v2 --exp_name test_bc_ant --n_iter 1 --expert_data cs285/expert_data/expert_data_Hopper-v2.pkl
```



expert data
----------
Hopper-v2
HalfCheetah-v2
Humanoid-v2
Walker2d-v2
Ant-v2


RUNS
====
With default params
Humanoid-v2 -> 2.1 % of expert policy
Walker-2d -> 7.5 % of expert policy
HalfCheeter-v2 -> 55.96 % of expert policy


***Initial data collection***
> - Increasing layers increases av return, relative to the size of the input of each policy. Larger inputs work better with large sizes, (e.g Humanoid - input: 376, layers: 200, n_size: 132) (HCheeter - input: 17, layers: 20, n_size: 64) Increasing network size for small inputs increases performance upto a certain size limit




Dagger
-----

**Humanoid**
```
python cs285/scripts/run_hw1_behavior_cloning.py --expert_policy_file cs285/policies/experts/Humanoid.pkl --env_name Humanoid-v2 --exp_name test_bc_ant --n_iter 1 --expert_data cs285/expert_data/expert_data_Humanoid-v2.pkl --do_dagger --n_iter=50 --batch_size 10000  --n_layers 20 --size 132 --eval_batch_size 2000  --train_batch_size 1000 --video_log_freq -1
```

**1/2 Cheeter-v2**

```
python cs285/scripts/run_hw1_behavior_cloning.py --expert_policy_file cs285/policies/experts/HalfCheetah.pkl --env_name HalfCheetah-v2 --exp_name test_bc_ant --n_iter 1 --expert_data cs285/expert_data/expert_data_HalfCheetah-v2.pkl --do_dagger --n_iter=10  --video_log_freq -1
```
