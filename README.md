## PrefixFTM: A Parallel Framework for Mining Frequent Tree
Following divide and conquer, this system treats each pattern to examine and extend as a task, and parallelizes all tasks as much as possible following the idea of divide and conquer. This allows it to use all CPU cores in a machine to mine frequent patterns over big data.

There are 2 applications on top of our framework. Here are the folder structures:

* system: the general-purpose programming interface
* app
    * treeminer: the parallel version developed on serial treeminer[1]
    * prefixtreespan: the gSpan parallel version developed on serial prefixtreespan[2]

[1] Mohammed J. Zaki. Efficiently mining frequent embedded unordered trees. Fundamenta Informaticae, 66(1-2):33–52, Mar/Apr 2005. Special issue on Advances in Mining Graphs, Trees and Sequences.

[2] Zou L., Lu Y., Zhang H., Hu R. PrefixTreeESpan: A Pattern Growth Algorithm for Mining Embedded Subtrees. In: Aberer K., Peng Z., Rundensteiner E.A., Zhang Y., Li X. (eds) Web Information Systems – WISE 2006. WISE 2006. Lecture Notes in Computer Science, vol 4255. Springer, Berlin, Heidelberg


Note that OpenMP is used and should be enabled in your Makefile. There are 3 run_XXX.cpp files for the 3 applications above. To compile each one, you may run "cp run_XXX.cpp run.cpp" and then run "make". The compiled "run" program can be renamed to a meaningful name for later use.

A sample command to run each program is put at the end of each each run_XXX.cpp file, which reads data from the sample data that we put in the folder of each application.

The following is the complete command:

./run -s [support_threshold] -i [input_file] -n [thread_number] -t [task_parallelism_threshold] -T [PDB_parallelism_threshold]

### Contact
Da Yan: http://www.cs.uab.edu/yanda

UAB Data Lab (or YanLab@UAB): http://vorlon.cs.uab.edu/bigdata

Email: yanda@uab.edu

### Contributors
Wenwen Qu

Da Yan
