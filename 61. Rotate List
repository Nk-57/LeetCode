/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode() : val(0), next(nullptr) {}
 *     ListNode(int x) : val(x), next(nullptr) {}
 *     ListNode(int x, ListNode *next) : val(x), next(next) {}
 * };
 */
class Solution {
public:
    ListNode* rotateRight(ListNode* head, int k) {
        if(head==nullptr ||  head->next==nullptr){
            return head;
        }
        ListNode* curr=head;
        int len=1;
        while(curr->next != nullptr){
            curr=curr->next;
            len++;
        }
        k=k%len;
        if(k==0){
            return head;
        }
        curr->next=head;
        ListNode* temp=head;
        for(int i=1;i<len-k;i++){
            temp=temp->next;
        }                      
        head=temp->next;
        temp->next=nullptr;
        return head;
    }
};
