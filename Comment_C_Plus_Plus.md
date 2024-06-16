# Comment: C Plus Plus

### 파일 주석
파일의 시작 부분에 파일의 목적, 작성자, 작성일 등을 기록합니다.
```cpp
/**
 * @file filename.h
 * @brief Brief description of the file's purpose.
 *
 * Detailed description of what the file does, its functionality, and any other 
 * relevant information.
 * 
 * @author Author Name
 * @date YYYY-MM-DD
 */
```

### 클래스 주석
클래스 정의 앞에 클래스의 목적과 사용 방법을 설명합니다.
```cpp
/**
 * @class ClassName
 * @brief Brief description of the class.
 *
 * Detailed description of the class, its purpose, and any important details about 
 * how to use it.
 */
```

### 함수 주석
함수 정의 앞에 함수의 역할, 매개변수, 반환 값 등을 설명합니다.
```cpp
/**
 * @brief Brief description of the function.
 *
 * Detailed description of the function, its purpose, and how it works. 
 * Additional information such as side effects or exceptions thrown.
 *
 * @param[in] param1 Description of the first parameter.
 * @param[in] param2 Description of the second parameter.
 * @return Description of the return value.
 */
```

### 멤버 변수 주석
클래스 멤버 변수 선언 시 변수의 목적과 용도를 설명합니다.
```cpp
class MyClass {
    /**
     * @brief Brief description of the member variable.
     *
     * Detailed description of what the member variable is used for, any constraints, 
     * and important information.
     */
    int m_memberVariable;
};
```

### 인라인 주석
코드의 중요한 부분이나 복잡한 로직을 설명하는 주석을 적절히 추가합니다.
```cpp
void MyClass::SomeFunction() {
    int value = 42;  // Initialize value with the answer to life, universe, and everything.

    // Loop through each element in the container.
    for (const auto& element : container) {
        ProcessElement(element);  // Process each element.
    }
}
```

### TODO 주석
나중에 수정할 부분이나 추가할 기능에 대해서는 `TODO:` 주석을 남깁니다.
```cpp
void MyClass::UnfinishedFunction() {
    // TODO: Implement the logic for this function.
}
```

### 주석 예제 통합
아래는 위의 모든 주석 스타일을 통합한 예제입니다.
```cpp
/**
 * @file example.h
 * @brief This file contains the definition of the Example class.
 *
 * The Example class demonstrates how to write detailed comments in C++. 
 * It includes file-level, class-level, and function-level comments.
 * 
 * @author John Doe
 * @date 2024-06-16
 */

#ifndef EXAMPLE_H
#define EXAMPLE_H

/**
 * @class Example
 * @brief This class provides an example of detailed C++ comments.
 *
 * The Example class serves as a demonstration for how to properly document 
 * a C++ class and its members.
 */
class Example {
public:
    /**
     * @brief Default constructor.
     *
     * Initializes a new instance of the Example class.
     */
    Example();

    /**
     * @brief Computes the sum of two integers.
     *
     * This function takes two integers as input and returns their sum.
     *
     * @param[in] a The first integer.
     * @param[in] b The second integer.
     * @return The sum of the two integers.
     */
    int Add(int a, int b) const;

private:
    /**
     * @brief Stores an integer value.
     *
     * This member variable holds an integer value used in the Example class.
     */
    int m_value;
};

#endif // EXAMPLE_H
```
