/**
 *  注册功能js
 *  2020.12.15
 *  萝卜
 */
$(function(){
  //调用验证插件
  $('#registerForm').validate({
    //验证规则
    rules:{
      username:{
        required:true,  //非空
        rangelength:[3, 6]  //长度验证
      },
      //验证密码
      password:{
        required:true,  //非空
        isPassword:true  //自定义的密码验证
      },
      //确认密码
      checkPassword:{
        required:true, //非空
        equalTo:"#password"  //验证密码一致性
      },
      tel:{
        required:true,  //非空
        isTel:true  //自定义的电话号码验证
      }
    },
    //提示信息
    messages:{
      //用户名提示信息
      username:{
        required:'用户名不能为空哦！',  //非空提示
        rangelength:'长度在3~6位哦'  //长度提示
      },
      password:{
        required:'密码不能为空哦',  //非空
        isPassword:'亲！输入5-10个，以字母开头,可带数字,“_”,“.”的字符串哟!'  //自定义验证密码提示
      },
      //确认密码验证信息
      checkPassword:{
        required:'请再次输入密码',  //非空
        equalTo:'两次密码不一致'  //验证密码一致性
      },
      //电话号码提示信息
      tel:{
        required:'电话号码不能为空',
        isTel:'电话号码格式不正确'
      }
    }
  })

  //密码自定义验证
  jQuery.validator.addMethod("isPassword",function(value,element) {
    var pwdReg = /^[a-zA-Z]{1}([a-zA-Z0-9]|[._]){4,9}$/;
    return this.optional(element) || (pwdReg.test(value));
});
  
  //手机号自定义验证
  jQuery.validator.addMethod("isTel",function(value, element){
    var telReg = /^[1]+[3,8,5,7]+\d{9}$/;
    return this.optional(element) || (telReg.test(value));
  });
})

  // $(function(){
  
  //   var ok1=false;
  //   var ok2=false;
  //   var ok3=false;
  //   var ok4=false;
  //   // 验证用户名
  //   $('input[name="username"]').focus(function(){
  //    $(this).next().text('用户名应该为3-20位之间').removeClass('state1').addClass('state2');
  //   }).blur(function(){
  //    if($(this).val().length >= 3 && $(this).val().length <=12 && $(this).val()!=''){
  //     $(this).next().text('输入成功').removeClass('state1').addClass('state4');
  //     ok1=true;
  //    }else{
  //     $(this).next().text('用户名应该为3-20位之间').removeClass('state1').addClass('state3');
  //    }
       
  //   });
  
  //   //验证密码
  //   $('input[name="password"]').focus(function(){
  //    $(this).next().text('密码应该为6-20位之间').removeClass('state1').addClass('state2');
  //   }).blur(function(){
  //    if($(this).val().length >= 6 && $(this).val().length <=20 && $(this).val()!=''){
  //     $(this).next().text('输入成功').removeClass('state1').addClass('state4');
  //     ok2=true;
  //    }else{
  //     $(this).next().text('密码应该为6-20位之间').removeClass('state1').addClass('state3');
  //    }
       
  //   });
  
  //   //验证确认密码
  //    $('input[name="repass"]').focus(function(){
  //    $(this).next().text('输入的确认密码要和上面的密码一致,规则也要相同').removeClass('state1').addClass('state2');
  //   }).blur(function(){
  //    if($(this).val().length >= 6 && $(this).val().length <=20 && $(this).val()!='' && $(this).val() == $('input[name="password"]').val()){
  //     $(this).next().text('输入成功').removeClass('state1').addClass('state4');
  //     ok3=true;
  //    }else{
  //     $(this).next().text('输入的确认密码要和上面的密码一致,规则也要相同').removeClass('state1').addClass('state3');
  //    }
       
  //   });
  
  //   //验证邮箱
  //   $('input[name="email"]').focus(function(){
  //    $(this).next().text('请输入正确的email格式').removeClass('state1').addClass('state2');
  //   }).blur(function(){
  //    if($(this).val().search(/\w+([-+.]\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*/)==-1){
  //     $(this).next().text('请输入正确的EMAIL格式').removeClass('state1').addClass('state3');
  //    }else{     
  //     $(this).next().text('输入成功').removeClass('state1').addClass('state4');
  //     ok4=true;
  //    }
       
  //   });
  
  //   //提交按钮,所有验证通过方可提交
  
  //   $('.submit').click(function(){
  //    if(ok1 && ok2 && ok3 && ok4){
  //     $('form').submit();
  //    }else{
  //     return false;
  //    }
  //   });
      
  //  });