<script>
let selected=10
</script>
<ul class="rating">
    <li>
        <input type="radio" id="num1" name="rating" value="1" on:change={onchange} checked={selected===1}/>
        <label for="num1">1</label>
    </li>
    <li>
        <input type="radio" id="num2" name="rating" value="2" on:change={onchange} checked={selected===2}/>
        <label for="num1">2</label>
    </li>
    <li>
        <input type="radio" id="num3" name="rating" value="3" on:change={onchange} checked={selected===3}/>
        <label for="num1">3</label>
    </li>
    <li>
        <input type="radio" id="num4" name="rating" value="4" on:change={onchange} checked={selected===4}/>
        <label for="num1">4</label>
    </li>
    <li>
        <input type="radio" id="num4" name="rating" value="4" on:change={onchange} checked={selected===5}/>
        <label for="num1">5</label>
    </li>
    <li>
        <input type="radio" id="num4" name="rating" value="4" on:change={onchange} checked={selected===6}/>
        <label for="num1">6</label>
    </li>
    <li>
        <input type="radio" id="num4" name="rating" value="4" on:change={onchange} checked={selected===7}/>
        <label for="num1">7</label>
    </li>
    <li>
        <input type="radio" id="num4" name="rating" value="4" on:change={onchange} checked={selected===8}/>
        <label for="num1">8</label>
    </li>
    <li>
        <input type="radio" id="num4" name="rating" value="4" on:change={onchange} checked={selected===9}/>
        <label for="num1">9</label>
    </li>
    <li>
        <input type="radio" id="num4" name="rating" value="4" on:change={onchange} checked={selected===10}/>
        <label for="num1">10</label>
    </li>
</ul>