<template>
    <div class="todo-header">
        <input type="text"
               placeholder="请输入你的任务名称，按回车键确认"
               v-model="name"
               @keyup.enter="save"/>
    </div>
</template>

<script>
export default {
    name: "TaskHeader",
    props: {
        // saveTask: {type:Function, required: true}
    },
    data() {
        return {
            name: ''
        }
    }, methods: {
        save() {
            if(this.name.length == 0) {
                console.log("不能为空");
                return;
            }
            // this.saveTask(this.name);
            // 触发自定义事件
            this.$emit('saveTask', this.name)
            this.name = '';
        }
    }
}
</script>

<style>
/*header*/
.todo-header input {
    width: 560px;
    height: 28px;
    font-size: 14px;
    border: 1px solid #ccc;
    border-radius: 4px;
    padding: 4px 7px;
}

.todo-header input:focus {
    outline: none;
    border-color: rgba(82, 168, 236, 0.8);
    box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 8px rgba(82, 168, 236, 0.6);
}
</style>
