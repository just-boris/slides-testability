## Параметризованные тесты

Несколько тестов в одном:

```
['a', 'b', 'c', 'd'].forEach(function(letter) {
    it('should set letter '+letter, function() {
        module.setLetter(letter);
        expect(module.getLetter()).toBe(letter)
    });
});
```