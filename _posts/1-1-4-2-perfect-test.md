## Идеальный тест

Должен быть коротким и ясным:

```
it('should be alright', function(){
    var module = new Module(config);
    module.doSomething();
    expect(module.property).toBe(correct);
});
```

<div class="fragment">
Общее выносим за скобки:

<pre><code class="javascript">beforeEach(function() {
   module = new Module(config);
   module.doSomething();
});
it('should be alright', function(){
    expect(module.property).toBe(correct);
});
it('should not have errors', function() {
    expect(module.errors.length).toBe(0);
});
</code></pre>
</div>