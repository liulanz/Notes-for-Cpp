![image](https://media.springernature.com/full/springer-static/image/art%3A10.1038%2Fnbt0704-909/MediaObjects/41587_2004_Article_BFnbt0704909_Fig1_HTML.gif)
'''
class Solution {
public:
    int uniquePaths(int m, int n) {
        vector<vector<int>>dp(n, vector<int>(m));
        if(m==1&&n==1)
            return 1;
        for(int i=1;i<m;i++)
        {
            dp[0][i]=1;
        }
        for(int i=1;i<n;i++)
        {
            dp[i][0]=1;
        }
        for(int i=1;i<n;i++)
        {
            for(int j=1;j<m;j++)
            {
                dp[i][j]=dp[i-1][j]+dp[i][j-1];
                cout<<dp[i][j]<<endl;
            }
        }
        
        return dp[n-1][m-1];
    }
};
'''
