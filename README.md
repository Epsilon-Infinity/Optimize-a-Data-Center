# Optimize-a-Data-Center
Hash code 2015 Qualification Task.

## Introduction

For over ten years, Google has been building data centers of its own design, deploying thousands of machines in locations around the globe. In each of these locations, batteries of servers are at work around the clock, running services we use every day, from Google Search and YouTube to the judge system of Hash Code.

Data center design is a multi­factor optimization problem. Surely, we want to get as much computing capacity as possible — the services need a lot of resources today and will be asking for more tomorrow. But maximizing the raw capacity is not the only goal: it’s equally important to ensure that the computing capacity is provided reliably even in the face of inevitable hardware failures.

## Task
Servers in a data center are physically divided into rows. Rows can share resources such as electric power. If such a shared resource fails, we assume that the entire row is lost and all servers in that row become unavailable.

Servers in a data center are also logically divided into pools. Each server belongs to exactly one pool, and provides it with some amount of computing resources, called capacity. The capacity of a pool is the sum of the capacities of the available servers in that pool.

To ensure reliability of a pool, it is therefore desirable to distribute its servers between different rows. Then, when a row fails, the pool can continue to operate on the servers from the remaining rows (albeit with a reduced capacity because of the unavailable servers). The guaranteed capacity of a pool is the minimum capacity it will have when at most one data center row goes down.

Given a schema of a data center and a list of available servers, your goal is to assign servers to slots within the rows and to logical pools so that the lowest guaranteed capacity of all pools is maximized.