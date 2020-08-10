## GS Quantify 2019

GS Quantify is the flagship coding organized by **Goldman Sachs, a leading global investment bank.** They have 
given real world problems that can solve in the realms of Computer Science, Machine learning, and quantitative aptitude.

**Machine Learning Problem - Lining Up Logs**

Logs are an integral part of Goldman Sach's day to day operations. We depend upon logs to monitor the behaviour of thousands of
applications which process millions of trades, help use manage risk, support algorithmic trading and so on. In all, these applications generate
hundreds of millions of log lines every day which engineers comb through to identify and rectify application failures.

However, different applications built by different engineers tend to communicate the same kinds of failures in different ways. This makes the process
of identifying similar failures across different applications difficult and tedious.

To that end, the log analytics team at Goldman Sachs is developing tools that would identify common kinds of failures. This would enable the
engineers to easily spot failures and assess who is best equipped to respond to such failures.

The Problem that you must solve is just this - given a set of log lines, assign each to a cluster. The overall goal of this problem
is to identify the intent of each log line and group log lines with the same intent in the same cluster.

**Example 1**
The following lines are all part of the same cluster that requires an API for a list of servers:

* gs-quantify-api 2019-30-06 13:00:10 Received 30 server IDs from API
* gs-quantify-log 2019-31-07 09:30:55 Received 1550 server UIDs from API
* gs-quantify-api 2019-08-31 13:30 Received 80 server UMMIDs from API

**Example 2**
The following belong to a cluster that queries a particular REST API:

* gs-quantify-api 2019-12-07 11:30:09.001001 Downloaded 81 records using "GET /magic_api/dataset_x.csv"
* gs-quantify-api 2019-12-07 11:30:09.001001 Saved 755 records using "POST /magic_api/dataset_y"


**Evaluation Criterion**
A pair wise log line scoring function which is defined as follows:

Let there be N log lines clustered into k clusters. Let L_i and L_j be two such log lines belonging to the same cluster
C_z which has a total of s_z elements. 

For each cluster we will compute a score given by:
![image](https://hrcdn.net/s3_pub/hr-assets/0/1570184392-55e63246ff-ClusterScore.PNG)

The function Score (L_i, L_j) will reward correct nuanced clustering and penalize incorrect clustering.

The overall score will be the average score across clusters given by:
![image](https://hrcdn.net/s3_pub/hr-assets/0/1570184758-d4148f7939-TotalScore.PNG)

Where k is the number of clusters into which the number of dataset has been divided.

**Selected in onsite finalist round among 500+ participants**
