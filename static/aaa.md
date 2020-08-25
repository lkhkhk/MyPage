


> Written with [StackEdit](https://stackedit.io/).
 
데이타베이스 변경관리를 위해서 영구브랜치의 버전을 관리한다.
영구브랸치에서 만드는 개발브랜치는 영구브랜치의 버전으로 초기화 한다.
개발브랜치를 영구브랜치에 병합할 때 영구브랜치의 버전을 증가시킨다.
영구 브랜치의 버전이 증가하면 개발 브랜치는 영구 브랜치를 병합하고 개발 브랜치의 버전을 영구 브랜치의 버전으로 변경한다.

|  | D |  |
|--|--|--|
| Create branch Develop | 0.0.0 |  |



|<td colspan=2> D | Fs | Rs | Hs | M |
| - | - | - | - | - | - | - |-|-|
|Create branch Develop | 0.0.0 | | | |
|Create branch Master from Develop | 0.0.0|  | | |**0.0.0** | 
| 3 <td rowspan=2 colspan=2>Create branch Feature(F1) from Develop | 0.0.0 | 0.0.0 | | | 0.0.0 | 
| | | **0.0.0(F1)** | | | | 
| 4 <td colspan=2>Merge branch Feature(F1) into Develop | **0.0.1(F1)** | 0.0.0(F1) | | | 0.0.0 | 
| 5 <td rowspan=2 colspan=2>Create branch Hotfix(H1) from Master | 0.0.1(F1) | | | 0.0.0 | 0.0.0 | 
| | | | | **0.0.0(H1)** | | 
| 6-1 <td rowspan=2 colspan=2>Merge branch Hotfix(H1) into Master | 0.0.1(F1) | | | 0.0.0 | 0.0.0 | 
| | | | | 0.0.0(h1) | **0.1.0(H1)** | 
| 6-2 <td rowspan=2 colspan=2>Merge branch Hotfix(H1) into Develop | 0.0.1(F1) | | | | 0.1.0(h1) | 
| | **0.1.1(H1)** | | | | | 
| 6-3 <td rowspan=2 colspan=2>Merge branch Hotfix(H1) into Release(R1) | 0.1.1(H1) | | | | 0.1.0(h1) | 
| | | | **0.1.1(H1)** | | 
| | | | | | | | | | 0.0.0(H1) | | 

| 8 <td rowspan=2 colspan=2>Create branch Release(R1) from Develop | 0.0.1(F1) | | 0.0.1(F1) | | 0.0.0 | | | | | **0.0.1(R1)** | | | 
| C <td colspan=2>Create branch Feature(F2) from Develop 
| C <td colspan=2>Merge branch Feature(F2) into Develop 
| C <td colspan=2>Create branch Feature(F3) from Develop 
| C <td colspan=2>Create branch Hotfix(H2) from Master

| C <td colspan=5>Create branch Master from Develop | | 0.0.0 | | | | 0.0.0 | 
| <td rowspan=2>triple | ddd | dddd| | | H1 | H1 | H1 | H1 | H1 | | | F1 | F1 | F1 | **H2** | | | | F2 | F2 | **R1** | | | | | **F3** | | | | | <td colspan=5>triple

| 0.1.2 | 0.1.2 | 0.1.1 | 0.1.0 | 0.1.0 |

-	[x] Create branch Develop
-	[x] Create branch Master from Develop
-	[x] Create branch Feature(F1) from Develop
-	[x] Merge branch Feature(F1) into Develop
-	[ ] Create branch Release(R1) from Develop
-	[x] Create branch Feature(F2) from Develop
-	[x] Merge branch Feature(F2) into Develop
-	[x] Create branch Hotfix(H1) from Master
-	[x] Merge branch Hotfix(H1) into Master, Develop, Release(R1)
-	[ ] Create branch Feature(F3) from Develop
-	[ ] Create branch Hotfix(H2) from Master

| 0.1.2 | 0.1.2 | 0.1.1 | 0.1.0 | 0.1.0 |

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIyODQ0Njg3XX0=
-->