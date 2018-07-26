

# single-page-design
https://github.com/kes3583/single-page-design.git
git init - new git repository
git clone /로컬/저장소/경로 or git clone 사용자명@호스트:/원격/저장소/경로

##work flow ##
# local directory -add- #index(stage) -commit- #Head

#add - first
git add <파일 이름>

#commit - 하지만 실제로 변경 내용을 확정하려면 아래 명령을 내려야 한답니다.하지만, 원격 저장소에는 아직 반영이 안 됐답니다.
git commit -m "이번 확정본에 대한 설명"

#로컬 저장소의 HEAD
git push origin master

git remote add origin <원격 서버 주소>

# Branch 가지치기 - test 후 master 가지로 돌아와 병합

# Merge - 원격저장소의 데이터를 로컬 저장소로 병합
#원격 저장소의 변경 내용이 로컬 작업 디렉토리에 받아지고(fetch), 병합(merge)

git pull

git merge <가지 이름>

#변경 내용을 병합하기 전에, 어떻게 바뀌었는지 비교해볼 수도 있어요.
git diff <원래 가지> <비교 대상 가지>

#로컬의 변경 내용을 되돌릴

##로컬의 변경 내용을 변경 전 상태(HEAD)
git checkout -- <파일 이름>

#로컬 master 가지가 저 이력을 가리키
git fetch origin
git reset --hard origin/master
