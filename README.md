# Simple NeRF Experimentation

This is a basic exploratory tensorflow implementation of the paper "NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis". It comprises of two exploration parts. One part consists of only startified sampling (coarse grained sampling) and the other part consists of bother startified as well as hierarchical sampling (fine-grained sampling).

The dataset utilizied is: http://cseweb.ucsd.edu/~viscomp/projects/LF/papers/ECCV20/nerf/tiny_nerf_data.npz

## Startified Sampling

I used following code as reference: https://github.com/bmild/nerf/blob/master/tiny_nerf.ipynb

I only perform uniform random sampling for getting 3D points along rays. I compare the function approximation between coordinate space to RGB-density space, as MLP, CNN and Attention Architecture. In following 360 degree view rendering comparison, MLP's overfitting capability serves to make it suitable for the rendering task.


https://github.com/antidianuj/simple_nerf/assets/47445756/13034943-1d2b-4d75-881f-6a59e1803e35




## Startified and Hiearchical Sampling

I used following pytorch based code for reference: https://github.com/yenchenlin/nerf-pytorch/blob/master/run_nerf.py.

I perform first uniform sampling, and then hiearchical sampling to sample additional points around these uniform random points. I compare the function approximation between coordinate space to RGB-density space, as MLP, CNN and Attention Architecture. In following 360 degree view rendering comparison, the results are not great, and requires further work. But MLP seems to be best architecture for NeRF task.



https://github.com/antidianuj/simple_nerf/assets/47445756/132da8cc-aa5f-4223-83cb-ccab5474525a

