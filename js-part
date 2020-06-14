var buttons = document.getElementsByClassName('button');
var display = document.getElementById('display_box');
var operand1 = null;
var operand2 = null;
var operator =null;

for (var i = 0; i <buttons.length; i++)
 {
	buttons[i].addEventListener('click', function() {
		// body...
		var value = this.getAttribute('data-value');
		if((display.textContent == '')&&(value== "+" || value== "*" || value== "/" || value== "%") )
		{
			display.textContent = "error";
		}
		else if(value == '+' )
		{
			operator ='+';
			operand1 = parseFloat(display.textContent);//see this is where u displaying  no? i am putting the no. in the operand 1 after the operator so that i can use tha
			display.textContent = "";

		}else if(value == 'clear')
		{
			display.textContent = "";
		}
		else if(value == 'del')
		{
			display.textContent = display.textContent.slice(0, -1);
		}
		else if(display.textContent.length > 12)
		{
			display.innerText = "Out of bound";
			// setTimeout(3000);
			// display.innerText ="";
		}
		else if(value == 'p-m' )
		{
			if(display.innerText.length == 0)
			{
				display.innerText == '';
			}
			else if(display.innerText[0] == '-'){
				display.innerText = display.innerText.slice(1,display.innerText.length);
			}
			else{
				display.innerText ="-"+display.innerText ;
			}

		}
		
		else if(value == '-')
		{	
			operator ='-';
			
			if(display.textContent.length == '0')
			{
				display.innerText = '-';
			}
			else
			{
			operand1 = parseFloat(display.textContent);////canwe keep things shrt dont type o long 
			display.textContent = "";
			}
			// so herewhere are u writing for disp of operstors
			//not displaying but storing in the operand1 the + or - u storing in operND1? you hhave to call me 
			// u said operator is not dispalying no where is code for display og operators
			//yes i havent displayed operator but eval is also not working my code is wrong i need to understand how to make it work
		}else if(value == '*')
		{
			operator ='*';
			operand1 = parseFloat(display.textContent);
			
			display.textContent = "";

		}
		else if(value == '/')
		{
		operator ='/';
		
		operand1 = parseFloat(display.textContent);
		display.textContent = "";
		}
		else if(value == '%')
		{
		operator ='/';
		operand1 = parseFloat(display.textContent)*100;
		display.textContent = '';
		
		}
		
		else if(value == '='){
			operand2 = parseFloat(display.textContent);
			// display.textContent = "";
			//use eval 
			var result =eval(operand1 + " " + operator+ " " + operand2);
			//show result on display
			// display.innerText = parseFloat(result.textContent);
			display.innerText = result;
			operator = null; 
			
		}
		else{
			display.innerText += value;
		}
	});
}
