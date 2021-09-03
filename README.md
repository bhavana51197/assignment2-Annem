#assignment2-Annem
# Venkata Bhavana Annem #
###### Kerala #######

At **India’s** southwestern-most tip, along the Arabian Sea coast, is the state of Kerala. 

This state, which is often referred to by its affectionate nickname, **God’s Own Country**.

kerala is a wonderful and beautiful mix of diverse cultures and cuisines.

**Be patient**

**VS code**

<hr/>

#### **ordered and unordered list** ####

1. Go to Kansas airport.
2. Board the flight from kansas to India(Kochi airport).
3. Book the hotel from yatra app.
     1. visit munnar.
        1. taste season mangoes.
        2. Try cocunt drink.
        3. Taste banana chips.
     2. visit beaches.
4. After exploring return to kansas.

* In Kerala Food is very famous, try out the following:
    * Appam With Ishtu 
    * Nadan Kozhi Varuthathu
* Explore the beaches.
    * Fort Kochi Beach
    * cherai Beach
* Munnar is good for trecking.

<hr/>

 [AboutMe file link](https://github.com/bhavana51197/assignment2-Annem/blob/main/AboutMe.md)

 <hr/>

 ### Table for the food recommended ###

 In this below table i suggested few of the famous food items present in the different places across the india
 and i have clearly mentioned the food price. 

 |food                 | food place | Price($) |
 |---------------------| ---------- | -------- |
 | Appam with ishtu    | Kerala     | 6.84     |
 | Mutton Kola Urundai | Tamilnadu  | 10.00    |
 | Chicken Biryani     | Hyderabad  | 12.00    |
 | Chow Chow Bhath     | Karanataka | 5.90     |

 <hr/>

 ### Pithy Quotes ###

 > If you cannot do great things, do small things in a great way.<br/>
 _~William Shakespeare_                                                        
 > If you look at what you have in life, you’ll always have more.
 >> Nested!
 > If you look at what you don’t have in life, you’ll never have enough.<br/>
 _~Robert Ervin Howard_

 <hr/>

 ### Code Fencing ###

 > Breadth-first search (BFS) is an algorithm for searching a tree data structure for a node that satisfies a given property.
 > It starts at the tree root and explores all nodes at the present depth prior to moving on to the nodes at the next depth level. 
 >> Nested!
 > Extra memory, usually a queue, is needed to keep track of the child nodes that were encountered but not yet explored.

 vector<vector<int>> adj;  // adjacency list representation
 int n; // number of nodes
 int s; // source vertex

 queue<int> q;
 vector<bool> used(n);
 vector<int> d(n), p(n);

 q.push(s);
 used[s] = true;
 p[s] = -1;
 while (!q.empty()) {
    int v = q.front();
    q.pop();
    for (int u : adj[v]) {
        if (!used[u]) {
            used[u] = true;
            q.push(u);
            d[u] = d[v] + 1;
            p[u] = v;
        }
    }
 }
 if (!used[u]) {
    cout << "No path!";
 } else {
    vector<int> path;
    for (int v = u; v != -1; v = p[v])
        path.push_back(v);
    reverse(path.begin(), path.end());
    cout << "Path: ";
    for (int v : path)
        cout << v << " ";
 }

 [Algorithm link](https://cp-algorithms.com/graph/breadth-first-search.html)

 > Depth-first search (DFS) is an algorithm for traversing or searching tree or graph data structures.
 > The algorithm starts at the root node (selecting some arbitrary node as the root node in the case of a graph) and explores as far as possible along each branch before backtracking.

 ```

 vector<vector<int>> adj; // graph represented as an adjacency list
 int n; // number of vertices

 vector<bool> visited;

 void dfs(int v) {
    visited[v] = true;
    for (int u : adj[v]) {
        if (!visited[u])
            dfs(u);
    }
 }
 vector<vector<int>> adj; // graph represented as an adjacency list
 int n; // number of vertices

 vector<int> color;

 vector<int> time_in, time_out;
 int dfs_timer = 0;

 void dfs(int v) {
    time_in[v] = dfs_timer++;
    color[v] = 1;
    for (int u : adj[v])
        if (color[u] == 0)
            dfs(u);
    color[v] = 2;
    time_out[v] = dfs_timer++;
 }
 ```
  [Code link](https://cp-algorithms.com/graph/depth-first-search.html)
