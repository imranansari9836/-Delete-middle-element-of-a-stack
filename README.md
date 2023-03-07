# -Delete-middle-element-of-a-stack
#Delete middle element of a stack
Input: 
Stack = {1, 2, 3, 4, 5}
Output:
ModifiedStack = {1, 2, 4, 5}


class Solution
{
    //Function to delete middle element of a stack.
    public void deleteMid(Stack<Integer>s,int sizeOfStack){
        // code here
        if(s.size()==Math.ceil((sizeOfStack+1)/2))
        {
            s.pop();
            return;
        }
        //Remove current item
        int x=s.pop();
        //Remove other elements
        deleteMid(s,sizeOfStack);
        s.push(x);
    } 
}
