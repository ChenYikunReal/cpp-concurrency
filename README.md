# C++多线程编程

1.派生4个线程，分别打印问候消息：
```cpp
#include <iostream>
#include <vector>
#include <cstdint>
#include <thread>

using namespace std;

void say_hello(uint64_t id) {
    cout << "Hello from thread: " << id << endl;
}

int main() {
    const uint64_t num_threads = 4;
    vector<thread> threads;
    for (uint64_t id = 0; id < num_threads; id++) {
        threads.emplace_back(say_hello, id);
    }
    for (auto& thread : threads) {
        thread.join();
    }
    return 0;
}
```

2.迭代计算第n个Fibonacci数的基本函数模板
```cpp
template <typename value_t, typename index_t>
value_t fibonacci(value_t n) {
    value_t a_0 = 0;
    value_t a_1 = 1;
    for (index_t index = 0; index < n; index++) {
        const value_t temp = a_0;
        a_0 = a_1;
        a_1 += temp;
    }
}
```

```cpp

```

```cpp

```

```cpp

```

```cpp

```

```cpp

```

```cpp

```

```cpp

```

```cpp

```
