# 读代码笔记
## ICBSSearch.cpp
### bool ICBSSearch::runICBSSearch()
- 用cost_upperbound维护了一个解的上界
- handle_type——fibonacci_heap当中元素的别名  
- 当min_f_val>=cost_upperbound时退出循环 
- 取出focal_list中的堆顶元素
- focal_list中按照num_of_collisions排序节点
- open_list中按照f_val排序节点
- shared_ptr c++标准库智能指针当中的一种，常用于有多个指针指向同一对象的需求时，它可以自动管理内存。
- conflict 五维元组（a_i,a_j,rectangle conflict, vertex(<0)/edge(>=0) conflict,t）
- ``` 
  struct PathEntry
  {
  int location;
  bool single;
  PathEntry(int loc = -1) { location = loc; single = false; }
  }; 
  ```
- ICBSNode 只存一个agent的路径和冲突等.
- 从focal_list中选择一个节点
- at(n) 安全地访问vector当中的第n个元素
- 625：：classifyConflicts

## Problem
- in SingleAgentICBS::FindPath,参数minlength用处？
- 