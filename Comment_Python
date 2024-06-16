#Comment: Python

### 1. 블록 주석

블록 주석은 코드의 특정 섹션이나 블록에 대한 설명을 제공하는 주석입니다. 여러 줄에 걸쳐 작성할 수 있으며, 각 줄 앞에 `#`을 붙입니다.

#### 작성 방법
- 블록 주석은 설명하는 코드와 같은 들여쓰기를 사용합니다.
- 각 줄 앞에 `#`을 붙이고, 주석 내용을 작성합니다.

#### 예시
```python
# 이 함수는 두 수를 더하고 결과를 반환합니다.
# 인자:
#     a (int): 첫 번째 숫자
#     b (int): 두 번째 숫자
# 반환값:
#     int: 두 수의 합
def add(a, b):
    return a + b
```

### 2. 인라인 주석

인라인 주석은 코드의 특정 라인에 대한 설명을 제공합니다. 주로 코드의 오른쪽에 위치하며, 코드와 주석 사이에 최소 두 칸의 공백을 둡니다.

#### 작성 방법
- 주석은 코드의 오른쪽에 위치합니다.
- 코드와 주석 사이에 최소 두 칸의 공백을 둡니다.

#### 예시
```python
x = x + 1  # x에 1을 더합니다.
y = x * 2  # x를 2배로 곱합니다.
```

### 3. 독스트링 (Docstring)

독스트링은 함수, 클래스, 모듈에 대한 설명을 제공합니다. 이는 해당 객체의 첫 번째 줄에 위치하며, 주로 삼중 따옴표(`"""` 또는 `'''`)로 묶습니다. 독스트링은 IDE나 도구에서 자동으로 인식되어 도움말로 제공됩니다.

#### 작성 방법
- 독스트링은 삼중 따옴표(`"""` 또는 `'''`)로 묶습니다.
- 첫 번째 줄에는 짧은 요약을 작성하고, 필요에 따라 두 번째 줄부터 상세 설명을 작성합니다.
- Google 스타일, NumPy 스타일 등 다양한 스타일을 사용할 수 있습니다.

#### Google 스타일 예시
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

#### NumPy 스타일 예시
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

### 4. 주석 작성 가이드라인

주석을 작성할 때에는 다음의 가이드라인을 따릅니다:

- **명확성**: 주석은 명확하고 이해하기 쉽게 작성해야 합니다.
- **간결성**: 불필요한 내용을 피하고, 간결하게 작성합니다.
- **관련성**: 주석은 관련된 코드 블록에 대한 설명만 포함해야 합니다.
- **업데이트**: 코드가 변경될 때마다 주석도 함께 업데이트해야 합니다.

### 5. 주석 작성 예시

#### 함수 주석
```python
def calculate_area(radius):
    """
    주어진 반지름을 사용하여 원의 면적을 계산합니다.

    Parameters
    ----------
    radius : float
        원의 반지름

    Returns
    -------
    float
        원의 면적
    """
    return 3.14 * radius ** 2
```

#### 클래스 주석
```python
class MyClass:
    """
    이 클래스는 예제 클래스입니다.

    Attributes
    ----------
    attribute1 : str
        첫 번째 속성
    attribute2 : int
        두 번째 속성
    """

    def __init__(self, attribute1, attribute2):
        """
        MyClass의 생성자

        Parameters
        ----------
        attribute1 : str
            첫 번째 속성
        attribute2 : int
            두 번째 속성
        """
        self.attribute1 = attribute1
        self.attribute2 = attribute2
```

#### 모듈 주석
```python
"""
이 모듈은 예제 모듈입니다.

모듈은 여러 함수와 클래스를 포함할 수 있습니다.
"""

def module_function():
    """
    이 함수는 모듈 내의 예제 함수입니다.
    """
    pass
```

### 주석 예제

다양한 주석 유형을 포함한 코드 예제입니다:

```python
# 이 함수는 주어진 목록에서 짝수를 반환합니다.
def get_even_numbers(numbers):
    """
    주어진 목록에서 짝수를 반환합니다.

    Parameters
    ----------
    numbers : list
        정수의 목록

    Returns
    -------
    list
        짝수로 구성된 목록
    """
    even_numbers = []  # 짝수를 저장할 목록

    for number in numbers:
        if number % 2 == 0:
            even_numbers.append(number)  # 짝수인 경우 목록에 추가

    return even_numbers

# 프로그램의 진입점
if __name__ == "__main__":
    sample_numbers = [1, 2, 3, 4, 5, 6]
    print(get_even_numbers(sample_numbers))  # [2, 4, 6]을 출력
```
