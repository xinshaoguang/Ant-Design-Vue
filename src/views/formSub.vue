<template>
  <a-form-item label="Gender">
    <a-input
    @blur="abc"
      v-decorator="[
        'gender',
        { rules: [{ required: true, message: 'Please input your gender!' }] },
      ]"
    >
 
    </a-input>
  </a-form-item>
</template>

<script>
export default {
  data() {
    return {
    //   formLayout: 'horizontal',
    //   form: this.$form.createForm(this, { name: 'coordinated' }),
    };
  },
  methods: {
      abc(){
        console.log(1)
        this.$emit('handle','gender','xin')
      }
    // handleSubmit(e) {
    //   e.preventDefault();
    //   this.form.validateFields((err, values) => {
    //     if (!err) {
    //       console.log('Received values of form: ', values);
    //     }
    //   });
    // },
    // handleSelectChange(value) {
    //   console.log(value);
    //   this.form.setFieldsValue({
    //     note: `Hi, ${value === 'male' ? 'man' : 'lady'}!`,
    //   });
    // },
  },
};
</script>
