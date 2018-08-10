
<details>
<summary>Click here to see full publications from [Loghub](https://github.com/logpai/loghub)</summary>
<p>

##### Publications using loghub datasets	
+ [**CCS'17**] Min Du, Feifei Li, Guineng Zheng, Vivek Srikumar. [DeepLog: Anomaly Detection and Diagnosis from System Logs through Deep Learning](https://acmccs.github.io/papers/p1285-duA.pdf). ACM Conference on Computer and Communications Security (CCS), 2017.
+ [**TDSC'17**] Pinjia He, Jieming Zhu, Shilin He, Jian Li, Michael R. Lyu. [Towards Automated Log Parsing for Large-Scale Log Data Analysis](http://jiemingzhu.github.io/pub/pjhe_tdsc2017.pdf). IEEE Transactions on Dependable and Secure Computing (TDSC), 2017.
+ [**ICWS'17**] Pinjia He, Jieming Zhu, Zibin Zheng, Michael R. Lyu. [Drain: An Online Log Parsing Approach with Fixed Depth Tree](http://jiemingzhu.github.io/pub/pjhe_icws2017.pdf). IEEE International Conference on Web Services (ICWS), 2017.
+ [**ICSE'16**] Qingwei Lin, Hongyu Zhang, Jian-Guang Lou, Yu Zhang, Xuewei Chen. [Log Clustering Based Problem Identification for Online Service Systems](http://ieeexplore.ieee.org/document/7883294/). International Conference on Software Engineering (ICSE), 2016.
+ [**DSN'16**] Pinjia He, Jieming Zhu, Shilin He, Jian Li, Michael R. Lyu. [An Evaluation Study on Log Parsing and Its Use in Log Mining](http://jiemingzhu.github.io/pub/pjhe_dsn2016.pdf). IEEE/IFIP International Conference on Dependable Systems and Networks (DSN), 2016.
+ [**ISSRE'16**] Shilin He, Jieming Zhu, Pinjia He, Michael R. Lyu. [Experience Report: System Log Analysis for Anomaly Detection](http://jiemingzhu.github.io/pub/slhe_issre2016.pdf). IEEE International Symposium on Software Reliability Engineering (ISSRE), 2016.
+ [**KDD'09**] Adetokunbo Makanju, A. Nur Zincir-Heywood, Evangelos E. Milios. [Clustering Event Logs Using Iterative Partitioning](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.503.7668&rep=rep1&type=pdf). ACM SIGKDD International Conference on Knowledge Discovery and Data Mining (KDD), 2009.
+ [**SOSP'09**] Wei Xu, Ling Huang, Armando Fox, David A. Patterson, Michael I. Jordan. [Detecting Large-Scale System Problems by Mining Console Logs](https://www.sigops.org/sosp/sosp09/papers/xu-sosp09.pdf). ACM Symposium on Operating Systems Principles (SOSP), 2009. 
+ [**DSN'07**] Adam J. Oliner, Jon Stearley. [What Supercomputers Say: A Study of Five System Logs](http://ieeexplore.ieee.org/document/4273008/). IEEE/IFIP International Conference on Dependable Systems and Networks (DSN), 2007.

</p>
</details>

## 1. Automated Log Parsing
[Towards Automated Log Parsing for Large-Scale Log Data Analysis](http://jiemingzhu.github.io/pub/pjhe_tdsc2017.pdf)

**Summary**: overview on log parsing, evaluation on POP parsing method

**Key points**
	
* log analysis techniques into 3 steps
	* log parsing	
	* matrix generation
	* log mining
* 4 existing log parsers ([papers and codes on those 4 parsers + POP](https://github.com/logpai/logparser))
	* SLCT
	* LogSig
	* IPLoM
	* LKE
* this paper purposes POP, a parallel log parsing method
* log parsing = list of _log events_ + _structured logs_ (log events = static content = template of log messages)
* POP 
	1. process domain knowledge
	2. hierarchical partition the logs into different groups
	3. for each group, constant parts are extractd to contruct log events
	4. merge similar groups based on hierarchical clustering on log events 

*Note*: the paper states that traditional log parsing relies on regular expressions; reasons why it is error-prone and inefficient:

* log grows rapidly
* open source, developers might be unaware of the orginal logging purpose


## 2. DeepLog

[DeepLog: Anomaly Detection and Diagnosis from System Logs through Deep Learning](https://acmccs.github.io/papers/p1285-duA.pdf)

**Summary**: Log pattern recognition with deep learning
	
**Key points**

* model a system log as a natural language sequence
* log patterns deviated from deep learning model 
	* Long Short-Term Memory/LSTM networks 
	
		<details>
		<summary>More info. on LSTM</summary>
		<p>	
		
					RNN = a deep learning model that forwards the output of a layer to the next input 
					LSTM network = instace of Recurrent Neural Network/RNN = used to solve 'the vanishing gradient' problem as a gating unit = which makes the decision of forgetting and remembering the input for future timestamps
					'the vanishing gradient' = the earlier layers of the network are the slowest to train = expotential small gradient = small update to the next layer = barely moving the weight
					'gradient' = rate at which cost changes with respect to weight or bias 
					cost = generated output - actual output
					
					Neural networks composed of: 
						1) input layer
						2) hidden layer
						3) output layer
					Neural networks = classifier by using, for example, forward progation; = for more complex example, it serves for pattern recognition (ie. deep net for facial recognition)
						
		* [The vanishing gradient](https://youtu.be/SKMpmAOUa2Q)
		* [Which deep network to use](https://www.youtube.com/watch?v=JjZDoojyzXQ)
		</p>
		</details>

		* log parser extracting only the log key(static content)
			* parameters in certain case as identifier
	
	
**Findings**

* system log data anomaly detection is classified into 3 groups
	* PCA based
	* invariant mining based
	* workflow based methods
	
## 3. An Evaluation Study on Log Parsing and Its Use in Log Mining
[An Evaluation Study on Log Parsing and Its Use in Log Mining](http://jiemingzhu.github.io/pub/pjhe_dsn2016.pdf)


**Summary**: ...
	
**Key points** 
...
	
<hr>

<details>
<summary>Click here for more information on [loglizer](https://github.com/logpai/loglizer)</summary>
<p>
Loglizer is an open-source python tool for automatic log-based anomaly detection with machine learning techniques. In this project, six popular anomaly detection methods are implemented and evaluated on two public datasets.
</p>
</details>

To Do...
<hr>
