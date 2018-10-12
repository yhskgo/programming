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

- auto형 변수: 초기값 필요
  - auto 변수명 = 초기값(상수 변수 함수 모두 가능)
- decltype형: 초기값 불필요
  - decltype(함수f())[선언할 변수]
  - decltype(변수)[선언할 변수]
  - decltype((변수))[선언할 변수]


🎓 인라인 함수
- 일반 함수: 메모리상 점프, 복잡한 과정
- 인라인 함수: 단순 과정 대체, 함수 정의부가 실행코드 대체하여 실행 속도 빠름, 단점은 함수 정의부가 길면 별로...
<pre><code>
inline 반환형 함수명(매개변수 목록);
</code></pre>
- ex)
<pre><code>
#include<iostream>
using namespace std;

class Jacob
{
  void Eat(int SteakWeight);
  inline void EatInline(int SteakWeight);
};

int main(void) {
  Jacob jacob;
  jacob.Eat(500);
  jacob.EatInline(500);
  return 0;
}

void Jacob::Eat(int SteakWeight)
{
  cout << "Eat()::Jacob is " << SteakWeight << "eat g steak" << endl;  
}

inline void Jacob::EatInline(int SteakWeight) {
  cout << "EatInline()::Jacob " << SteakWeight << "eat g steak" << endl;
}
</code></pre>

🎓 람다 함수
- lamda 함수: 인라인 함수 like, also 가독성, C++11이상 부터 사용 가능
- [] [=] [&]
<pre><code>
#include <iotream>
using namespace std;

Class Jacob {
  public:
    void eat(int steakWeight);
    inline void eatInline(int steakWeght) {
      cout << "eatInline()::Jacob is" << steakWeight << "g steak" << endl;
    }   
};

int main(void)
{
  Jacob jacob;
  jacob.eat(1000);
  jacob.eatInline(1000);
  [](int steakWeight){cout << "eatLamda()::Jacob is eating" << steakWeight << "g steak" << endl;}(1000);
  return 0;
}

void Jacob::eat(int steakWeight){
  cout << "eat()::Jacob eat " << steakWeight << "g steak" << endl;
}
</code></pre>
