## Model이란?
>> 데이터에 접속하고 관리하도록 도와주는 객체

## Model 생성 & 적용
1) models.py
~~~
<div>
class Designer(models.Model):
    image = models.ImageField(upload_to = 'images/')
    name = models.CharField(max_length = 50)
    address = models.CharField(max_length = 255)
    description = models.TextField()
<div>
~~~
##### 모델 명의 첫 글자는 무조건 대문자!
2) Terminal 


>> python manage.py makemigrations        <DB가 알아듣도록 번역하기>


>> python manage.py migrate               <번역한 내용을 DB에 적용>

🎗 마이그레이션 파일 생성 및 적용
* 마이그레이션 파일 (초안) 생성하기 : makemigrations
* 해당 마이그레이션 파일을 DB에 반영하기 : migrate

* migrations
>> 모델 변경내역 히스토리 관리


>> 모델의 변경내역을 DB Schema (데이터베이스 데이터 구조)로 반영시키는 효율적인 방법을 제공


>> models.py에 코드 입력

## Admin에게 Model 알려주기
>> Django는 Admin 제공


>> from .models import Designer


>> admin.site.register(Designer)
