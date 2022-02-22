class Solution {
public:
    ListNode* sortList(ListNode* head) {
        ListNode* t=head;
        vector<int> a;
        while(t)
        {
            a.push_back(t->val);
            t=t->next;
        }
        sort(a.begin(),a.end());
        t=head;
        int i=0;
        while(t)
        {
            t->val=a[i];
            t=t->next;
            i++;
        }
        return head;
    }
};
