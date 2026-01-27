---
created: 2026-01-28T06:50
updated: 2026-01-28T07:07
---
# controller와 restcontroller 의 차이는?

# 내 답변
controller는 mvc 모델에서 사용자와 view,model 레이어를 이어주는 레이어로 대부분 url로 호출 되었을 때 해당하는 비지니스 로직을 수행하고 view 레이어를 이어주는 역할을 한다

restController는 이러한 컨트롤러의 역할을 하나 동작하는 웹이 REST의 성질을 가질 때 주로 사용한다
restController를 사용하면 사용자의 요청에 의해 리턴 값을 view레이어가 아닌 응답의 body 부분에 해당하는 값을 자동으로 변환해 리턴해준다 

# 답변

두 어노테이션 차이점은 HTTP 응답 처리 방식에 있다

@Controller
주로 뷰를 반환하는 컨트롤러를 정의할때 사용됨
메서드가 반환한 값은 뷰 리절버에 의해 해석되어 jsp,Thymeleaf등 같은 템플릿 엔진을 통해 html을 생성한다

@RestController
주로 RESTful 웹 서비스 api를 정의할때 사용된다
메서드가 반환하는 값은 자동으로 json 또는 xml 형식으로 변환되어 http 응답 본문에 포함됨
@Controller 와 @ResponseBody 의 결합된 형태이다

# 배운 점
REST 에 대한 개념을 헷갈려한다
질문이 기술적이라면 기술적으로 답해야한다

# 함께 보면 좋은 자료
[[RESTful]]