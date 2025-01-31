# 키친포스

## 요구 사항

- 식당의 판매 정보 관리를 하는 포스기를 구현한다.
- 메뉴 그룹(Menu Group)
    - 새로운 메뉴 그룹을 추가할 수 있다.
        - [ ] 메뉴 그룹의 식별번호는 중복될 수 없다.
        - [ ] 이름이 없는 메뉴 그룹은 추가할 수 없다.
    - 메뉴 그룹의 목록을 조회할 수 있다.
        - [ ] 추가된 메뉴 그룹은, 목록을 조회할 때 보여야 한다.
- 메뉴(Menu)
    - 새로운 메뉴를 추가할 수 있다.
        - [ ] 메뉴의 식별번호는 중복될 수 없다.
        - [ ] 메뉴의 가격은 필수 값이며 음수가 될 수 없다.
        - [ ] 기존에 존재하는 메뉴 그룹에 메뉴가 속해야한다.
        - [ ] 메뉴는 반드시 한개 이상의 product 로 구성되어야 한다.
        - [ ] 메뉴를 구성하는 product 들은, 이미 추가된 product 여야만 한다.
        - [ ] 메뉴 안의 한 product 수량(quantity)은 음수일 수 없다.
        - [ ] 메뉴의 가격은 각 product 의 가격과 수량을 곱해서 전부 더한 값보다 작아야한다.
        - [ ] 메뉴의 이름은 필수값이며, 비어있을 수 없다.
        - [ ] 메뉴의 이름은 저속해서는 안된다. (should not be profanity)
    - 메뉴의 가격을 수정할 수 있다.
        - [ ] 수정하는 가격은 필수값이다.
        - [ ] 수정하는 가격은 음수일 수 없다.
        - [ ] 수정할 메뉴는 이미 추가된 메뉴여야 한다.
        - [ ] 메뉴의 가격은 각 product 의 가격과 수량을 곱해서 전부 더한 값보다 작아야한다.
    - 메뉴가 보여지도록 할 수 있다.
        - [ ] 보여지는 메뉴는 조회할 수 있어야 한다.
    - 메뉴가 숨겨지도록 할 수 있다.
        - [ ] 숨겨진 메뉴는 조회가 불가능해야 한다.
    - 메뉴들의 목록을 조회할 수 있다.
        - [ ] 추가하거나 수정한 메뉴들이 메뉴 목록에 반영되어야 한다.
- 주문 테이블(Order Table)
    - 새로운 주문 테이블을 추가할 수 있다.
        - [ ] 주문 테이블의 식별번호는 중복될 수 없다.
        - [ ] 새로 추가된 테이블은 비어있으며, 0명의 손님이 앉아있다.
    - 주문 테이블에 사람이 앉았음을 표시할 수 있다.
        - [ ] 이미 추가된 테이블만 조작할 수 있다.
        - [ ] 주문 테이블이 비어있지 않다고 표시되어야 한다.
    - 주문 테이블이 비게 되었음을 표시할 수 있다.
        - [ ] 이미 추가된 테이블만 조작할 수 있다.
        - [ ] 주문 테이블이 비었다고 나타나야 한다.
        - [ ] 주문 테이블의 앉아있는 손님 숫자가 0명이 되어야 한다.
    - 주문 테이블에 앉아있는 손님의 숫자를 변경할 수 있다.
        - [ ] 앉아있는 손님의 숫자는 음수가 될 수 없다.
        - [ ] 이미 추가된 테이블만 손님 숫자를 변경할 수 있다.
        - [ ] 비어있지 않은 테이블만 손님 숫자를 변경할 수 있다.
    - 주문 테이블들의 목록을 조회할 수 있다.
        - [ ] 추가하거나 수정한 주문 테이블들이 주문 테이블 목록에 반영되어야 한다.
- 상품(Product)
    - 새로운 상품을 추가할 수 있다.
        - [ ] 상품의 식별번호는 중복될 수 없다.
        - [ ] 상품의 가격은 필수값이며, 음수일 수 없다.
        - [ ] 상품의 이름은 필수값이며, 저속해서는 안된다.
    - 상품의 가격을 수정할 수 있다.
        - [ ] 상품의 가격은 필수값이며 음수일 수 없다.
        - [ ] 이미 추가된 상품만 수정할 수 있다.
        - [ ] 상품 가격 수정으로 인해, 상품의 합한 값보다 더 비싸진 메뉴가 있다면, 메뉴가 숨겨져야 한다.
    - 상품들의 목록을 조회할 수 있다.
        - [ ] 추가하거나 수정한 상품들이 상품 목록에 반영되어야 한다.

## 용어 사전

| 한글명 | 영문명 | 설명 |
| --- | --- | --- |
| 주문 테이블 | Order Table | 주문이 이루어지는 테이블 |
| 테이블 그룹 | Table Group | 테이블들의 그룹 |
| 주문 | Order | 실제로 이루어진 주문 |
| 메뉴 | Menu | 주문 가능한 메뉴 |
| 메뉴 그룹 | Menu Group | 메뉴들의 그룹 |
| 상품 | Product | 메뉴가 제공하는 상품. 한 상품이 여러개의 메뉴에 속할 수도 있다. |
| 비속어 | Profanity | 이름을 지을때 필터링해야하는 단어이다. |
| 손님 숫자 | Number Of Guests | 한 테이블에 앉아있는 손님의 숫자를 뜻한다. |
| 공석 | Empty | 테이블이 비어있는지 그 여부를 나타낸다. |
| 표시 | display | 메뉴를 표시해야함을 뜻한다. |
| 숨김 | hide | 메뉴를 숨겨야한을 뜻한다. |

## 엔티티 분석

- 테이블(Order Table)
    - 주문이 이루어지는 곳을 테이블이라 부른다.
    - 여러개의 테이블은 하나의 테이블 그룹에 속한다.
    - 테이블은 새로 추가될 수 있다.
    - 테이블에 사람이 앉아있는지 비어있는지 확인할 수 있다.
    - 테이블에 비어있는지 여부를 변경할 수 있다.
    - 테이블에 사람이 몇명 앉아있는지 확인할 수 있다.
    - 테이블에 사람이 몇명 앉아있는지 변경할 수 있다.
    - 테이블들의 목록을 조회할 수 있다.
- 주문(Order)
    - 주문이 어느 테이블에서 이루어졌는지 알 수 있어야 한다.
    - 주문은 메뉴를 단위로 이루어진다.
    - 한 주문에 여러개의 메뉴를 시킬 수 있다.
- 메뉴(Menu)
    - 메뉴는 여러 종류와 여러개의 상품으로 이루어져있다.
    - 메뉴는 하나의 메뉴 그룹에 속한다.
    - 메뉴는 새로 추가될 수 있다.
    - 추가된 메뉴는 보여지거나, 숨겨져서 보여지지 않을 수도 있다.
    - 메뉴는 이름과 가격을 가진다.
    - 메뉴의 가격은 수정될 수 있다.
    - 메뉴들의 목록을 조회할 수 있다.
- 상품(Product)
    - 상품은 여러 메뉴에 중복되어 속해있을 수 있다.
    - 상품은 새로 추가될 수 있다.
    - 상품은 이름과 가격을 가진다.
    - 상품의 가격은 수정될 수 있다.
    - 상품들의 목록을 조회할 수 있다.

## 모델링

![ERD](erd.png)

- table_group
    - 테이블을 그룹 번호로 묶는다.
- order_table
    - 한 테이블 그룹에 속한 테이블들을 나타냄
    - 테이블이 비어있는지(empty), 몇명의 손님이 테이블에 있는지에 대한 정보가 있다.
- orders
    - 테이블에서 일어난 주문들
    - 주문 시간과 주문 상태 정보가 있다.
- menu_group
    메뉴들을 그룹으로 묶는다.
- menu
    - 주문 가능한 메뉴들이다.
    - 메뉴 이름과 가격에 관한 정보가 있다.
- product
    - 메뉴에서 제공하는 상품들이다.
    - 상품의 이름과 가격 정보가 있다.
- order_line_item
    - 주문에서 메뉴를 몇개나 시켰는지 나타낸다.
- menu_product
    - 메뉴에서 해당 상품을 몇개나 제공하는지 나타낸다.

## API Doc

### Menu Group

#### POST /api/menu-groups

메뉴 그룹을 추가

#### GET /api/menu-groups

메뉴 그룹의 목록을 조회

### Menu

#### POST /api/menus

메뉴를 추가

#### PUT /api/menus/{menuId}/price

메뉴의 가격을 수정

#### PUT /api/menus/{menuId}/display

메뉴가 보여지도록 수정

#### PUT /api/menus/{menuId}/hide

메뉴가 숨겨지도록 수정

#### GET /api/menus/{menuId}

메뉴들의 목록을 조회

### Order Table

#### POST /api/order-tables

주문 테이블을 추가

#### PUT /api/order-tables/{orderTableId}/sit

주문 테이블에 사람이 앉았음을 표시

#### PUT /api/order-tables/{orderTableId}/clear

주문 테이블이 비어있음을 표시

#### PUT /api/order-tables/{orderTableId}/number-of-guests

주문 테이블에 앉아있는 손님의 숫자를 변경

#### GET /api/order-tables

주문 테이블들의 목록을 조회

### Product

#### POST /api/products

상품을 추가

#### PUT /api/products/{productId}/price

상품의 가격을 수정

#### GET /api/products

상품들의 목록을 조회
