### Lecture2-6_Learning_Latent_Plans_from_Play.pdf

This paper uses auto-encoder for imitation learning

encoder: 
input: current state, concact[current state,goal state]
latent space:
encoding the above two into same latent space mean, variance, and minimize their kl-divergence
decoder: 
input the relevant latent vector, current state, goal state, and output the next timestep action

<img width="482" alt="Screenshot 2023-04-18 at 17 39 29" src="https://user-images.githubusercontent.com/91216581/232737605-20e2157d-25a9-469d-9697-3ea293867156.png">

### Lecture2-6_Learning_to_Reach_Goals_via_Iterated_Supervised_Learning.pdf

This paper smartly utilize the unwanting trajectories, which did not manage to reach the goal, by relabeling it to another goal. Taking state, goal state, as policy network input, it solves the problem of low efficiency of simulations.

<img width="733" alt="Screenshot 2023-04-18 at 17 58 00" src="https://user-images.githubusercontent.com/91216581/232742486-8843eb0e-f5f9-4bdd-913a-25294b47942d.png">

