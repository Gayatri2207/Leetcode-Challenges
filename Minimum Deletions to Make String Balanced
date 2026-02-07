class Solution {
    public int minimumDeletions(String s) {
        int n = s.length();
        Stack<Character> st = new Stack<>();
        int ans = 0;
        
        for(char ch : s.toCharArray()) {
            if(ch=='b') {
                st.push('b');
            }
            else {
                // ch == 'a'
                // If 'a' comes after 'b', we have an inversion - delete one char
                if(!st.isEmpty()) {
                    ans++;
                    st.pop();
                }
            }
        }
        return ans;
    }
}
