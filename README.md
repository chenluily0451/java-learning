# java基础



一、 重写与重载的区别(2018-07-30)

1. 重写就是重新写一遍的意思。其实就是在子类中把父类本身有的方法重新写一遍。子类继承了父类原有的方法，但有时子类并不想原封不动的继承父类中的某个方法，所以在**方法名，参数列表，返回类型(除过子类中方法的返回值是父类中方法返回值的子类时)**都相同的情况下， 对方法体进行修改或重写，这就是重写。但要注意子类函数的访问修饰权限不能少于父类的。 

        public class Father {
    
            public static void main(String[] args) {
                // TODO Auto-generated method stub
                Son s = new Son();
                s.sayHello();
            }
        
            public void sayHello() {
                System.out.println("Hello");
            }
        }
    
        class Son extends Father{
        
            @Override
            public void sayHello() {
                // TODO Auto-generated method stub
                System.out.println("hello by ");
            }
        
        }
**重写 总结**：
 
发生在父类与子类之间 

方法名，参数列表，返回类型（除过子类中方法的返回类型是父类中返回类型的子类）必须相同 

访问修饰符的限制一定要大于被重写方法的访问修饰符（public>protected>default>private) 

重写方法一定不能抛出新的检查异常或者比被重写方法申明更加宽泛的检查型异常


2. 重载(Overload) 