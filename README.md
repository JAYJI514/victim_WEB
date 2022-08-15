# victim_WEB
READ ME

PenTEST WEB version info

펜테스트용 웹서버로 아래 버전을 사용하였습니다.
WEB Sever :  Apache HTTP Server, version 2.4.
Programming : PHP Version 8.0.1
DB : MySQL Community Server


common.php에 설정된 DB연결 내역을 변경한다

ID와 PW는
root / password로 기본값 설정되어있으니
Mysql 에 설정된 계정을 입력합니다.


추가로 아래 쿼리 값을 DB에 입력하여 기본 게시글 DB를 생성합니다.  

create database pentest;
use pentest;
create table members(
idx int not null auto_increment,
id varchar(30),
password varchar(100),
name varchar(50),
email varchar(30),
company varchar(30),
primary key(idx)
)DEFAULT CHARSET = utf8;
create table insecure_board(
idx int not null auto_increment,
title varchar(50),
content text,
id varchar(20),
writer varchar(30),
password varchar(50),
file varchar(50),
regdate date,
secret varchar(2),
primary key(idx)
)DEFAULT CHARSET = utf8;
create table customer_info(idx int, id varchar(15), password varchar(30), jumin varchar(15));
