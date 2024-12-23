<script>
    export let style='primary'
    export let type='button'
    export let disabled=false;
</script>

<button {type} {disabled} class="{style}">
    <slot></slot>
</button>
<style>
    button{
        color: aqua;
        border:0;
        border-radius: 8px;
        width:100px;
        height:40px;
        cursor:pointer;
    }
    .primary{
        background-color: #202142;
    }
    .secondary{
        background:#ff6a95;
    }
    button:hover{
        transform:scale(0.98);
        opacity:0.9;
        }
    button:disabled{
        background-color: #cccccc;
        cursor:auto;
        color:#333;
    }
    button:disabled:hover{
       transform: scale(1);
       opacity:1;
    }
</style>