# nodejs--async-
nodejs 同步执行控制实例




# // async function timeout() {
# //     return '1.hello world'
# // }
# //
# // // async 返回一个promise对象 ，then获取
# // timeout().then(result => {
# //     console.log(result);
# // })
# // console.log('1.虽然在后面，但是我先执行');

# // function doubleAfter2seconds(num) {
# //     return new Promise((resolve, reject) => {
# //         setTimeout(() => {
# //             resolve( num)
# //         }, 2000);
# //     } )
# // }
# // async function testResult() {
# //     let result = await doubleAfter2seconds('2秒之后输出我');
# //     let result2 = await doubleAfter2seconds('3');
# //     let result3 = await doubleAfter2seconds('2');
# //     let result4 = await doubleAfter2seconds('1');
# //     let result5 = await doubleAfter2seconds('爱就像蓝天白云，晴空万里，忽然暴风雨');
# //     console.log(result);
# //     console.log(result2);
# //     console.log(result3);
# //     console.log(result4);
# //     console.log(result5);
# //
# //     console.log('完毕')
# // }
# // testResult()
# //


#let p = new Promise((resolve, reject) => {
 #   setTimeout(resolve, 1000, '111');
#});
#p.then(
 #   res => {
  #      console.log(res);
    #    return new Promise((resolve, reject) => {
   #         setTimeout(resolve, 1000, '2222222');
    #    });
  #  }
#).then(
#        res =>
 #       {console.log(res)
 #          return new Promise((resolve, reject) => {
  #              setTimeout(resolve, 1000, '333');
 #           });}
 #   ).then(
  #      res=>{
#            console.log(res)
# return new Promise((resolve, reject) => {
 #   setTimeout(resolve, 1000, '444');
 # })}
# ).then(
 #   res=>{
  #      console.log(res)
  #  }
# );
