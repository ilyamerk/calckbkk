
# Salary Calculator (GitHub Pages)

Готовый самостоятельный HTML-калькулятор.

## Публикация на GitHub Pages

1. Создайте публичный репозиторий, например `salary-calc`.
2. Загрузите файлы `index.html` и `salary-calc.html` в корень репозитория.
3. В настройках репозитория откройте **Settings → Pages**.
4. В разделе **Build and deployment** выберите:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` / `/root` (обычно `main`) и директория `/ (root)`
5. Сохраните. Через минуту сайт будет доступен по адресу:
   `https://<ваш_логин>.github.io/salary-calc/`

## Использование в Битрикс24

Вставьте на страницу HTML-блок с iframe:

```html
<iframe id="salaryCalcFrame"
        src="https://<ваш_логин>.github.io/salary-calc/"
        style="width:100%;border:0;display:block;min-height:1200px;background:transparent"
        scrolling="no"></iframe>
<script>
window.addEventListener('message',function(e){
  if(!e.data || e.data.type!=='salaryCalcHeight') return;
  var f=document.getElementById('salaryCalcFrame');
  if(f) f.style.height = Math.max(1200, e.data.height) + 'px';
});
</script>
```

Готово.
