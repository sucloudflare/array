<h1>Métodos de Arrays no JavaScript</h1>
    <p>Este README descreve os principais métodos de manipulação de arrays no JavaScript. Cada método tem uma função específica e ajuda a transformar, filtrar e analisar os dados. Aqui você encontrará explicações detalhadas de cada método, exemplos de código e dicas práticas para uso.</p>

  <h2>Resumo para Decorar: Métodos de Arrays no JavaScript</h2>

   <h3>1. <code>map()</code></h3>
    <p><strong>Descrição:</strong> Cria um novo array transformando cada item com base em uma função fornecida.</p>
    <p><strong>Sintaxe:</strong></p>
    <pre><code>const novoArray = array.map(callback);</code></pre>
    <div class="code-block">
        <strong>Exemplo:</strong>
        <pre><code>const numeros = [1, 2, 3];
const dobrados = numeros.map(num => num * 2); // [2, 4, 6]</code></pre>
    </div>
    <p><strong>Uso comum:</strong> Modificar todos os itens de um array, como multiplicar, alterar strings ou objetos.</p>

  <h3>2. <code>forEach()</code></h3>
    <p><strong>Descrição:</strong> Executa uma função para cada item do array. Não retorna um novo array.</p>
    <p><strong>Sintaxe:</strong></p>
    <pre><code>array.forEach(callback);</code></pre>
    <div class="code-block">
        <strong>Exemplo:</strong>
        <pre><code>const frutas = ['maçã', 'banana', 'uva'];
frutas.forEach(fruta => console.log(fruta));
// Saída: maçã, banana, uva</code></pre>
    </div>
    <p><strong>Uso comum:</strong> Realizar operações como exibir valores ou alterar variáveis externas.</p>

  <h3>3. <code>filter()</code></h3>
    <p><strong>Descrição:</strong> Cria um novo array com os itens que passam em um teste fornecido como função.</p>
    <p><strong>Sintaxe:</strong></p>
    <pre><code>const novoArray = array.filter(callback);</code></pre>
    <div class="code-block">
        <strong>Exemplo:</strong>
        <pre><code>const numeros = [10, 15, 20, 25];
const maioresQue15 = numeros.filter(num => num > 15); // [20, 25]</code></pre>
    </div>
    <p><strong>Uso comum:</strong> Filtrar itens que atendem a uma condição específica.</p>

   <h3>4. <code>reduce()</code></h3>
    <p><strong>Descrição:</strong> Reduz o array a um único valor, combinando seus elementos com base em uma função acumuladora.</p>
    <p><strong>Sintaxe:</strong></p>
    <pre><code>const resultado = array.reduce(callback, valorInicial);</code></pre>
    <div class="code-block">
        <strong>Exemplo:</strong>
        <pre><code>const numeros = [1, 2, 3, 4];
const soma = numeros.reduce((acumulador, atual) => acumulador + atual, 0); // 10</code></pre>
    </div>
    <p><strong>Uso comum:</strong> Somar valores ou combinar itens de um array.</p>

  <h3>5. <code>find()</code></h3>
    <p><strong>Descrição:</strong> Retorna o primeiro item do array que passa no teste fornecido.</p>
    <p><strong>Sintaxe:</strong></p>
    <pre><code>const item = array.find(callback);</code></pre>
    <div class="code-block">
        <strong>Exemplo:</strong>
        <pre><code>const usuarios = [{nome: 'Ana'}, {nome: 'Bruno'}, {nome: 'Carla'}];
const usuario = usuarios.find(user => user.nome === 'Bruno'); // {nome: 'Bruno'}</code></pre>
    </div>
    <p><strong>Uso comum:</strong> Encontrar o primeiro item que atende a um critério específico.</p>

   <h3>6. <code>findIndex()</code></h3>
    <p><strong>Descrição:</strong> Retorna o índice do primeiro item que passa em um teste.</p>
    <p><strong>Sintaxe:</strong></p>
    <pre><code>const indice = array.findIndex(callback);</code></pre>
    <div class="code-block">
        <strong>Exemplo:</strong>
        <pre><code>const usuarios = [{nome: 'Ana'}, {nome: 'Bruno'}, {nome: 'Carla'}];
const indice = usuarios.findIndex(user => user.nome === 'Bruno'); // 1</code></pre>
    </div>
    <p><strong>Uso comum:</strong> Obter o índice do item que atende a uma condição.</p>

  <h3>7. <code>some()</code></h3>
    <p><strong>Descrição:</strong> Verifica se ao menos um item do array passa no teste fornecido.</p>
    <p><strong>Sintaxe:</strong></p>
    <pre><code>const resultado = array.some(callback);</code></pre>
    <div class="code-block">
        <strong>Exemplo:</strong>
        <pre><code>const numeros = [10, 20, 30, 40];
const existeMaiorQue25 = numeros.some(num => num > 25); // true</code></pre>
    </div>
    <p><strong>Uso comum:</strong> Verificar rapidamente se um array contém um item que atenda a uma condição.</p>

  <h3>8. <code>every()</code></h3>
    <p><strong>Descrição:</strong> Verifica se todos os itens do array passam no teste fornecido.</p>
    <p><strong>Sintaxe:</strong></p>
    <pre><code>const resultado = array.every(callback);</code></pre>
    <div class="code-block">
        <strong>Exemplo:</strong>
        <pre><code>const numeros = [10, 20, 30];
const todosMaioresQue15 = numeros.every(num => num > 15); // false</code></pre>
    </div>
    <p><strong>Uso comum:</strong> Garantir que todos os itens do array atendam a uma condição.</p>

  <h3>9. <code>concat()</code></h3>
    <p><strong>Descrição:</strong> Junta dois ou mais arrays em um único array.</p>
    <p><strong>Sintaxe:</strong></p>
    <pre><code>const novoArray = array1.concat(array2);</code></pre>
    <div class="code-block">
        <strong>Exemplo:</strong>
        <pre><code>const frutas = ['maçã', 'banana'];
const vegetais = ['cenoura', 'brócolis'];
const alimentos = frutas.concat(vegetais); // ['maçã', 'banana', 'cenoura', 'brócolis']</code></pre>
    </div>
    <p><strong>Uso comum:</strong> Combinar dados de diferentes arrays.</p>

  <h3>10. <code>includes()</code></h3>
    <p><strong>Descrição:</strong> Verifica se o array contém um determinado valor.</p>
    <p><strong>Sintaxe:</strong></p>
    <pre><code>const resultado = array.includes(valor);</code></pre>
    <div class="code-block">
        <strong>Exemplo:</strong>
        <pre><code>const frutas = ['maçã', 'banana', 'uva'];
const temBanana = frutas.includes('banana'); // true</code></pre>
    </div>
    <p><strong>Uso comum:</strong> Verificar se um array contém um valor específico.</p>

   <h3>11. <code>slice()</code></h3>
    <p><strong>Descrição:</strong> Retorna uma cópia de uma parte do array sem modificá-lo.</p>
    <p><strong>Sintaxe:</strong></p>
    <pre><code>const novoArray = array.slice(inicio, fim);</code></pre>
    <div class="code-block">
        <strong>Exemplo:</strong>
        <pre><code>const numeros = [1, 2, 3, 4, 5];
const subArray = numeros.slice(1, 3); // [2, 3]</code></pre>
    </div>
    <p><strong>Uso comum:</strong> Obter uma porção de um array existente.</p>
