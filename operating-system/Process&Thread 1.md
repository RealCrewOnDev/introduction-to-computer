# 프로세스와 스레드(1탄)  


## 프로세스란?  

- 컴퓨터에서 연속적으로 실행되고 있는 컴퓨터 프로그램  
- 프로그램이 구동이 되어, 주메모리에 적재되면, 메모리 상에서 실행되는 작업의 단위  
- `작업` 이라고도 부른다. (작업관리자에 들어가면 프로세스라고 써있는걸 볼 수 있음!)  

## 프로세스 특징  

- 하나의 프로세서(CPU)는 한 순간 하나의 프로세스만 실행할 수 있다!  
> 그런데 컴퓨터를 쓰다보면 우리는 여러개의 프로세스를 동시에 실행한다.  
> 음악을 들으며~ 문서작업하다가~ 카카오톡도 하고~ 어떻게 동시에 가능할까?  
==> 하나의 프로세서가 빠르게 프로세스들을 왔다리 갔다리 하는 것이다! --> 이것이 바로 멀티태스킹!  

- 하나의 작업을 여러개의 프로세서(CPU)가 하는 것!(듀얼코어..쿼드코어..등등) --> 이것은 멀티프로세싱!  


## 프로세스 생명주기(LifeCycle)  

![프로세스상태](../images/프로세스와스레드2.PNG)  

- 생성(new)  
- 준비(ready)    
- 실행
- 대기(waiting)  
- 종료(terminated)  

## 프로세스 제어블록(PCB)  

- 프로세스 제어블록이란?  

커널의 자료구조이다.  
프로세스의 정보를 포함하고 있다.  
모든 프로세스는 고유한 PCB를 갖는다.  
프로세스 생성 시 만들어지고, 프로세스가 종료되면 삭제된다.  
프로세스의 중요 정보를 포함하고 있기 때문에, 일반 사용자가 접근하지 못하도록 보호된 메모리 영역에 있다.  


- PCB 포함정보  
 ![PCB 포함정보](../images/프로세스와스레드3.PNG)  
 
 
- 문맥교환(Context Switching)  

CPU가 이전의 프로세스 상태를 PCB에 보관하고, 또 다른 프로세스의 정보를 PCB에서 읽어, 레지스터에 적재하는 과정!  
레지스터에 프로세스 정보가 바뀌는 것이다.  
위의 프로세스 상태에서 interrupt 가 발생하는 과정이 문맥교환이 일어나는 것이다.  
> 예를 들어 현재 실행 중인 프로세스가 있다.  
> 그런데 우선순위가 먼저인 프로세스가 들어왔다.  
> 지금 실행하는 프로세스를 실행상태에서 준비상태로 변경하고,  
> 우선순위가 높은(현재 준비상태) 프로세스를 실행상태로 변경한다.  
> 이것이 바로 문맥교환!  

## 프로세스 메모리 구조  

![프로세스메모리구조](../images/프로세스와스레드4.PNG)

- Code 코드  
- Data 전역변수  
- Heap 동적메모리 할당  
- Stack 지역변수  


### 참고자료  

(https://jhnyang.tistory.com/33)  
(http://tcpschool.com/)  


 
 




  
