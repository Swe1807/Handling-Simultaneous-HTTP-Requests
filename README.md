# Handling-Simultaneous-HTTP-Requests
Handling Simultaneous HTTP Requests

This project aims at:
1. Designing an algorithm which can handle simultaneous HTTP Requests that a server
receives from various clients.
2. Compare the algorithm with pre-existing algorithms (FCFS, SJF, Round Robin).

To implement on local system following assumptions have been taken:

1. the server has got several pending requests..(to implement this, initially the requests have been stored (5 requests are accepted in 1 go)so that they can be handled at the same time).
2. file size determines the job duration..more the size of the requested file, more is its burst time.

Algorithms:

following algorithms have been implemented:
1. First Come First Serve (FCFS).
2. Shortest Job First (SJF).
3. Round Robin.
4. Self created algorithm namely, Best Job First(BJF).

Best Job First:
This algorithm gives importance to both the requests that have come earlier and also to those which have lesser burst time...
it calculates the priorities on these basis and then accordingly respond to them.

For example
Lets consider a set of values and see how the algorithm executes these requests.
The order in which the requests were made along with their individual processing time is as
follows:
Request 1 : 14
Request 2 : 10
Request 3 : 11
Request 4 : 07
Request 5 : 08

How our algorithm works??

Order of execution of any Request = sno of arrival + sno of processing time
Sno of arrival:
Request 1: 1
Request 2: 2
Request 3: 3
Request 4: 4
Request 5: 5

Sno of processing time:

Request 1: 5
Request 2: 3
Request 3: 4
Request 4: 1
Request 5: 2

Priority value of Request 1 = 1 + 5 = 6
Priority value of Request 2 = 2 + 3 = 5
Priority value of Request 3 = 3 + 4 = 7
Priority value of Request 4 = 4 + 1 = 5
Priority value of Request 5 = 5 + 2 = 7

Therefore the order of response will be as follows:
Request 2
Request 4
Request 1
Request 3
Request 5

To run the code:
Send 5 Http Requests to the server after running the server code(in python, namely server.py) and corresponding respond will be send along with the complete processing stages and a plot comparing the 4 algorithms.
