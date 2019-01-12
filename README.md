
* 변수
  
  [Java] String name = "abc";		->	[Kotlin] val name = "abc"

* 객체생성

  [Java] Person person = new Person	->	[Kotlin] val person = Person(name)

* Null 허용/비 허용

  1. Null 허용
    Ex) val foo: String? = null 
  2. Null 비 허용
    Ex) val bar: String = "bar"

* val / var

  - val : final 의미 (수정불가)
  - var : values 수정 가능

* List

  1. listOf : add() 사용 불가
     Ex) val immutable: List<String> = listOf("foo", "bar", "baz")
  2. MutableListof : add() 사용 가능
     Ex) val mutable: MutableList<String> = MutableListof("foo", "bar", "baz");

*메서드

    fun gerrt(name: String) : Unit {		Unit -> Void
    }						Void 같은 경우 생략도 가능


*클래스&인터페이스 선언

*조건문 

  1. if문은 동일
  2. Switch
   [Java] switch	            ->		[Kotlin] when
   Ex)
        when(count) {
	1 -> 
	else -> 
        }
   3. for, for-each 
   Ex)
        val items = listof("foo", "bar", "baz")
        for(item in items){
        }
   
  
* 비트연산자

   [Java] int foo = ( 2 | 4 ) << 1;  ->		[Kotlin] val foo: Int = (2 or 4) shl 1
   [Java] char c 65;	             ->		[Kotlin] val c : Char = 65 (X) : 문자열만 가능하며 toChar() 사용하면 가능
						[Kotlin] val c : Char = 'A' (O)
						[Kotlin] val code : Int = 65
						[Kotlin] val ch : Char = code.toChar()
							



   ||, &&, ! 는 자바와 동일


* 생성자

   [Java] class명{ }           	   ->	        [Kotlin]init{}

* Setter/Getter

  아래의 형태로 해두면 자동으로 Setter/Getter 사용 가능
    val name : String? = null
    var name : String? = null

* 접근제한자 

  public    : 어디서든 사용 가능
  internal  : 같은 모듈에서 사용 가능.
  protected : private + subclass 에서까지 사용 가능.
  private   : 해당 클래스 or 인터페이스 내부에서만 사용 가능.

  접근제한자 없는 경우 public 으로 간주하며, Kotlin에서 internal 접근제한자가 추가 됨.
    

* 기타 

  - String.format() 자바와 동일
  - val length : Int = 3000
  - val lengthText : String = String.format("Length: %d meters"), length)
    > 위의 코드 단축 : val lengthText : String = "Length: $length meters"
  - TextLenth
  - leteinit var address : String?
    leteinit : 나중에 값 할당되며 var 프로퍼티만 사용가능
  
