# 2021.8.3. TIL (2.Automation with python)


### openpyxl를 이용하여 엑셀 데이터 읽기 (Read)
1. 엑셀 파일 읽기
```python
from openpyxl import load_workbook

wb = load_workbook('simple_data.xlsx')
data = wb.active

print(data['A1'].value)
print(data['A2'].value)
print(data['B1'].value)
print(data['B2'].value)
```
---

2. 행, 열 데이터를 읽기
```python
from openpyxl import load_workbook

wb = load_workbook('simple_data.xlsx')
data = wb.active

# 한 행을 출력해보기
row = data['2']
for cell in row:
    print(cell.value)

print('-'*20)

# 한 열을 출력해보기
col = data['A']
print(col)
for cell in col:
    print(cell.value)

```

---

 
3. 영역으로 데이터 읽기
```python
from openpyxl import load_workbook

wb = load_workbook('simple_data.xlsx')
data = wb['sheet_test']

area = data['A1:B2']
for row in area:
    for cell in row:
        print(cell.value)


cols = data['A:B']
for col in cols:
    for cell in col:
        print(cell.value)

print('-'*20)

rows = data['1:2']
for row in rows:
    for cell in row:
        print(cell.value)
```

---

4. iter_rows() 활용하여 행 데이터 읽기
```python
from openpyxl import load_workbook

wb = load_workbook('test_data.xlsx', read_only=True)
data = wb.active

for row in data.iter_rows():
    for cell in row:
        print(cell.value)
```

---


### 엑셀 파일에 데이터 쓰기 (Write)
1. 새로운 시트를 만들어서 그 시트에 데이터 입력
```python
from openpyxl import Workbook

wb = Workbook()
ws = wb.create_sheet('sheet_test2')

ws['A1'] = 'alghost'
ws['B1'] = 'test'

wb.save('result.xlsx')

```

---


2. 반복문(for문)을 사용하여 데이터 쓰기
```python
from openpyxl import Workbook

wb = Workbook()
ws = wb.create_sheet('sheet_test3')

ws.append(['Number', 'Name'])

for i in range(10):
    ws.append([i, str(i) + ' data'])

wb.save('result2.xlsx')

data = wb.active
for line in data.iter_rows():
    print(line)
```
