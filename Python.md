# Python

### 1. 코드 레이아웃

#### 1.1. 들여쓰기
- 4칸의 스페이스를 사용합니다. (탭을 사용하지 않습니다.)

#### 1.2. 최대 줄 길이
- 한 줄은 79자를 넘지 않도록 합니다.

#### 1.3. 빈 줄
- 최상위 함수 및 클래스 정의 사이에는 두 줄을 띄웁니다.
- 클래스 내부의 메서드 정의 사이에는 한 줄을 띄웁니다.

```python
class MyClass:
    def method_one(self):
        pass

    def method_two(self):
        pass


def function_one():
    pass


def function_two():
    pass
```

### 2. 들여쓰기 및 연속된 코드 줄

#### 2.1. 가로로 긴 표현식
- 가로로 긴 표현식은 괄호로 묶어서 여러 줄에 걸쳐 작성할 수 있습니다.

```python
def long_function_name(
        var_one, var_two, var_three,
        var_four):
    print(var_one)
```

#### 2.2. 백슬래시를 사용한 줄 바꿈
- 백슬래시를 사용해 줄을 바꿀 수 있지만, 가독성을 위해 권장되지 않습니다.

```python
with open('/path/to/some/file/you/want/to/read') as file_1, \
     open('/path/to/some/file/being/written', 'w') as file_2:
    file_2.write(file_1.read())
```

### 3. 공백 사용

#### 3.1. 연산자 주변의 공백
- 연산자 앞뒤에 한 칸의 공백을 둡니다.

```python
x = 1 + 2
y = x * 3
```

- 인자 목록의 콤마 뒤에는 한 칸의 공백을 둡니다.

```python
def my_function(a, b, c):
    return a + b + c
```

#### 3.2. 괄호, 대괄호, 중괄호 내부의 공백
- 괄호, 대괄호, 중괄호 내부에는 공백을 두지 않습니다.

```python
my_list = [1, 2, 3]
my_dict = {'key': 'value'}
```

#### 3.3. 콜론과 쉼표 뒤의 공백
- 콜론(:)과 쉼표(,) 뒤에는 공백을 둡니다.

```python
if x == 4: print(x, y); x, y = y, x
```

### 4. 주석

#### 4.1. 블록 주석
- 블록 주석은 코드와 같은 들여쓰기를 사용하여 작성합니다. 각 줄의 주석 앞에 `#`을 붙입니다.

```python
# 이 함수는 두 수를 더합니다.
def add(a, b):
    return a + b
```

#### 4.2. 인라인 주석
- 인라인 주석은 코드와 주석 사이에 최소 두 칸의 공백을 둡니다.

```python
x = x + 1  # x에 1을 더합니다.
```

### 5. 이름 규칙

#### 5.1. 변수와 함수 이름
- 소문자와 밑줄을 사용합니다.

```python
my_variable = 10

def my_function():
    pass
```

#### 5.2. 클래스 이름
- CamelCase를 사용합니다.

```python
class MyClass:
    pass
```

#### 5.3. 상수 이름
- 모두 대문자를 사용하고, 단어 사이는 밑줄로 구분합니다.

```python
PI = 3.14
MAX_SIZE = 100
```

### 6. 문자열

#### 6.1. 작은 따옴표와 큰 따옴표
- 작은 따옴표(`'`) 또는 큰 따옴표(`"`) 중 하나를 선택하여 일관되게 사용합니다.

```python
string1 = "Hello, world"
string2 = 'Python'
```

#### 6.2. 멀티라인 문자열
- 트리플 따옴표(`"""` 또는 `'''`)를 사용합니다.

```python
multi_line_string = """This is a
multi-line string."""
```

### 7. Docstring

- 함수, 클래스, 모듈에 대한 설명은 Docstring을 사용합니다. Docstring은 함수, 클래스, 모듈의 첫 번째 줄에 위치해야 합니다.
- Google 스타일과 NumPy 스타일 중 하나를 선택하여 사용합니다.

**Google 스타일**:
```python
def fetch_data(path: str) -> dict:
    """
    데이터 파일에서 데이터를 로드합니다.

    Args:
        path (str): 데이터 파일의 경로

    Returns:
        dict: 로드된 데이터
    """
    pass
```

**NumPy 스타일**:
```python
def fetch_data(path: str) -> dict:
    """
    데이터 파일에서 데이터를 로드합니다.

    Parameters
    ----------
    path : str
        데이터 파일의 경로

    Returns
    -------
    dict
        로드된 데이터
    """
    pass
```

### 8. import문

- import문은 항상 파일의 최상단에 위치합니다.
- import 순서는 표준 라이브러리, 서드 파티 라이브러리, 로컬 라이브러리 순으로 합니다.

```python
import os
import sys

import numpy as np
import pandas as pd

from my_module import my_function
```
