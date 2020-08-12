## 가상환경이란?
>> 자신이 원하는 Python 환경 구축을 위해 필요한 모듈만 담아 놓는 바구니

## Django 명령어 모음
* [Django 패키지 설치] : pip install django

* [Django 프로젝트 생성] : django - admin startproject <프로젝트명> .

* [Django App 생성] : python manage.py startapp <App 이름>

* [Django 로컬 서버 시작 ] : python manage.py runserver

# Django의 Project & App
## Project
* setting.py: 전체 프로젝트를 관리하는 설정 파일
* urls.py: 프로젝트의 URL 관리 파일
* wsgi.py & asgi.py: 프로젝트를 서비스하기 위한 파일
* __init__.py: 해당 디렉토리가 Python Pakage의 일부임을 Python에게 알려주는 파일

## App
* views.py: 웹 요청을 받고, 전달받은 데이터를 처리해서 가공하는 파일
* models.py: Database와 관련된 다양한 역할 수행
* admin.py: 관리자 관련 파일
* apps.py: Project에서 App의 존재를 알려줄 때 활용되는 파일
홈페이지 출력 순서

## Home 페이지 출력하기
1. settings.py: Project에게 App의 존재 알리기
2. Templates: User에게 보여줄 HTML 파일 만들기
3. views.py: 요청이 들어오면 HTML 파일을 열어주는 함수 정의
4. urls.py: url 요청을 views와 연결하기
