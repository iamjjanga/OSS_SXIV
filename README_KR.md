![sxiv](http://muennich.github.com/sxiv/img/logo.png "sxiv")

**단순한 X 이미지 뷰어**

SXIV는 빠른 이미지 보기를 특징을 가진 가장 기본적인 이미지 뷰어입니다. 이 프로그램은 VI(visual editor) 키 바인딩을 가지고 있고 창관리자를 바둑판 식으로 배열하여 잘 작동합니다. 프로그램의 코드는 작은 단위에서 유지되고 사용자가 필요에 따라 커스텀하고 파고들기에 용이하게 만들어져 있습니다.


주요 특징
--------

* 기본 이미지 동작 (예: 확대/축소, 수평 회전, 회전)
* 키 커스텀, 마우스 버튼 매핑 (in *config.h*)
* 썸네일 모드 : 모든 이미지들 선택적으로 미리 볼 수 있는 격자
* 빠른 다시불러오기를 위한 썸네일 캐시 기능
* 다중 프레임 이미지 지원
* GIF 파일을 모든 프레임에서 불러오고, GIF 애니메이션을 재생
* 상태줄에 이미지 정보 표시


스크린샷
-----------

**이미지 모드 :**

![Image](http://muennich.github.com/sxiv/img/image.png "Image mode")

**썸네일 모드 :**

![Thumb](http://muennich.github.com/sxiv/img/thumb.png "Thumb mode")


설치
------------

sxiv를 설치하기 위해서는 다음 명령을 사용합니다 
명령어 :

    $ make
    # make install

후자의 명령은 관리자권한을 필요로 합니다. 기본값으로, sxiv는 "/usr/local"의 고유 경로를 사용하여 설치합니다. 전체 실행 경로는 "/usr/local/bin/sxiv"가 될것입니다.

사용자는 다음 두번째 명령어를 통해 선택적으로 디렉터리르 변경하여 sxiv를 설치할 수 있습니다.
명령어 :

    # make PREFIX="/your/dir" install

sxiv 특정 설정의 설치 시간은 config.h에서 찾을 수 있습니다. 필요에 따라 그것을 확인하고 바꿀 수 있습니다. 만약 config.h 파일이 없다면, 다음 명령을 이용해서 생성합니다 :

    $ make config.h


사용법
-----

sxiv를 사용하기 위해 [man page](http://muennich.github.com/sxiv/sxiv.1.html)의 정보를 참조하십시오. 한국어 버전은 man_kr.md를 참조하시기 바랍니다.


다운로드 & 변경 사항
--------------------


사용자는 [sxiv](https://github.com/muennich/sxiv) GitHub의 소스코드 저장소 살펴보거나 git을 통한 다음 명령어를 통해 복사할 수 있습니다

    git clone https://github.com/muennich/sxiv.git

**안정화 버전 배포**

**[v24](https://github.com/muennich/sxiv/archive/v24.tar.gz)**
*(October 27, 2017)*

  * 변경이 있을시 현재의 이미지를 자동으로 다시 불러옵니다.
  * -e 옵션은 (예: 꼬리표달기)같은 기능을 다른 X window에 내장하는 기능을 도와줍니다.
  * 새로운 옵션 -p는 임시 파일과 캐시를 생성하는 것을 막습니다.
  * (탐색, 확대/축소, 수평회전)을 마우스만으로 접근할 수 있게 기본적인 마우스 매핑을 더 단순화 했습니다.

**[v1.3.2](https://github.com/muennich/sxiv/archive/v1.3.2.tar.gz)**
*(December 20, 2015)*

  * 더이상 인자값이 아닌 외부 key 조작으로 표준입력의 파일경로를 얻을 수 있습니다.
  * 백그라운드에서 보이지 않는 썸네일을 캐시합니다.
  * 썸네일에 감마 조정을 적용합니다.

**[v1.3.1](https://github.com/muennich/sxiv/archive/v1.3.1.tar.gz)**
*(November 16, 2014)*

  * config.h 생성에 지연을 만드는 에러를 수정하였습니다.
  * -c 옵션 동작시 일어나는 세그먼트 오류를 수정했습니다.

**[v1.3](https://github.com/muennich/sxiv/archive/v1.3.tar.gz)**
*(October 24, 2014)*

  * EXIF 태그로 부터 썸네일을 얻어옵니다. (libexif 필요)
  * config.h에 정의된 크기로 썸네일을 확대/ 축소 지원합니다.
  * giflib 버전에 에러를 수정하였습니다. >= 5.1.0

**[v1.2](https://github.com/muennich/sxiv/archive/v1.2.tar.gz)**
*(April 24, 2014)*

  * `Ctrl+x` 로 정의한 외부 키 장치를 추가하였습니다.
  * 새로운 키 바인딩`{`/`}` 감마값을 변경할 수 있습니다. (by András Mohari)
  * 슬라이드쇼를 지원하고, `-S` 옵션이나 `s` 토글키로 사용가능합니다.
  * 어플리케이션 아이콘을 추가하였습니다. (created by 0ion9)
  * 알파 레이어에 배경 체커보드를 만들었습니다.
  * Option `-o` only prints files marked with `m` key
  * 옵션 `-o`는 표시하는 키인 `m`과 파일을 출력합니다.
  * Fixed rotation/flipping of multi-frame images (gifs)
  * 다중 프레임 이미지 (GIF)의 회전/수평회전를 고정하였습니다.

**[v1.1.1](https://github.com/muennich/sxiv/archive/v1.1.1.tar.gz)**
*(June 2, 2013)*

  * 다양한 버그를 수정하였습니다.

**[v1.1](https://github.com/muennich/sxiv/archive/v1.1.tar.gz)**
*(March 30, 2013)*

  * 사용자 설정 가능한 내용을 창의 하단부 상태표시줄에 추가하였습니다.
  * 새로운 키보드 단축키 `\ / |` : 이미지를 수직/수평으로 뒤집습니다.
  * 새로운 키보드 단축키 `Ctrl+6` : 마지막/대체 이미지로 이동합니다.
  * 자체적 EXIF 기반의 조작을 추가하고, libexif에 의존을 제거하였습니다.
  * 다양한 버그 수정

**[v1.0](https://github.com/muennich/sxiv/archive/v1.0.tar.gz)**
*(October 31, 2011)*

  * 다중 프레임 이미지와 GIF 애니메이션을 지원합니다.
  * POSIX compliant (IEEE Std 1003.1-2001)

**[v0.9](https://github.com/muennich/sxiv/archive/v0.9.tar.gz)**
*(August 17, 2011)*

  * 키와 마우스 매핑을 식별가능하게 만들었습니다.(in config.h)
  * 완성된 코드를 재설정하였습니다.

**[v0.8.2](https://github.com/muennich/sxiv/archive/v0.8.2.tar.gz)**
*(June 29, 2011)*

  * POSIX-compliant Makefile;  NetBSD아래에서 컴파일합니다.

**[v0.8.1](https://github.com/muennich/sxiv/archive/v0.8.1.tar.gz)**
*(May 8, 2011)*

  * 전적으로 EWMH-compliant가 아닌, 윈도우 관리자 아래에 전체 창모드를 고정하였습니다. 

**[v0.8](https://github.com/muennich/sxiv/archive/v0.8.tar.gz)**
*(April 18, 2011)*

  * 썸네일 캐싱을 지원합니다.
  * 현재 이미지에 외부명령(예, j[egtran, convert)를 동작하는 기능을 추가하였습니다.

**[v0.7](https://github.com/muennich/sxiv/archive/v0.7.tar.gz)**
*(February 26, 2011)*

  * 디렉터리 목록들을 `-r`명령 옵션을 사용하여 재정렬합니다.
  * 이미지 모드에 커서를 숨깁니다.
   * 전체적인 썸네일 모드의 기능으로, Return 키를 사용하여 이미지와 썸네일 모드를 변경 합니다.

**[v0.6](https://github.com/muennich/sxiv/archive/v0.6.tar.gz)**
*(February 16, 2011)*

  * 버그 수정 : 창제목에 umlauts로 파일이름을 표시합니다.
  * 기본 썸네일을 지원합니다.

**[v0.5](https://github.com/muennich/sxiv/archive/v0.5.tar.gz)**
*(February 6, 2011)*

  * 새로운 명령 옵션 : `-r` : 주어진 디렉터리에 모든 이미지를 불러옵니다.
  *  새로운 키 단축키 : `w` : 창에 맞게 이미지 크기를 재조정합니다; `W` : 이미지 크기에 맞게 창크기를 재조정합니다.

**[v0.4](https://github.com/muennich/sxiv/archive/v0.4.tar.gz)**
*(February 1, 2011)*

   * 새로운 명령 옵션 ㅣ `-F`, `-g` : 고정된 창크기를 사용하고 적용합니다.
  * 새로운 키 단축키 : `r`: 현재이미지 다시 불러오기

**[v0.3.1](https://github.com/muennich/sxiv/archive/v0.3.1.tar.gz)**
*(January 30, 2011)*

  * `make install`을 사용시 실행가능한 setuid를 설정하지 않습니다.
  * 가운데 마우스 버튼을 누르는 동안 이미지를 pan합니다.

**[v0.3](https://github.com/muennich/sxiv/archive/v0.3.tar.gz)**
*(January 29, 2011)*

  * 새로운 명령 옵션 : `-d`, `-f`, `-p`, `-s`, `-v`, `-w`, `-Z`, `-z`
  * 추가적인 마우스 매핑들 : 좌/우 클릭을 통한 다음/ 이전이미지로 이동, 마우스 휠로 이미지를 스크롤(수직적 이동은 shift 키를 눌러야합니다.), 이미지 확대/ 축소는 Ctrl 키를 누른 상태에서 마우스 휠로 작동합니다.

**[v0.2](https://github.com/muennich/sxiv/archive/v0.2.tar.gz)**
*(January 23, 2011)*

  * 버그 수정 : 창 크기 재조정 작동 수정
  * 새로운 키보드 단축키 : `g / G` : 처음과 마지막 이미지로 이동합니다; `[ / ]`: 10씩 이미지를 정/역방향 이동합니다.
  * 마우스 휠로 확대/추구소를 지원합니다(by Dave Reisner)
  * 전체화면모드를 추가하였습니다.

**[v0.1](https://github.com/muennich/sxiv/archive/v0.1.tar.gz)**
*(January 21, 2011)*

  * 처음 배포


