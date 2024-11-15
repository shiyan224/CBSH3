# 读代码笔记
## ICBSSearch.cpp
### bool ICBSSearch::runICBSSearch()
- 用`cost_upperbound`维护了一个解的上界
- `handle_type`——`fibonacci_heap`当中元素的别名  
- 当`min_f_val>=cost_upperbound`时退出循环 
- 取出`focal_list`中的堆顶元素
- `focal_list`中按照`num_of_collisions`排序节点
- `open_list`中按照`f_val`排序节点
- `shared_ptr` c++标准库智能指针当中的一种，常用于有多个指针指向同一对象的需求时，它可以自动管理内存。
- `conflict` `5-tuple（a,b,c,d,e）`
	- a : `agent_i`
	- b : `agent_j`
	- c : <0 for rectangle conflict, vertex id otherwise
	- d : <0 for vertex conflict, another vertex for edge conflict
	- e : `t` for vertex conflict, `t + 1` for edge conflict
- ```struct PathEntry
  {
  int location;
  bool single;
  PathEntry(int loc = -1) { location = loc; single = false; }
  }; 
- `ICBSNode`只存一个`agent`的路径和冲突等.
- 从`focal_list`中选择一个节点
- `at(n)` 安全地访问vector当中的第n个元素
- `625：classifyConflicts`
- `106:int ICBSSearch::computeHeuristics(ICBSNode& curr)`计算heuristic
	- `292:bool ICBSSearch::buildDependenceGraph(ICBSNode& node)`建立冲突图
	- 
## Problem
- `in SingleAgentICBS::FindPath`,参数`minlength`用处？
- in `class ICBSSearch`:`vector<list<Constraint>> initial_constraints;`干啥用？
- 