# openssw 컴퓨터공학과 20185034학번 김태완 
# readme 파일 작성

# getopt
shellscript로 프로그램을 만들다 보면 실행 인자 및 옵션을 필요로 하는 
경우가 많이 있습니다. shellscript에서 실행 옵션을 구현을 하는 방법은 
getopt 함수를 쓰면 매우 간단해집니다.

간단한 실행 옵션 예제
이 파일은 실행 옵션 기능을 확인하기 위해 간단히 만든 스크립트입니다. 
크게 사용법, 실행 옵션 설정, 실행 옵션 확인 이렇게 세 부분으로 나뉘어 
있습니다. 
필요한 옵션을 만들 때에는 빨간색으로 표시된 부분을 주의해서 변경해야 
합니다.

- 인자가 있는 실행 옵션

옵션 뒤에 ":"를 붙여줍니다. 아래 예에서는 "m" 옵션과 "u"옵션이 
해당합니다.

- 인자가 없는 실행 옵션

옵션만 정의합니다. 아래 예에서는 "f", "q", "v", "d", "g", "h" 옵션이 
해당합니다.

# getopts

쉘 에서 명령을 실행할 때 옵션을 사용하는데요. 스크립트 파일이나 함수를 
실행할 때도 동일하게 옵션을 사용할 수 있습니다. 
사용된 옵션은 다른 인수들과 마찬가지로 $1, $2, ... positional parameters 
형태로 전달되므로 스크립트 내에서 직접 옵션을 해석해서 사용해야 됩니다. 이때 옵션 해석 작업을 쉽게 도와주는 명령이 getopts 입니다.

옵션에는 short 옵션과 long 옵션이 있는데 getopts 명령은 short 옵션을 
처리합니다.

- short 옵션의 특징
short 옵션은 다음과 같이 여러 가지 방법으로 사용할 수 있습니다. 
그러므로 getopts 명령을 이용하지 않고 직접 옵션을 해석해 처리한다면 
옵션 처리에만 스크립트가 복잡해질 수 있습니다.

- long 옵션의 경우
--posix, --warning level 와 같은 형태로 사용되는 long 옵션은 
short 옵션과는 달리 붙여 쓸 수가 없기 때문에 사용방법이 간단하여 
직접 해석해서 처리하는 것이 어렵지 않습니다. 


 # sed

- 파일 또는 입력을 한번에 한행씩 처리하여 화면으로 출력한다.
- 파일의 마지막행까지 처리를 완료하면 종료한다.
- 직접 파일을 수정하지 않고 메모리의 임시기억장소에 저장하고 편집한다.
- sed 편집기는 입력파일의 전체행에 대하여 작업을 진행하는데 
  주소를 지정하면 편집하고자 하는 행을 선택할수 있다.

- sed 형식 
- sed 'command' filename
- sed 'value' member

# awk

- 자료 처리 및 레포터 생성에 사용하는 프로그래밍 언어.
- 입력 데이터로 표준입력이나 여러개의 파일 또는 다른 프로세스의 결과를 사용할수 있다.
- 데이터를 조작할수 있기 때문에 쉘스크립트나 소규모데이터베이스 관리에서 중요하게 사용된다.
- 사용자가 지정한 패턴 검색이나 특별한 작업을 수행하기 위해 파일을 행단위로 조사
- 특정한 작업이 정의 되지 않은 패턴에 대해서는 단지 출력만 한다.
- 패턴없이 액션이 정의되면 해당 액션에 의해 지정된 모든행에 대해서 처리가 이루어진다.

- awk 형식
- awk 'pattern' 파일명
- awk "{action}" 파일명
- awk 'pattern {action}' 파일명
