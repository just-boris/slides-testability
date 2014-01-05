## Советы

**3. Генерируйте тесты и тестовые данные**

Тестов должны быть короткими, но их должно быть много. Таким образом легко протестировать всю функциональ&shy;ность и быстро найти в чем же проблема.

Например, вот 4 теста в одном:

```
['a', 'b', 'c', 'd'].forEach(function(letter) {
    it('should set letter '+letter, function() {
        module.setLetter(letter);
        expect(module.getLetter()).toBe(letter)
    });
});
```