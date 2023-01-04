#https://leetcode.com/problems/evaluate-reverse-polish-notation/
#150. Evaluate Reverse Polish Notation

#include <bits/stdc++.h>
using namespace std;

int evaluatePosFxExpression(string exp)
{

    stack<int> st;

    for (int i = 0; i < exp.size(); i++)
    {
        char ch = exp[i];

        // If c is a digit
        if (ch >= '0' && ch <= '9')
        {

            int temp = (int)(ch - '0');
            st.push(temp);
        }
        // Otherwise it is an operator.
        else
        {

            int op1 = st.top();
            st.pop();

            int op2 = st.top();
            st.pop();

            switch (ch)
            {
            case '+':
                st.push(op2 + op1);
                break;
            case '-':
                st.push(op2 - op1);
                break;
            case '*':
                st.push(op2 * op1);
                break;
            case '/':
                st.push(op2 / op1);
                break;
            }
        }
    }

    return st.top();
}

// Main function
int main()
{

    string expression;
    cin>>expression;

    cout << evaluatePosFxExpression(expression) << endl;
}
