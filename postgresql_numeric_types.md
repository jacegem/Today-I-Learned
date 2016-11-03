# Postgresql Numeric Types

https://www.postgresql.org/docs/9.0/static/datatype-numeric.html


# 8.1. 숫자 유형 Numeric Types

숫자 유형은 2, 4, 8 바이트 정수, 4, 8 바이트 부동 소수점 숫자, 선택 정밀도수로 구성되어 있습니다. 
표 8-2 는 가능한 숫자 유형을 나열 하였습니다.

표 8-2. 숫자 유형

| 명칭 | 저장 크기 | 설명 | 범위 |
| -- | -- | -- | -- |
| 0:2 | 1:2 | 2:2 | 3:2 |
| 0:3 | 1:3 | 2:3 | 3:3 |
| 0:4 | 1:4 | 2:4 | 3:4 |
| 0:5 | 1:5 | 2:5 | 3:5 |
| 0:6 | 1:6 | 2:6 | 3:6 |
| 0:7 | 1:7 | 2:7 | 3:7 |
| 0:8 | 1:8 | 2:8 | 3:8 |
| 0:9 | 1:9 | 2:9 | 3:9 |
| 0:10 | 1:10 | 2:10 | 3:10 |
	 		
smallint	2 bytes	small-range integer	-32768 to +32767
integer	4 bytes	typical choice for integer	-2147483648 to +2147483647
bigint	8 bytes	large-range integer	-9223372036854775808 to 9223372036854775807
decimal	variable	user-specified precision, exact	no limit
numeric	variable	user-specified precision, exact	no limit
real	4 bytes	variable-precision, inexact	6 decimal digits precision
double precision	8 bytes	variable-precision, inexact	15 decimal digits precision
serial	4 bytes	autoincrementing integer	1 to 2147483647
bigserial	8 bytes	large autoincrementing integer	1 to 9223372036854775807