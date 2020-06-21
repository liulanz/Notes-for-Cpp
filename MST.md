A minimum spanning tree or minimum weight spanning tree is a subset of the edges of a connected, edge-weighted undirected graph that connects all the vertices together, without any cycles and with the minimum possible total edge weight. 

How to do it => Use kruscal Algorithm (Union Find knowledge is needed)

```
//Assume Edges are given format [from,to,cost]

vector<vector<int>>edges; //assume is given
int N; //number of nodes

//we need to sort the edges array base on the cost
int total=0;
sort(edges); //please implement it... not familiar with c++
vector<int> nums(N);
for(int i=0;i<N;i++)nums[i]=i;
for(vector<int>&tuple:edges){
    int v1=tuple[0],v2=tuple[1],cost=tuple[2];
    int root1=find(nums,v1);
    int root2=find(nums,v2);
    if(root1!=root2){
        total+=cost;
        nums[root1]=root2;
    }
    cout<<"The minimum spanning cost is "<<cost<<endl;
}




int find(vector<int>&nums,int x){
    if(nums[x]==x)return x;
    int root=find(nums,nums[x]);
    nums[x]=root;
    return root;
}

```

