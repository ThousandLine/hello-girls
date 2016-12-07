# hello-girls
just another repository
function fn(arr){
    if(arr.length==2){
        return [arr[0]+arr[1],arr[1]+arr[0]]
    }else{
        var temp=[];
        for(var i=0;i<arr.length;i++){
            var num=arr.splice(i,1);
            var balanceList=fn(arr);

            for(var k=0; k < balanceList.length; k++){
                temp.push(num+balanceList[k]);
            }
            arr.splice(i,0,num);
        }
        return temp;
    }
}
var arr=["a","b","c","d"]
document.write(fn(arr))
