The comand lines to run the docker(on local terminal)
1. xhost +
2. git clone https://github.com/rllab-MARL/pbl_orbit_docker.git
3. cd docker_0 
4. ./build.sh
5. ./run.sh

   
After entering the container(a terminal for docker container)
1.  ./orbit.sh -i
2.  ./orbit.sh -e
3. orbit -p -m pip install wandb

After this, please stop the docker, and git stash the skrl and rl_games directory.(above controlled local terminal)
1. docker stop orbit-2022.2.0_pbl
2. cd <this repo dir>
2. cd src/skrl
3. git stash
4. cd ../rlgames
5. git stash

After git stash, start the docker again


7. docker start orbit-2022.2.0_pbl
8. docker exec -it orbit-2022.2.0_pbl bash



The command lines for all the four testings are:(a terminal for docker container)

1. orbit -p source/standalone/workflows/skrl_discrete/train.py --task Isaac-MA-Transportskrl-v0 --num_envs 64

2. orbit -p source/standalone/workflows/skrl_discrete/train.py --task Isaac-MA-Transportskrl-v0 --num_envs 64 --headless



