# Road-Network-Analysis-in-Neo4j

Objective

To understand and apply Neo4j’s graph database capabilities by loading a road network dataset and executing various Cypher queries. This assignment will help you build skills in data loading, query optimization, and network analysis within Neo4j.

Datasets 
Your dataset will represent connections between cities, with each connection having a specified distance. The data should be structured in a CSV file with three columns: city1, city2, and distance. For example:
city1   City2       Distance
Atlanta Dallas      800
El Paso Nashville   500
Detroit Chicago     300
Chicago Boston      190

TASKS: Part 1: Generating the Dataset

You can generate a dataset for this assignment using a simple Python generator or using the Faker library. Make sure your dataset adheres to the following criteria:
Network Structure: Ensure the dataset represents a connected road network with distances between specified cities.
Uniqueness: Ensure that there are no duplicate entries for city pairs in the city1 and city2 columns. If the same city pair appears multiple times (e.g., city1 to city2 with a distance of 300 miles), modify your dataset to prevent this repetition (same as city2 city 1). Each pair of cities should only appear once with a specific distance. If there are multiple routes or paths between the same cities, consider differentiating them by adding a unique identifier or using an alternative method to avoid exact duplicates.
Size: Generate a dataset of 10000 rows (200 nodes, and to 3000 unique edges). Unique road connections between these cities with different distances.
The cities that you will use are listed in the attached text files (cityNames.txt).
Connectivity: Ensure that each city has multiple incoming and outgoing paths to create a realistic network.
With 3,000 edges, each city would have an average of 15 connections (incoming and outgoing), which is both rich in connectivity and reasonable in complexity.


TASKS PART 2: Answer the following questions

Main Tasks:
1. List Roads from/to a Specific City with Distances and Destinations
 Retrieve all roads (connections) from or to a specific city (e.g., "Atlanta") and show the destination cities and distances.
2. Find Roads Longer than a Specific Distance
 Retrieve connections where the distance is greater than a specific value (e.g., 100 km), showing both cities and the distance.
3. Count the Number of Roads Connected to a Specific City
 Count how many roads (connections) are connected to a specific city (e.g., "Miami").
4. Find Cities Connected to a City with a Distance Below a Specific Value
 List all cities directly connected to a city (e.g., "Dallas") with a distance under a specific threshold (e.g., 100 km).
5. List All Roads Leading to a Specific City
 List all roads leading to a specific city (e.g., "Los Angeles").
6. Calculate the Total Distance of All Roads Connected to a City
 Calculate the total distance of all roads connected to a specific city (e.g., "Memphis").
7. Find the Shortest Road Between Two Cities
 Retrieve the shortest road (minimum distance) between two specific cities (e.g., "Chicago" and "Houston").
8. Find Cities Connected to Both 'Denver' and 'Seattle'
 Retrieve all cities directly connected to both "Denver" and "Seattle".
9. List Cities with More Than 3 Connections and Their Connections
 List cities with more than 3 direct connections and display each connection.
10. Calculate the Total Distance of All Connections in the Network
 Calculate the total distance of all connections in the network.


Extra credits:
1. Identify Cities with Exactly Two Connections
Find cities that have exactly two direct connections (either incoming or outgoing).
2. List Cities with Both Incoming and Outgoing Connections
Find cities that have both incoming and outgoing connections, listing the total count of each type.
3. Identify the Top 3 Pairs of Cities with the Longest Direct Distances
Identify the top three pairs of cities with the longest direct distance between them.


Deliverables

Cypher Code:
Provide the Neo4j Cypher queries used to complete each of the tasks.
Ensure that each query is clearly documented, with explanations on the purpose and functionality of the query.
Dataset Generation Code:
Provide the Python code (or any other method used like Neo4j software itself) that generates the dataset for testing.
Ensure the dataset is structured correctly with 200 cities and 3,000 unique connections (or according to the dataset specification provided).
Include any necessary modifications to ensure that no city pair is repeated in the dataset (e.g., "Atlanta" to "New York" should appear only once).

Important Dataset Rules:

No Self-Connections: A city cannot be connected to itself. In other words, city1 cannot be the same as city2 (e.g., Atlanta to Atlanta is not allowed).
Separate Directions: If two cities are connected, list both directions separately. For example, Atlanta to New York and New York to Atlanta are separate relationships.
Results Documentation:
For each query, present the results clearly:
Use text outputs, tables, or screenshots (limit the results to 10 for easier interpretation).
Ensure that the data retrieved or calculated by each query is shown clearly, including the final output for every task.
Provide any necessary explanations for the results, such as what the data represents and how it answers the task.


Analysis and Observations:
Write a brief analysis comparing the performance and ease of querying within Neo4j.
Highlight any differences, challenges, or insights gained during the execution of the tasks.
Focus on how Neo4j handles graph-related queries (e.g., shortest paths, aggregation, counting connections) and any specific observations related to the graph nature of the data.
