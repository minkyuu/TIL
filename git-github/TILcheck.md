# codereview 프로세스

1. code review를 위한 브랜치를 생성한다.
git branch "브랜치 이름"

2. main 브랜치에서 방금 만든 code review 브랜치로 이동한다.
git switch "이동할 브랜치 이름"
git checkout "이동할 브랜치 이름"

3. 이제 이 브랜치에 코드 리뷰를 받을 파일을 작성한다.
ex) num_picker.py

4. 작성한 파일은 브랜치안에서 변경되었으니 git add 를 한다.
git add "num_picker.py"

5. commit 을  한다. 
- git commit + vim 커밋 작성

6. push 를 할 때는 브랜치가 main이 아니라 code review 브랜치로 지정해주어야 한다!
git push origin "code review 브랜치 이름"

7. 이렇게 push 까지 마치고 나면 Github에 다음과 같은 문구가 나타난다.
"This branch is 1 commits ahead of main"

8. 그러면 옆에 있는 Contribute 버튼을 눌러서  Open pull request 버튼을 누른다.

9. 위에는 자신이 작성한 코드에 대한 설명을 작성하는 것으로 제목과 내용을 작성하면 된다.
- 추가적으로 아래쪽에서 자신이 작성했던 코드를 볼 수 있다.

10. 오른쪽 탭 최상단을 보면 Reviewers라는 탭이 있다. 여기서 Reviewer를 정할 수 있다.
#Reviewer 추가 process
- repository창의 메인 nav 버튼들 중 setting 버튼 클릭
- Manage access 버튼 클릭
- 하단에 Invite a collaborator 버튼 클릭
- Search by username으로 invite 메일을 전송한다.


11. Reviewer를 정하고 pull request를 한다.


12. Review는 pull request에 대해 comment, approve를 선택할 수 있다.
- comment는 아직 수정할 부분에 대한 내용을 requester에게 전달하는 기능이다.
- approve는 request에 만족하여 브랜치의 내용을 main에 merge하겠다는 기능이다.

