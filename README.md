# ASP for Bus Route Planning

**Authors:** Teeradaj Racharak (JAIST, Japan), Suyee Mon (KMITL, Thailand), and Rathachai Chawuthai (KMITL, Thailand) 

**Contacts:** racharak [at] jaist [dot] ac [dot] jp, 65016131 [at] kmitl [dot] ac [dot] th, rathachai [dot] ch [at] kmitl [dot] ac [dot] th

**Disclaimer:** This repository contains executable source codes supporting our submission to KR 2024 (KR in the Wild Track). 

## Folder Documentation
This repository contains data and code for finding shortest-path bus plans using **Answer Set Programming (ASP) methods**. The primary data file is **'bus_plan.csv'**, and notebooks in the **'Experiments_code'** folder perform various analyses on this data using ASP.

###Data
**bus_plan.csv:** This file contains the bus route data needed to find the shortest path. Each row represents a different aspect of the bus plan, including routes, bus stops, and minimum times.

###Experiments_code 
The **'Experiments_code'** folder contains notebooks that utilize Answer Set Programming (ASP) methods. Below is a brief description of each:

1. **Finding_Min_Transfer_1_hop.ipynb:** This notebook uses ASP methods to identify routes with the minimum number of transfers within a single hop. It aims to find the most efficient routes that require only one travel exchange.
2. **Finding_Min_Transfer_2_hops.ipynb:** This notebook is similar to the one-hop analysis; this notebook extends the search to routes that require up to two transfers, using ASP methods to identify efficient routes with minimal travel exchange within two travel exchanges.
3. **Finding_Min_Transfer_3_hops.ipynb:** This notebook extends the transfer analysis to 3 travel exchanges using ASP methods. It finds routes that require up to three transfers and evaluates their efficiency.
4. **Finding_Minimum_Time_Difference_Route.ipynb:** This notebook uses ASP to analyze routes and find those with the minimum time difference between consecutive bus stops, aiming to identify the fastest routes by minimizing the total travel time.
5. **Finding_Minimum_Time_Same_Route.ipynb:** Focuses on finding the routes with the minimum travel time on the same route using ASP methods. It evaluates the time efficiency of the shortest routes without considering transfers.
6. **Shortest_Path_Finding_for_Bus_Simulation.ipynb:** This notebook finds the shortest path of bus routes for minimum time and minimum transfer on the simulated bus route plan. 

## Paper 

**Title:** Solving an Industrial-Scale Bus Route Finding in Public Transport Network using Modular Answer Set Programming

**Abstract:** Finding user-satisfied bus routes subject to the minimal travel time and the number of route transfers is a challenging problem in transportation networks. In our context, bus routes and bus stations form a directed graph. Thus, a solution to finding the user-satisfied bus routes is a route path between two given stations satisfying a collection of different user’s constraints. While this problem could be related to existing research, such as, the study of graph traversal and path finding algorithms. We show that our problem is more suited to formalizing the navigation system in terms of an answer set programming (ASP) rather than solving the more common graph traversal problems such as the well-known Dijkstra’s algorithm, which only provides a statically single solution with lowest cost. An empirical evaluation on a real-world bus network shows how well our ASP encoding works in producing a wide range of high-quality solutions that explore the trade-off between the two optimization criteria, all the while keeping Dijkstra’s result as a point of comparison. The findings show promise for extending to richer transit representations and optimization objectives beyond the two considered here.


