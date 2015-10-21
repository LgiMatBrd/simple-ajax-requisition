# SIMPLE AJAX REQUISITION

Code created to show other developers how simple it is to run a query in ajax.

# REQUIRED

```bash
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
```

# USAGE

It's simple, just add this code to your HTML.
```bash
<script>
/********************************************/
/* FUNÇÃO PARA ENVIAR A REQUISIÇÃO POR AJAX
/********************************************/
$("form").submit(function (_event_) {
     _event_.preventDefault();
     var meuForm = this;
     var meuajax;
     meuajax = $.param($(meuForm).serializeArray());
     meuajax = meuajax;
     post = meuajax;
     $.postJSON = function(url, data, func) { $.post(url+(url.indexOf("?") == -1 ? "?" : "&")+"callback=?", data, func, "json"); }
     $.postJSON( URL, { ajax: meuajax }, resultado);
});
</script>
``` 
