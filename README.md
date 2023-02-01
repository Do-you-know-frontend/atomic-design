# Atomic Design

brad frost의 [아토믹 디자인](https://atomicdesign.bradfrost.com/chapter-2/)은 화학적 관점에서 영감을 얻은 디자인 시스템이다. 

![https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c56df7b7-07ef-4983-a6cb-c5b0001b734d/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094525Z&X-Amz-Expires=86400&X-Amz-Signature=cf83d0829d21bb2119036d541dbc3bd1a54bf2168da02711f6e3708117546031&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c56df7b7-07ef-4983-a6cb-c5b0001b734d/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094525Z&X-Amz-Expires=86400&X-Amz-Signature=cf83d0829d21bb2119036d541dbc3bd1a54bf2168da02711f6e3708117546031&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

모든 것은 `atom`(원자)으로 구성되어있고 `atom`(원자)들이 서로 결합하여 `molecule`(분자)이 되고, `molecule`는 더 복잡한 `organism`(유기체)으로 결합하여 궁극적으로 모든 물질을 생성한다. 

아토믹 디자인에서는 이 개념을 차용해서 컴포넌트를 `atom`, `molecule`, `organism`, `template`, `page`의 5가지 레벨로 나눈다.

![https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c565a0db-7db8-4a28-bdc2-2892ef32127f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094635Z&X-Amz-Expires=86400&X-Amz-Signature=58121fd1a8221ba585271d6fe0822a17ea5bc1e954110b8b3618bb3b6951c4ee&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c565a0db-7db8-4a28-bdc2-2892ef32127f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094635Z&X-Amz-Expires=86400&X-Amz-Signature=58121fd1a8221ba585271d6fe0822a17ea5bc1e954110b8b3618bb3b6951c4ee&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

단계별로 추상적인 것에서 구체화하는 단계를 가진다. 리액트의 컴포넌트 방식의 개발에 아주 잘 어울린다.

![[https://atomicdesign.bradfrost.com/chapter-2/](https://atomicdesign.bradfrost.com/chapter-2/)](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3c41d2f6-78b2-448f-93f5-ac752788e4f9/Untitled.png)

[https://atomicdesign.bradfrost.com/chapter-2/](https://atomicdesign.bradfrost.com/chapter-2/)

## Atom

말 그대로 원자. 더 이상 쪼갤 수 없는 컴포넌트이다. 

단일 `html element`, 텍스트, 애니메이션, 컬러 팔레트, 레이아웃도 포함될 수 있다. 디자인 시스템 개발에 유용하다.

![https://s3.us-west-2.amazonaws.com/secure.notion-static.com/9bd487bb-fff6-4c63-8913-6ed9eb80b56e/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T095322Z&X-Amz-Expires=86400&X-Amz-Signature=7e7c6a234b257f180557a4580d50c4c9895e4a70143af12e0f1f7502e9aaa588&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/9bd487bb-fff6-4c63-8913-6ed9eb80b56e/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T095322Z&X-Amz-Expires=86400&X-Amz-Signature=7e7c6a234b257f180557a4580d50c4c9895e4a70143af12e0f1f7502e9aaa588&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

## Molecule

여러 `atom`을 조합해 고유한 특성을 가진다. 아래 경우에는 `button` 아톰을 클릭해 `form`을 전송하는 `molecule`로 정의할 수 있다. 

한가지 일만 하는 것(SRP, Single Responsibility Principle)이 중요하다. 

![https://s3.us-west-2.amazonaws.com/secure.notion-static.com/cd866e27-179c-4589-a416-b01d498709eb/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094704Z&X-Amz-Expires=86400&X-Amz-Signature=008ed71238d1bde2d05a92ba8c2e134ce3b98af87b3e6862af485190ff55561e&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/cd866e27-179c-4589-a416-b01d498709eb/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094704Z&X-Amz-Expires=86400&X-Amz-Signature=008ed71238d1bde2d05a92ba8c2e134ce3b98af87b3e6862af485190ff55561e&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

`molecule`의 SRP는 재사용성과 UI에서의 일관성, 테스트하기 쉬운 조건이라는 이점을 가진다.

## Organism

`organism`은 앞 단계보다 좀 더 복잡하고 서비스에서 표현될 수 있는 명확한 영역과 특정 컨텍스트를 가진다.

“헤더 영역”과 같이 명확한 영역과 특정 컨텍스트(문맥)를 가진다. `atom`, `molecule`에 비해 좀 더 구체적으로 표현되고 컨텍스트를 가지기 때문에 `atom`과 `molecule`에 비해 상대적으로 재사용성이 낮아진다.

`molecules`로부터 `oraganisms`을 만드는 것은 독립적이고 재사용 가능하고 확장 가능한 컴포넌트들을 만들도록 한다.

![https://s3.us-west-2.amazonaws.com/secure.notion-static.com/35fc90d5-4d3f-42ce-90d5-1e5398b37bb1/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094735Z&X-Amz-Expires=86400&X-Amz-Signature=50d21fa76c0082dfabc167b056a285e09f333b5324710370375de34851ada252&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/35fc90d5-4d3f-42ce-90d5-1e5398b37bb1/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094735Z&X-Amz-Expires=86400&X-Amz-Signature=50d21fa76c0082dfabc167b056a285e09f333b5324710370375de34851ada252&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

![https://bradfrost.com/wp-content/uploads/2013/06/organism-examples.jpg](https://bradfrost.com/wp-content/uploads/2013/06/organism-examples.jpg)

## Template

페이지를 만들 수 있도록 여러 개의 `organism`, `molecule`들로 구성된다.

`template`들은 매우 구체적이다. 그리고 상대적으로 추상적인 `molecule`과 `organism`에게 컨텍스트를 제공한다.
실제 컴포넌트를 레이아웃에 배치하고 구조를 잡는 와이어프레임이다. 실제 콘텐츠가 없는 page 수준의 스켈레톤이라고 정의할 수 있다.

![https://s3.us-west-2.amazonaws.com/secure.notion-static.com/2c8b4e6b-72a6-462b-854c-b878c299c662/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094748Z&X-Amz-Expires=86400&X-Amz-Signature=837936348df5a4713552c8697e65673e8570cc93e2e868389df51f86cd4ce5be&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/2c8b4e6b-72a6-462b-854c-b878c299c662/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094748Z&X-Amz-Expires=86400&X-Amz-Signature=837936348df5a4713552c8697e65673e8570cc93e2e868389df51f86cd4ce5be&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

## Page

유저가 볼 수 있는 실제 콘텐츠를 담는다. `template`의 구체적인 인스턴스이다.

장바구니 페이지에 유저가 담은 상품이 없거나 10개를 담는 다양한 `template`의 인스턴스를 볼 수 있다.

![https://s3.us-west-2.amazonaws.com/secure.notion-static.com/d2b1dd02-7160-44a5-bf07-fc510a2061e2/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094806Z&X-Amz-Expires=86400&X-Amz-Signature=ac26c9e91226cfde639ebc857015fbd730a9ae110433f876cdb43bb13b817e6e&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/d2b1dd02-7160-44a5-bf07-fc510a2061e2/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094806Z&X-Amz-Expires=86400&X-Amz-Signature=ac26c9e91226cfde639ebc857015fbd730a9ae110433f876cdb43bb13b817e6e&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

## **Molecule과 Organism 을 나누는 기준의 주관성**

`molecule`은 `atom`으로 구성되어 SRP에 따라 1가지 책임을 지고, `organism`은 `atom`, `molecule`, `organism`으로 구성되어 서비스에서 Layout을 기준으로 나눌 수 있는 영역을 갖게 된다.

![https://s3.us-west-2.amazonaws.com/secure.notion-static.com/d81e9e58-eb9b-4b57-b6c1-419b6466a362/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094831Z&X-Amz-Expires=86400&X-Amz-Signature=31aa288d6281a010d1d9608810151d72a98153e321e888de0f4447da244507c5&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/d81e9e58-eb9b-4b57-b6c1-419b6466a362/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094831Z&X-Amz-Expires=86400&X-Amz-Signature=31aa288d6281a010d1d9608810151d72a98153e321e888de0f4447da244507c5&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

작성한 컴포넌트에 컨텍스트가 있는 경우에는 `organism`으로, 컨텍스트 없이 UI 적인 요소로 `SRP`를 지킬 수 있다면 재사용하기 쉬운 `molecule`로 작성

`molecule`의 컴포넌트 네이밍은 컨텍스트 없이 주로 UI 적인 네이밍이 포함된다. 

반면에 `organism` 네이밍은 컨텍스트가 포함된다.

판단하기 모호할 경우에는 일단 `organism`으로 작성한 후에 코드 리뷰를 통해 적절하게 변경할 수 있도록 논의를 나눈다.

## ****Organism을 나누는 기준****

`organism`은 UI에서 명확한 영역을 갖는다. 이 명확한 영역에 대한 정의는 주관적이라 여러 가지 방식으로 해석될 수 있다.

![https://s3.us-west-2.amazonaws.com/secure.notion-static.com/d394c02d-f546-45f4-ae6f-3c78d6862890/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094902Z&X-Amz-Expires=86400&X-Amz-Signature=7e29574cecdcb7b172e03cfb9dea219b91d6b630f96df82d2234e77fc79016c3&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/d394c02d-f546-45f4-ae6f-3c78d6862890/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094902Z&X-Amz-Expires=86400&X-Amz-Signature=7e29574cecdcb7b172e03cfb9dea219b91d6b630f96df82d2234e77fc79016c3&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

극단적으로는 A와 같이 큰 영역을 `organism`이라고 할 수 있고, B와 같이 비슷한 유형의 책임을 그루핑하여 구분할 수 있다.

A보다는 B와 같이 공통된 컨텍스트를 묶어 `organism` 컴포넌트로 표현하면 적당한 책임을 가진 컴포넌트를 작성할 수 있다. 

예를 들어 `CommentListToolbar` 컴포넌트의 경우 댓글 데이터를 다루는 책임을 가지고 있습니다. 또한 `Comment` 컴포넌트는 레이아웃이나 `Comment`를 리스트로 표현할 때 여백 처리를 쉽게 할 수 있습니다.

# **다시 돌아온 난제 - moecules과 organisms의 구분**

Atomic Design Pattern에서 `moecules`과 `organisms`이 문제가 되는 것은 명확한 분류기준이 없기 때문이다. 

### **뷰 컴포넌트와 비즈니스 컴포넌트로 먼저 나눠보자.**

일단 크게 컴포넌트를 2가지로 먼저 분리해보기로 하였습니다.

1. 뷰 컴포넌트(공통 컴포넌트)
2. 비즈니스 컴포넌트

뷰 컴포넌트는 `Input`, `Radio`, `Checkbox` 등 다른 프로젝트에서도 재사용이 할 수 있는 컴포넌트들입니다. 

비즈니스 컴포넌트는 그 프로젝트에서만 사용하는 데이터를 보여주기 위한 컴포넌트입니다. 

캘린더로 치면 일정 상세 팝업과 같은 컴포넌트입니다. 물론 비즈니스 컴포넌트들은 일부 뷰 컴포넌트의 조립을 통해서 만들어지지만, 그 프로젝트에서만 쓰이는 경우가 대부분이고 내부 상태관리 데이터와 강하게 결합이 되어 있는 컴포넌트를 의미합니다.

> 뷰 컴포넌트(공통): props를 이용한 독립된 형태
> 
> 
> **비즈니스 컴포넌트: 상태관리를 이용한 데이터와 결합하여 있는 컴포넌트**
> 

### **뷰 컴포넌트의 atoms > moecules > organisms**

뷰 컴포넌트에서의 `atoms`은 외부 의존성이 하나도 없기 때문에 `import`가 없는 컴포넌트가 `atom`이 됩니다. 

외부 의존성을 가지는 컴포넌트의 경우 `moecules`이 됩니다. 예를 들어 ‘SelectBox = (input + dropdown)’인 방식입니다. 

modal popup과 같이 독립적인 형태는 `organisms`으로 구분하였습니다.

### **비즈니스 컴포넌트의 atoms > moecules > organisms**

`moecules`는 엔티티를 나타내는 컴포넌트들을 모아둡니다. 좀 더 쉽게 이해하고 판단하기 쉽도록 array에 속한 컴포넌트들이라고 규칙을 정해봤습니다. 

`organisms`는 `moecules`의 아닌 것의 컴포넌트 집합입니다. 

`template`은 레이아웃을 의미합니다. 

`pages`는 상태가 다를 때 구분하는 용도로 사용합니다. (권한이 없어 사용을 하지 못할 때...) 이게 당연히 정답이 아니고 더 나은 구조를 계속 고민하고 있다.

# 이 또한 디자인 패턴…

- 우선 Atomic 디자인의 각 단계가 linear한 프로세스가 아니라는 것을 알아야 한다.
- `atom` 이 모여서 `molecule`이 되고  `molecule`이 모여 `organism`이 되고.. 이런 규칙이 딱 박혀있는 것이 아니라 각 요소들을 조합하여 `molecule`을 구성하고, `organism`을 구성하는 느낌으로 생각해야 한다.
- 각 요소들을 어떻게 분류하고, 실제로 적용할지 결정하는 것은 개발자에게 달렸다.

![https://s3.us-west-2.amazonaws.com/secure.notion-static.com/0621cb18-e62d-4269-bcbc-939003874c29/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094925Z&X-Amz-Expires=86400&X-Amz-Signature=5a7d297c67d61afb3276ac0978a1c558bc483d5d8174dc9ddb7e4c27b875184c&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/0621cb18-e62d-4269-bcbc-939003874c29/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T094925Z&X-Amz-Expires=86400&X-Amz-Signature=5a7d297c67d61afb3276ac0978a1c558bc483d5d8174dc9ddb7e4c27b875184c&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

## **아토믹 디자인은 왜 인기가 많나요?**

![https://sumini.dev/static/0b761fd98cc9beda00713399eddddabc/5ea4d/directory.png](https://sumini.dev/static/0b761fd98cc9beda00713399eddddabc/5ea4d/directory.png)

아토믹 디자인의 최대 장점은 바로 간단 명료하다는 것이다.

`Atom`, `Molecule`, `Organism`, `Template`, `Page`라는 이름으로 컴포넌트들을 분류하고, 이들이 합쳐져 상위 레벨의 컴포넌트를 완성하는 구조는 그럴싸하고, 직관적이고, 멋지다.

또한 UI의 복잡성을 효과적으로 억제할 수 있다. 중복되는 컴포넌트를 줄일 수 있고, 결과적으로 개발소요시간을 단축할 수 있다.

만들어진 컴포넌트들을 나열해보면 멋지고 체계적인 컴포넌트 테이블을 만들 수도 있다.

## **Atomic pattern의 단점**

### **러닝 커브가 매우 높다. (for 비개발자)**

기본적으로 아토믹 디자인은 컴포넌트 개념에 대한 높은 이해도를 필요로 한다.

각 컴포넌트들을 어떻게 분류할지가 꽤나 모호하고 논의할 여지가 많다. 예시와 함께 설명하겠다.

**1) 비슷하게 생겼지만 다른 분류의 컴포넌트가 존재한다.**

![https://sumini.dev/static/6c998fb229cc422e9536851b6f7da85e/1b853/molecule-cart-item-card.png](https://sumini.dev/static/6c998fb229cc422e9536851b6f7da85e/1b853/molecule-cart-item-card.png)

예를 들어, 위의 이미지에서 삭제버튼은 `atoms/button`으로, 구독버튼은 `molecules/button/channel-subscribe`로 구현했다.

구독버튼은 일반적인 버튼들과 다르게 **구독중이라는 state를 가지며, 이에 따라 다르게 작동**하기 때문이다. (구독중이 아닐 땐 구독, 구독중일 땐 구독취소)

`atoms/toggle-button`이라는 분류를 추가하는 방법도 생각해볼 수 있겠지만, 모든 토글버튼이 구독버튼과 동일하게 기능할 것이라고 기대하기 힘들기 때문에 현실적으로 어렵다.

**2) UI/UX가 모두 상당히 유사하지만, 개발 복잡도 때문에 분리하는게 나은 경우도 있다.**

컴포넌트의 특성과 관계 없이 순전히 개발적인 이유에서 분류를 바꿔야하는 경우도 있다.

![https://sumini.dev/static/9b78eb0f0342e2909b836167dfc5f3c8/03e1f/admin-buttons.png](https://sumini.dev/static/9b78eb0f0342e2909b836167dfc5f3c8/03e1f/admin-buttons.png)

위의 이미지는 핔 파트너 어드민의 테이블 상단에서 사용되는 버튼들이다.

여기서 새로고침버튼은 `atom`이고 엑셀/CSV 다운로드버튼은 `molecule`이다.

이유는 엑셀/CSV 다운로드버튼의 `click handler function`이 다른 버튼들보다 훨씬 거대하기 때문이다.

테이블의 data를 알맞게 formatting하는 함수, 전화번호/가격 등의 값들을 보기 좋게 parsing 하는 함수가 필요해 로직이 굉장히 길다.

atoms/button을 사용하면 이런 함수들을 모두 parent 컴포넌트에 위치시키고 onClick prop으로 전달해야한다..

parent 컴포넌트의 코드가 불필요하게 복잡해지기 때문에 분리할 수 밖에 없다.

**3) 이 모호하고 복잡한 분류를 기획자/디자이너가 설계해야한다.**

여기서 문제는 아토믹디자인이 컴포넌트 단위 디자인 및 개발을 실현하기 위해서, 설계를 기획자/디자이너가 맡아야한다는 것이다.

프론트엔드 이해도가 없는 신입 디자이너와 함께하고 있다면, 그들에게 **컴포넌트 단위의 체계적인 UI 설계를 기대하긴 정말 힘들다.**

React 컴포넌트의 state, prop 개념은 생각보다 비개발자가 100% 이해하기 어렵다.

어떤 컴포넌트가 스스로 데이터를 fetch할 수도, prop으로 전달받을 수도 있다는 것과 이 두 가지의 케이스별 구분 방법을 비개발자에게 온전히 이해시키는 것은 매우 힘들거나 불가능에 가깝다.

하지만 아토믹디자인을 제대로 적용하기 위해선 기획/디자인 단계에서부터 컴포넌트 단위의 체계화된 설계가 이뤄져야한다.

결국 당신은 체계적인 시스템을 완성하기 위해 모든 UI 논의 회의에 참석해야할 것이다.

이는 매우 비효율적이며, 기획자/디자이너에게 컴포넌트 분류에 대해서 설명해야하기 때문에 오히려 **의사소통 비용이 증가한다.**

### **개발자에게도 러닝 커브가 높다.**

세상에는 아토믹 디자인을 아는 개발자보다 모르는 개발자가 훨씬 많다.

새로운 개발자가 합류할 때마다 이 모호한 체계를 학습시켜야하며, 이는 학습 비용의 증가로 이어진다.

또 작은 컴포넌트 단위들을 합쳐 상위 레벨의 컴포넌트를 완성한다는 아토믹 디자인의 기본 철학은, 바꿔 말하면 상위 레벨의 컴포넌트를 만들기 위해 프로젝트 내에 존재하는 모든 작은 컴포넌트들을 학습하고 고려해야한다는 것이다.

새로 합류한 개발자에게 이를 알려주기 위해 기존 방식보다 훨씬 많은 문서와 예시가 필요할 것이다.

### **UI 변화에 유연하지 않다.**

기획/디자인의 전 과정이 컴포넌트 단위로 철두철미하게 이뤄진다면 정말 좋겠지만, 대부분의 경우엔 그렇지 않다.

기획/디자인 변경에 따라 서로 다른 두 컴포넌트를 하나로 합쳐야할 수 있고, 그 반대의 상황도 있을 수 있다.

또한 폰트 사이즈, 두께 등의 사소한 변경점들이 컴포넌트 체계에 치명적인 영향을 줄 수도 있다. 기획자/디자이너는 state/prop에 대한 이해도가 낮거나 없을 것이기 때문이다.

![https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a039c959-3433-4e91-9b26-bd3ebb5a616b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T095106Z&X-Amz-Expires=86400&X-Amz-Signature=26c5c39d8bea772a5119a75800a560e35e0eb2325359beaf8f70f0053e10905a&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a039c959-3433-4e91-9b26-bd3ebb5a616b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230201%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230201T095106Z&X-Amz-Expires=86400&X-Amz-Signature=26c5c39d8bea772a5119a75800a560e35e0eb2325359beaf8f70f0053e10905a&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject)

기존 Atomic Design에서는 재사용 가능한 컴포넌트를 만들기 위해, 아래 그림과 같이 Pages 단계에서 상태와 로직을 정의하고, 상태나 로직을 `Template`, `Organism`, `Molecule`, `Atoms`에 Props로 쭉 내려주어야 합니다.

이렇게 Props를 내려 꽂았을 때 만약에 `Page`에서 `Template`으로 내려줘야 할 State의 자료형이 바뀐다면,`Template`의 매개 변수를 바꿔줘야 하고, 이에 따라 `Organism`의 매개 변수도 바꿔줘야 하고, `Molecule`의 매개 변수를 바꿔줘야 하고, `Atom`의 매개 변수를 바꿔줘야 합니다. `State`의 자료형이 바뀌었을 때, 상당히 많은 부분의 코드가 바뀌어야 한다는 점이 우리에게 단점으로 다가왔습니다.

아토믹 디자인은 어느 정도의 변화 또는 대형 변화에는 최적화된 패턴이라 할 수 있습니다. 

그러나 변화가 누적되면서 각각을 구성하는 컴포넌트가 많아질 때는 답이 없습니다. 심지어 컴포넌트 간 의존성이 상하로 발생하기 때문에 **하위 컴포넌트에서 예상치 못한 에러가 발생하게 되면 모든 상위 컴포넌트가 엉망이 되는 일이 생기게 됩니다.**

# 이외의 디자인 패턴

## Presentational and Container 패턴

- Presentational 컴포넌트와 Container 컴포넌트로 나누어 개발한다.
- Presentational 컴포넌트는 가능한 작게 만들고, app에 대해 완전히 모르기 때문에 다른 app에서도 사용이 가능해야 한다. UI에 관한 상태만 가진다.
- Container 컴포넌트는 어떠한 동작을 할 지(로직)를 책임진다. 절대로 DOM 마크업 구조나 스타일을 가져서는 안된다. 상태를 가지고 있고, side-effect를 발생시킬 수 있다.

## 정리

프로젝트가 작을 때 Atomic Design Pattern을 활용하면 기존보다 훨씬 더 선명해지는 체계와 의식적으로 컴포넌트를 계층별로 배치하게 해주는 걸 알게 됐습니다. 

알파벳 순서로 잘 정리된 폴더구조를 보면서 계층에 대해서 많이 배우게 되고 체계가 잡힌다는 것도 알게 되었습니다.

그러나 점점 프로젝트가 커지다 보면 컴포넌트들을 도메인이나 의미와 관계없이 계층으로만 5단계로 나누는 것에서 한계점을 느끼게 됩니다. 그러면서 점점 모호해지는 구분으로 인해서 잘 만든 컨벤

션과 새로운 구조가 필요하다는 것도 알게 되었습니다

이를 위해서는 원자 단위를 보수적으로 관리할 필요가 있고, 이벤트 핸들링에 대해서는 수동적으로 관리할 필요가 있습니다. 또한 입력 필드와 같이 데이터를 처리하는 값에 대해선 원자 단위보다는 **한 단계 위인 분자 수준의 컴포넌트에서 관리하는 게 방어적 프로그래밍**이 될 수 있습니다.

**분류기준을 많이 만들어 두고, 그에 맞는 좋은 이름을 붙이고, 여기에 명확한 규칙을 만들어보는 것이 방법** 인 것 같습니다.
