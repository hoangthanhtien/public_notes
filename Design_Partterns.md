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
	
	>- Đảm bảo rằng một class sẽ chỉ có duy nhất một instance
	>- Cung cấp một điểm truy cập global tới instance đó

2. **Cách implement**
	Có nhiều cách để implement nhưng sẽ tuân theo hai bước thông dụng:
	- Đặt default constructor thành private, để ngăn các object khác sử dụng `new`  để tạo một instance khác của Singleton class
	- Tạo một static creation method hoạt động như một constructor. Method này thực chất sẽ gọi private constructor để tạo một object rồi lưu nó vào trong một static field. Tất cả các lần call tới method này đều sẽ trả về object được cache đó
3. Cấu trúc
	![[Pasted image 20220403224205.png]]

```python

```