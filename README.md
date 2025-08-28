
# Salary Calculator — GitHub Pages

Готовый `index.html` для публикации на GitHub Pages.

## Публикация
1) Создайте публичный репозиторий, напр. `salary-calc`.
2) Загрузите `index.html` в корень репозитория.
3) В репозитории: **Settings → Pages → Build and deployment** → Source: **Deploy from a branch**, Branch: **main** / **/(root)**.
4) Откройте URL вида: `https://<ваш_логин>.github.io/<репозиторий>/`.

## Встраивание в Битрикс24
```html
<iframe id="salaryCalcFrame"
        src="https://<ваш_логин>.github.io/<репозиторий>/"
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
