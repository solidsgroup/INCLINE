INCLINE Resources
=================


Allocations
-----------

.. table::
   :widths: 20,60
	    
   +----------------------------------------+----------------------------------------+
   | Allocation Type                        | Description                            |
   +========================================+========================================+
   | ``REAS Account``                       | Allocation for activities related to   |
   |                                        | research projects described here.      |
   |                                        | Granted on a quarterly basis based on  |
   |                                        | competitive proposal process.          | 
   +----------------------------------------+----------------------------------------+
   | ``CRSE Account``                       | Allocation for course-related          |
   |                                        | activities. Allocations granted on a   |
   |                                        | quarterly basis based on competitive   |
   |                                        | proposal.                              |
   +----------------------------------------+----------------------------------------+
   | ``MISC Account``                       | Limited “seed” accounts given on a     |
   |                                        | first-come-first-served basis. Limits  |
   |                                        | predetermined by committee based on    |
   |                                        | demand and resources.                  |
   +----------------------------------------+----------------------------------------+
   | ``EXTR Account``                       | Accounts for all off-campus and RMACC  |
   |                                        | users. Granted by competitive          |
   |                                        | proposal. Limits determined by         |
   |                                        | committee.                             |
   +----------------------------------------+----------------------------------------+



Queues
------
..
   Note: See
   https://github.com/fraoustin/sphinx_fontawesome/blob/master/sphinx_fontawesome/constant.py
   for list of fontawesome icons


.. table::
   :widths: 20,30,30

   +-------------------+------------------------------------------+
   | **Queue Name**    | **Description**                          |
   +-------------------+------------------------------------------+
   | ``compute``       | Standard workhorse queue for jobs that   |
   |                   | use the compute nodes.                   |
   |                   +-----------+------------------------------+
   |                   | |clock-o| | |stack-overflow|             |
   |                   | 12 Hours  | 10 Jobs                      |
   +-------------------+-----------+------------------------------+
   | ``compute-dev``   | High-priority queue with tight limits on |
   |                   | job length and queue number. Use for     |
   |                   | testing code but not for production runs.|
   |                   +-----------+------------------------------+
   |                   | |clock-o| | |stack-overflow|             |
   |                   | 1 Hour    | 1 Job                        |
   +-------------------+-----------+------------------------------+
   | ``compute-long``  | Low-priority queue with unlimited job    |
   |                   | length. Only one job allowed in the queue|
   |                   | at a time                                |
   |                   +-----------+------------------------------+
   |                   | |clock-o| | |stack-overflow|             |
   |                   | Unlimited | 1 Job                        |
   +-------------------+-----------+------------------------------+
   | ``gpu``           | Queue for running jobs on the GPU nodes  |
   |                   |                                          |
   +-------------------+------------------------------------------+
   | ``hm``            | Queue for running jobs on the high memory|
   |                   | nodes                                    |
   +-------------------+------------------------------------------+
   | ``hetero``        | Special queue for jobs that use any      |
   |                   | combination of compute, GPU, and high    |
   |                   | membory nodes.                           |
   |                   |                                          |
   +-------------------+------------------------------------------+


Calculating Computing Units
---------------------------

INCLINE resources are described in terms of **CPU Hours** (CPUH).
One standard CPUH is defined as one hour of allocated use by a ``compute`` node.
**Important**: the CPUH will be billed to your account regardless of whether the node is fully utilized.

Time allocated on specialty nodes are denoted differently.
One hour of allocated time by a ``gpu`` node is a GPU-CPUH; an hour of allocated time by a ``high memory`` node is a HM-CPUH.
Resources for CPUH, GPU-CPUH, and HM-CPUH are billed independently, and are non-transferrable.

.. admonition:: Example 1

		Alice needs to run 10 large CFD simulations.
		She estimates that, running with approximately 2000 MPI processes (no special memory requirements), each simulation will complete in four hours.

		To run a concurrent job with 2000 MPI processes will require 8 nodes. (8 x 256 threads = 2048).
		Each job will then require (4 hours) x (8 nodes) = 32CPUH.
		Therefore, Alice should request at least 320CPUH.

.. admonition:: Example 2

		Bob is working on a fictitious machine learning project that will require extensive data processing.
		He estimates that training and testing his model will take 2 days on a single A100 GPU.
		(There is no way to split the job across multiple GPUs; it must be done serially.)
		Afterwards, the data analysis will take about 30 hours on a high memory node.

		Even though Bob will only be using one of the two GPUs on a ``gpu`` node, he must request time on the entire node.
		Because he also needs to use a ``high memory`` node, he must specify that allocation independently from the ``gpu`` node.
		Therefore, he should request **48 CPU-CPUH** and **30 HM-CPUH**.
		
		
		

	  


