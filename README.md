# INFERNAL_BATTLE
UE single player combat game

Created a single-player arcade game using Unreal Engine and C++ towards the fulfillment of the small project requirements of the course IT-306 Artificial Intelligence & Expert Systems.

We used the A* Search Algorithm to for real-time shortest path selection between the computer-controlled opponent and the user-controlled character. This enables the agent to efficiently track and attack the player. 

The algorithm for A* implementation is as follows:
  1. Take input from the user and update the player’s position.
  2. Based on the updated position of the player, calculated the heuristic values of the nodes in the arena and the associated costs.
  3. Take the nearest node with lowest heuristic value and push it in the closed list from the open list. Then, remove it from open list.
  4. If the destination node is reached, break the loop.
  5. Try to update node position for the current edge to make paths more precise unless heuristic is not admissible (overestimates), in which case, we have to use constant values for given node to avoid creating cycles.
  6. If the node is already in the open list and the new result is worse, skip.
  7. If the node is already visited and processed, and the new result is worse, skip.
  8. Repeat the steps 3 to 7 till the open list becomes empty.

  In our project, we have used a slightly modified A* algorithm. It differs in the state being a right-angled triangle instead of a square, thereby resulting in a more optimized searching.
