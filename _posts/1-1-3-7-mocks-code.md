## Заглушки (mocks)

```javascript
//объявление
var ModuleMock = jasmine.createSpy('Module').andReturn({
    init: jasmine.createSpy('module.init'),
    foo: jasmine.createSpy('module.foo'),
    bar: jasmine.createSpy('module.bar')
});
//пример использования
var module = new ModuleMock(),
    app = new App(module);
```