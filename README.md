

#cmp2beans

##What
利用java的反射机制，比较两个实体类的属性值是否相等，字符串支持正则表达式匹配，同时支持只对两个实体类的字符类型进行比较。

Compare two java beans with java Reflection.

##Features
* 比较两个实体类的属性值是否相等
* 支持正则比较两个字符串
* 支持只比较字符串


* Compare two java beans
* Support regular string comparison 
* Support only compare string in two beans.

##Demo
```java
public class Run {
    public static void main(String[] args) throws Exception {
		Cmp2beans cmp2beans=new Cmp2beans();
		Host whiteHost=new Host();
		Host blackHost=new Host();
		
		List whiteDogs=new ArrayList();
		List blackDogs=new ArrayList();
		whiteDogs.add(new Dog("jia",10.5));
		blackDogs.add(new Dog("ji[\\s\\S]*", 10.5));
		
		whiteHost.setAge(30);
		whiteHost.setCat(new Cat("tom", 3));
		whiteHost.setDogs(whiteDogs);
		blackHost.setAge(30);
		blackHost.setCat(new Cat("tom", 2));
		blackHost.setDogs(blackDogs);
		
		cmp2beans.compare(whiteHost, blackHost, true, false);
		
	}
}
```
```java
public class Host {
    public String name;
	public int age;
	public double high;
	public Cat cat;
	public List<Dog> dogs;
	public String getName() {
		return name;
	}
	public void setName(String name) {
		this.name = name;
	}
	public int getAge() {
		return age;
	}
	public void setAge(int age) {
		this.age = age;
	}
	public double getHigh() {
		return high;
	}
	public void setHigh(double high) {
		this.high = high;
	}
	public Cat getCat() {
		return cat;
	}
	public void setCat(Cat cat) {
		this.cat = cat;
	}
	public List<Dog> getDogs() {
		return dogs;
	}
	public void setDogs(List<Dog> dogs) {
		this.dogs = dogs;
	}
}
```
```java
public class Cat {
    public String name;
	public int age;
	public Cat(String name,int age){
		this.name=name;
		this.age=age;
	}
	public String getName() {
		return name;
	}
	public void setName(String name) {
		this.name = name;
	}
	public int getAge() {
		return age;
	}
	public void setAge(int age) {
		this.age = age;
	}
}
```
```java
public class Dog {
    public String name;
	public double wight;
	public Dog(String name,double wight){
		this.name=name;
		this.wight=wight;
	}
	public String getName() {
		return name;
	}
	public void setName(String name) {
		this.name = name;
	}
	public double getWight() {
		return wight;
	}
	public void setWight(double wight) {
		this.wight = wight;
	}
	
}
```

##Weibo
weibo:[@孔子日的对](http://weibo.com/zwsq123/)
