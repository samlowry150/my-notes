# Project: *A ball that falls down.*
### 1: try to create a animation of a ball that is falling towards the ground with a set speed.
*hint: y +=1;*
### 2: change the animation so that the ball is rising towards the sky.
*hint:y += -1;*

# Global and local variables
- Global variables can be used from anywhere within the program. 
- local variables can typically only be used from within the scope they were defined.

# POST increment and PRE increment.

```
void setup() {
  int a = 2;
  println(a++); // prints 2
  println(++a); // prints 4
}
```

**Post-increment (a++):** In post-increment, the value of the variable is first used in the expression, and then it is incremented. So, the current value of the variable is used, and then the variable is incremented by 1.

**Pre-increment (++a):** In pre-increment, the variable is incremented first, and then its value is used in the expression. So, the variable is incremented by 1, and then its updated value is used in the expression.

- [[NO.12]]
