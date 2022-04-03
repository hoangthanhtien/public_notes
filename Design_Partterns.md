## Phân loại Desgin Patterns
Có 3 nhóm chính:
- **Creational Pattern**: Cung cấp giải pháp để tạo ra các object và che giấu logic của việc tạo ra nó thay vì tạo trực tiếp bằng từ khóa `new`. Giúp cho chương trình trở nên mềm dẻo hơn trong việc quyết định object nào cần được tạo ra trong những tình huống được đưa ra.
	- Factory Method
	- Abstract Factory
	- Builder
	- Prototype
	- Singleton
- **Structural Pattern**: Thiết lập và định nghĩa quan hệ giữa các đối tượng
	- Adapter
	- Bridge
	- Compsite
	- Decorator
	- Facade
	- Flyweight
	- Proxy
- **Behavioral Pattern**: Thực hiện các hành vi của đối tượng , sự giao tiếp giữa các object với nhau.
	- Interpreter
	- Template method
	- Chan of Responsibility
	- Command
	- Iterator
	- Mediator
	- Memento
	- Observer
	- Strategy
	- Visitor

---
### Creawtional Patterns
#### Singleton
1. **Singleton là gì?**
Trong lập trình hướng đối tượng, đôi khi sẽ cần có một object chứa data có thể được truy xuất từ mọi nơi. Điều này có thể đạt được bằng cách sử dụng biến toàn cục, tuy nhiên nó sẽ vi phạm tinh đóng gói (Encapsulation) trong OOP. Đây chính là lúc cần ứng dụng **Singleton pattern**

2. Nguyên tắc khi Implement
	1. **private constructor** để hạn chế truy cập từ bên ngoài
	2. Đặt **private static final variable** đảm bảo biến chỉ được khởi tạo trong class
	3. Có một method **public static** để trả về instance được khởi tạo ở trên
3. Các cách implement
	1. **Eager initialization** - Singleton Class được khởi tạo ngay khi được gọi đến
		```java
		public class EagerInitializedSingleton{
			private static final EagerInitialiezedSingleton	INSTANCE = new EagerInitializedSingleton();
			// Private constructor để tránh client applications sử dụng constructor 
			private EagerInitializedSingleton(){
			
			}
	
			public static EagerInitializedSingleton getInstance(){
	
			}
		}
		```