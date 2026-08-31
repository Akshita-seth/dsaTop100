1. Soln:
- Using min heap fro top K largest freq elements ( )
- customm comparator
struct customComparator {
    bool operator()(const pair<int,int>& a, const pair<int,int>& b) {
        return a.first > b.first;   // first only if freq is stored first in pair of min heap 
        // min-heap: smaller frequency has higher priority
    }
};
- Use map for storing freq
- Traverse over the freq map
- push in pairs
