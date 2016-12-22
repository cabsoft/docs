확장자를 md 로 하면 웹에서 마크다운을 사용할 수 있는지를 테스트 합니다.

# 소스트리에서 ssh로 레포지터리 연결하는 방법

https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/

소스트리에서 원격 레포지터리에 깃허브를 설정하면서 ssh key 를 생성하면
{사용자_홈_디렉토리}/.ssh/
아래에 퍼블릭키와 프라이빗 키가 생성됩니다.
이걸 운영체제에서 사용하는 ssh agent 에 추가해주면 됩니다.
osx의 경우라면, ''' $ ssh-add ~/.ssh/id_rsa ''''
로 하면 됩니다.
https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/

- [안드로이드 다운 디자인과 개발](http://realignist.me/code/2016/05/25/better-android-developer-guide.html) 
