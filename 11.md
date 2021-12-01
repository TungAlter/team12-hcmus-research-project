# Research Project 11: Proxy
## I. What Is Proxy ?
Assumed that you have a computer system in your organization that being used by two type of users. One of them is employees (aka Users) which have limited access to some of the functions on the system. The others one is Managers (aka Admins) which have all access to Users functions as well of some of the function that only them allowed to run.

The easy solution for this problem in OOP would be using Inheritance:<br><br>
![](https://raw.githubusercontent.com/trunghieumickey/team12-hcmus-research-project/main/naive.png)
```c++
class User{
	protected:
		string someData;
	public:
		void UserFunction(){
			cout << "UserFunction";
		}
};

class Admin : public User{
	public:
		void AdminFuction(){
			cout << "AdminFuction";
		}
};
```

But this does come up with a few problems. One of them is that a User pointer couldn't be contain an admin very well in case your app also have to support an Admin to run their functions
```c++
User *Joe = new Admin;
Joe->AdminFunction();
```
```
Error: no member named 'AdminFunction' in 'User'
```
Even if you somehow work around that (like using interpreter programing language). It would still halt when Users try to run Admin only functions and it could breakdown the whole system. It would be way better if the program is responded to the Users that they can't run Admin function but still effective at protecting the system from being exploits from Users.

## II. Advantages and Drawbacks of Proxy Design

## III. Types of Proxy and it real world examples

## IV. Reference Sources
- https://www.geeksforgeeks.org

## VI. About Our Team

### Group Members

- Lê Trần Trung Hiếu [20127158] [@trunghieumickey](https://github.com/trunghieumickey)
- Nguyễn Hoàng Gia Huy [20127186] [@giahuyday](https://github.com/giahuyday)
- Thái Văn Thiên [20127631] [@thienhk15](https://github.com/thienhk15)
- Lê Phan Duy Tùng [20127661] [@TungAlter](https://github.com/TungAlter)

*github accounts included to tracking commits on github

### Class Info
- Class ID: **20CLC01**
- Subject: 	Object Oriented Programming
- Instructors: Nguyễn Lê Hoàng Dũng
- Project subject: Proxy
- Project ID : 11
