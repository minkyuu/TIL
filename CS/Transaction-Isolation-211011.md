### 2021.10.11. TIL (Transaction Isolation Level)

## Transaction Isolation Level (트랜잭션 격리 수준)

>: 트랜잭션에서 일관성 없는 데이터를 허용하도록 하는 수준을 말한다.

<br>

### Q. Isolation Level이 필요한 이유는?

* DB는 ACID 특징과 같이 트랜잭션이 독립적인 수행을 하도록 한다.

* 이를 위해 Locking을 통해 어떤 트랜잭션이 DB를 다루는 동안 다른 트랜잭션이 관여하지 못하도록 막는 것이 필요하다.

* But! 무조건 Locking으로 동시에 수행되는 수많은 트랜잭션들을 순서대로 처리하는 방식으로 구현할 경우, DB의 성능이 떨어질 수 밖에 없다.

* 그렇다고 해서 성능을 높이기 위해 Locking 범위를 줄인다면 잘못된 값이 처리될 수 있는 문제가 발생한다.

    > (따라서 최대한 효율적인 Locking 방법이 필요하여 Isolation Level이 등장함)

<br>

## Isolation Level 종류

1. Read Uncommited (Level 0)

2. Read Commited    (Level 1)

3. Repeated Read     (Level 2)

4. Serializable          (Level 3)

<br>

---

## 1. Read Uncommited (Level 0)

* SELECT 문장이 수행되는 동안 해당 데이터에 Shared Lock이 걸리지 않는 계층

* "트랜잭션이 처리 중"이거나 "아직 Commit되지 않은 데이터(Uncommited)"를 다른 트랜잭션이 읽는 것(Read)을 허용한다.


    > 데이터베이스의 일관성을 유지하는 것이 불가능하다.

<br>

## 2. Read Commited (Level 1)

* SELECT 문장이 수행되는 동안 해당 데이터에 Shared Lock이 걸리는 계층

* 트랜잭션이 수행되는 동안 다른 트랜잭션이 접근할 수 없어 대기하게 된다.

* 트랜잭션이 완료됐거나 Commit이 이루어진 데이터만 조회가 가능하다.

* SQL 서버의 Default 레벨

<br>

## 3. Repeated Read (Level 2)

* 트랜잭션이 완료될 때까지 SELECT 문장이 사용하는 모든 데이터에 Shared Lock이 걸리는 계층

* 트랜잭션의 범위 내에서 조회한 데이터 내용이 항상 동일함을 보장한다.

    > (다른 사용자들은 해당 데이터 수정 불가능!)

<br>

## 4. Serializable (Level 3)

: 트랜잭션이 완료될 때까지 SELECT 문장이 사용하는 모든 데이터에 Shared Lock이 걸리는 계층

: 완벽한 읽기 일관성 모드를 제공한다.

: 다른 사용자는 트랜잭션 영역에 해당되는 데이터에 대한 수정 및 입력 불가능

 
<br>
 
## 낮은 단계의 Isolation Level로 조정하였을 때 발생하는 현상들

### 1. Dirty Read

>: 커밋되지 않은 수정중인 데이터를 다른 트랜잭션에서 읽을 수 있도록 허용할 때 발생하는 현상이다.

>: 어떤 트랜잭션에서 아직 실행이 끝나지 않은 다른 트랜잭션에 의한 변경사항을 보게되는 경우

 

### 2. Non-Repeated Read

>: 한 트랜잭션에서 같은 쿼리를 두 번 수행해야 할 때, 두 쿼리 사이에 다른 트랜잭션 값을 수정 or 삭제하면서 두 쿼리의 결과가 상이하게 나타나는 일관성이 깨지는 현상



### 3. Phantom Read

>: 한 트랜잭션 안에서 일정 범위의 레코드를 두 번 이상 읽었을 때, 첫번째 쿼리에서는 없었던 레코드가 두번째 쿼리에서는 나타나는 현상

<br>

## ※ Isolation Level 조정 시 고려사항

>: Isolation Level은 동시성과 데이터 무결성이 연관되어 있다.

>: 동시성을 증가시키면 (= Level을 낮추면) 데이터 무결성에 문제가 발생하고, 데이터 무결성을 유지하려고 하면 (= Level을 높이면) 동시성이 떨어지고 이에 따라 비용이 증가하게 된다.
