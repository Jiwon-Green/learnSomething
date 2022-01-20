### 안되는것
안드로이드 스튜디오에서 브랜치에서 작업완료 & pr & merge까지 다하고 <br>
프로젝트 터미널에서 master 에서 `git pull origin master` 하려고 했는데

```remote: Repository not found. fatal: repository 'https://github.com/~~~/~~~.git/' not found```
라고 하믄서 안됨

예전에 깃헙 혼자 야매로 할 때 이미 등록했던 계정이 뭔가 연결이 안맞아서 그런가 싶었음

1. 안스에 지금 쓰는 계정이 등록 안됐나 해서 `File-Settings-Version Control-GitHub` 보니 등록은 되어있었고 다시 해도 안됐음 ㅠ
2. 권한 없는거같아서 토큰 권한 중에 `repo` `admin:org` `gist` 주었음. 근데도 안됨 ~!!

### 해결
윈도우 `자격증명관리자` 들어가서 보니 깃헙 등록된 계정이 다른 계정으로 되어있었다! <br>
역시 예전에 등록된거랑 꼬엿다,, 어이없어ㅋ; <br>
심지어 토큰도 아니고 ID/PW으로 연결되어있었다 <br>
그래서 지금 쓰고있는 `계정이메일/토큰`으로 편집 해주고 다시 pull 땡기니 됐다!!

^,^
