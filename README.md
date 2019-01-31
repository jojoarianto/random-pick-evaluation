# Random Pick Evaluation

## Quickstart
- Open browser (Chrome, Mozilla)
- Login to cybercampus
- Navigate to your evaluation page
- Open inspect elements (Ctrl+Shift+i) on windows or (Cmd+Option+i) on mac
- On inspect elements window, click Console section
- Copy & paste code below

```javascript
var valueOptions = Array(3,4); // baik, sangat baik
$('input:radio[name*="nilai"]').filter('[value="'+valueOptions[0]+'"]').attr('checked', true); // default

$('input:radio[name*="nilai"]').each(function() {
    var random = valueOptions[Math.floor(Math.random()*valueOptions.length)];
    $(this).filter('[value="'+random+'"]').attr('checked', true);
});
```

- Press enter
- Back to your evaluation page
- Save it!

### Code Explaination

```javascript
// random value you want
var valueOptions = Array(3,4);
// means valueOptions : 
//        Sering / Baik / Cukup jelas,
//        Selalu / Sanat Baik / Sangat jelas
```

- 1 => Tidak Pernah / Buruk / Tidak jelas
- 2 => Jarang / Kurang baik / Kurang jelas
- 3 => Sering / Baik / Cukup jelas
- 4 => Selalu / Sangat baik / Sangat jelas
- 0 => Tidak Ada Pendapat

Thanks!