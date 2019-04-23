# remove default padding top while using ListView
```
padding: EdgeInsets.zero || MediaQuery.removePadding
```
# Clipboard
```
Clipboard.setData(new ClipboardData(text: data));
Clipboard.getData('text/plain').then((results) {
  print(results.text);
});
```
