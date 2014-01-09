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
Но некоторые действия можно вынести за скобки, если они повторяются в разных тестах:

<pre><code class="javascript">beforeEach(function() {
   module = new Module(config);
});
it('should be alright', function(){
    module.doSomething();
});
afterEach(function() {
    expect(module.property).toBe(correct);
});
</code></pre>
</div>