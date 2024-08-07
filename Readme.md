# Queue Process

### 폴더명으로 Folder ID 값가져오기 
- `/odata/Folders`
	- `$filter` `DisplayName eq 'KABANG01'`
	- ```sh
	https://fdx.local/default/DefaultTenant/orchestrator_/odata/Folders?%24filter=DisplayName%20eq%20'KABANG01'
	```
	- ```sh
	curl -X 'GET' \
  'https://fdx.local/default/DefaultTenant/orchestrator_/odata/Folders?%24filter=DisplayName%20eq%20'\''KABANG01'\''' \
  -H 'accept: application/json' \
  -H 'authorization: Bearer exampletoken'
	```
	- Id: `52`
	
### 특정 폴더의 Queue ID 값 가져오기
- `https://fdx.local/default/DefaultTenant/orchestrator_/odata/QueueDefinitions`
- Id: `12`
- Name: `PostRegInquiry`

### 컬럼
- `in_dt_PostReg(lastRowNum)("날짜")`
- `in_dt_PostReg(lastRowNum)("시간")`
- `in_dt_PostReg(lastRowNum)("발생국")`
- `in_dt_PostReg(lastRowNum)("처리현황")`

### 기타
- `out_TransactionItem.SpecificContent("regNumber")`