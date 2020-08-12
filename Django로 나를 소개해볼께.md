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

## QuerySet이란?
>> 전달받은 모델의 객체 목록

>> query 란 데이터베이스에 정보를 요청해주는 것을 의미하며 파이썬으로 작성한 코드가 sql 로 매핑되어 queryset 이라는 자료 형태로 값이 넘어오게 됩니다. 이는 순회가능한 데이터로서 이를 이용하여 1개 이상의 데이터를 불러와 사용

* views.py
>> Model의 존재 알려주기
~~~
<div>
from .models import Designer
</div>
~~~


>> Queryset을 Templates로 보내기
~~~
<div>
def home(request):
    designers = Designer.objects.all()
    return render(request, 'home.html' ,{'designers':designers})
</div>
~~~

* Queryset & Method : 전달받은 객체 목록, 그리고 이를 다루는 법
* PK : Model을 통해 생성된 객체들을 구분할 수 있는 고유한 키
* Path Convertor : 여러 객체의 url을 계층적으로 다룰 수 있도록 도와주는 도구
* get_object_or_404 : 객체를 가져오려 했는데 없을 경우 나타나는 에러







