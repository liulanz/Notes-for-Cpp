```
class NumArray {
    int tree[];//1-index based
    int A[];
    int arr[];
    public NumArray(int[] A) {
        this.A=A;
        arr=new int[A.length];
        tree=new int[A.length+1];
        int sum=0;
        for(int i=0;i<A.length;i++){
            update(i,A[i]);
        }
        for(int x:tree)System.out.println(x);
    }
    
    public void update(int i, int val) {
        int dif=val-arr[i];
        arr[i]=val;
        i++;
        while(i<tree.length){
            tree[i]+=dif;
            i+=(i&-i);
        }
    }
    
    public int sumRange(int i, int j) {
        return pre(j+1)-pre(i);
    }
    
    public int pre(int i){
        int sum=0;
        while(i>0){
            sum+=tree[i];
            i-=(i&-i);
        }
        return sum;
    }
}

/**
 * Your NumArray object will be instantiated and called as such:
 * NumArray obj = new NumArray(nums);
 * obj.update(i,val);
 * int param_2 = obj.sumRange(i,j);
 */
```
