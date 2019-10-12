# metaprogramming
```
//It's perfectly possible to template a class on an integer rather than a type. We can assign the templated value to a variable, or otherwise manipulate it in a way we might with any other integer literal:

unsigned int x = N;
//In fact, we can create algorithms which evaluate at compile time (from Wikipedia):

template <int N>
struct Factorial 
{
     enum { value = N * Factorial<N - 1>::value };
};

template <>
struct Factorial<0> 
{
    enum { value = 1 };
};

// Factorial<4>::value == 24
// Factorial<0>::value == 1
void foo()
{
    int x = Factorial<4>::value; // == 24
    int y = Factorial<0>::value; // == 1
}
```
---
# constexpr
