System Overview
===============

Computational Nodes
-------------------

INCLINE contains 30 dedicated nodes for computation.
The majority are ``COMPUTE`` nodes, which are CPU only and 2GB/core, but INCLINE also contains two ``HIGH MEMORY`` nodes (16GB/core) and two ``GPU`` nodes, each with two NVIDIA A100 GPUs.
Specifics are outlined in the table below.


+-----------+-----+----------+--------------+--------+----------+
|Type       |QTY  |CPU Type  | Cores/Threads| Memory | GPU      |
|           |     |          |              |        |          |
|           |     |          |              |        |          |
+===========+=====+==========+==============+========+==========+
|``COMPUTE``|26   |2x AMD    | 128C/256T    |256GB   |None      |
|           |     |EPYC 7662 |              |        |          |
|           |     |          |              |        |          |
+-----------+-----+----------+--------------+--------+----------+
|``HIGH     |2    |2x AMD    | 128C/256T    |2048GB  |None      |
|MEMORY``   |     |EPYC 7662 |              |        |          |
|           |     |          |              |        |          |
+-----------+-----+----------+--------------+--------+----------+
|``GPU``    |2    |2x AMD    | 64C/128T     |1024GB  |2x NVIDIA |
|           |     |7452      |              |        |A100      |
|           |     |          |              |        |          |
+-----------+-----+----------+--------------+--------+----------+


Other Nodes
-----------




High Speed File System
----------------------

Normal File System
------------------

High Speed Interconnect
-----------------------

Networking
----------

