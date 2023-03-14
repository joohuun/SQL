### SQL 문법정리

### DML(Data Manipulation Language)
- insert
- update
- delete
- select

### DDL(Data Definition Language)
- create
- alter
- drop
- truncate
- rename

### DCL(Data control Language)
- grant
- rollback
- savepoint

***

### Create                  
- 테이블 생성            
create table 테이블이름(     
    칼럼명 데이터타입 조건,       
    칼럼명 데이터타입 조건,       
    ...     
    칼럼명 데이터타입 조건            
);          

- ex)            
create table customer(      
    ID          int             not null,       
    name        varchar(20)     not null,           
    age         int             not null,       
    address     char(25),       
    salary      decimal(18,2)           
);      

--------

### 사용자 
- 사용자 조회    
> use mysql;    
> SELECT user, host from user;      

- 사용자 생성    
> CREATE user '사용자'@'host' identified by '비밀번호';    
> ex) 내부접근을 허용하는 사용자 추가      
> CREATE user 'test'@'localhost' identified by '1234';      
> ex) 외부접근을 허용하는 사용자 추가       
> CREATE user 'test'@'%' identified by '1234';      
> ex) 특정 ip만 접근을 허용하는 사용자 추가      
> CREATE user 'test'@'10.10.1.100' identified by '1234';        

- 사용자 제거
> DROP user '사용자'@'host';       

- 사용자 권한 부여         
> ex) 모든 데이터베이스의 모든 테이블에 권한 부여        
> GRANT ALL privileges on *.* '사용자'@'host';
> ex) 특정 데이터베이스의 모든 테이블에 권한 부여      
> GRANT ALL privileges on DB명.* '사용자'@'host';          
> ex) 특정 데이터베이스의 특정 테이블에 권한 부여      
> GRANT ALL privileges on DB명.테이블명 '사용자'@'host';        
