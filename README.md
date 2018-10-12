🎓 Modern C++
-------------------------------
🎓 C++의 주요 특징
- 멀티테스킹 확장, 런타임 성능 향상, 완전한 새로운 기능
- 런타임 성능 향상: 머티태스킹 메모리 모델, 가변인장 등 문법 제공, 메모리와 계산속도 최적화
- std:tr1 namespace lib std included
- C++14: C++11 버그 수정 약간 계정
- C++ 자체 표준 표준 라이브러리 포함 STL(Standard Template Library) 포함
- ✋ ADT: 객체 속성 기능 도출 과정의 모델링 추상화 설계 단계 Abstract Data Type C++ header file 산출물
-------------------------------

🎓 Namespace
- using namespace std
<pre><code>
namespace 네임스페이스명
{
   선언내용; (클래스, 함수, 변수 등을 정의)
}

#include <iostream>
using namespace std;
namespace first {
    int value =1;
}
namespace second {
    int value =2;
}
int main() {
    cout << first::value;
    cout << sencond::value;
}
</code></pre>




- 자료형 별칭 만들기
  - using [별칭] = [기존자료형] 
    - using block = double;
<pre><code>
int main() {
    using block = double;
    using chain = int;
      
    block eos = 123.40;
    chain ether = 678;
       
}
</code></pre>




