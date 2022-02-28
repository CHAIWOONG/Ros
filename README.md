# ROS
___
## ROS (Robot Operating System)
- 로봇용 오픈소스 * 메타 운영 체제
- 여러 프로세스 사이의 통신 부분을 담당하는 중간 다리 역할 수행
- 중간 통신 과정을 담당하여, Process를 분리하여 처리를 효율적으로 할 수 있음

## ROS 중요 개념
- Package : ROS 소프트웨어를 구성하는 주요 단위, ROS노드, ROS 독립 라이브러리, 데이터 세트, 구성 파일 3rd party 소프트웨어로 구성
  
  - include : 패키지에서 사용하느 헤더 파일이 있는 폴더 (.h file)
  - msg : 새로운 메시지를 정의할 떄, 메시지 유형이 포함된 폴더 (.msg file) 
  - src/package_name : 소스 코드를 포함하는 폴더 (.c, .cpp file)
  - srv : 새로운 서비스를 정의할 때, 서비스 유형이 포함된 폴더 (.srv file)
  - scripts : 실행 가능한 Python 스크립트를 포함하는 폴더 (.py .bash .sh file)
  - CMakeList.txt : Cmake 빌드 설정 파일
  - package.xml : 패키지 매니페스트 파일
- Master : 마스터를 통해, 노드의 이름을 등록하고, 검색하여 정보를 얻을 수 있음
- Node : ROS의 최소 단위의 프로세스. 실제 하나의 역할만 하도록 권장되어 있음, Node와 Node 사이의 통신은 메시지, 서비스, 파라미터를 통해 통신 가능
- Parameter Server : Master에 값을 전달하여, 코드 실행 중에 값을 변경 가능
- Bags : ROS에서 데이터를 저장 및 불러올 때 사용하며, Master에서 확인 가능한 Topic들을 모두 저장 가능하며, 이를 다시 재생하는 기능 제공
- Messages : 노드 사이의 전달하는 데이터
- Topics : 메시지를 식별하기 위해 이름을 붙여놓은 것. Topic을 보내는 것을 Publish, 받는 것을 Subscribe라고 함
- Services : 입력이 있을 때만 동작하는 형태의 데이터 송수신을 의미
- ### 노드 간의 통신 방법
  - Topic : 단방향 통신으로 연속적으로 데이터를 송수신하느 경우에 사용(ex. 센서 데이터)
  - Service : 양방향 통신으로 노드 간의 통신 요청과 동시에 응답하여 처리가 필요한 경우 사용
  - Action : Service와 유사. 장기적으로 수행되는 프로세스에서 피드백을 제공하는 양방향 통신

## ROS 명령어
ROS 명령어는 터미널에서 특정 기능이나 프로그램을 실행할 떄, 사용하는 인터페이스
- roscd : 위치한 ros 패키지의 폴더로 이동
- rosed : ros 패키지 내부 파일을 편집하는 명령어
- roscore : master를 실행하는 명령어
- rosrun : 패키지의 노드를 실행하는 명령어
- roslaunch : 여러 개의 노드 및 master도 함께 실행하는 명령어 (rosrun을 여러번 사용할 필요가 없다)
- rostopic : 등록된 Topic을 다루는 명령어
- rosnode : 등록된 Node를 다루는 명령어
- rosparam : 등록된 Parameter를 다루는 명령어
- rosbag : 등록된 Topic들을 저장 및 재생하기 위한 명령어
- rosmsg : 등록된 Message 유형을 다루는 명령어
- catkin_create_pkg : 새로운 패키지를 생성하는 명령어
- catkin_make : catkin 작업 공간의 C++ 파일을 빌드하는 명령어
- rosdep : 시스템 의존성 파일들을 설치하기 위한 명령어
- rviz : 3D 시각화를 위한 rviz를 실행하는 명령어
- rqt : 데이터 시각화를 위한 rqt를 실행하는 명령어
