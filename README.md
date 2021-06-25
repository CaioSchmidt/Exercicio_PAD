// Questão 1 - Crie uma função que retorna a string “Olá, ” concatenada com um argumento text (a ser passado para a função) e com ponto de exclamação “!” no final.

var text = 'Caio'
function nome(text)
{
  console.log("Olá " + text + "!")
}
nome(text)

// Questão 2 - Crie uma função que dado dois valores e uma Callback (passados como parâmetros), mostre no console a soma, subtração, multiplicação ou divisão desses valores, dependendo da função Callabck.

function operacoes(val1,val2,callback)
{
  console.log(callback(val1,val2))
}
operacoes(4,5,function(var1,var2)
{
  return var1 + var2;
})
operacoes(4,5, function(var1,var2)
{
  return var1 - var2
})
operacoes(4,5, function(var1,var2)
{
  return var1 / var2
})
operacoes(4,5, function(var1,var2)
{
  return var1 * var2
})

// Questão 3 - Crie uma função que recebe um valor e uma callback como parâmetro, que retorna uma outra função que recebe um parâmetro e chama essa callback que verifica se um número inteiro passado na primeira função como parâmetro é divisível por um outro numero passado pela função interna e retorne true ou false.

function um(x,callback){
  return function dois(y){
    callback(x,y)
  }
}

var var1 = um(80,function(val1,val2){
  if(val1%val2 == 0){
    console.log('true')
  }else
  {
    console.log('false')
  }
})
var1(7)

// Questão 4 - Crie uma função que recebe um número (de 1 a 12) e retorne o mês correspondente como uma string. Por exemplo, se a entrada for 2, a função deverá retornar “fevereiro”, pois este é o 2° mês.

function numMeses(num) {
  if (num == 1) {
    console.log("janeiro")
  }
  if (num == 2) {
    console.log("Fevereiro")
  }
  if (num == 3) {
    console.log("Março")
  }
  if (num == 4) {
    console.log("Abril")
  }
  if (num == 5) {
    console.log("Maio")
  }
  if (num == 6) {
    console.log("Junho")
  }
  if (num == 7) {
    console.log("Julho")
  }
  if (num == 8) {
    console.log("Agosto")
  }
  if (num == 9) {
    console.log("Setembro")
  }
  if (num == 10) {
    console.log("Outubro")
  }
  if (num == 11) {
    console.log("Novembro")
  }
  if (num == 12) {
    console.log("Dezembro")
  }
}
numMeses(11)

// Questão 5 - Crie uma função que receba dois números e retorne se o primeiro é maior ou igual ao segundo dependendo da função Callback.

function numeros(num1,num2, callback)
{ 
  return callback(num1,num2)
}

numeros(7,7, function(x,y){
  if (x > y) {
    console.log("o primeiro número é maior")
  }
  if (x < y) {
    console.log("o primeiro número é menor")
  }
  else{
    console.log("os números são iguais")
  }
})
