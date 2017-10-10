var message = prompt();

function cipher(message,des){
    //Comprobamos que el texto es válido
    var val=/^[A-z\s]*$/
    if(message===""||(!val.test(message))) {alert('El texto no es valido o esta vacio, intente otra vez:');
     }
    //abecedario
    var abe='ABCDEFGHIJKLMNOPQRSTUVWXYZ';
      var des=des%(abe.length) ,r1='';
        des=des<0?abe.length+des:des;
    for(var i=0;i<message.length;i++){
        //Desplazamos el abecedario
      l1 =String.fromCharCode((message.charCodeAt(i)-65+des)%abe.length + 65);
        r1 +=l1;

    }

    alert(r1);
}


cipher( message,33);
