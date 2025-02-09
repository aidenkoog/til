# Expected Questions

Organized expected questions & answers

## Algorithm

- 알고리즘 정의와 특징을 설명
    - 정의: 알고리즘(Algorithm)은 주어진 문제를 해결하기 위한 일련의 절차나 규칙의 집합
    - 특징
        - 명확성 (Definiteness): 각 단계는 정확하고 모호함이 없어야 한다
        - 입력 (Input): 0개 이상의 입력이 존재한다
        - 출력 (Output): 최소한 1개 이상의 결과(출력)가 있어야 한다
        - 유한성 (Finiteness): 유한한 단계 내에 종료해야 한다.
        - 효율성 (Effectiveness): 모든 연산이 기계적으로 수행 가능해야 한다.

- 알고리즘의 성능을 평가하는 기준
    - 시간 복잡도(Time Complexity)
        - 알고리즘이 수행하는 연산의 개수를 측정하여 입력 크기에 따른 실행 시간 증가율을 평가한다.
        - 일반적으로 Big-O 표기법을 사용해 표현한다.
    - 공간 복잡도(Space Complexity)
        - 알고리즘이 실행될 때 필요한 메모리 사용량을 평가한다.
        - 추가적인 데이터 구조(배열, 리스트, 스택 등)가 필요한 경우 공간 복잡도가 증가할 수 있다.

- 시간 복잡도(Time Complexity)와 공간 복잡도(Space Complexity)의 차이점 설명
    - 시간 복잡도는 알고리즘이 실행되는 시간의 효율성을 평가하는 개념
        - 입력 크기(n)가 증가할 때 연산 횟수가 어떻게 변하는지 분석한다.
    - 공간 복잡도는 알고리즘이 실행되는 동안 사용하는 메모리 공간을 분석하는 개념이다.
    - 예시
        - 선형 탐색(Linear Search)
            - 시간복잡도: O(n), 공간복잡도: O(1)
        - 이진 탐색(Binary Search)
            - 시간복잡도: O(logn), 공간복잡도: O(1)
        - 병합 정렬(Merge Sort)
            - 시간복잡도: O(nlogn), 공간복잡도: O(n)
        - 퀵 정렬(Quick Sort)
            - 시간복잡도: O(nlogn)(평균), 공간복잡도: O(logn)

- Big-O 표기법과 주요 Big-O 표기법 예제 설명
    - Big-O 표기법: 알고리즘의 시간 복잡도를 표현하는 수학적 표기법으로, 입력 크기(n)에 따른 실행 시간 증가율을 나타낸다.
    - 주요 Big-O 표기법 예제
        - O(1) / 상수 시간 / 배열 인덱스 접근
        - O(log n) / 로그 시간 / 이진 탐색
        - O(n) / 선형 시간 / 선형 탐색
        - O(n log n) / 로그 선형 시간 / 병합 정렬, 퀵 정렬(평균)
        - O(n²) / 이차 시간 / 버블 정렬, 삽입 정렬
        - O(2ⁿ) / 지수 시간 / 피보나치 수열(재귀)

- Best case, Worst case, Average case의 개념과 차이점을 설명
    - Best Case
        - 가장 이상적인 상황에서 알고리즘이 실행되는 경우
        - 예: 이진 탐색(Binary Search)에서 찾으려는 값이 첫 번째 요소에 있는 경우 → O(1)
            - 정렬된 배열에서 임의의 중간값을 찾고자 하는 값과 비교하여 좌측 또는 우측을 대상으로 탐색을 하는 알고리즘
            - 임의의 중간값 선정 후 찾고자 하는 값 비교 과정을 계속 반복한다
    - Worst Case
        - 가장 나쁜 상황에서 알고리즘이 실행되는 경우
        - 예: 선형 탐색(Linear Search)에서 찾는 값이 배열의 마지막 요소에 있는 경우 → O(n)
            - 배열이나 리스트에서 특정 값을 찾기 위해 처음부터 끝까지 하나씩 순차적으로 확인하는 탐색 알고리즘
    - Average Case
        - 모든 가능한 입력에 대한 평균적인 수행 시간
        - 예: 퀵 정렬(Quick Sort)에서 랜덤한 피벗 선택 → O(n log n)

- 시간 복잡도가 O(n)인 알고리즘과 O(n²)인 알고리즘의 차이를 실제 사례와 함께 설명
    - O(n) 알고리즘 예시 (선형 탐색)
        ```python
        def linear_search(arr, target):
        for i in range(len(arr)):
            if arr[i] == target:
                return i
        return -1
        ```
    - O(n²) 알고리즘 예시 (버블 정렬)
        ```python
        def bubble_sort(arr):
            n = len(arr) # example: [5, 4, 1, 2, 9]
            for i in range(n): # n = 5
                for j in range(0, n - i - 1): # 0, 4, 0, 3, 0, 2
                    if arr[j] > arr[j + 1]: #arr[0] > arr[1]
                        arr[j], arr[j + 1] = arr[j + 1], arr[j] #arr[0], arr[1] = arr[1], arr[0], swap
        ```
        - 알고리즘 분석
            - 예: [5,4,1,2,9]라 가정할 때 전체 아이템 개수만큼 반복문을 돈다.
            - Set 1 (0,4), 1세트가 끝나면 가장 큰 수는 배열의 맨뒤에 위치하게 된다.
                - 1) [4,5,1,2,9]
                - 2) [4,1,5,2,9]
                - 3) [4,1,2,5,9]
                - 4) [4,1,2,5,9] 
            - Set 2 (0,3)
                - 1) [1,4,2,5,9]
                - 2) [1,2,4,5,9]
                - 3) [1,2,4,5,9]
            - Set 3 (0,2)
            - Set 4 (0,1)
    - 차이점
        - O(n) 알고리즘은 데이터 크기가 증가해도 비교적 빠르게 실행되지만, O(n²) 알고리즘은 입력 크기가 커질수록 실행 속도가 매우 느려진다.

- 분할 정복(Divide and Conquer) 기법과 주요 예제 제시
    - 개요
        - 큰 문제를 작은 문제로 나누어 해결한 후, 이를 합쳐서 최종 결과를 얻는 알고리즘 설계 기법
    - 핵심 개념
        - 분할(Divide): 문제를 더 작은 부분 문제(subproblems)로 나눈다
        - 정복(Conquer): 나눠진 작은 문제를 해결한다
        - 병합(Combine): 해결한 작은 문제들을 합쳐서 최종 해결책을 도출한다
        - 이 방식은 재귀(Recursion)를 많이 활용하며, 복잡한 문제를 해결하는 데 자주 사용됨
    - 분할정복 사용되는 대표적인 알고리즘
        - 병합 정렬 (Merge Sort) / O(n log n) / 배열을 반으로 나눈 후 정렬하여 합침
        - 퀵 정렬 (Quick Sort) / 평균 O(n log n) / 피벗을 기준으로 분할 후 정렬
        - 이진 탐색 (Binary Search)	/ O(log n) / 정렬된 배열을 반씩 나누며 탐색
        - 최근접 점 쌍 문제 (Closest Pair of Points) / O(n log n) / 좌표평면에서 가장 가까운 두 점을 찾음
        - 스트라센 행렬 곱셈 (Strassen’s Matrix Multiplication) / O(n².⁸) / 일반 행렬 곱셈보다 빠름
        - FFT(Fast Fourier Transform) / O(n log n) / 푸리에 변환을 빠르게 수행
    - 분할 정복(DC) 기법의 장점과 단점
        - 장점
            - 복잡한 문제 해결 가능
                - 정렬, 탐색, 행렬 연산 등에서 효율적인 해결 방법을 제공함.
            - 병렬 처리(Parallel Processing)에 유리함
                - 작은 문제를 독립적으로 해결할 수 있어 병렬 연산이 가능함.
            - 빠른 실행 속도
                - 정렬 알고리즘(병합 정렬, 퀵 정렬) 등에서 O(n log n) 성능을 제공.
        - 단점
            - 재귀(Recursion)로 인한 함수 호출 비용 발생
                - 스택 오버플로우(Stack Overflow) 위험 있음
            - 추가적인 메모리 사용
                - 병합 정렬처럼 새로운 배열을 사용하면 O(n) 추가 공간이 필요할 수도 있음.
            - 피벗 선택이 중요한 경우(퀵 정렬)
                - 잘못된 피벗을 선택하면 최악의 경우 O(n²) 성능이 될 수 있음.
    - 분할 정복(DC) 주요 예제
        - 병합정렬
            - 정의: 병합 정렬은 배열을 계속 반으로 나눈 후(Divide), 각각 정렬한 후 병합(Conquer & Combine)하는 정렬 알고리즘
            - 병합 정렬의 과정
                - 배열을 절반으로 계속 나눈다.
                - 크기가 1이 되면 정렬된 상태로 간주한다.
                - 나눠진 두 개의 정렬된 배열을 하나로 합친다(병합).
            - 병합 정렬 코드 예시
                ```python
                def merge_sort(arr):
                    if len(arr) <= 1:
                        return arr  # 원소가 1개 이하이면 그대로 반환

                    # 1. 분할 (Divide)
                    mid = len(arr) // 2
                    # 0부터 mid-1까지의 요소, 0,1,2
                    left_half = merge_sort(arr[:mid])
                    # mid부터 끝까지의 요소, 3,4,5,6
                    right_half = merge_sort(arr[mid:])
                    # 2. 정복 & 병합 (Conquer & Combine)
                    return merge(left_half, right_half)

                def merge(left, right):
                    result = []
                    i = j = 0

                    # 두 리스트를 정렬된 순서대로 병합
                    while i < len(left) and j < len(right):
                        if left[i] < right[j]:
                            result.append(left[i])
                            i += 1
                        else:
                            result.append(right[j])
                            j += 1

                    # 남은 원소 추가
                    result.extend(left[i:])
                    result.extend(right[j:])
                    return result

                    # 사용 예제 (Entry Point)
                    arr = [38, 27, 43, 3, 9, 82, 10]
                    sorted_arr = merge_sort(arr)
                    print(sorted_arr)
                ```
        - 퀵정렬
            - 정의: 퀵 정렬은 피벗(Pivot)을 설정하고, 이를 기준으로 작은 값과 큰 값으로 나눈 뒤 각각 정렬하는 방식
            - 퀵 정렬의 과정
                - 피벗(Pivot)을 설정한다.
                - 피벗보다 작은 값은 왼쪽, 큰 값은 오른쪽으로 정렬한다.
                - 각각을 다시 퀵 정렬로 정렬한다.
            - 퀵 정렬 코드 예시
                ```python
                def quick_sort(arr):
                if len(arr) <= 1:
                    return arr  # 원소가 1개 이하이면 그대로 반환

                pivot = arr[len(arr) // 2]  # 피벗 설정 (중간값)
                left = [x for x in arr if x < pivot]  # 피벗보다 작은 값
                middle = [x for x in arr if x == pivot]  # 피벗과 같은 값
                right = [x for x in arr if x > pivot]  # 피벗보다 큰 값

                return quick_sort(left) + middle + quick_sort(right)  # 재귀 호출

                # 사용 예제 (Entry Point)
                arr = [38, 27, 43, 3, 9, 82, 10]
                sorted_arr = quick_sort(arr)
                print(sorted_arr)

                # 참고 List Comprehension 다른 표현
                [x for x in arr if x < pivot]

                result = []
                for x in arr:
                    if x < pivot:
                        result.append(x)
                ```
        - 이진탐색
            - 정의: 이진 탐색은 정렬된 배열에서 탐색 범위를 반씩 줄여가며 값을 찾는 알고리즘 (반씩 줄이는 과정을 반복)
            - 이진 탐색의 과정
                - 배열의 중간값과 찾으려는 값을 비교한다.
                - 같으면 찾은 것이고, 크면 왼쪽 부분을 탐색, 작으면 오른쪽 부분을 탐색한다.
                - 이 과정을 찾을 때까지 반복한다.
            - 이진탐색 코드 예시
                ```python
                # 기준 인덱스를 계속 변화시키면서 값을 찾는 방식
                def binary_search(arr, target):
                    left, right = 0, len(arr) - 1
                    while left <= right:
                        mid = (left + right) // 2  # 중간값 찾기
                        if arr[mid] == target:
                            return mid  # 찾음
                        elif arr[mid] < target:
                            left = mid + 1  # 오른쪽 탐색
                        else:
                            right = mid - 1  # 왼쪽 탐색

                    return -1  # 못 찾음

                # 사용 예제 (정렬된 배열 필요, Entry Point)
                arr = [3, 9, 10, 27, 38, 43, 82]
                target = 27
                result = binary_search(arr, target)
                ```

- 동적 계획법(Dynamic Programming) 정의와 대표적 예제 제시
    - 정의: 큰 문제를 작은 문제로 나누어 해결한 후, 그 결과를 저장하여 동일한 문제를 다시 풀지 않도록 하는 최적화 기법
    - 핵심 개념
        - 최적 부분 구조 (Optimal Substructure)
            - 큰 문제를 작은 문제로 나누어 해결할 수 있어야 한다.
            - 예: 피보나치 수열에서 F(n) = F(n-1) + F(n-2)
        - 중복되는 부분 문제 (Overlapping Subproblems)
            - 동일한 작은 문제가 여러 번 반복해서 나타난다.
            - 예: F(5)를 구할 때 F(3)을 여러 번 계산하는 경우, F(5) = F(4) + F(3), F(4) 구할때도 F(3)에 대한 계산이 또 이루어짐
        - 메모이제이션 (Memoization) 또는 반복(Tabulation) 사용
            - 이미 계산한 결과를 저장하여 다시 계산하지 않도록 한다.
            - Dictionary 등에 이전 결과값 저장 후 사용
    - 동적 계획법 접근 방식
        - 탑다운(Top-Down) (재귀 + 메모이제이션)
            - 큰 문제를 작은 문제로 나누고, 결과를 저장하며 푸는 방식
        - 바텀업(Bottom-Up) (반복문 + 테이블 사용)
            - 작은 문제부터 차근차근 해결하여 큰 문제를 해결하는 방식
    - 대표적 동적 계획법 문제 예시
        - 피보나치 수열 (Fibonacci Sequence)
            - 피보나치 수열은 다음과 같이 정의: F(n) = F(n-1) + F(n-2)
            - 조건: F(0) = 0, F(1) = 1
            - 재귀 (일반적인 방법, 중복 계산이 많아 시간 복잡도 O(2ⁿ)로 매우 비효율적)
                ```python
                def fib(n):
                    if n <= 1: # 0, 1
                        return n
                    return fib(n-1) + fib(n-2)
                print(fib(10))  # 55
                ```
            - 동적 계획법 (탑다운: 메모이제이션 활용, 이전 결과를 memo에 저장하여 중복 계산을 방지하고 시간 복잡도: O(n) (한 번씩만 계산))
                ```python
                # 딕셔너리(해시 테이블)를 사용한 메모이제이션
                memo = {}
                def fib(n):
                    # 딕셔너리 내 값이 존재하면 재연산 없이 그대로 반환
                    if n in memo:
                        return memo[n]
                    # 0 또는 1이면 그대로 반환
                    if n <= 1:
                        return n
                    # 재귀 연산 후 반환되는 값 저장
                    memo[n] = fib(n-1) + fib(n-2)
                    return memo[n]
                print(fib(10))  # 55
                ```
            - 동적 계획법 (바텀업: 반복문 활용)
                - 코드 설명 및 추후 개선점 설명
                    - dp 테이블을 활용해 작은 문제부터 차근차근 해결 (반복문 사용)
                    - 메모리를 줄이려면 dp 배열 없이 변수 2개만 사용 가능 (O(1) 공간 사용 가능)
                    - 시간 복잡도: O(n) (반복문 한 번만 사용)
                ```python
                def fib(n):
                    dp = [0] * (n + 1)  # DP 테이블 초기화, 0으로 초기화
                    dp[1] = 1   # 0: 0(초기화), 1: 1
                    for i in range(2, n + 1):
                        dp[i] = dp[i-1] + dp[i-2]
                    return dp[n]
                print(fib(10))  # 55
                ```
            - 그외 대표적 동적 계획법(DP) 문제
                - 0-1 배낭 문제 (Knapsack Problem)
                    - 문제: 무게 제한이 있는 배낭에 최대 가치를 갖는 물건을 선택하여 넣는 문제
                    - 동적 계획법을 사용하여 해결 가능 (O(nW) 시간 복잡도)
                - 최장 공통 부분 수열 (LCS: Longest Common Subsequence)
                    - 문제: 두 문자열이 주어질 때, 가장 긴 공통 부분 수열의 길이를 구하는 문제
                    - 동적 계획법을 사용하여 해결 가능 (O(nm) 시간 복잡도)
    - DP vs DC (분할 정복(Divide and Conquer)) 비교
        - 동적 계획법 (DP)
            - 중복되는 부분 문제 해결 결과를 저장하여 재사용
            - 피보나치 수열, 배낭 문제, LCS
        - 분할 정복 (DC)
            - 문제를 더 작은 문제로 나누어 해결 후 병합
            - 병합 정렬, 퀵 정렬, 이진 탐색
        - DP는 "중복 계산이 많을 때" 분할 정복보다 효율적이다

- 알고리즘을 설계할 때 고려해야 할 요소 설명
    - 개요
      - 효율성, 정확성, 확장성 등의 다양한 요소를 고려해야 함
      - 이 요소들을 잘 고려해야 성능이 뛰어나고 유지보수가 쉬운 최적의 알고리즘 코딩 가능
    - 고려 필요 요소
      - 정확성 (Correctness)
        - 알고리즘이 모든 입력에 대해 정확한 결과를 도출해야 함
        - 모든 경우의 수를 고려하고, 예외 상황에서도 올바르게 동작하는지 확인해야 함
        - 예제 테스트 및 경계값 테스트를 통해 검증 필요
        - 예시
            - 정렬 알고리즘이 입력 배열을 항상 오름차순(또는 내림차순)으로 정렬하는지 확인
            - 숫자를 더하는 알고리즘에서 음수, 0, 큰 수 등 다양한 입력값에 대해 올바르게 동작하는지 테스트
      - 시간 복잡도 (Time Complexity)
        - 알고리즘이 실행되는 속도를 나타내는 지표
        - 입력 크기 n이 커질수록 실행 시간이 어떻게 변하는지 분석
        - Big-O 표기법으로 성능 평가
        - 예: O(1) < O(log n) < O(n) < O(n log n) < O(n²) < O(2ⁿ) < O(n!)
        - 예시
            - O(n²)인 버블 정렬보다 O(n log n)인 퀵 정렬을 사용하는 것이 효율적
            - 탐색할 데이터가 많을 경우 이진 탐색(O(log n))을 사용하면 선형 탐색(O(n))보다 빠름
      - 공간 복잡도 (Space Complexity)
        - 알고리즘이 실행될 때 필요한 메모리 사용량
        - 추가적인 데이터 구조(배열, 리스트, 해시맵 등)를 사용할 경우 메모리 효율성 고려
        - 인플레이스 알고리즘(in-place algorithm)을 사용하면 추가 공간 사용을 줄일 수 있음
        - 예시
            - 퀵 정렬은 평균적으로 O(log n)의 추가 공간이 필요하지만, 병합 정렬은 O(n)의 추가 공간이 필요
            - 피보나치 수열을 재귀(O(2ⁿ))로 계산하면 메모리 사용이 많아지므로 동적 계획법(DP, O(n))을 활용해 최적화 가능
      - 단순성 (Simplicity, Readability)
        - 코드는 명확하고 직관적으로 설계해야 함
        - 복잡한 알고리즘보다는 이해하기 쉽고 유지보수하기 쉬운 알고리즘이 바람직
        - 가독성이 좋은 변수명과 명확한 주석 작성
        - 예시
            - 한 줄로 압축한 복잡한 코드보다, 단계별로 설명이 잘 된 명확한 코드가 유지보수에 유리
            - 너무 많은 중첩된 반복문 대신 함수 분리 및 재사용성 고려
      - 확장성 (Scalability)
        - 입력 데이터가 커질 때 성능 저하 없이 확장 가능한지 고려
        - 데이터 크기가 100일 때와 1,000,000일 때의 성능 차이를 분석
        - 병렬 처리(멀티스레딩, GPU 가속 등) 가능성도 고려
        - 예시
            - 단일 서버에서 동작하는 알고리즘이 아닌, 분산 처리(Distributed Computing) 가능한 구조로 설계
            - 트래픽이 증가할 경우 부하 분산(Load Balancing)을 고려하여 알고리즘을 최적화
      - 재사용성 (Reusability)
        - 알고리즘이 다양한 문제에서도 재사용 가능하도록 일반화
        - 특정 문제에 한정된 알고리즘보다는 모듈화하여 여러 곳에서 활용 가능하도록 설계
        - 예시
            - 정렬 알고리즘을 특정 데이터 유형에 한정하지 않고, 범용적으로 사용할 수 있도록 제너릭(Generic) 함수로 구현
            - 재귀 알고리즘을 반복문으로 변환하여 재사용성을 높임
      - 경계값 & 예외 처리 (Edge Cases & Error Handling)
        - 알고리즘이 비정상적인 입력값에서도 안정적으로 동작하는지 확인
        - 입력값이 너무 크거나 작을 때, 음수, 빈 값 등을 고려하여 예외 처리 추가
        - 예시
            - 리스트가 비어 있을 때 오류 발생 방지 (if len(arr) == 0: 처리)
            - 입력값이 음수일 경우 처리 (if n < 0: 예외 처리)
      - 최적화 가능성 (Optimization)
        - 처음부터 최적의 알고리즘을 설계하기 어려우므로, 점진적인 최적화 과정 필요
        - 알고리즘이 실제 환경에서 병목현상(Bottleneck)이 발생하는 부분을 분석하고 개선
        - 예시
            - 정렬된 배열에서 선형 탐색(O(n)) 대신 이진 탐색(O(log n))을 활용
            - 메모이제이션(Memoization) 기법을 적용해 중복 계산 최소화

- 메모이제이션(Memoization) 셜명과 예제 기술
  - 설명
    - 이전에 계산한 결과를 저장하여, 동일한 연산을 반복하지 않도록 최적화하는 기법
    - 중복 계산을 줄여 알고리즘의 성능을 개선하는 방식으로, 주로 재귀 함수에서 사용
    - 핵심 개념
      - 이전에 계산한 값을 저장하여 중복 계산 방지
      - 재귀적 알고리즘(피보나치, 팩토리얼)에서 성능 최적화
      - 공간을 사용하여 시간을 절약 (시간 복잡도 감소)

- 다이나믹 프로그래밍(DP)과 분할 정복(D&C)의 차이점 서술
  - 차이점 개요
    - 모두 재귀적 접근 방식을 사용하는 알고리즘 기법
    - 문제 해결 방식과 중간 결과의 활용 방식에서 중요한 차이점 존재
  - 동적 계획법(Dynamic Programming, DP)
    - 정의
      - 큰 문제를 작은 문제로 나누어 해결하고, 중복되는 부분 문제의 결과를 저장하여 재사용하는 기법
      - 최적 부분 구조(Optimal Substructure)와 중복 부분 문제(Overlapping Subproblems) 특성을 가짐
    - 특징
	  - 중복된 계산을 피하기 위해 메모이제이션(Memoization) 또는 테이블(Tabulation) 기법 사용
      - 부분 문제의 해결 결과를 저장하여 재사용하는 것이 핵심.
	  - 주로 최적화 문제(Optimization Problems)에 사용됨
        - 최단 경로, 배낭 문제, LIS 등
  - 분할 정복(Divide and Conquer, D&C)
    - 정의
	  - 문제를 작은 문제로 나누고, 각각을 독립적으로 해결한 후, 결과를 조합하여 최종 결과를 얻는 방식
      - 최적 부분 구조(Optimal Substructure) 특성을 가짐
    - 특징
	  - 각 하위 문제가 독립적(Independent Subproblems)으로 해결됨
	  - 중복된 계산을 피하지 않음 → DP와 달리, 같은 부분 문제가 여러 번 계산될 수 있음
	  - 재귀적으로 하위 문제를 해결한 후, 최종적으로 합침(Merge 과정이 중요)
  - 결론
    - DP는 “중복 문제를 저장하고 재사용할 때”, D&C는 “독립적인 문제를 나눠 해결할 때” 사용한다

- 탐욕 알고리즘(Greedy Algorithm)이란 무엇인가? 장점과 단점을 설명하시오.
- 백트래킹(Backtracking) 기법이란 무엇인가? 예제를 설명하시오.
- 브루트 포스(Brute Force) 알고리즘의 개념과 장점, 단점을 설명하시오.
- NP-문제란 무엇인가? P vs NP 문제를 설명하시오.
- NP-완전(NP-Complete) 문제와 NP-난해(NP-Hard) 문제의 차이점을 설명하시오.
- 트레이드오프(Trade-off)란 무엇인가? 알고리즘 설계에서의 예제를 설명하시오.
- 버블 정렬(Bubble Sort)의 동작 방식과 시간 복잡도를 설명하시오.
- 선택 정렬(Selection Sort)의 동작 원리와 특징을 설명하시오.
- 삽입 정렬(Insertion Sort)의 과정과 시간 복잡도를 설명하시오.
- 병합 정렬(Merge Sort) 알고리즘의 개념과 적용 사례를 설명하시오.
- 퀵 정렬(Quick Sort)의 피벗 선택 방법과 성능에 미치는 영향을 설명하시오.
- 힙 정렬(Heap Sort)의 개념과 구현 방법을 설명하시오.
- 기수 정렬(Radix Sort)과 카운팅 정렬(Counting Sort)의 차이점을 설명하시오.
- 정렬 알고리즘의 안정성(Stable Sort)이란 무엇인가?
- O(n log n) 정렬 알고리즘을 비교하고 특징을 설명하시오.
- 비교 기반 정렬과 비비교 기반 정렬의 차이를 설명하시오.
- 선형 탐색(Linear Search)의 개념과 시간 복잡도를 설명하시오.
- 이진 탐색(Binary Search)의 개념과 구현 방법을 설명하시오.
- 깊이 우선 탐색(DFS)과 너비 우선 탐색(BFS)의 차이점을 설명하시오.
- DFS와 BFS가 각각 유리한 문제 유형을 설명하시오.
- 해시 테이블(Hash Table)의 구조와 충돌 해결 방법을 설명하시오.
- 해싱(Hashing)에서 충돌(Collision) 해결 방법을 설명하시오.
- 그래프의 정의와 주요 용어(정점, 간선, 가중치 등)를 설명하시오.
- 인접 행렬과 인접 리스트의 차이점을 설명하시오.
- 최단 경로 문제란 무엇인가? 대표적인 알고리즘을 설명하시오.
- 다익스트라(Dijkstra) 알고리즘의 개념과 적용 사례를 설명하시오.
- 벨만-포드(Bellman-Ford) 알고리즘의 개념과 한계를 설명하시오.
- 플로이드-워셜(Floyd-Warshall) 알고리즘의 개념과 활용 사례를 설명하시오.
- 최소 신장 트리(MST)란 무엇인가?
- 크루스칼(Kruskal) 알고리즘의 개념과 구현 방법을 설명하시오.
- 프림(Prim) 알고리즘과 크루스칼 알고리즘의 차이점을 설명하시오.
- KMP(Knuth-Morris-Pratt) 문자열 검색 알고리즘의 개념과 구현 방법을 설명하시오.
- 보이어-무어(Boyer-Moore) 알고리즘의 특징과 시간 복잡도를 설명하시오.
- 라빈-카프(Rabin-Karp) 알고리즘의 원리와 적용 사례를 설명하시오.
- 접미사 배열(Suffix Array)의 개념과 활용 방안을 설명하시오.
- 애너그램(Anagram) 검사 알고리즘을 구현하는 방법을 설명하시오.
- A* (A-Star) 알고리즘의 개념과 활용 사례를 설명하시오.
- 네트워크 플로우(Network Flow) 알고리즘의 개념과 적용 사례를 설명하시오.
- 최대 유량 문제(Maximum Flow Problem)란 무엇인가?
- 포드-풀커슨(Ford-Fulkerson) 알고리즘의 개념과 구현 방법을 설명하시오.
- 최소 컷(Minimum Cut) 문제란 무엇인가?
- P vs NP 문제란 무엇이며, 현재 연구 동향을 설명하시오.
- 밀러-라빈(Miller-Rabin) 소수 판별법이란 무엇인가?
- 서포트 벡터 머신(Support Vector Machine)의 개념과 활용 방안을 설명하시오.
- 다중 집합(Multiset) 문제를 해결하는 방법을 설명하시오.
- 분수 Knapsack 문제와 0-1 Knapsack 문제의 차이를 설명하시오.
- 트리(Tree) 자료구조에서 DFS와 BFS의 차이점을 설명하시오.
- 페르마의 소정리(Fermat’s Little Theorem)란 무엇인가?
- RSA 암호화 알고리즘에서 소수를 이용하는 이유를 설명하시오.
- 스택(Stack)과 큐(Queue)의 차이점을 설명하시오.
- 덱(Deque, Double-ended Queue)의 개념과 활용 사례를 설명하시오.
- 우선순위 큐(Priority Queue)의 개념과 구현 방식(힙 구조 포함)을 설명하시오.
- 트리(Tree)와 그래프(Graph)의 차이점을 설명하시오.
- 이진 트리(Binary Tree)와 이진 탐색 트리(Binary Search Tree, BST)의 차이점을 설명하시오.
- AVL 트리와 레드-블랙 트리(Red-Black Tree)의 차이점을 설명하시오.
- B-트리(B-Tree)와 B+트리(B+ Tree)의 구조와 활용 사례를 설명하시오.
- 트라이(Trie) 자료구조란 무엇인가? 사용 사례를 설명하시오.
- 동적 연결 리스트(Linked List)와 배열(Array)의 차이점을 설명하시오.
- 이중 연결 리스트(Doubly Linked List)의 구조와 장점을 설명하시오.
- 원형 연결 리스트(Circular Linked List)의 개념과 활용 방안을 설명하시오.
- 정렬 알고리즘에서 안정 정렬(Stable Sort)과 불안정 정렬(Unstable Sort)의 차이점을 설명하시오.
- 팀 정렬(Timsort)의 개념과 활용 사례를 설명하시오.
- 셸 정렬(Shell Sort)의 개념과 시간 복잡도를 설명하시오.
- Pigeonhole 정렬 알고리즘의 개념과 사용 사례를 설명하시오.
- 내부 정렬(Internal Sorting)과 외부 정렬(External Sorting)의 차이점을 설명하시오.
- O(n log n) 정렬 알고리즘을 비교하고 어떤 상황에서 어떤 정렬이 유리한지 설명하시오.
- 특정 데이터 크기(예: 1억 개)의 숫자를 정렬해야 할 때 가장 적합한 알고리즘을 선택하고 이유를 설명하시오.
- 해시 함수(Hash Function)의 개념과 이상적인 조건을 설명하시오.
- 체이닝(Chaining)과 개방 주소법(Open Addressing)의 차이점을 설명하시오.
- 퍼펙트 해시(Perfect Hashing)란 무엇인가?
- 블룸 필터(Bloom Filter)의 개념과 사용 사례를 설명하시오.
- 선형 탐색(Linear Search)와 이진 탐색(Binary Search)의 차이를 설명하시오.
- 점프 탐색(Jump Search)와 보간 탐색(Interpolation Search)의 개념과 차이점을 설명하시오.
- 그래프 탐색에서 DFS가 BFS보다 유리한 경우와 반대의 경우를 설명하시오.
- 위상 정렬(Topological Sorting)의 개념과 구현 방법을 설명하시오.
- 유니온-파인드(Union-Find) 알고리즘의 개념과 활용 사례를 설명하시오.
- 최소 스패닝 트리(MST)에서 크루스칼 알고리즘과 프림 알고리즘의 차이점을 설명하시오.
- 네트워크 플로우(Network Flow) 문제를 해결하는 방법을 설명하시오.
- 이중 연결 그래프(Biconnected Graph)란 무엇인가?
- 그래프에서 강한 연결 요소(Strongly Connected Components, SCC)의 개념을 설명하시오.
- Z-알고리즘(Z-Algorithm)의 개념과 활용 사례를 설명하시오.
- 라빈-카프(Rabin-Karp) 알고리즘의 시간 복잡도를 분석하시오.
- 보이어-무어(Boyer-Moore) 알고리즘이 KMP 알고리즘보다 빠를 수 있는 이유를 설명하시오.
- 접미사 트리(Suffix Tree)의 개념과 활용 방안을 설명하시오.
- 편집 거리(Edit Distance) 알고리즘(Levenshtein Distance)의 개념을 설명하시오.
- 롤링 해시(Rolling Hash)의 개념과 활용 방안을 설명하시오.
- RSA 암호화 알고리즘의 원리와 수학적 기반을 설명하시오.
- 대칭키 암호화(Symmetric Encryption)와 비대칭키 암호화(Asymmetric Encryption)의 차이점을 설명하시오.
- AES(Advanced Encryption Standard) 알고리즘의 원리를 설명하시오.
- 해시 함수(Hash Function)의 주요 특징과 안전한 해시 알고리즘(SHA, MD5 등)의 차이점을 설명하시오.
- 디피-헬만 키 교환(Diffie-Hellman Key Exchange) 방식의 개념을 설명하시오.
- 블록 암호(Block Cipher)와 스트림 암호(Stream Cipher)의 차이를 설명하시오.
- 의사 결정 트리(Decision Tree)의 개념과 활용 사례를 설명하시오.
- 랜덤 포레스트(Random Forest) 알고리즘의 원리와 장점을 설명하시오.
- 신경망(Neural Network)의 개념과 활성화 함수(Activation Function)의 역할을 설명하시오.
- 서포트 벡터 머신(SVM)의 개념과 커널 트릭(Kernel Trick)의 활용을 설명하시오.
- K-최근접 이웃(K-Nearest Neighbor, KNN) 알고리즘의 개념과 단점을 설명하시오.
- 유전자 알고리즘(Genetic Algorithm)의 개념과 적용 사례를 설명하시오.
- 분할 정복(Divide and Conquer)과 동적 계획법(Dynamic Programming)의 차이점을 설명하시오.
- 탐욕 알고리즘(Greedy Algorithm)의 특징과 한계를 설명하시오.
- 메타휴리스틱 알고리즘(Metaheuristic Algorithm)의 개념과 예제를 설명하시오.
- 근사 알고리즘(Approximation Algorithm)의 개념과 활용 사례를 설명하시오.
- NP-완전 문제(NP-Complete)의 개념과 대표적인 문제를 설명하시오.
- 시뮬레이티드 어닐링(Simulated Annealing)의 개념과 활용 사례를 설명하시오.
- 트리(Tree)란 무엇이며, 트리의 주요 특징을 설명하시오.
- 이진 탐색 트리(BST)의 개념과 탐색, 삽입, 삭제 연산의 시간 복잡도를 설명하시오.
- AVL 트리와 레드-블랙 트리(Red-Black Tree)의 차이점을 설명하시오.
- B-트리(B-Tree)의 구조와 활용 사례를 설명하시오.
- B+ 트리(B+ Tree)와 B-트리의 차이점을 설명하시오.
- 트리 순회(Tree Traversal) 방식인 전위 순회(Preorder), 중위 순회(Inorder), 후위 순회(Postorder)의 차이점을 설명하시오.
- 레드-블랙 트리(Red-Black Tree)의 삽입과 삭제 시 재구성 과정에 대해 설명하시오.
- K-ary 트리란 무엇이며, 이진 트리와의 차이점을 설명하시오.
- Huffman 트리의 개념과 텍스트 압축에 활용되는 원리를 설명하시오.
- 볼록 껍질(Convex Hull) 알고리즘의 개념과 구현 방법을 설명하시오.
- 최근접 점 쌍(Closest Pair of Points) 문제를 해결하는 방법을 설명하시오.
- 회전하는 캘리퍼스(Rotating Calipers) 기법의 개념과 활용 사례를 설명하시오.
- 점 내 포함 문제(Point-in-Polygon, PIP)의 개념과 해결 방법을 설명하시오.
- 브루트 포스(Brute Force)를 이용한 볼록 껍질 알고리즘의 시간 복잡도를 분석하시오.
- 피보나치 수열을 재귀(Recursive)와 동적 계획법(DP)으로 구현하는 방법을 비교하시오.
- 최장 공통 부분 수열(Longest Common Subsequence, LCS) 알고리즘의 개념과 구현 방법을 설명하시오.
- 배낭 문제(Knapsack Problem)에서 0-1 Knapsack과 Fractional Knapsack의 차이점을 설명하시오.
- 행렬 체인 곱셈(Matrix Chain Multiplication) 알고리즘을 설명하시오.
- 최장 증가 부분 수열(Longest Increasing Subsequence, LIS)의 개념과 구현 방법을 설명하시오.
- 그래프 색칠 문제(Graph Coloring Problem)란 무엇인가?
- 최소 색칠 문제(Minimum Graph Coloring)를 해결하는 방법을 설명하시오.
- 4색 정리(Four Color Theorem)의 개념과 의미를 설명하시오.
- NP-완전 문제로서의 그래프 색칠 문제의 특징을 설명하시오.
- 백트래킹을 이용한 그래프 색칠 알고리즘을 설명하시오.
- 근사 알고리즘(Approximation Algorithm)이란 무엇이며, 활용 사례를 설명하시오.
- 여행하는 외판원 문제(Travelling Salesman Problem, TSP)에서 근사 알고리즘을 적용하는 방법을 설명하시오.
- 시뮬레이티드 어닐링(Simulated Annealing)의 개념과 최적화 문제 해결에의 적용을 설명하시오.
- 유전 알고리즘(Genetic Algorithm)의 개념과 동작 원리를 설명하시오.
- 개미 군집 최적화(Ant Colony Optimization, ACO) 알고리즘의 개념과 활용 사례를 설명하시오.
- 입자 군집 최적화(Particle Swarm Optimization, PSO) 알고리즘의 개념과 활용 사례를 설명하시오.
- 에라토스테네스의 체(Sieve of Eratosthenes) 알고리즘의 개념과 활용 사례를 설명하시오.
- 유클리드 호제법(Euclidean Algorithm)을 이용한 최대공약수(GCD) 구하는 방법을 설명하시오.
- 확장 유클리드 알고리즘(Extended Euclidean Algorithm)의 개념과 활용 방안을 설명하시오.
- 모듈러 연산(Modular Arithmetic)이란 무엇이며, RSA 암호화와의 관계를 설명하시오.
- 중국인의 나머지 정리(Chinese Remainder Theorem, CRT)의 개념과 활용 사례를 설명하시오.
- 페르마의 소정리(Fermat’s Little Theorem)의 개념과 활용 방안을 설명하시오.
- 로지스틱 회귀(Logistic Regression)의 개념과 활용 사례를 설명하시오.
- K-평균 군집화(K-Means Clustering) 알고리즘의 개념과 활용 사례를 설명하시오.
- 랜덤 포레스트(Random Forest) 알고리즘의 개념과 장점을 설명하시오.
- 신경망(Neural Network)의 활성화 함수(Activation Function) 개념을 설명하시오.
- 그래디언트 부스팅(Gradient Boosting)과 XGBoost의 차이점을 설명하시오.
- 딥러닝에서 CNN(Convolutional Neural Network)과 RNN(Recurrent Neural Network)의 차이점을 설명하시오.
- 분할 정복과 동적 계획법의 차이점을 실제 사례와 함께 설명하시오.
- BFS와 DFS를 이용한 문제 해결 사례를 설명하시오.
- 메모이제이션(Memoization) 기법이 필요한 경우와 그 장점을 설명하시오.
- 문제 해결을 위해 알고리즘을 선택할 때 고려해야 할 요소는 무엇인가?
- 문제 해결 전략에서 탐욕 알고리즘을 적용할 수 있는 조건은 무엇인가?
- 최소 공통 조상(Lowest Common Ancestor, LCA) 문제의 개념과 해결 방법을 설명하시오.
- 세그먼트 트리(Segment Tree)의 개념과 활용 사례를 설명하시오.
- 펜윅 트리(Fenwick Tree, Binary Indexed Tree)의 개념과 구현 방법을 설명하시오.
- 트라이(Trie) 자료구조의 개념과 활용 사례를 설명하시오.
- 그래프에서 타잔(Tarjan)의 알고리즘을 이용한 강한 연결 요소(SCC) 찾기 방법을 설명하시오.
- 벨만-포드 알고리즘과 다익스트라 알고리즘의 차이점을 비교하시오.
- 플로이드-워셜 알고리즘과 벨만-포드 알고리즘의 차이점을 설명하시오.
- 그래프에서 최단 경로 문제를 해결하기 위해 다익스트라, 벨만-포드, 플로이드-워셜 중 어떤 것을 선택해야 하는지 설명하시오.
- 최대 독립 집합(Maximum Independent Set)의 개념과 해결 방법을 설명하시오.
- 최소 컷-최대 유량(Min-Cut Max-Flow) 정리를 설명하시오.
- 조합(Combination)과 순열(Permutation)의 개념과 차이점을 설명하시오.
- 파스칼의 삼각형(Pascal’s Triangle)과 이항 계수(Binomial Coefficient)의 관계를 설명하시오.
- 카탈란 수(Catalan Number)의 개념과 활용 사례를 설명하시오.
- 스타링 수(Stirling Number)의 개념과 활용 사례를 설명하시오.
- 모듈러 역원(Modular Inverse)과 확장 유클리드 알고리즘(Extended Euclidean Algorithm)을 이용한 계산 방법을 설명하시오.
- 중국인의 나머지 정리(Chinese Remainder Theorem, CRT)의 개념과 활용 사례를 설명하시오.
- 폴라드 로(Pollard Rho) 알고리즘을 이용한 소인수 분해(Factorization) 방법을 설명하시오.
- 아호-코라식(Aho-Corasick) 알고리즘의 개념과 활용 사례를 설명하시오.
- Z-알고리즘(Z-Algorithm)을 이용한 문자열 검색 방법을 설명하시오.
- 접미사 트리(Suffix Tree)와 접미사 배열(Suffix Array)의 차이점을 설명하시오.
- 문자열 정렬을 위한 버켓 정렬(Bucket Sort)의 개념과 구현 방법을 설명하시오.
- 롤링 해시(Rolling Hash) 기법을 이용한 서브스트링 검색 방법을 설명하시오.
- 퍼셉트론(Perceptron) 알고리즘의 개념과 활용 사례를 설명하시오.
- 확률적 경사 하강법(Stochastic Gradient Descent, SGD)의 개념과 적용 사례를 설명하시오.
- 신경망(Neural Network)에서 과적합(Overfitting)을 방지하는 방법을 설명하시오.
- 앙상블 학습(Ensemble Learning)의 개념과 랜덤 포레스트(Random Forest)와 부스팅(Boosting)의 차이를 설명하시오.
- 서포트 벡터 머신(SVM)의 핵심 개념과 커널 기법(Kernel Trick)을 설명하시오.
- 허프만 코딩(Huffman Coding) 알고리즘의 개념과 압축 원리를 설명하시오.
- 런-길이 부호화(Run-Length Encoding, RLE) 알고리즘의 개념과 활용 사례를 설명하시오.
- BWT(Burrows-Wheeler Transform)의 개념과 데이터 압축에서의 활용 방법을 설명하시오.
- Lempel-Ziv-Welch(LZW) 압축 알고리즘의 개념과 구현 방법을 설명하시오.
- 데이터베이스 인덱싱에서 B-트리(B-Tree)와 해시 인덱싱의 차이점을 설명하시오.
- 멀티스레딩(Multi-threading)과 병렬 처리(Parallel Processing)의 차이점을 설명하시오.
- 뮤텍스(Mutex)와 세마포어(Semaphore)의 차이점을 설명하시오.
- 데드락(Deadlock)의 개념과 예방 방법을 설명하시오.
- 생산자-소비자 문제(Producer-Consumer Problem)를 해결하는 방법을 설명하시오.
- 스핀락(Spinlock)의 개념과 사용 사례를 설명하시오.
- 분산 알고리즘(Distributed Algorithm)의 개념과 주요 활용 사례를 설명하시오.
- 양자 컴퓨팅(Quantum Computing)에서의 알고리즘(예: Shor’s Algorithm, Grover’s Algorithm)의 개념을 설명하시오.
- 딥러닝에서 사용하는 최적화 기법(Adam, RMSProp 등)의 개념을 설명하시오.
- 강화 학습(Reinforcement Learning)의 개념과 Q-learning, SARSA 알고리즘의 차이점을 설명하시오.
- 최신 AI 및 알고리즘 연구에서 가장 주목받는 기술 동향을 설명하시오.
- 고급 암호화 기법(예: 동형 암호, 격자 기반 암호)의 개념을 설명하시오.
- 블록체인(Blockchain)에서 사용되는 해시 알고리즘과 블록 검증 방법을 설명하시오.
- 생체 인식(Biometrics)에서 딥러닝을 활용한 얼굴 인식 및 지문 인식 알고리즘을 설명하시오.
- 자율 주행 자동차에서 활용되는 알고리즘(예: SLAM, Dijkstra, A*)을 설명하시오.
- 분산 시스템에서의 합의 알고리즘(Consensus Algorithm)의 개념과 종류를 설명하시오.
- 리더 선출 알고리즘(Leader Election Algorithm)의 개념과 활용 사례를 설명하시오.
- Paxos 알고리즘의 개념과 분산 환경에서의 적용 사례를 설명하시오.
- Raft 알고리즘의 원리와 Paxos와의 차이점을 설명하시오.
- 블록체인(Blockchain)에서 사용되는 합의 알고리즘(PoW, PoS 등)의 개념과 차이점을 설명하시오.
- 분산 해시 테이블(Distributed Hash Table, DHT)의 개념과 활용 사례를 설명하시오.
- 클라우드 컴퓨팅에서 사용되는 오토스케일링(Auto Scaling) 알고리즘의 개념을 설명하시오.
- 컨테이너 오케스트레이션(Container Orchestration)에서 사용되는 스케줄링 알고리즘을 설명하시오.
- 강화 학습에서 사용하는 DQN(Deep Q-Network)의 개념과 활용 사례를 설명하시오.
- AlphaGo가 사용한 MCTS(Monte Carlo Tree Search) 알고리즘의 개념과 적용 방법을 설명하시오.
- GAN(Generative Adversarial Network)의 개념과 활용 사례를 설명하시오.
- 트랜스포머(Transformer) 모델의 구조와 기존 RNN, CNN과의 차이점을 설명하시오.
- 딥러닝에서 BERT(Bidirectional Encoder Representations from Transformers)의 개념과 활용 사례를 설명하시오.
- YOLO(You Only Look Once) 알고리즘의 개념과 실시간 객체 탐지에서의 활용 방법을 설명하시오.
- 자율주행 자동차에서 사용되는 SLAM(Simultaneous Localization and Mapping) 알고리즘을 설명하시오.
- 양자 컴퓨팅에서 Shor’s Algorithm이 기존 암호화 체계를 위협하는 이유를 설명하시오.
- 딥러닝 기반의 알고리즘 압축 기술(Pruning, Quantization 등)의 개념과 활용 사례를 설명하시오.
- 연합 학습(Federated Learning)의 개념과 데이터 보호를 위한 활용 사례를 설명하시오.
- 프로세스 스케줄링(Process Scheduling) 알고리즘의 종류와 차이점을 설명하시오.
- CPU 스케줄링에서 SJF(Shortest Job First)와 Round Robin(RR)의 차이점을 설명하시오.
- 다중 스레딩(Multi-threading)과 멀티프로세싱(Multi-processing)의 차이점을 설명하시오.
- 병렬 컴퓨팅에서 OpenMP와 MPI의 차이점을 설명하시오.
- 동기(Synchronous)와 비동기(Asynchronous) 프로그래밍의 개념과 활용 사례를 설명하시오.
- GPU 연산에서 CUDA와 OpenCL의 차이점을 설명하시오.
- Task Scheduling에서 DAG(Directed Acyclic Graph)를 활용하는 방법을 설명하시오.
- PageRank 알고리즘의 개념과 웹 검색 엔진에서의 활용 사례를 설명하시오.
- TF-IDF(Term Frequency-Inverse Document Frequency)의 개념과 검색 엔진에서의 활용을 설명하시오.
- 협업 필터링(Collaborative Filtering)의 개념과 추천 시스템에서의 활용 방법을 설명하시오.
- 콘텐츠 기반 필터링(Content-Based Filtering)의 개념과 활용 사례를 설명하시오.
- 하이브리드 추천 시스템(Hybrid Recommendation System)의 개념과 적용 사례를 설명하시오.
- 자연어 처리(NLP)에서 Word2Vec과 FastText의 차이점을 설명하시오.
- 검색 엔진 최적화(SEO)에서 사용되는 주요 알고리즘을 설명하시오.
- PID(비례-적분-미분) 제어 알고리즘의 개념과 활용 사례를 설명하시오.
- 칼만 필터(Kalman Filter)의 개념과 센서 데이터 융합에서의 활용 방법을 설명하시오.
- A* (A-Star) 알고리즘의 개념과 로봇 경로 탐색에서의 활용 방법을 설명하시오.
- D* 알고리즘과 A* 알고리즘의 차이점을 설명하시오.
- RRT(Rapidly-exploring Random Tree) 알고리즘의 개념과 로봇 경로 계획에서의 활용을 설명하시오.
- ACID(원자성, 일관성, 고립성, 지속성)의 개념과 데이터베이스에서의 적용 방법을 설명하시오.
- 2단계 잠금(2-Phase Locking, 2PL) 기법의 개념과 활용 사례를 설명하시오.
- 트랜잭션 스케줄링에서 직렬 가능성(Serializability)의 개념을 설명하시오.
- 데이터베이스 샤딩(Sharding)과 파티셔닝(Partitioning)의 차이점을 설명하시오.
- NoSQL과 RDBMS의 차이점을 설명하고, 각 기술이 적합한 사례를 설명하시오.
- 동형 암호(Homomorphic Encryption)의 개념과 활용 사례를 설명하시오.
- 격자 기반 암호(Lattice-Based Cryptography)의 개념과 기존 암호화 방식과의 차이점을 설명하시오.
- 블록체인의 해시 함수(Hash Function)가 보안성을 보장하는 원리를 설명하시오.
- TLS(Transport Layer Security) 핸드셰이크 과정과 보안 프로토콜을 설명하시오.
- OAuth와 OpenID Connect의 차이점과 활용 사례를 설명하시오.
- 엣지 컴퓨팅(Edge Computing)에서의 데이터 처리 알고리즘을 설명하시오.
- 5G 네트워크에서 MEC(Multi-access Edge Computing)의 개념과 활용 사례를 설명하시오.
- 양자 내성 암호(Post-Quantum Cryptography)란 무엇이며, 현재 연구 동향을 설명하시오.
- 디지털 트윈(Digital Twin) 기술과 활용 사례를 설명하시오.
- IoT(Internet of Things)에서 사용되는 효율적인 데이터 압축 및 전송 알고리즘을 설명하시오.
- 시스템 부하 분산(Load Balancing) 알고리즘의 개념과 주요 기법을 설명하시오.
- 라운드 로빈(Round Robin)과 가중치 기반 라운드 로빈(Weighted Round Robin)의 차이점을 설명하시오.
- 서버 부하 분산에서 해시 기반 로드 밸런싱(Hash-Based Load Balancing)의 개념을 설명하시오.
- 캐시 일관성(Cache Consistency) 문제를 해결하는 방법을 설명하시오.
- CDN(Content Delivery Network)에서 사용되는 캐싱 및 최적화 기법을 설명하시오.
- LRU(Least Recently Used)와 LFU(Least Frequently Used) 캐싱 알고리즘의 차이점을 설명하시오.
- 대규모 데이터베이스 시스템에서 샤딩(Sharding)과 리플리케이션(Replication)의 차이를 설명하시오.
- RAID(Redundant Array of Independent Disks) 레벨별 성능 차이와 활용 사례를 설명하시오.
- 장애 감지(Fault Detection) 알고리즘의 개념과 활용 사례를 설명하시오.
- 분산 시스템에서 장애 감지와 복구를 위한 하트비트(Heartbeat) 알고리즘을 설명하시오.
- 백업 및 복구(Backup & Recovery) 전략에서 Snapshotting 기법을 설명하시오.
- 데이터 무결성(Data Integrity)을 보장하는 방법과 관련 알고리즘을 설명하시오.
- 장애 조치(Failover)와 장애 복구(Failback)의 차이를 설명하시오.
- 침입 탐지 시스템(IDS: Intrusion Detection System)에서 사용되는 이상 탐지(Anomaly Detection) 알고리즘을 설명하시오.
- 머신러닝을 이용한 보안 위협 탐지 기법을 설명하시오.
- 방화벽(Firewall)과 침입 방지 시스템(IPS: Intrusion Prevention System)의 차이를 설명하시오.
- DDoS(Distributed Denial of Service) 공격 탐지 및 대응 알고리즘을 설명하시오.
- 해시 기반 메시지 인증 코드(HMAC: Hash-based Message Authentication Code)의 원리를 설명하시오.
- 웹 애플리케이션 보안에서 SQL 인젝션 탐지 및 방어 방법을 설명하시오.
- 사이버 보안에서 공인 키 인프라(PKI: Public Key Infrastructure)의 역할과 알고리즘을 설명하시오.
- 유전 알고리즘(Genetic Algorithm)을 활용한 최적화 기법을 설명하시오.
- 시뮬레이티드 어닐링(Simulated Annealing) 알고리즘의 개념과 활용 사례를 설명하시오.
- 강화 학습에서 Q-learning과 SARSA의 차이를 설명하시오.
- 차량 경로 최적화(Vehicle Routing Problem, VRP)에서 사용되는 알고리즘을 설명하시오.
- 선형 계획법(Linear Programming)과 정수 계획법(Integer Programming)의 차이를 설명하시오.
- 라그랑주 승수법(Lagrange Multiplier)과 최적화 문제 해결에서의 활용을 설명하시오.
- 동적 계획법(DP)을 활용한 최소 비용 경로 문제 해결 방법을 설명하시오.
- 컨테이너 오케스트레이션(Container Orchestration)에서 사용되는 스케줄링 알고리즘을 설명하시오.
- 마이크로서비스 아키텍처(Microservices Architecture)에서 서비스 디스커버리(Service Discovery) 알고리즘을 설명하시오.
- 클라우드 환경에서 사용되는 무상태(State-less)와 상태 저장(State-full) 아키텍처의 차이를 설명하시오.
- 서버리스(Serverless) 컴퓨팅에서 동적 리소스 할당 알고리즘을 설명하시오.
- API Gateway에서 사용되는 부하 분산 및 캐싱 전략을 설명하시오.
- 엣지 컴퓨팅(Edge Computing)에서 사용되는 데이터 필터링 및 처리 알고리즘을 설명하시오.
- IoT(Internet of Things)에서 저전력 네트워크 프로토콜(LPWA, LoRa, NB-IoT)의 차이를 설명하시오.
- IoT 디바이스에서 데이터 동기화를 위한 분산 알고리즘을 설명하시오.
- 실시간 스트리밍 데이터 처리에서 CEP(Complex Event Processing)의 개념과 알고리즘을 설명하시오.
- MQTT(Message Queuing Telemetry Transport) 프로토콜과 데이터 송수신 최적화 기법을 설명하시오.
- 양자 컴퓨팅(Quantum Computing)에서 슈어(Shor's Algorithm)의 개념과 기존 암호 체계에 미치는 영향을 설명하시오.
- 양자 컴퓨터에서 그로버(Grover’s Algorithm)를 활용한 데이터 검색 최적화 방법을 설명하시오.
- AI 기반 코드 자동 생성 모델(예: GitHub Copilot)의 알고리즘 원리와 활용 사례를 설명하시오.
- 컴퓨터 아키텍처(Computer Architecture)의 주요 구성 요소와 역할을 설명하시오.
- CISC와 RISC 프로세서의 차이점을 설명하시오.
- 파이프라이닝(Pipelining)의 개념과 성능 향상 효과를 설명하시오.
- 스레드(Thread)와 프로세스(Process)의 차이점을 설명하시오.
- 가상 메모리(Virtual Memory)의 개념과 페이지 교체(Page Replacement) 알고리즘을 설명하시오.
- 페이지 교체 알고리즘(FIFO, LRU, Optimal)의 개념과 성능 비교를 설명하시오.
- 세그먼테이션(Segmentation)과 페이징(Paging)의 차이점을 설명하시오.
- 동기식 I/O와 비동기식 I/O의 차이점을 설명하시오.
- 커널 모드(Kernel Mode)와 사용자 모드(User Mode)의 차이를 설명하시오.
- 데이터베이스 정규화(Normalization) 과정과 이상현상(Anomaly) 해결 방법을 설명하시오.
- 정규형(NF: Normal Form)의 개념과 1NF, 2NF, 3NF, BCNF의 차이를 설명하시오.
- 인덱스(Index)의 개념과 B-Tree 인덱스와 Hash 인덱스의 차이점을 설명하시오.
- 데이터베이스 트랜잭션(Transaction)에서 고립성(Isolation)의 중요성과 격리 수준(Isolation Level)을 설명하시오.
- 알고리즘 설계에서 "컴퓨팅 사고(Computational Thinking)"의 개념과 중요성을 설명하시오.
- 알고리즘의 정확성(Correctness)을 증명하는 방법을 설명하시오.
- 순환식(Recurrence Relation)의 개념과 마스터 정리(Master Theorem)의 활용 방법을 설명하시오.
- 다항 시간 알고리즘(Polynomial-Time Algorithm)과 비다항 시간 알고리즘(Non-Polynomial-Time Algorithm)의 차이를 설명하시오.
- 탐욕 알고리즘(Greedy Algorithm)이 최적해를 보장할 수 있는 조건을 설명하시오.
- 셸 정렬(Shell Sort)의 개념과 시간 복잡도를 설명하시오.
- 팀 정렬(Timsort)의 원리와 기존 정렬 알고리즘과의 차이를 설명하시오.
- 비교 기반 정렬(Comparison-Based Sort)과 비비교 기반 정렬(Non-Comparison-Based Sort)의 차이를 설명하시오.
- 특정한 상황(거의 정렬된 데이터, 랜덤 데이터)에서 최적의 정렬 알고리즘을 선택하는 기준을 설명하시오.
- 메모리 제약이 있는 환경에서 적합한 정렬 알고리즘을 선택하는 방법을 설명하시오.
- 점프 탐색(Jump Search)의 개념과 활용 방안을 설명하시오.
- 보간 탐색(Interpolation Search)의 개념과 이진 탐색(Binary Search)과의 차이점을 설명하시오.
- 피보나치 탐색(Fibonacci Search)의 개념과 이진 탐색과의 차이점을 설명하시오.
- 기수 트리(Radix Tree, Patricia Tree)의 개념과 활용 사례를 설명하시오.
- B-트리(B-Tree)와 B+트리(B+ Tree)의 차이점을 설명하시오.
- 트리(Tree)와 그래프(Graph)의 차이를 설명하시오.
- 오일러 경로(Eulerian Path)와 해밀턴 경로(Hamiltonian Path)의 차이점을 설명하시오.
- 그래프에서 두 노드 간 최단 경로 문제를 해결하는 다양한 알고리즘(Dijkstra, Bellman-Ford, Floyd-Warshall 등)의 비교를 설명하시오.
- A* (A-Star) 알고리즘에서 휴리스틱(Heuristic) 함수가 중요한 이유를 설명하시오.
- 네트워크 플로우(Network Flow) 문제에서 이분 매칭(Bipartite Matching)을 해결하는 방법을 설명하시오.
- 보이어-무어(Boyer-Moore) 알고리즘이 KMP(Knuth-Morris-Pratt) 알고리즘보다 빠른 경우를 설명하시오.
- 라빈-카프(Rabin-Karp) 알고리즘이 사용하는 해싱(Hashing) 기법을 설명하시오.
- 롤링 해시(Rolling Hash)와 해밍 거리(Hamming Distance)의 개념을 설명하시오.
- 접미사 배열(Suffix Array)과 접미사 트리(Suffix Tree)의 차이점을 설명하시오.
- LCS(Longest Common Subsequence)와 LCS(Longest Common Substring)의 차이점을 설명하시오.
- 동적 계획법에서 "중복 계산 방지"를 위한 메모이제이션(Memoization)과 탑다운(Top-Down) 방식의 차이를 설명하시오.
- 동적 계획법과 그리디 알고리즘의 차이를 설명하고, 각각을 적용할 수 있는 대표적인 문제를 설명하시오.
- 행렬 체인 곱셈(Matrix Chain Multiplication) 알고리즘을 설명하시오.
- 배낭 문제(Knapsack Problem)에서 0-1 Knapsack과 Fractional Knapsack의 차이를 설명하시오.
- Floyd-Warshall 알고리즘을 동적 계획법으로 해결하는 과정과 시간 복잡도를 설명하시오.
- 탐욕 알고리즘(Greedy Algorithm)이 NP-완전 문제에서 최적해를 보장할 수 있는 경우를 설명하시오.
- 근사 알고리즘(Approximation Algorithm)의 개념과 대표적인 예제(TSP, Vertex Cover 문제)를 설명하시오.
- 유전 알고리즘(Genetic Algorithm)의 개념과 최적화 문제에서의 활용 사례를 설명하시오.
- 시뮬레이티드 어닐링(Simulated Annealing) 알고리즘이 지역 최적해(Local Optimum) 문제를 해결하는 방법을 설명하시오.
- 파티클 스웜 최적화(Particle Swarm Optimization, PSO)의 개념과 활용 사례를 설명하시오.
- 볼록 껍질(Convex Hull) 알고리즘의 개념과 활용 사례를 설명하시오.
- 최근접 점 쌍(Closest Pair of Points) 문제를 해결하는 방법을 설명하시오.
- 회전하는 캘리퍼스(Rotating Calipers) 기법을 설명하고 활용 가능한 문제를 설명하시오.
- 포인트 인 폴리곤(Point in Polygon) 문제의 해결 방법을 설명하시오.
- 라인 세그먼트 교차(Line Segment Intersection) 문제를 해결하는 알고리즘을 설명하시오.
- 트랜스포머(Transformer) 모델의 구조와 기존 RNN, CNN과의 차이를 설명하시오.
- 딥러닝에서 배치 정규화(Batch Normalization)의 원리와 효과를 설명하시오.
- 강화 학습에서 DQN(Deep Q-Network)과 PPO(Proximal Policy Optimization)의 차이점을 설명하시오.
- GAN(Generative Adversarial Network)에서 생성자(Generator)와 판별자(Discriminator)의 역할을 설명하시오.
- 그래프 신경망(GNN, Graph Neural Network)의 개념과 활용 사례를 설명하시오.
- 양자 알고리즘에서 Shor’s Algorithm이 기존 RSA 암호화를 위협하는 이유를 설명하시오.
- 양자 내성 암호(Post-Quantum Cryptography)의 개념과 필요성을 설명하시오.
- 블록체인의 해시 알고리즘(Hash Algorithm)이 보안성을 보장하는 원리를 설명하시오.
- 동형 암호(Homomorphic Encryption)의 개념과 활용 사례를 설명하시오.
- Zero-Knowledge Proof(영지식 증명)의 개념과 보안 응용 사례를 설명하시오.
- 확률과 통계를 활용한 알고리즘 최적화 기법을 설명하시오.
- 랜덤화 알고리즘(Randomized Algorithm)의 개념과 활용 사례를 설명하시오.
- 모듈러 연산(Modular Arithmetic)의 개념과 RSA 암호화에서의 활용을 설명하시오.
- 밀러-라빈(Miller-Rabin) 소수 판별 알고리즘을 설명하시오.
- 페르마 소정리(Fermat’s Little Theorem)와 소수 판별에서의 활용을 설명하시오.
- 스패닝 트리(Spanning Tree)와 최소 신장 트리(MST)의 차이를 설명하시오.
- 다이나믹 그래프(Dynamic Graph)의 개념과 업데이트 시 최단 경로를 유지하는 방법을 설명하시오.
- 전방 탐색(Forward Search)과 역방향 탐색(Backward Search)의 차이를 설명하시오.
- 이진 인덱스 트리(Binary Indexed Tree, Fenwick Tree)의 개념과 활용 사례를 설명하시오.
- Heavy-Light Decomposition을 활용한 트리 쿼리 최적화 기법을 설명하시오.
- 그래프 색칠 문제(Graph Coloring Problem)와 그 활용 사례를 설명하시오.
- 평면 그래프에서 4색 정리(Four Color Theorem)의 개념과 증명을 설명하시오.
- Vertex Cover 문제의 정의와 근사 알고리즘을 설명하시오.
- 클러스터링(Coarsening) 기법을 이용한 그래프 압축 방법을 설명하시오.
- 그래프 컷(Graph Cut) 알고리즘과 이미지 분할에서의 활용을 설명하시오.
- DP에서 상태 압축(State Compression) 기법을 설명하시오.
- 분할 정복(Divide and Conquer)과 동적 계획법(Dynamic Programming)의 차이를 설명하시오.
- DP 최적화 기법 중 Convex Hull Trick을 설명하시오.
- DP 최적화 기법 중 Knuth Optimization을 설명하시오.
- 가변 길이 배열을 다루는 DP 문제 해결 방법을 설명하시오.
- 네트워크 플로우(Network Flow)에서 최소 컷-최대 유량 정리를 설명하시오.
- 헝가리안 알고리즘(Hungarian Algorithm)의 개념과 이분 매칭(Bipartite Matching)에서의 활용을 설명하시오.
- Push-Relabel Algorithm을 활용한 최대 유량 문제 해결 방법을 설명하시오.
- Edmonds-Karp Algorithm을 활용한 네트워크 유량 최적화 방법을 설명하시오.
- 네트워크 플로우를 활용한 다중 경로 라우팅 최적화 기법을 설명하시오.
- 강화 학습에서 MCTS(Monte Carlo Tree Search)의 개념과 활용을 설명하시오.
- 그래프 신경망(GNN, Graph Neural Network)의 개념과 활용 사례를 설명하시오.
- 최신 딥러닝 모델에서 Transformer의 성능을 최적화하는 알고리즘을 설명하시오.
- 하이퍼 파라미터 튜닝(Hyperparameter Tuning)에서 Bayesian Optimization의 개념과 활용을 설명하시오.
- 연합 학습(Federated Learning)의 개념과 보안 강화 기법을 설명하시오.
- 확률 알고리즘(Probabilistic Algorithm)의 개념과 주요 활용 사례를 설명하시오.
- 수학적 최적화 문제에서 라그랑주 승수법(Lagrange Multiplier)의 개념을 설명하시오.
- 베이즈 정리(Bayes' Theorem)를 활용한 알고리즘 최적화 방법을 설명하시오.
- 몬테카를로 방법(Monte Carlo Method)과 의사 난수 발생(Pseudo Random Number Generation)의 차이를 설명하시오.
- KMP 알고리즘에서 실패 함수(Failure Function)의 개념과 역할을 설명하시오.
- 라빈-카프 알고리즘에서 해싱 충돌(Hash Collision) 문제를 해결하는 방법을 설명하시오.
- 문자열 집합에서 유사 문자열 검색을 최적화하는 알고리즘을 설명하시오.
- Levenshtein Distance(편집 거리)의 개념과 문자열 비교에서의 활용을 설명하시오.
- 네트워크 플로우 문제에서 다중 소스-다중 싱크(Multi-Source, Multi-Sink) 문제를 해결하는 방법을 설명하시오.
- 최소 비용 유량(Minimum Cost Flow) 문제를 해결하는 알고리즘을 설명하시오.
- 강화 학습에서 정책 그래디언트(Policy Gradient) 알고리즘의 개념과 활용을 설명하시오.
- 최신 딥러닝 모델에서 Transformer를 기반으로 한 최적화 알고리즘을 설명하시오.
- 생성형 AI(Generative AI)에서 Diffusion Model이 사용되는 원리를 설명하시오.
- 자율 주행에서 강화 학습을 활용한 의사결정 알고리즘을 설명하시오.
- 최근 연구에서 가장 주목받는 알고리즘 최적화 기법을 설명하시오.
- 고급 암호화 알고리즘(예: 동형 암호, 격자 기반 암호)의 개념과 활용을 설명하시오.
- 알고리즘 공학(Algorithm Engineering)이란 무엇이며, 기존 알고리즘 연구와의 차이점을 설명하시오.
- 최근 빅데이터 알고리즘 연구에서 가장 중요한 이슈는 무엇인가?
- 양자 알고리즘(Quantum Algorithm) 중 Grover's Algorithm이 데이터 검색에서 제공하는 속도 향상 효과를 설명하시오.