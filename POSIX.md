# POSIX

### POSIX?

POSIX는 이식 가능한 운영 체제 인터페이스(Portable Operating System Interface)의 약어입니다. 이것은 IEEE에서 지정한 표준 집합으로, 운영 체제 간의 호환성을 유지하기 위해 사용됩니다. 따라서 POSIX 표준을 준수하는 소프트웨어는 POSIX 표준을 준수하는 다른 운영 체제와 호환될 수 있습니다.

그 이유로 우리가 Linux 및 Unix 기반 운영 체제에서 사용하는 대부분의 도구는 거의 동일하게 작동합니다. 예를 들어, ps 명령을 사용하면 OpenBSD, Debian 및 macOS에서 동일하게 작동해야 합니다.

<br>

`운영체제의 종류`

다양한 종류의 운영 체제가 있습니다. 이 중에서도 주요한 종류는 다음과 같습니다.

- **실시간 운영 체제 (RTOS)** : 이러한 시스템은 데이터를 실시간으로 처리하도록 설계되어, 데이터가 수신되는 대로 처리할 수 있습니다. 예를 들어 `VxWorks, QNX` 등이 있습니다.
- **단일 사용자, 단일 작업 운영 체제** : 이러한 운영 체제는 한 번에 하나의 사용자가 한 프로그램만 실행할 수 있도록 설계되어 있습니다. 예를 들어 `MS-DOS, CP/M` 등이 있습니다.
- **단일 사용자, 다중 작업 운영 체제** : 이러한 운영 체제는 단일 사용자가 여러 프로그램을 동시에 실행할 수 있도록 허용합니다. 예를 들어 `Microsoft Windows, macOS` 등이 있습니다.
- **다중 사용자 운영 체제** : 이러한 운영 체제는 여러 사용자가 동시에 같은 컴퓨터에 액세스할 수 있도록 허용합니다. 예를 들어 `UNIX, Linux` 등이 있습니다.
- **분산 운영 체제** : 이러한 운영 체제는 독립적인 컴퓨터 그룹을 관리하고 하나의 컴퓨터처럼 보이게합니다. 예를 들어 `Apache Hadoop, Google File System` 등이 있습니다.
- **임베디드 운영 체제** : 이러한 운영 체제는 모바일 폰 및 기타 휴대용 장치와 같이 제한된 리소스를 가진 작은 장치에서 실행되도록 설계되었습니다. 예를 들어 `Android, iOS` 등이 있습니다.

<br>

`우리가 일상에서 보는 운영체제`

Windows와 macOS는 `기본적으로 싱글태스킹 운영 체제`이지만, `멀티태스킹 기능`을 갖추고 있습니다.

Windows에서는 한 번에 하나의 프로그램이나 작업만이 전면에서 실행될 수 있지만, 운영 체제는 여러 프로그램이나 작업을 동시에 백그라운드에서 실행할 수 있습니다. 예를 들어, 전면에서 문서를 작업하면서 백그라운드에서 여러 프로그램을 실행할 수 있습니다. 이것은 전면에서는 싱글태스킹 운영 체제이지만, 멀티태스킹을 하는 것처럼 보입니다.

반면, `macOS`는 여러 프로그램이나 작업을 동시에 실행할 수 있는 `멀티태스킹 운영 체제`입니다. Windows와 마찬가지로, 사용자가 전면에서 프로그램이나 작업을 수행하는 동안 여러 프로그램이 백그라운드에서 실행될 수 있습니다. 하지만 Windows와 달리, macOS는 동시에 여러 창이나 심지어 여러 데스크탑을 전면에 표시할 수 있기 때문에 사용자는 여러 작업을 동시에 수행할 수 있습니다.

<br>

`window, macOS 와 POSIX`

윈도우 및 macOS는 모두 UNIX 및 Linux에서 비롯되었습니다. macOS는 Darwin이라는 UNIX와 비슷한 운영 체제를 기반으로 하고 있으며, Windows는 시간이 지남에 따라 UNIX와 Linux의 일부 요소를 채택했습니다. 그러나 양쪽 운영 체제 모두 POSIX 표준과 완전히 호환되지 않습니다. POSIX 표준은 이 표준을 준수하는 다른 운영 체제 간의 호환성을 보장하기 위해 사용됩니다.

<br></br>

`POSIX 버전`

POSIX가 참조하는 표준 집합은 IEEE Std 1003.n-yyyy로, n은 IEEE Std 1003.1과 같은 버전 번호로 대체될 수 있습니다. 우리는 IEEE Std 1003.1을 POSIX.1로도 참조할 수 있습니다. 현재 POSIX.1의 버전은 IEEE Std 1003.1-2017입니다.

POSIX.1은 응용 프로그램 이식성, C 인터페이스 및 프로세스 생성 및 종료, 프로세스 환경 조작, 파일 및 디렉토리 액세스 및 간단한 입출력과 같은 기본 작업을위한 시스템 서비스의 동작을 정의합니다.

반면에, POSIX.2는 명령 인터프리터, 이식 가능한 쉘 프로그래밍, 사용자 환경 및 관련 유틸리티를 설명합니다. 두 표준 모두 기존 UNIX 관행과 경험에 강력하게 영향을 받았습니다.

<br></br>

`C API`

POSIX는 C 언어를 기반으로 표준을 정의합니다. 따라서 프로그램은 소스 코드 수준에서 다른 운영 체제로 이식 가능합니다. 그러나 우리는 표준화 된 어떤 언어에서도 구현할 수 있습니다.

POSIX C API는 ANSI C 표준에 다음과 같은 기능을 추가합니다.

- 파일 조작
- 프로세스, 스레드, 공유 메모리 및 스케줄링 매개 변수
- 네트워킹
- 메모리 관리
- 정규 표현식

<br>

### 개념

POSIX는 C API 외에도 프로그램 작성을 위한 규칙을 추가했습니다. `포인터 유형의 초기화`와 `동시 실행에 대한 안전성`과 같은 규칙을 추가했으며, 이미 사용 중인 경우 `메모리 수정을 제한하는 메모리 동기화 규칙`을 시행합니다. 이외에도, `디렉토리 보호 및 파일 액세스에 대한 보안 메커니즘`을 명시합니다.


<br>

### 환경 변수

<br>

**예약된 환경 변수**

- `COLUMN`은 터미널 화면의 너비를 정의합니다.
- `HOME`은 사용자의 홈 디렉토리 경로를 정의합니다.
- `LOGNAME`은 사용자의 로그인 이름을 정의합니다.
- `LINES`는 사용자가 선호하는 터미널 화면 라인을 정의합니다.
- `PATH`는 실행 가능한 이진 파일을 위한 콜론으로 구분된 경로를 정의합니다.
- `PWD`는 현재 작업 디렉토리를 정의합니다.
- `SHELL`은 현재 사용 중인 셸을 정의합니다.
- `TERM`은 터미널 유형을 정의합니다.

**POSIX 표준은 각 범주에 대해 다음 환경 변수를 정의합니다.**

- 문자 분류에 대한 `LC_TYPE`
- 문자의 순서를 정의하는 `LC_COLLATE`
- 통화 형식에 대한 `LC_MONETARY`
- 숫자 형식에 대한 `LC_NUMERIC`
- 날짜 및 시간 형식에 대한 `LC_TIME`
- 프로그램 메시지 (정보 메시지 및 로그 포함)에 대한 `LC_MESSAGES`

<br>

### 정규 표현식

`정규 표현식(RE)은 텍스트를 찾기 위한 검색 패턴을 정의하는 문자열입니다.`

 C 표준 라이브러리는 RE을 구현하며, awk, sed, grep 등의 프로그램에서 백엔드로 사용됩니다.

POSIX 준수 구현에서는 **기본 정규 표현식(BRE)** 또는 **확장된 정규 표현식(ERE)**을 사용할 수 있습니다. 

BRE은 텍스트 검색을 위한 기본 표기법을 제공하며, ERE은 더 많은 표기법을 지원합니다. `대부분의 POSIX 준수 유틸리티는 BRE에 크게 의존`하며, 고급 텍스트 조작 유틸리티는 ERE도 지원합니다.

<br>

또한, BRE와 ERE에 대해 다음과 같은 몇 가지 요구 사항이 적용됩니다.

- BRE과 ERE은 `NUL 문자로 끝나는 문자열`에서 작동해야 합니다.
- 리터럴 이스케이프 시퀀스와 새 줄 문자는 정의되지 않은 결과를 생성합니다. 따라서 프로그램에서 이들을 일반 문자로 처리해야 합니다.
- POSIX는 RE 또는 일치할 텍스트에서 명시적 NUL 문자의 사용을 허용하지 않습니다.
- 우리의 구현은 기본적으로 대소문자를 구분하지 않는 검색을 수행할 수 있어야 합니다.
- 우리의 RE 길이는 256바이트를 초과해서는 안 됩니다.

<br>

### 디렉터리 구조

대부분의 메이저한 리눅스 배포판은 파일 시스템 계층 표준(Filesystem Hierarchy Standard, FHS)을 준수합니다.

`FHS는 설정 가능한 트리 형태의 디렉터리 구조를 정의합니다.` 계층 구조에서 첫 번째 디렉터리는 루트 디렉터리이며, 모든 다른 디렉터리, 파일 및 특수 파일은 그것에서 분기됩니다.

<br>

tree 유틸리티는 디렉터리 구조를 더 잘 드러낼 수 있습니다.

```
$ tree / -d -L 1
/
├── bin -> usr/bin
├── boot
├── dev
├── etc
├── home
├── lib64 -> usr/lib
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin -> usr/bin
├── sys
├── usr
└── var
```

<br>

계층 구조는 구성 가능하지만, 우리의 프로그램은 루트 디렉터리와 /dev 디렉터리 아래에 파일이나 디렉터리를 만들지 않아야 합니다.

 그러나 XDG 기본 디렉터리와 같은 사용자 디렉터리 아래에 파일 및 디렉터리를 만들 수 있습니다. 또한, 우리는 /tmp 디렉터리를 사용하여 일시적인 파일 및 디렉터리를 만들 수도 있습니다.

 <br>

### 유틸리티

UNIX/Linux 환경에서 유틸리티에 익숙해지면 대부분의 유틸리티가 동일한 동작을 수행한다는 것을 알 수 있습니다. 

예를 들어, 우리는 거의 모든 UNIX/Linux 유틸리티에 대해 -h 옵션이 도움말 텍스트를 인쇄한다는 것을 알고 있습니다. 

이 일관성은 POSIX에서 설명하는 규칙 덕분입니다. POSIX는 프로그래머가 우리의 유틸리티 프로그램을 구현하는 방법에 대해 여러 가지 규칙을 정의합니다.

POSIX는 우리의 유틸리티 프로그램에서 다음과 같은 인수 구문을 구현하는 것을 권장합니다.

```
utility_name [-a][-b][-c option_argument]
[-d|-e][-f[option_argument]][operand...] <parameter name>
```

<br>

여기서 세분화해 보겠습니다.

- `utility_name`은 옵션과 인수가 뒤따르는 유틸리티의 이름입니다.
- `대괄호 안의 항목은 선택적`이며, 생략할 수 있습니다
- -a와 -b는 `프로그램 기능을 활성화하거나 비활성화하는 플래그`입니다.
- `-c 옵션은 공백 문자로 구분된 인수`를 기대합니다.
- `-d와 -e 옵션은 여러 가지 중에서 하나만 선택하여 사용할 수 있음`을 나타냅니다.
- `-f 옵션은 옵션과 옵션 인수를 공백 없이 함께 사용하며, 인수 없는 옵션은 다음 인수를 옵션 인수로 처리하지 않아야 합니다.`
- `operand`는 텍스트 파일과 같은 유틸리티가 처리하는 모든 것이 될 수 있습니다.
- `피연산자 뒤의 점 세 개(...)는 유틸리티에 영향을 주는 피연산자를 0개 이상 입력할 수 있다는 것`을 나타냅니다.
- `각도 괄호 안의 항목은 실제 값으로 대체해야 합니다.`
- 또한, 유틸리티에서 필요한 옵션에 대해서는 괄호를 생략할 수 있습니다. 많은 옵션을 갖는 복잡한 유틸리티의 경우, 옵션을 그룹화할 수 있습니다.

<br>

```
utility_name [-axyDnPo][-l arg][operand]
```

유틸리티 구문 외에도, POSIX는 유틸리티를 구현할 때 일련의 지침을 사용하도록 권장합니다.

<br>

>**참고**
>
> https://www.baeldung.com/linux/posix