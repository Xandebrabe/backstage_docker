# backstage_docker

## Atividade Ponderada - S2M10

### Passo a passo

- Instalação do backstage:
´npx @backstage/create-app@latest --skip-install´

Com aplicação criada, execute no root da aplicação: 

´yarn install´

Quando as depedências forem instaladas, execute no root da aplicação os comandos:

´yarn install --frozen-lockfile´

´yarn tsc´

´yarn build:backend´

Altere:

´ENV NODE_ENV production´

por 

´ENV NODE_ENV development´

no dockerfile do package backend, e por fim execute no root da aplicação os comandos:

´docker image build . -f packages/backend/Dockerfile --tag backstage --no-cache´  

´docker run -it -p 7007:7007 backstage´

### Evidências da aplicação

Aplicação rodando:

![Print1](/assets/app_running1)

![Print2](/assets/app_running2)

![Print1](/assets/app_running3)

Docker Desktop Image:

![Print1](/assets/docker_running)
