# UEFA-2025-Euro-Spain-Women-s-Team-Pass-Network

The goal of this project is to visualize and analyze team passing structure using network theory — highlighting which players serve as central hubs and how the ball moves through different parts of the pitch.

This project explores how teams build and distribute possession by analyzing passing networks using soccer event data. By constructing directed graphs of completed passes for each match, we calculate centrality metrics such as degree centrality and betweenness centrality to measure how influential each player is within their team’s passing structure.

To go beyond network theory, we integrate advanced metrics like:
 - xG Chain: Credits a player for any involvement in a possession that leads to a shot.
 - xG Buildup: Measures a player’s contribution to build-up play, excluding shots and key passes.

Visualizations include annotated pass network maps and side-by-side comparisons with xG metrics to assess the relationship between player centrality and attacking output. This work can support tactical analysis, scouting, and team performance evaluation by identifying hidden playmakers and strategic tendencies.



📈 **Key Visuals**

I decided to focus on the losing team Spain, hoping to find some clues from their passing network to see any trends that perhaps to identify any mistakes along with analyzing if these passing networks lend to any substantial opportunities for shots at goal. The size of the nodes are proportional to the degree centrality. The larger the degree centrality, the larger the node associated with the player. Some players do not have nodes around them which indicate a degree centrality of 0. This commonly occurs for players who were substituted late into the game before it ended and did not compelete any passes to the other players.

<img src="docs/Spain Women's Pass Network vs England (Euro 2025 Finals).png" alt="Spain Women's Pass Network vs England (Euro 2025 Finals)" width="600"/>

Spain shot the ball 23 times. The quality of the shots are judged by the xG metric provided by statsbomb. I chose to focus on passes within those possessions that led to high quality shots. I defined high quality as any shots that had an expected goal of over 0.2 and only 2 possessions led to shots that fit that category. Down below you can see the passes for both of these possessions.

<img src="docs/Possession 51.png" alt="Possession 51" width="600"/>
<img src="docs/Possession 198.png" alt="Possession 198" width="600"/>

Down below is a cumulative xG graph for the entire game, comparing Spain and England's chances. Despite Spain having better chances for much of the game, they could not capitalize on their opportunities and they let the game be decided by penalties.

<img src="docs/Cumulative xG.png" alt="Cumulative xG" width="600"/>

Below is a bar graph comparing Spain and England's xGChain and xGBuildup as a team. Based on the previous line plot, it is no surprise that Spain had higher xGChain and xGBuildup across the match.

<img src="docs/Spain vs England (xgChain and xGBuildup).png" alt="Spain vs England (xgChain and xGBuildup)" width="600"/>

I wanted to investigate the relationship between degree centrality and xGChain. Does being a key hub mean that a player is consistently involved in generating possessions that lead to high quality shots. Ideally, this should be the case. It is possible the player can be a central hub and serve as a respite and calming influence for the rest of the team while they are in a frenzy and just simiply pass the ball laterally or backwards. However, players who serve as hubs should also be making a concerted effort to attack and push the ball forward into the opposing team's side of the pitch. 

The scatterplots below show Spain's relationship between degree centrality and xGChain with their finals match against England along with the teams in the rest of the tournament

[Degree Centrality vs xGChain (Spain vs England)](https://linkforce1.github.io/UEFA-2025-Euro-Spain-Women-s-Team-Pass-Network/Degree%20Centrality%20vs%20xGChain%20(Spain%20vs%20England).html)
<img src="docs/Degree Centrality vs xGChain (Spain vs England).png" alt="Degree Centrality vs xGChain (Spain vs England)" width="700" height="700"/>

[Degree Centrality vs xGChain - Spain (Euros 2025)](https://linkforce1.github.io/UEFA-2025-Euro-Spain-Women-s-Team-Pass-Network/Degree%20Centrality%20vs%20xGChain%20-%20Spain%20(Euros%202025).html)
<img src="docs/Degree Centrality vs xGChain - All Matches.png" alt="Degree Centrality vs xGChain - All Matches" width="800" height = "800"/>

