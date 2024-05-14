# JS-API
## PRIMER
### Picking
#### Screen에서 파트 선택하고 TextBox에 파트 ID 표기
파트를 선택하기 위해서는 먼저 선택할 파트가 있는 Model을 가져와야 한다. Model은 Model class로 다음과 같이 가져올 수 있다.

```Java
var m = Model.GetFromID(1);
```

Screen에서 마우스 클릭으로 파트를 선택하기 위해 Part class의 Pick 함수를 사용하여 파트를 선택하고 다음과 같이 파트를 가져옵니다. 여기서 m은 위에서 얻은 모델입니다.

```Java
var part = Part.Pick('Pick part from screen', m);
```

만약 GUI Builder에서 TB_PartID라는 TextBox widget을 생성하였다면 다음으로 TextBox에 파트 ID를 입력할 수 있습니다.

```Java
gui.Window1.TB_PartID.text = part.pid;
```

