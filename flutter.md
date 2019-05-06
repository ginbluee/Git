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
# The getter 'alertDialogLabel' was called on null

I've found a solution to the problem, had to add fallback to localizationsDelegates, as follows:

```
localizationsDelegates: [
    .....
    const FallbackCupertinoLocalisationsDelegate(),
]
```
And the delegate:

```
class FallbackCupertinoLocalisationsDelegate
    extends LocalizationsDelegate<CupertinoLocalizations> {
  const FallbackCupertinoLocalisationsDelegate();

  @override
  bool isSupported(Locale locale) => true;

  @override
  Future<CupertinoLocalizations> load(Locale locale) =>
      DefaultCupertinoLocalizations.load(locale);

  @override
  bool shouldReload(FallbackCupertinoLocalisationsDelegate old) => false;
}
```
