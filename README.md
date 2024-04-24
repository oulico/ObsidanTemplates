# ObsidanTemplates
Instruction for setting obsidian &amp; Template I use (written in Korean)


## 핸즈온 소개

이 문서는 Obsidian 설정에 대해 단계별로 안내합니다. 

## 필요한 도구 및 재료

- obsidian : 문서편집기
- 드롭박스 계정 혹은 구글 드라이브: 자동 백업에 사용
- 플러그인

### Community Plugins

| 플러그인 명                                                                                                                                                      | 설명                                                 | 필수설치여부 | 모바일여부 | 비고  |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- | ------ | ----- | --- |
| [automatic-table-of-contents](https://publish.obsidian.md/hub/02+-+Community+Expansions/02.05+All+Community+Expansions/Plugins/automatic-table-of-contents) | 자동으로 목차를 넣을 수 있음                                   |        |       |     |
| [calendar](https://publish.obsidian.md/hub/02+-+Community+Expansions/02.05+All+Community+Expansions/Plugins/calendar)                                       | 달력. 날짜 클릭하면 해당 날짜가 제목인 문서가 생성됨. 데일리노트와 함께 사용하면 좋음. | ✅      |       |     |
| [cycle-through-panes](https://publish.obsidian.md/hub/02+-+Community+Expansions/02.05+All+Community+Expansions/Plugins/cycle-through-panes)                 | 탭 간 전환                                             |        |       |     |
| [dataview](https://publish.obsidian.md/hub/02+-+Community+Expansions/02.05+All+Community+Expansions/Plugins/dataview)                                       | 문서데이터를 파싱해서 한 화면에 보여줌                              | ✅      |       |     |
| [homepage](https://publish.obsidian.md/hub/02+-+Community+Expansions/02.05+All+Community+Expansions/Plugins/homepage)                                       | 옵시디언을 켤때마다 보여주는 홈 화면                               | ✅      |       |     |
| [nldates-obsidian](https://publish.obsidian.md/hub/02+-+Community+Expansions/02.05+All+Community+Expansions/Plugins/nldates-obsidian)                       | 자연어를 날짜로 바꿔줌. `@Today`라고 작성하면 알아서 현재 날짜를 기입함       | ✅      |       |     |
| [obsidian-advanced-codeblock](https://publish.obsidian.md/hub/02+-+Community+Expansions/02.05+All+Community+Expansions/Plugins/obsidian-advanced-codeblock) | 코드블럭 개선                                            | ✅      |       |     |
| [obsidian-charts](https://publish.obsidian.md/hub/02+-+Community+Expansions/02.05+All+Community+Expansions/Plugins/obsidian-charts)                         | 데이터 시각화해서 차트로 보여줌                                  |        |       |     |
| [obsidian-format-code](https://publish.obsidian.md/hub/02+-+Community+Expansions/02.05+All+Community+Expansions/Plugins/obsidian-format-code)               | 옵시디언용 prettier                                     | ✅      |       |     |
| [obsidian-tasks-plugin](https://publish.obsidian.md/hub/02+-+Community+Expansions/02.05+All+Community+Expansions/Plugins/obsidian-tasks-plugin)             | 일정관리. Todo리스트 작성가능                                 | ✅      |       |     |
| [obsidian-vimrc-support](https://publish.obsidian.md/hub/02+-+Community+Expansions/02.05+All+Community+Expansions/Plugins/obsidian-vimrc-support)           | 자신이 사용하는 .vimrc를 옵시디언에서도 쓸 수 있음                    |        |       |     |
| [remotely-save](https://publish.obsidian.md/hub/02+-+Community+Expansions/02.05+All+Community+Expansions/Plugins/remotely-save)                             | 드롭박스 등을 이용해서 무료로 실시간 백업할 수 있음                      | ✅      |       |     |
| [table-editor-obsidian](https://publish.obsidian.md/hub/02+-+Community+Expansions/02.05+All+Community+Expansions/Plugins/table-editor-obsidian)             | 테이블 작성 및 수정                                        |        |       |     |
|                                                                                                                                                             |                                                    |        |       |     |
|                                                                                                                                                             |                                                    |        |       |     |

### Official Plugins

| 플러그인명            | 설명                                                                         | 필수여부 |
| ---------------- | -------------------------------------------------------------------------- | ---- |
| Audio recorder   | 녹음기능                                                                       |      |
| Backlinks        | 링크로 연결된 문서 표시                                                              |      |
| Bookmarks        |                                                                            |      |
| Canvas           | 그림 그리기(구조도 등)                                                              |      |
| Command palette  | 명령어 사용                                                                     |      |
| Daily notes      | 오늘 날짜의 노트를 생성                                                              | ✅    |
| File recovery    |                                                                            |      |
| Files            |                                                                            |      |
| Format converter |                                                                            |      |
| Graph view       | 그래프로 문서간 연결을 시각화                                                           |      |
| Note composer    |                                                                            |      |
| Page preview     | 링크에 마우스 올리면 그 문서를 프리뷰함                                                     |      |
| Properties view  | 문서의 메타정보 확인                                                                |      |
| Quick Switcher   |                                                                            |      |
| Search           |                                                                            |      |
| Tags view        |                                                                            |      |
| Templates        | 특정 폴더에 템플릿을 저장해서 문서 생성시 사용하거나 Dailynote와 함께 사용해서 매일 같은 형식의 문서를 생성하게 할 수 있음 | ✅    |
| Word Count       |  글자수 세기                                                                    |      |



## 단계별 지침

### 단계 1: 드롭박스로 실시간으로 sync하도록 하기

1. https://github.com/remotely-save/remotely-save/blob/master/docs/dropbox_review_material/README.md

### 단계 2: 폴더 구조 설정하기
```shell
├── Attachments
├── DailyNotes
├── GTD
└── Knowledges
    ├── Book
    ├── Memo
    ├── MyLogs
    ├── Templates
    ├── Wiki
    └── 직장
```
1. 위의 구조로 폴더를 생성합니다. 
	- Attachments: 문서에 첨부되는 모든 이미지들을 여기에 저장
	- DailyNotes: 날짜가 제목인 데일리 노트들
	- GTD: 프로젝트 단위로 분리해 일정 및 투두리스트 기록
	- Knowledges: 공부하거나 배운 것, 문서화한 것 등을 위키 형태로 저장. 하위에 폴더로 분리해서 저장 관리하고 있지만, 그냥 모든 문서를 때려넣고 각 문서에 태그를 달아서 관리하는 방법도 나쁘지 않음.(태그랑 링크로 관리하는 편이 그래프 뷰에서 예쁘게 보임. 본인은 해당 폴더를 다른 데에 복사해서 이동시킬 일이 있을 것 같아서 폴더로 관리하면서 태그를 함께 사용.)
		- Book: 독서한 내용을 정리. 템플릿 사용.
		- Memo: 그냥 메모장
		- MyLogs: 매주 금요일에 GTD회고 시간을 가지면서 완료된 일감들을 여기에 기록함.
		- Templates: 템플릿 모음
		- Wiki: 공부한 것들 모음
		- 직장: 직장내에서 사용하는 지식에 대한 Wiki


### 단계 3: 템플릿 만들기

자주 사용하는 템플릿을 저장해서 사용합니다. Dailynote에서 이 기능을 사용해서 특정 템플릿의 노트를 생성하도록 합니다.

1. 템플릿 폴더를 지정하기( 단계 2에서 만든 템플릿 폴더의 path를 설정에 넣어줍니다.)
        ![](Screenshots/Pasted%20image%2020240424103740.png)

        
2. 템플릿 폴더에 사용할 템플릿을 저장하기 (별첨한 템플릿을 사용하면 됩니다)

| 템플릿 명                    | 용도                        | 필수 여부 |
| ------------------------ | ------------------------- | ----- |
| Daily.md                 | 데일리노트                     | ✅     |
| Archive.md               | 인터넷에서 본 내용을 그대로 기록하기      |       |
| 기능기획.md                  | 새로운 기능을 기획할 때             |       |
| 기술연구.md                  | 새로운 기술을 연구할 때             |       |
| 지식.md                    | 위키작성                      |       |
| 핸즈온.md                   | 설치 혹은 사용법 등을 핸즈온 형식으로 문서화 |       |
| 스크럼 회의록.md               | 스크럼 회의록                   |       |
| 책 - 메인템플릿.md             | 책 전체 요약. 챕터별 요약 문서와 링크.   |       |
| 책 - 챕터 별 메모 템플릿.md       | 책 챕터별 요약.                 |       |
| 단계별로 설명한 프로젝트 문서화 템플릿.md | 프로젝트 문서화                  |       |
| CS.md                    | 컴퓨터 공학 wiki               |       |
| 기타 등등                    |                           |       |


### 단계 4: Daily note를 사용해서 매일 작업한 문서 등을 로그로 남기기
> 단계 3에서 템플릿을 다운받아서 설정한 상태여야합니다.
 
1. 설정에서 단계2에서 설정한 path를 기입해줘야합니다.
 ![](Screenshots/Pasted%20image%2020240424103905.png)

### 단계 5: Task를 사용하고 이를 이용해서 GTD 방법론에 입각한 Todo list 만들기

> 사전에 GTD방법론의 사용법을 숙지하고 있어야 합니다.
> 1.떠오르는 생각, 갑자기 생긴 일 등은 Capture에 등록합니다.
>2.Capture에 러프하게 작성된 일의 성격을 분류합니다. 공적인 일은 `@work`, 사적인 일은 `@home`으로 분류합니다.
>3. Due date를 설정합니다. 
>4. 각각의 할일을 프로젝트 별로 분류합니다. 별도로 생성되어있는 프로젝트 파일로 옮깁니다.(shift + cmd + k)

참고 링크:
https://facedragons.com/productivity/set-up-gtd-in-obsidian/


1. Capture 파일 만들기

**문서 예시**
```Capture.md
> 다음의 단계에 따라 일감을 정리합니다
> 1. 생각나는 대로 적습니다
> 2. 일의 특성에 따라 `@work` 혹은 `@home` 접미사를 붙입니다
> 3. 일정을 정하고 우선순위를 체크합니다. (가능하면 일을 뽀모도로 단위로 나눕니다. 오전 4뽀모도로, 오후 6뽀모도로를 사용합니다.)
> 4. 접미사가 붙은 것들은 `shift` + `ctrl` + `k`를 클릭하여 프로젝트명으로 정리합니다
> 5. Dashboard로 이동해 일감을 확인하고 일을 시작합니다

- [ ] 퇴근길에 우유 사가기 @home 
- [ ] mysql 설치하기 @work 
```

2. 프로젝트 별 파일을 생성하기

**문서 예시** (경로: `GTD/Projects/Dev-server-setting.md`)
```Dev-server-setting.md
> 개발 서버 인프라 구성을 위한 프로젝트입니다 

- [ ] mysql 설치하기 @work 
```

3. Dashboard 파일을 만들기 (경로: `GTD/Dashboard.md`, 파일은 첨부파일을 확인할 것. 사용전에 `dataviewjs`, `chart` 등 사용되는 모든 플러그인이 활성화되어 있는지 확인할 것.)

4. Dashboard 파일을 홈페이지로 설정하기
![](Screenshots/Pasted%20image%2020240424103740.png)


## 추가 팁

- 테마 변경하기 : https://anpigon.tistory.com/332
- 자잘한 플러그인들: https://alive-wong.tistory.com/66

## 문제 해결

- 여러 기기에서 싱크하다가 뻑난 것인지 갑자기 옵시디언이 이상하게 작동할 때 -> Community Plugin을 비활성화한다음에 다시 활성화하면 됨.
- 모바일 기기에서 드롭박스를 이용해서 싱크하려면 -> 별도의 앱을 깔아서 싱크해줘야함.(`Dropsync`)

## 참고 자료

- GTD란 무엇인가: https://m.blog.naver.com/hasajon/220648576335
