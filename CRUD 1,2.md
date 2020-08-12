# CRUD
* Get / Post
>> 클라이언트에서 서버로 요청을 보내는 방법

## 1. Get 
>> Data를 "URL"에 포함시켜 전송
>> 전송하는 길이에 제약 0
>> Caching 가능
(REST에서 데이터 조회에 활용)
>> READ에서 활용


## 2. POST
>> Data를 "Body"에 넣어 전송
>> 전송하는 길이에 제약 x
>> Caching 불가능
>> CREATE / UPDATE 에서 활용

## 3. CREATE
>> 새로운 객체를 생성해 Data를 저장

* 객체 생성
~~~
<div>
if request.method == 'POST':
	post = Designer()
~~~
</div>
* 입력 Data 저장
~~~
<div>
post.name = request.POST['name']
post.address = request.POST['address']…
</div>
~~~
* 입력 Data 저장
~~~
<div>
post.save()
</div>
~~~


## 4. DELETE
:제거가 필요한 객체를 찾아 삭제

* 객체 탐색
~~~
<div>
post = get_object_or_404(Designer, pk = designer_id)
</div>
~~~
* 객체 삭제
>> post.delete()
* Home으로 이동
>> return redirect('home')

## 5. UPDATE
: 정보 수정이 필요한 객체를 찾아 Data를 새롭게 저장

* 객체 탐색
~~~
<div>
post=get_object_or_404(Designer, pk = designer_id)

if requset.mothod == 'POST':
</div>
~~~
* 입력 Data 저장
~~~
<div>
post.name = request.POST['name']
post.address = request.POST['address']…
</div>
~~~
* 입력 Data(POST 객체) 저장

>> post.save()

## 6. 패키지 종속성 관리
>> 내 환경에서 어떤 패키지를 어떤 버전으로 사용하고 있는지 알려주는 것

