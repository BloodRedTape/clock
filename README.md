# Simple to use std::chrono wrapper
## Inspired by SFML Clock
### Example
```c++

#include <iostream>
#include "clock.hpp"

int main(){
    Clock clock; // here clock starts

    // Long code...

    float seconds = clock.GetElapsedTime().AsSeconds();
    std::cout << "Long code took " << seconds << "seconds" << std::endl; 
}

```

### Reuse clock
```c++

#include <iostream>
#include "clock.hpp"

int main(){
    Clock clock; // here clock starts

    // First piece of long code...

    float seconds = clock.GetElapsedTime().AsSeconds();
    std::cout << "First piece of long code " << seconds << "seconds" << std::endl; 

    //reset clock to 0
    clock.Reset();

    // Second piece of long code...

    int64_t nanoseconds = clock.GetElapsedTime().AsNanoseconds();
    std::cout << "Second piece of long code " << nanoseconds << "nanoseconds" << std::endl; 


}

```
