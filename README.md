# 오픈소스 과제 (리눅스 명령어와 메크로 명령어 정리!)

> ## 1)Top 명령어
> 
>> top명령어는 현재 OS의 상태를 나타내주는 CLI 어플리케이션이다.
>>
>> 여기서 그럼 CLI 어플리 케이션은 무엇인가?
>> CLI 어플리케이션은 App center 서비스를 사용하고 실행할 명령 시퀀스를 스크립팅하는 도구이다.
>> 또한 top 명령어는 메모리 사용량, CPU사용량등을 나타내주며 top이 실행되는 동안 주기적으로 업데이트를 해줘서 실시간으로 확인 가능하다.
>>
>> <img src= "https://user-images.githubusercontent.com/105635950/170813632-cea6a599-caca-4bc5-a632-c7af30299ca7.png" width ="75%" height ="75%"/>
>>
>> ### 시스템 현재 시간, OS가 살아있는 시간, 유저 세션수
>> 
>> 이렇게 제 컴퓨터의 실시간 os의 상태를 알수 있다. 이제 이 그림에 대한 설명을 할것이다. 
>> 맨 첫줄 의 절반은 시스템의 현재 시간과 os가 살아있는 시간과 유저 세션수를 순서대로 표시해 놓은것 이다.
>>
>> ### Load Average
>>
>> 다음은 load Average구간으로 CPU load의 이동 평균을 표시하는 영역이다.
>>
>> ### Task
>> 
>> 2번째 줄에는 Task에 관한 내용이다. Tasks는 현재 프로세스들의 상태를 나태내주는 영역이다. 
>> Total은 전체 프로세스, running은 running 상태인 프로세스, sleeping은 대기상태인 process, stopped는 종료된 프로세스, zombies는 좀비상태인 프로세스의 수를 나타낸다.
>> 
>> Task 아래줄인 3번째 줄의 %Cpu는 cpu의 사용량을 나타내는 영역이다. 이 영역은 cpu가 어떻게 사용되고 있는지 보여주는 영역이다. 
>> us는 프로세스의 유저 영역에서의 cpu 사용률이고 sy는 시스템, ni는 프로세스의 우선순위 설정에 사용하는 cpu 사용률이고 id는 사용하지 않는 비율, wa는 IO즉 input output이 완료될때가지 기다리고 있는 cpu 양이다. hi는 하드웨어 si는 소프트웨어를 나타내고 st는 VM에서 사용하는 cpu 사용률이다. 
>>
>> ### 디테일 영역
>> 
>> 다음 줄부터 표 전까지의 줄은 메모리 사용량을 나타내는 영역이다. RAM의 메모리 영역을 첫번째 줄에서 그리고 아랫줄에서는 디스크를 메모리 처럼 이용하는 Swap 메모리 영역이다. 
>> 이제 표처럼 보이는 영역이 있다. 이 영역은 디테일 영역으로 현재 실행되고있는 프로세스에 대한 상세한 내용이 나오게 된다. 
>> 위 디테일 영역의 말을 정리해 보겠다.
>> * PID
>>> * PID는 프로세서 ID이다.  
>> * USER 
>>> * 해당 프로세서의 USER 이름이다.
>> * PR , NI 
>>> * PR은  커널에 의해서 스케줄링되는 우선순위를 나타낸다.
>>> * NI는 PR에 영향을 주는 nice라는 값이라고 한다.
>> * VIRT, RES, SHR, %MEM
>>> * 이 명령어 들은 해당 필드들의 프로세스의 메모리와 관련이 있다.
>>> * VIRT는 heap,stack과 같은 메모리를 포함한다
>>> * REST는 RAM에서 사용중인 메모리를 나타낸다.
>>> * SHR은 다른 프로세스와 공유중인 공유메모리를 나타낸다.
>>> * %MEM은 RAM에서 RES가 차지하는 비율을 나타낸 것이다. 
