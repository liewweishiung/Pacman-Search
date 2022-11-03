  <img src="./assets/Ghost.PNG" border="10">
 <p align="center">
   <h1 align="center">Pacman Search</h1>
</p>
<p align="center">
  <img src="https://imgur.com/P22qeZM.gif" border="10">
</p>

---
Requires Python 2.x
---
Offline:
1. Install Anaconda: https://www.anaconda.com/products/distribution
2. Clone this repository: git clone https://github.com/liewweishiung/Pacman-Search
3. Create a new environment: conda create -n py2 python=2.7 anaconda -y
4. Activate new environment: conda activate py2
5. Navigate to the folder where you cloned the repository: cd <insert folder location here>
6. Run the codes below.
---
An array of AI techniques is employed to playing Pac-Man <img src="./assets/PacmanAgent.PNG" width="25" height="21" border="10">. Following `Informed, Uninformed and Adversarial Search` algorithms are implemented in this project.
- **Informed Search**: 
  - Breadth First Search
  - Depth First Search
  - Uniform Cost Search
- **Uninformed Search**: 
  - A* Search
- **Adversarial Search**: 
  - Minimax Search
  - Alpha-Beta Pruning

## 1. Depth First Search
>  Expand deepest node.
```python
cd Informed and Uninformed Search
python pacman.py -l mediumMaze -p SearchAgent -z .8 --frameTime 0.05
```
<p align="center">
  <img src="./assets/PacmanDFS.gif" width="550" height="323" border="10">
</p>

## 2. Breadth First Search
> Expand shallowest node.
``` python
cd Informed and Uninformed Search
python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs -z .8 --frameTime 0.05
```
<p align="center">
  <img src="./assets/PacmanBFS.gif" width="550" height="323" border="10">
</p>

## 3. Uniform Cost Search
> Expand least cost node.
```python
cd Informed and Uninformed Search
python pacman.py -l mediumMaze -p SearchAgent -a fn=ucs -z .8 --frameTime 0.05
```
<p align="center">
  <img src="./assets/PacmanUCS.gif" width="550" height="323" border="10">
</p>

## 4. A* Search
> Minimize the total estimated solution cost.
```python
cd Informed and Uninformed Search
python pacman.py -l mediumMaze -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic -z .8 --frameTime 0.05
```
<p align="center">
  <img src="./assets/PacmanAStar.gif" width="550" height="323" border="10">
</p>

## 5. Adversarial Search (Minimax)
> Max maximizes results, Min minimizes results. Compute each node’s minimax value’s the best achievable utility against an optimal adversary.
``` python
cd Adversarial Search
python pacman.py -p MinimaxAgent -l smallClassic -a depth=2 --frameTime 0
```
<p align="center">
  <img src="./assets/PacmanMiniMax.gif" width="550" height="323" border="10">
</p>

```python
If you lose, try increasing depth because depth matters.
```

## 6. Alpha-Beta Pruning
> Minimax: generates the entire game search space. Alpha-Beta algorithm: prune large chunks of the trees.
``` python
cd Adversarial Search
python pacman.py -p AlphaBetaAgent -l smallClassic -a depth=3 --frameTime 0
```
<p align="center">
  <img src="./assets/PacmanAplhaBeta.gif" width="550" height="323" border="10">
</p>

```python
If you lose, try increasing depth because depth matters.
```

## References
[UC Berkeley's introductory artificial intelligence course, CS 188.](http://ai.berkeley.edu/home.html)
