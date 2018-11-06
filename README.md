# js-splice-sort-slice-join-split-
splice , sort, slice, join, split 


   1）splice(从第几位开始，截取多少长多度，在截取切口处添加新的数据)

           var arr=[1,2,3,5]
    
            arr.splice(3,0)  //1 2 3 4 5
 
            arr.splice(1,2)   //1 4 5


   2） sort // 排序

        1.必须写两个形参
        2.看返回值
            1）当返回值为负数时，那么前面的数放在前面
            2）为整数时，那么后面的数在前面
            3）为0时，不动

                  var arr=[10,29,0,2,9]       
                    arr.sort(function(a,b){
                	   if(a>b){
                       return 1
                     }else{
                       return -1
                     }
                  })
                 console.log(arr)   //[0, 2, 9, 10, 29] 

             
               var arr=[1,2,3,4,5]       
                  arr.sort(function(){
                   return   Math.random()-0.5
                  })
                console.log(arr)   //[0, 2, 9, 10, 29]    

              var test={
                name:"张安",
                age:90
                }
              var test1={
                name:"lisi",
                age:80
              }
              var test2={
                name:"张三",
                age:8
              }
              var arr=[test,test1,test2];
               arr.sort(function(a,b){
                  if(a.age>b.age){
                    return 1
                  }else{
                    return-1
                  }
               })
               //[ {name: "张三", age: 8} {name: "lisi", age: 80}{name: "张安", age: 90}]
              console.log(arr)  


    3）slice(从该位开始截取，截取到该位(截取数不包括该位) )

             var arr=[1,2,3,4,5]
  
             var num=arr.slice(1,3)   //[2, 3]											

																
    4）join()与split() 这两个方法是互逆的
		
           join()  //把数组转化成字符串(以什么隔空)
             var arr=[1,2,3,4,5,6];
             arr.join("-")   //"1-2-3-4-5-6"

            split  //它是字符串的方法  他可以把字符串转换成 数组 (以什么符号拆分成数组)

             var str="12 3 45 67"; 
              str.split(" ") //["12", "3", "45", "67"]
             var str="12-3-45-67";
             str.split("-")  //["12", "3", "45", "67"]

  






 
