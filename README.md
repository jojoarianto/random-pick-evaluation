# Random Pick Evaluation

Quickstart
- Open browser (Chrome, Mozilla)
- Login to cybercampus
- Navigate to your evaluation page
- Open inspect elements (Ctrl+Shift+i) on windows or (Cmd+Option+i) on Mac
- On inspect elements window, click Console section
- Copy & Paste code below

```javascript
var valueOptions = Array(3,4); // cukup jelas, sangat jelas
var row = $('input:radio[name*="nilai"]');
for (var i = row.length - 1; i >= 0; i--) {
    var random = valueOptions[Math.floor(Math.random()*valueOptions.length)]
    $(row[i]).filter('[value="'+random+'"]').attr('checked', true);
}
```

- Enter
- Back to your evaluation page
- Save

### Code Explaination

```javascript
// random value you want
var valueOptions = Array(3,4);
// means : valueOptions : 
//    Sering / Cukup jelas,
//    Selalu / Sangat jelas

```

- 1 => Tidak Pernah / Tidak jelas
- 2 => Jarang / Kurang jelas
- 3 => Sering / Cukup jelas
- 4 => Selalu / Sangat jelas
- 0 => Tidak Ada Pendapat