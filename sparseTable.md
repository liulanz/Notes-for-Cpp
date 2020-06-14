Leetcode 303 sparse Table solution

class NumArray {
    int sparse[][];
    int A[];
    public NumArray(int[] A) {
        this.A=A;
        sparse=new int[A.length][31];
        for(int i=0;i<A.length;i++){
            sparse[i][0]=A[i];
        }
        for(int j=1;j<=30;j++){
            for(int i=0;i+(1<<j)<=A.length;i++){
                sparse[i][j]=sparse[i][j-1]+sparse[i+(1<<(j-1))][j-1];
            }
        }
    }
    public int sumRange(int L, int R) {
        int sum = 0;
        for (int j = 30; j >= 0; j--) {
            if (L+(1 << j) <= R+1) {// check if in range
                sum += sparse[L][j];
                L+=1<< j;
            }
        }
        return sum;
    }
}
