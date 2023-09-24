The comand lines to run the docker
1. xhost +
2. git clone -b yano https://github.com/rllab-MARL/pbl_orbit_docker.git
3. cd docker_0 
4. ./build.sh
5. ./run.sh
After entering the container, in the current directory
6. ./orbit.sh -i
7. ./orbit.sh -e
8. orbit -p -m pip install wandb
After this, please stop the docker, and git stash the skrl and rl_games directory.
---------- docker stop orbit-2022.2.0_pbl(on another terminal)
10. cd ../src
11. cd skrl
12. git stash
13. cd ../rlgames
14. git stash
After git stash, start the docker again
15. docker start orbit-2022.2.0_pbl
16. docker exec -it orbit-2022.2.0_pbl bash

The command lines for all the four testings are:
17. orbit -p source/standalone/workflows/skrl_discrete/train.py --task Isaac-MA-Transportskrl-v0 --num_envs 64
18. orbit -p source/standalone/workflows/skrl_discrete/train.py --task Isaac-MA-Transportskrl-v0 --num_envs 64 --headless



