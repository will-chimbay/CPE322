# CPE322
## My name is **William Chimbay**, 

*Welcome to my repo, I'm a third year Computer Engineering major*

> Here we'll engange in working on:
> - coding assignments
> - developing projects
> - and miscelaneous tomfoolery
---
[TESTING A LINK](https://github.com/will-chimbay/CPE322/tree/main)
---
LIST OF ITEMS TO INCLUDE | Assignment 0
1. heading
2. bold
3. italic
4. block quote
5. ordered list
6. unordered list
7. `code` (see below)
8. horizontal rule
9. link
10. image (see below)

## Image of an image of an image:
<img width="408" alt="image" src="https://github.com/will-chimbay/CPE322/assets/123396327/71ff2caf-d991-430f-be0e-5fec476735d1">

## CODE (ex. of array manipulation):
```
int countEvens(int x[], int n)
{
    int count = 0;
    for(int i = 0; i < n; i++)
    {
        if( x[i] % 2 == 0)
        {
            count ++;
        }
    }    
    return count;
}
void addToEach(float x[], int n, float delta)
{
    for(int i = 0; i < n; i++)
    {
        x[i] = x[i] + delta;
    }
}
void range_reverse(int x[], int n, int a, int b)
{
    for(int i = 0; i < n; i++)
    {
        if(x[i] == a)
        {
            x[i] = b;
        }
        else if(x[i] == b)
        {
            x[i] = a;
        }
    }
}
void compact(int x[], int n, int a, int b)
{
    int i, j;
    for (i = 0, j = 0; i < n; i++) 
    {
        if (i < a || i > b) 
        {
            x[j++] = x[i];
        }
    }
    for (; j < n; j++) 
    {
        x[j] = 0;
    }
}

int main() {
    // example for bit operation
    cout << "Question 1-----------------------------------" << endl;
    int arr1[] = {1,2,3,4,5,6,7,8,9,10};
    int res1 = countEvens(arr1, sizeof(arr1) / sizeof(int));
    cout << "# even numbers: " << res1 << endl;
    cout << "Question 2-----------------------------------" << endl;
    float arr2[] = {1.0, 2.0, 3.0, 4.0};
    float delta = 0.5;
    addToEach(arr2, sizeof(arr2) / sizeof(arr2[0]), delta);
    cout << "array after added delta is:" << endl;
    for (auto a: arr2) {
        cout << a << ", ";
    }
    cout << endl;
    cout << "Question 3-----------------------------------" << endl;
    int arr3[] = {1,2,3,4,5,6,7,8,9,10};
    range_reverse(arr3, sizeof(arr3) / sizeof(int), 1, 4); // reverse element between index 1 and 4, -> 1,5,4,3,2,6,7,8,9,10
    cout << "array after range reverse is:" << endl;
    for (auto a: arr3) {
        cout << a << ", ";
    }
    cout << endl;
    cout << "Question 4-----------------------------------" << endl;
    int arr4[] = {1,2,3,4,5,6,7,8,9,10};
    compact(arr4, sizeof(arr4) / sizeof(int), 1, 4);
    cout << "array after compact is:" << endl; // after compact, array should be 1,6,7,8,9,10,0,0,0,0
    for (auto a: arr4) {
        cout << a << ", ";
    }
    cout << endl;
    return 0;
}
```

> [NOTE!]
>
> *this ReadMe will be updated frequently*
