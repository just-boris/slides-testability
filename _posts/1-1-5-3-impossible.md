## Без тестов вообще никак

```javascript
it('should format time', function() {
    expect(formatTime(false)).toBe('0');
    expect(formatTime(1100)).toBe('1s 100ms');
    expect(formatTime(25*3600*1000+62000)).toBe('25h 1m');
});
```

{% include fragment.html %}
Больше мне не нужно ждать 25 часов, чтобы воспроизвести баг!
<img style="" src="img/crying-face.jpg">
