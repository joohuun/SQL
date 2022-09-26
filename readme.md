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
create table 테이블이름 (     
    칼럼명 데이터타입 조건,       
    칼럼명 데이터타입 조건,       
    ----     
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

