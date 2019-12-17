# 강의 정리중

{% embed url="https://github.com/spring-projects/spring-petclinic" %}

이 위 링크가 이 강의에서 사용되는 소스이다.

1~2강은 인텔리제이에 프로젝트 받아오는 과정.

3강

log를 debug레벨로 보고싶을때 spring-boot 프로젝트인 경우 src/resoruces/application.properties 

여기서 

```text
# logging.level.org.springframework.web=DEBUG
```

윗 부분을 주석처리 해제하면 됨. - 기존에는 info level이었음

주석해제하고 실행하

o.s.web.servlet.DispatcherServlet : Initializing Servlet 'dispatcherServlet'

등등 dispatcherServlet이 열일하는게 보임.  스프링이 제공하는 디스패처서블렛이 초기화된걸 볼 수 있음.



근데 왜 

```text
java -jar target/*.jar
```

위 명령어를 치면 잘 되는데 이 명렁어 전에 ctrl+shift+f10으로 자바파일을 실행시켰을때 css가 왜 안먹을까 의문

이클립스랑 비슷하게 디버그모드 실행시켜서 볼 수 있고 옆에 variable탭에서 변수들 확인가능하다.

f8 한줄 실행 f9 진행



```text
@GetMapping("/owners/find")
public String initFindForm(Map<String, Object> model) {
    model.put("owner", new Owner());
    return "owners/findOwners";
}
```

여기서 return 된 값은 view를 의미하는데 resources/owners/findOwners를 찾으면 됨.

강의 과제 - firstname으로 검색바꾸고 %firstname% 바꿔줘야됨.

```text
@Query("SELECT DISTINCT owner FROM Owner owner left join fetch owner.pets WHERE owner.firstName LIKE :firstName%")
```

Like:%firstName% 이 아니라 :앞에 붙여줘야됨 %:firstName% 이렇게.

그리고 age 추가해주는데 db에 컬럼이 없어서 안됨.

application.properties에 db스키마파일이랑 db데이터파일이 어디저장되어있는지 나옴.



5강

IOC

스프링에서 쓰는 객체를 Bean이라 한다.

6강

인텔리제이 클래스 옆에 초록원 모양이 있으면 bean으로 등록되있는거다.

ioc 컨테이너 안에 있는 bean들만 서로 의존성 주입을 해줄 수 있다.











