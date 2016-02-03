#### ppwebdevnomongo_note

- cp5
Four level rest api  
Level1: The swamp of POX  
Level2: Resources  
Level3: HTTP verbs  
Level4: Hypermedia Controls  

Only reach last level is rest api. Others are restful api.  


- cp6

mocha test, fail if one test fail.
```
mocha x.js --bail
```

Three styles of chai
```
const assert = require('chai').assert;
const expect = require('chai').expect;
const should = require('chai').should();
```
use:
```
assert.isArray(foo, "message");
expect(foo).to.be.an('array','message');
foo.should.be.an('array','message');
```
helper methods:
```
assert.strictEqual(foo,'bar');
assert.lengthOf(foo,3);

expect(foo).to.equal('bar');
expect(foo).to.have.length(3);

foo.should.be.equal('bar');
foo.should.have.length(3);
```
also refer to see other methods.  



sinon spy  

```
const obj = {
method:function(arg){return arg;}
}

const spy = sinon.spy(obj,'method');
obj.method(1);
obj.method(2);
```
Tests:
```
spy.callCount.should.equal(2);
spy.withArgs(1).calledOnce.should.be.true;
spy.neverCalledWith(3).should.be.true;
```
Advanced test:
```
const secondCall = spy.getCall(1);
const secondCallFirstArgument=spy.secondCall.args[0];
secondCall.returned(2).should.be.true;
```




