# Integration of Bike-sharing with Public Transport

This code presents an algorithm to solve a bi-level optimization problem.
The upper-level problem aims to optimize pricing (for bike-sharing, public transport, and combined modes), tolls for cars, and fleet sizing for both bike-sharing and public transportation systems. The objective function at this level is social welfare, which includes two main components — operators' surplus and consumers' surplus — along with two optional components: health benefits and climate change cost.
The design variables in the upper-level model are pricing and fleet sizing for the multi-modal transportation network.
The lower-level problem is a modified user equilibrium model, used to evaluate both route choice and mode choice by users within the network. The decision variables at this level are demand and traffic/passenger flows across different transportation modes.
The upper-level problem is solved using a genetic algorithm, while the lower-level problem is addressed using a modified Method of Successive Averages (MSA).
The lower-level model is embedded as a function within the upper-level algorithm, allowing both levels to be solved iteratively.

To test the reliability and effectiveness of the algorithm, we applied it to a well-known example from the literature: Mandl’s network, which consists of 15 nodes and 29 links. The nodes serve as origins, destinations, and stations. Some input data — such as the OD matrix and free-flow travel times — are available in previous studies, while other attributes, including link lengths and capacities, were assumed by the authors.
In addition, public transportation lines were defined between OD pairs with higher demand, based on assumptions in the literature.
Although Mandl’s network is a conceptual example, we aimed to calibrate the model using data from a single real-world region — Switzerland. This choice is motivated by the fact that one of our future case studies will focus on the Swiss city of Geneva, while another will examine a city in Germany. Using Swiss-based empirical information allows us to maintain consistency in behavior modeling and calibration across our example and next real-world case.
