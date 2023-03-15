<template>
  <div class="cpf-container">
    <button @click="gerarCPF()">Gerar CPF</button>
    <div class="cpf-cartao">
        <p> {{ cpf }} </p>
    </div>
  </div>
</template>

<script>

export default {
    components: {

    },
    data () {
        return {
            cpf: ''
        }
    },
    methods: {
        gerarCPF () {
            function geradorCPF () {

                function aleatorio () {
                    var cpf = Math.round(Math.random () * 9)
                    return cpf
                }

                var cpfNum = []

                for (let i = 0; i <= 10; i++) {
                    cpfNum.push(aleatorio())
                    if (cpfNum.length == 3 || cpfNum.length == 7) {
                        cpfNum.push('.')
                    } else if (cpfNum.length == 11) {
                        cpfNum.push('-')
                    }
                }

                return cpfNum.join('')
            }

            this.cpf = geradorCPF()
        }
    }
}

</script>

<style>

.cpf-container {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.cpf-container button {
    height: 30px;
    width: 100px;
    background-color: rgb(48,82,209);
    color: #fff;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-weight: bold;
    border-style: none;
    margin: 10px;
    border-radius: 5px;
}

.cpf-container button:hover {
    cursor: pointer;
    box-shadow: 0 0 5px rgb(25, 46, 124);
}

.cpf-cartao {
    height: 200px;
    width: 340px;
    background-image: url(../assets/cpf.png);
    background-size: cover;
    border-radius: 10px;
}

p {
    position: relative;
    width: 150px;
    top: 100px;
    left: 10px;
    color: #fff;
    background-color: rgb(48,82,209);
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-weight: bold;
    font-size: 18px;
}

</style>