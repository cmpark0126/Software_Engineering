## **Requirement Gathering**
---
### Analyze Requirements
FR: Functional Requirements
NFR: Non-Functional Requirements

1. Grading Server
    - 한 번에 접근할 수 있는 유저의 수
    - 백업 서버

1. Add User
    - 기관

1. Class
    - 포함 정보 (NFR)
        * 담당 교수(1..\*)
        - TA(0..\*)
        - 학생(0..\*)
    - 생성 권한 (FR)
        - [Who has authority]는 Class 게시판을 생성가능
    - 정보 권한 (NFR) (추후에는 정보 접근과 수정 권한을 나누어서 생각)
        - [Who has authority]는 Class에 대해 모든 정보에 접근 및 수정 가능
        - 담당 교수는 Class에 대해 모든 정보에 접근 및 수정 가능
        - TA는 담당 교수가 권한을 허락한 정보에 접근 및 수정 가능
        - 학생은 자기 자신에 대한 것과 수업에 관하여 공개된 정보에만 접근 및 수정 가능

1. Coding Test 출제
    - 포함정보
        - Test case(1..\*)
        - 시작 시간(0..1) // if start time set empty, it will be start just after construct coding test.
        - 끝 시간(1)
        - 유효 IP(0..\*)
    - 권한
        - 담당 교수가 출제 가능
        - TA의 경우 담당 교수의 허가가 있을 경우 출제 가능

1. Coding Test 응시

1. Coding Test 응답 제출

1. Coding Test 채점

### **I. Functional Requirements**
1. Grading Server
    -

1. 프로그램 구동 환경
    - The system should allow user can access the system on a particular operating system environment: particularly the OS on the school computer

1. 프로그램 자체 특징
    - 프로그램은

1. Add User
    - 특정 기관에서 제공하는 이메일을 가지고 특정 기관 회원으로 가입할 수 있다.

1. Class board
    - The system should allow a user who has authority to create the class board particular information to make class board: list of professors in charge of class and list of students attending class

1. Set Coding Test
    - The system should allow a user who has authority to set coding Test with particular information to make coding Test: list of usable programming languages, list of test cases, start and end time of the coding test and list of accessible IP address to set limit areas taking coding test.

1. Take Coding Test
    - The system should allow all users in a particular class to access coding test which is set by a professor or a user acting as a proxy of a professor during test time.

    - The system should allow all users who take a coding test to use the compiler of the system to test their code before submitting.

    - The system should allow all users who take a coding test to select programming language among the list of programming languages which is set by a professor in charge of a class or a user acting as a proxy of a professor like a teaching assistant

    - The system should allow all users who take a coding test to recognize the time of the server and the remaining time of the coding test to avoid confusing answer submission time

    - 응시자는 스스로 Test case를 만들어서 프로그램 테스트에 사용할 수 있으며, 이 때에 시스템은 디버깅 메세지를 모두 볼 수 있다.
    - 응시자는 출제자가 등록한 Test Case는 볼 수 없으며, Test case의 디버깅 메세지를 볼 수 없다.


1. Coding Test 응답 제출
    -

1. Coding Test 채점


### **II. Non-Functional Requirements**
1. Grading Server
    - The solution shall be at 100 percent available for all users who in situation taking coding test. If the system faces the situation that cannot handle all users request service, the system needs to provide service to users who in the situation taking the coding test preferentially.
    (Available)

    - The solution shall be at 100 percent available for all users who in situation taking coding test.

1. 프로그램 구동 환경

1. 프로그램 특징
    - 유저를 권한에 따라 나누어야 한다.

1. Add User
    -

1. Class board
    - The System shall give authority to create the class board which helps professor manage the class associated with grading issues like setting coding test and giving a grade to students only a dean or a user acting as a proxy of a dean. (Security)

1. Coding Test 출제
    - The System shall give authority to set coding test only a professor in charge of a class or a user acting as a proxy of a professor like a teaching assistant. (Security)

1. Coding Test 응시
    - The System shall block access to server with unapproved method to protect set of information like test cases of coding test and grading. (Security)

1. Coding Test 응답 제출

1. Coding Test 채점
    - The System shall block unapproved access to the server to protect the set of information like test cases of coding test and grading. (Security)
