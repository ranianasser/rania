#include<stdio.h>
#include<stdlib.h>

#define minimumOf(a,b) (a<b) ? a : b;

struct node{
    int data;
    struct node* next;
    int min;
};

void push(struct node **head_ref, int new_data){
    struct node* new_node = (struct node *)malloc(sizeof(struct node));
    new_node->data = new_data;

    if(*head_ref == NULL)
        new_node->min = new_data;
    else
        new_node->min = minimumOf(new_data,(*head_ref)->min);

    new_node->next = *head_ref;
    *head_ref = new_node;
}
int minimum(struct node *head){
    return head->min;
}

int pop(struct node **head_ref){
    int pop_data = (*head_ref)->data;
    (*head_ref) = (*head_ref)->next;
    return pop_data;
}

void printList(node *head){
    while(head != NULL){
        printf("%d->", head->data);
        head = head->next;
    }
    printf("\b\n");
}

int main(){
    struct node* a = NULL;

    push(&a, 100);
    push(&a, 24);
    push(&a, 16);
        push(&a, 19);
    push(&a, 50);
    printList(a);
    printf("Minimum is:%d\n", minimum(a));
    printf("Popped:%d\n",pop(&a));
    printf("Minimum is:%d\n", minimum(a));
    printf("Popped:%d\n",pop(&a));
    printf("Minimum is:%d\n", minimum(a));
    printf("Popped:%d\n",pop(&a));
    printf("Minimum is:%d\n", minimum(a));
    printf("Popped:%d\n",pop(&a));
    printf("Minimum is:%d\n", minimum(a));
}
