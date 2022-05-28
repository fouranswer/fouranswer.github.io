---
layout: single
title:  "첫 포스팅 및 jekyll 설치 방법"
categories: github
tag : [jekyll]
toc: true
toc_sticky: true
---

# Hello world 
this is my first Jekyll blog post.
I hope you like it!

첫 번째 포스팅 테스트. 
잘 올라가나?


## 코드 표시 테스트

``` python
# ~ 물결 표시!!    ₩₩₩python
print("hello, world!!")
```


# github.io 설치 방법

## 20220427 - pc에서 로컬 개발환경 설정을 진행

macbook 기준 - 인터넷 상에서 찾은 것들을 같이 추가해놓았다.


https://jekyllrb.com/docs/installation/macos/
https://youtu.be/0TeHUqSAb6Q



brew update

brew install chruby ruby-install

ruby-install ruby

echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc

echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc

echo "chruby ruby-3.1.1" >> ~/.zshrc

It should show ruby 3.1.1p18 (2022-02-18 revision 53f5fc4236) or a newer version.

gem install jekyll

자 여기까지 했는데 permission 문제가 발생했다..


https://happymemoryies.tistory.com/21

rbenv를 통해서 해결할 수 있나보다. python에서도 venv 인가 있었던 것으로 기억나는데, 비슷한 컨셉인듯.

brew install rbenv

rbenv install -l 

rbenv install 3.1.2

rbenv global 3.1.2


nano ~/.zshrc

zshrc 내용

source /opt/homebrew/opt/chruby/share/chruby/chruby.sh

source /opt/homebrew/opt/chruby/share/chruby/auto.sh
// chruby ruby-3.1.1  # 어떤 용도인지는 모르겠으나... 이걸 했을때 zsh에서 로드가 안되나보다.

// rbenv
export PATH=~/.rbenv/bin:$PATH
eval "$(rbenv init -)"

저장

source ~/.zshrc

gem install bundler
gem install jekyll

cd ../fouranswer.github.io... 해당 폴더로 이동

bundle install

bundle add webrick

bundle exec jekyll serve    // 이제 큰 설정이 바뀔 때는 이 명령으로 다시 실행해준다.


# test1

## test2

### test3

# test2
## test3


