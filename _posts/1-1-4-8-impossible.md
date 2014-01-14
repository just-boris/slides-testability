## Без тестов вообще никак

```javascript
it('should format time', function() {
    expect(formatTime(false)).toBe('0');
    expect(formatTime(null)).toBe('0');
    expect(formatTime(0)).toBe('0');
    expect(formatTime(345)).toBe('345ms');
    expect(formatTime(1000)).toBe('1s');
    expect(formatTime(1100)).toBe('1s 100ms');
    expect(formatTime(60000)).toBe('1m 0s');
    expect(formatTime(140000)).toBe('2m 20s');
    expect(formatTime(4201000)).toBe('1h 10m');
    expect(formatTime(3601000)).toBe('1h 0m');
    expect(formatTime(25*3600*1000+62000)).toBe('25h 1m');
});
```

{% include fragment.html %}
Больше мне не нужно ждать 25 часов, чтобы воспроизвести баг!
<img style="" src="img/crying-face.jpg">
