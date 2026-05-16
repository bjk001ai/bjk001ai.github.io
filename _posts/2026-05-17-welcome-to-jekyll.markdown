---
layout: post
title:  "Jekyll를 이용하여 10분만에 만들기"
date:   2026-05-17 01:39:11 +0900
categories: jekyll update
---
1. GitHub가입
2. Ruby 설치 (Windows)
    - rubyinstaller.org/downloads 접속
    - Ruby+Devkit 다운 (rubyinstaller-devkit-4.0.3-1-x64)
    - 설치 중 마지막에 ridk install 창이 뜨면 Enter 누르기
    - 설치 완료 후 터미널(cmd)에서 확인 ruby -v
    - gem install jekyll bundler
    - jekyll -v
    - jekyll new my-blog
    - cd my-blog
    - bundle exec jekyll serve
3. GitHub 새로운 repository 생성
    - bjk001ai.github.io
4. my-blog 를 push
    {% highlight ruby %}
    git init
    git remote add origin https://github.com/bjk001ai/bjk001ai.github.io.git
    git add .
    git commit -m "첫 블로그 시작"
    git push -u origin master
    {% endhighlight %}
5. GitHub Pages 활성화
    github.com/bjk001ai/bjk001ai.github.io 접속
    상단 Settings 탭 클릭
    왼쪽 메뉴에서 Pages 클릭
    Branch 를 master 로 선택 → Save

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
