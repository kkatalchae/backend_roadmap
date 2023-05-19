# POSIX

`POSIX?`

POSIX는 이식 가능한 운영 체제 인터페이스(Portable Operating System Interface)의 약어입니다. 이것은 IEEE에서 지정한 표준 집합으로, 운영 체제 간의 호환성을 유지하기 위해 사용됩니다. 따라서 POSIX 표준을 준수하는 소프트웨어는 POSIX 표준을 준수하는 다른 운영 체제와 호환될 수 있습니다.

그 이유로 우리가 Linux 및 Unix 기반 운영 체제에서 사용하는 대부분의 도구는 거의 동일하게 작동합니다. 예를 들어, ps 명령을 사용하면 OpenBSD, Debian 및 macOS에서 동일하게 작동해야 합니다.

<br></br>

`운영체제의 종류`

다양한 종류의 운영 체제가 있습니다. 이 중에서도 주요한 종류는 다음과 같습니다.

- **실시간 운영 체제 (RTOS)** : 이러한 시스템은 데이터를 실시간으로 처리하도록 설계되어, 데이터가 수신되는 대로 처리할 수 있습니다. 예를 들어 VxWorks, QNX 등이 있습니다.
- **단일 사용자, 단일 작업 운영 체제** : 이러한 운영 체제는 한 번에 하나의 사용자가 한 프로그램만 실행할 수 있도록 설계되어 있습니다. 예를 들어 MS-DOS, CP/M 등이 있습니다.
- **단일 사용자, 다중 작업 운영 체제** : 이러한 운영 체제는 단일 사용자가 여러 프로그램을 동시에 실행할 수 있도록 허용합니다. 예를 들어 Microsoft Windows, macOS 등이 있습니다.
- **다중 사용자 운영 체제** : 이러한 운영 체제는 여러 사용자가 동시에 같은 컴퓨터에 액세스할 수 있도록 허용합니다. 예를 들어 UNIX, Linux 등이 있습니다.
- **분산 운영 체제** : 이러한 운영 체제는 독립적인 컴퓨터 그룹을 관리하고 하나의 컴퓨터처럼 보이게합니다. 예를 들어 Apache Hadoop, Google File System 등이 있습니다.
- **임베디드 운영 체제** : 이러한 운영 체제는 모바일 폰 및 기타 휴대용 장치와 같이 제한된 리소스를 가진 작은 장치에서 실행되도록 설계되었습니다. 예를 들어 Android, iOS 등이 있습니다.

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

## C API

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