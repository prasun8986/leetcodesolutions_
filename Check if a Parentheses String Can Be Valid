class Solution {
public:
    bool canBeValid(string s, string locked) {
        if (s.length() % 2 != 0 ) return false;
        int open = 0, balance = 0;
         for (int i = 0; i < s.length(); ++i) {
            open += (locked[i] == '1' ? (s[i] == '(' ? 1 : -1) : 1);
            if (--balance < 0) balance = 0;
            if (open < 0) return false;
        }
        open = 0, balance = 0;
        for (int i = s.length() - 1; i >= 0; --i) {
            open += (locked[i] == '1' ? (s[i] == ')' ? 1 : -1) : 1);
            if (--balance < 0) balance = 0;
            if (open < 0) return false;
        }
        return true;
    }
};
