
mkDir  -- make directory
cd ~/MyProject -- change directory
cd github/single-page-design
cd ../  -- 상위 디렉토리 

touch Readme.txt -- create a file

git status -- to have a look for status of the current repo
git add Readme.txt -- add 
git commit -m “Add Readme.txt” -- commit message

git remote add origin https://github.com/kes3583/kes3583.github.io.git -- connect local to remote and assign the current repo on github as origin
git remote -v -- list of the origin
git push / git push origin master -- upload to remote git


# 로컬 프로젝트 폴더가 있을 경우 
1. open terminal app
2. go to your local project directory -$ cd project/portfolio
3. user 설정 - git config - -global user.email “Your email address”
4. 
5. git init - new git repository
6. git clone /로컬/저장소/경로 or git clone 사용자명@호스트:/원격/저장소/경로
-- git clone https://github.com/kes3583/javascript30.git
##work flow ##
# local directory -1.add- to #index(stage) -2.commit- to #Head - 3. remote add origin 4. push

1.add - first
git add <파일 이름> -- 한개의 파일 
git add .  -- 모든 파일 
git add <foldername>/ -- 폴더

2.commit - 하지만 실제로 변경 내용을 확정하려면 아래 명령을 내려야 한답니다.하지만, 원격 저장소에는 아직 반영이 안 됐답니다.
git commit -m "이번 확정본에 대한 설명"


3.git remote add origin <원격 서버 주소> -- 로컬저장소와 원격저장소 연결.

-- git remote add origin https://github.com/kes3583/kes3583.github.io.git

4.로컬 저장소의 HEAD
--git push origin master


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
