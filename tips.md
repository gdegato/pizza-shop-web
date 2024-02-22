wrapper.find: assíncrono
wrapper.get: se não encontrar, dá erro
wrapper.query: se nao encontrar, retorna nulo

const statusText = wrapper.getByText('Pendente')
const badgeElement = wrapper.getByTestId('badge')
wrapper.debug()//mostra o código HTML no console
console.log(statusText.outerHTML) //mostra apenas a linha 

quando não puder identificar o conteúdo de uma tag(veja exemplo abaixo que não retorna nada, deve colocar um data-testid para localizar.

  <span
   data-testid="badge"
    className="h-2 w-2 rounded-full bg-rose-500"
    />

    getByRole: procura pela tag, ex: 
     const nextPageButton = wrapper.getByRole('button', {
      name: 'Próxima página',
    })

    Instalação de bibliotecas:  npm i -D @testing-library/user-event
    para realizar eventos de clicks e demais interações dos usuários