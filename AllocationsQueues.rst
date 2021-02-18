Allocation and Queues
=====================


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
