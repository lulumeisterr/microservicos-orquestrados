# Sobre.
 Aplicar convenções/padrões de microservicos utilizando tecnicas para buscar resiliencia, eficiencia e robustez.

# Patterns e conceitos a serem utilizados.
  - Gateway: sera utilizado como proxy reverso como porta de entrada para se connectar com os microservicos responsavel por centralizar as requisições.
  - Service Discovery: Será responsavel por resolver problemas de mapeamento de endereços de rede para
    reconhecer novas instancias de maquinas por meio de ip e porta pois se estamos sendo gerenciado por um provedor cloud as maquinas contem ips dinamicos.
    Caso uma maquina pare de funcionar o service discovery por meio de health-check é responsavel por desregistrar a maquina para que você sempre tenha dados     consistentes.
   
  - Service Register : Sera armazenados todas as maquinas por meio de ip e porta.
  - Load Balance : O balanceamento de carga visa otimizar o uso de recursos, maximizar o throughput, minimizar o tempo de resposta e evitar a sobrecarga de qualquer recurso único

# Tecnologias.
  - .NETCORE 6
    - ORM : EFCore
  - Ocelot 
     - API GATEWAY (https://docs.microsoft.com/pt-br/dotnet/architecture/microservices/multi-container-microservice-net-applications/implement-api-gateways-with-ocelot)
     - Service Discovery (https://ocelot.readthedocs.io/en/latest/features/servicediscovery.html)
  - Load Balance.
    - Nginx
  - Docker
  
# Ideia de arquitetura.
 
 ![image](https://user-images.githubusercontent.com/25963928/192132000-22a296f2-8102-4e8b-acb1-a9d2ba26b574.png)

 # Rodando a imagem da aplicação local
   Entre na raiz do projeto e execute os comandos abaixo.
    - docker-compose up --build
