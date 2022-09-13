# BasicNetLogoSimModels

> There are three models, **Shelling Model**, **Opinion Dynamic model**, and **Complex Network model**, realized by Netlogo

## **Shelling model**

> Diea: reporduce Shelling model

### Dynamic algorithm
- Agents are assigned with initial color
- Move if #neighbors of different color > bearable threshold (#neighbors * proportion-wanted) and there exists patches where different neighbors < bearable threshold

## **Opinion Dynamic model**

> Idea: reproduce work [The dissemination of culture: A model with local convergence and global polarization](https://www.jstor.org/stable/pdf/174371.pdf). Each agenst has multi-dimentional cultures, #demention := slider numFeatures; for each dimention, the scale of its value is int \in [1: numTraits].

### Dynamic algorithm
- Agents are separated by borders, the deeper the color of the border is, the larger the distance between the two agents

- Agent update one dimension of its opinion by coping the value of the value of a neighbor's opinion on that dimension. Neighbor is selected based on the similarity, higher similarity indicate a higher chance to interact.

- If two neighbors has the same culture, they will build a link. By this mechanism, an opinion network among the agents will be constructed. Finally, report # cultures

## **Complex Network model**

> Idea: reproduce work [Small worlds and cultural polarization](https://www.tandfonline.com/doi/pdf/10.1080/0022250X.2010.532261). Agents who have a directed small world network update their opinion based on their neighbors opinion.

### Dynamic algorithm
- Each agent has a multidimensional opinion, the dimension of opinion is decided by slider `k`; the value of each dimension of opinion is a double [0,1]
- Links between agents have weight, the larger the opinion distance is, the smaller the weight is. Weight can be set to be \in [0,1] or [-1,1] by switch button
- Update agents' opinion in each dimension by the weighted average of neighbors influence


