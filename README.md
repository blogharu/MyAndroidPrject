# MyAndroidPrject

안드로이드 공부 1

이 내용은 제가 https://www.tutorialspoint.com/android/android_hello_world_example.htm 에서 공부한 내용을 다룬 글이다.

기본적으로 app/src/main 에 있는 폴더와 파일을 기준으로 설명한다.

java 폴더에 있는 java 파일은 앱을 구성하는 코드들이 들어있다.

res 폴더에는 여러가지 폴더가 있는데 각각의 이름에 따라 앱에서 사용되는 그림(drawable), 문자열 또는 특정 값(valuses), 화면 구성(layout) 등등 필요한 내용이 들어있다. res 폴더의 요소를 사용하기 위해서는 java 파일에서 R.폴더이름.파일이름 또는 R.폴더이름.태그이름 과 같은 방식으로 접근이 가능하다. 

예시

IgmageView imageView = (ImageView) findViewById(R.id.myimageview);
imageView.setImageResource(R.drawable.myimage); //myimage.png 라는 파일이 res/drawable 폴더에 들어있다.

TextView msgTextView = (TextView) findViewById(R.id.msg);
msgTextView.setText(R.string.hello); // res/values/string.xml 파일에 <string  name="hello">Hello, World!</string> 과 같이 hello 를 이름으로 하는 태그가 들어있다.

xml 파일 에서는 다음과 같이 접근 가능하다.

<--res/values/string.xml-->

<?xml version="1.0" encoding="utf-8"?>
<resources>
   <color name="opaque_red">#f00</color>
   <string name="hello">Hello!</string>
</resources>

<--어떤 layout xml 파일-->

<EditText xmlns:android="http://schemas.android.com/apk/res/android"
   android:layout_width="fill_parent"
   android:layout_height="fill_parent"
   android:textColor="@color/opaque_red"
   android:text="@string/hello" />

AndroidManifest.xml 파일은 앱의 기본적인 특징을 설명하고 각각의 요소를 정의한다.

