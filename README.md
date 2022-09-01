Part A. Session -- Path mapping

S1: double_direction
S2: lane_change
S3: single_direction
S4: t_junction

Part B. A introduction to the files.
### 1. Specification
    * law_specification.txt: the formal specification of the 13 testable articles in Chinese traffic laws.
    * violation_formulae.json: all the violation formulae transformed from law_specification.txt.
    * law-violation-map.json: a matching between articles and their violation formuale.

### 2. Data_Set
	* Original_Scenario_Scripts: the four scenario scripts used in our work: Intersection with Double-Direction Roads (S1), Lane Changing in the Same Road (S2), Intersection with Single-Direction Roads (S3), T-Junction (S4).
	* Rawdata_From_LawBreaker: the existing trace data in the four scenarios from LawBreaker.
	* Encoded_Action_Sequences: the enocded action sequences from the rawdata.
	* Action_Space: the action space for the encoded ation sequences in each session.

### 3. ABLE_Source_Code

	* README.md: how to setup our project.
	* testing_engines/gflownet/generator/pre_process: encoding scenarios and decoding action sequences.
	* testing_engines/gflownet/GFN_Fuzzing.py: the entry of our testing algorithm.
	* testing_engines/gflownet/generator: our scenario generator based on customized gflownet.

### 4. Experiment_Data

	* RQ1: the data in Research question 1, including the discovered violations and difficulty degree.
		* For example, file sub_law_violation_2.json consists of the scenario violating No.2 formula and the trace data.
	* RQ2: the relation between the number of discovered violations and the number of runs.
	* RQ3: the discovered violations by the two alternative methods, i.e., active+max and inactive+new.

