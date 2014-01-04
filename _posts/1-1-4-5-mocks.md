## Советы

**2. Правильно пишите заглушки (mocks)**

Заглушки должны быть простыми и без внутренней логики. В Jasmine для их создания удобно использовать шпионов:

```javascript
var ModuleMock = jasmine.createSpy('Module').andReturn({
        init: jasmine.createSpy('module.init'),
        foo: jasmine.createSpy('module.foo'),
        bar: jasmine.createSpy('module.bar')
    });
```

используем:

```javascript
function App(module){
   module.init();
}
var module = new ModuleMock(),
    app = new App(module);
expect(module.init).toHaveBeenCalled();
expect(module.foo).not.toHaveBeenCalled();
```