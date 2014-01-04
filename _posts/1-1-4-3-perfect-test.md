## Идеальный тест

```
it('should be alright', function(){
    var module = new Module(config);
    module.doSomething();
    expect(module.property).toBe(correct);
});
```