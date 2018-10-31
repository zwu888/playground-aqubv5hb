# description: 
 There can only be one function with the same signature. Altering the cv qualification of parameters does not change the function signature.  Therefore the two foo functions have the same signature and the program is ill-formed.

```C++ runnable
#include <iostream>

int foo(int x, int y)
{
  return x+y;
}

int foo(const int x, const int y)
{
  return x+y+1;
}

int main(int argc, char** argv)
{
  const int x = 3;
  const int y = 2;

  std::cout << foo(x,y) << std::endl;

  return 0;
}
