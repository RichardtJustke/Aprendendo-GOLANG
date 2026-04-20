# Aprendendo Go

![Gopher no modo foco](gifs/0_NCKH5j7mncvMVBcR.gif)

## Sobre

Este repositório documenta minha evolução prática em Go, do zero até nível Big Tech.

Cada pasta, exercício e projeto aqui existe para construir base forte de computação, backend real e sistemas distribuídos.

## Objetivo

- Entrar em Big Tech com Go como stack principal.
- Dominar backend de produção: API, banco, concorrência, performance e escala.
- Construir portfólio com projetos reais e código de nível profissional.

## Stack principal

- Go
- PostgreSQL
- TypeScript
- Redis
- Kafka
- Kubernetes

## Roadmap Big Tech (2-3 anos)

- Fase 00 | Fundação CS | ABR-JUN (ano 1)
  - Foco: fundamentos de computador, redes, Linux e estruturas de dados.
  - LeetCode: Easy, 2-3x/semana.
  - Conceitos a dominar:
    - Sistema de arquivos (inode, permissões, hard/soft links)
    - Processos e threads (PID, context switch, sinais)
    - Memória (heap, stack, ponteiros, alocação)
    - Rede (TCP/IP, HTTP/1.1, DNS, sockets)
    - Estruturas de dados (array, linked list, stack, queue, hash map, árvore binária)
    - Algoritmos de ordenação (bubble, merge, quick sort)
    - Complexidade algorítmica (O(n), big O)
  - Atividades para validar:
    - Listar processos rodando em /proc e explicar cada campo
    - Implementar insertion sort e merge sort do zero
    - Fazer requisição HTTP GET manual via netcat (sem curl)
    - Criar arquivo binário e ler com seek
    - Implementar linked list com inserção e remoção
    - Medir tempo de execução de 3 algoritmos e comparar complexidade
  - Projetos: ambiente Linux, estruturas em Go, algoritmos com benchmark, clone de curl, leitor de processos, KV store em arquivo.
  - Marco: explicar o caminho completo de uma URL ate a resposta.

- Fase 01 | Go Raiz | JUL-AGO (ano 1)
  - Foco: Go idiomatico sem framework e sem ORM.
  - LeetCode: Easy/Medium.
  - Conceitos a dominar:
    - Tipos básicos, zero values e casting
    - Funções (receivers, defer, panic/recover)
    - Interfaces e duck typing
    - Goroutines e channels
    - Mutex e sync primitives (RWMutex, WaitGroup, Cond)
    - Generics (type parameters)
    - Reflection e struct tags
    - Context para cancelamento e timeout
  - Atividades para validar:
    - Implementar interface Reader/Writer do zero
    - Criar goroutines comunicando via channels
    - Resolver race condition com RWMutex
    - Escrever função genérica que funciona com []int e []string
    - Usar reflection para mapear struct em map
    - Fazer defer e panic/recover funcionarem juntos
    - Cancelar goroutine via context
  - Projetos: HTTP server puro, grep clone, locking com goroutines, LRU cache, mini ORM, worker pool.
  - Marco: escrever Go com fluidez e boas praticas.

- Fase 02 | Backend Real | SET-OUT (ano 1)
  - Foco: API de producao com Go + PostgreSQL + TypeScript.
  - LeetCode: Medium, 4x/semana.
  - Conceitos a dominar:
    - SQL (DDL/DML, joins, indexes, transactions, constraints)
    - Database drivers e conexão pooling
    - REST API design (status codes, headers, idempotência)
    - JWT e autenticação/autorização
    - Hashing (bcrypt) e criptografia
    - Middleware chain e dependency injection
    - JSON marshaling/unmarshaling
    - Testing (unit tests, mocks, test fixtures)
    - TypeScript básico (tipos, interfaces, async/await)
  - Atividades para validar:
    - Criar schema SQL completo com constraints
    - Executar query com prepared statements
    - Implementar middleware de logging
    - Fazer login com JWT e refresh token
    - Hash senha com bcrypt e validar
    - Escrever 3 testes de integração com banco real
    - Consumir a API Go com fetch em TypeScript tipado
    - Testar transação com rollback
  - Projetos: auth completa, migrations SQL, OpenAPI tipado, upload async, rate limiter, testes de integracao.
  - Marco: API em producao sendo consumida por cliente TypeScript.

- Fase 03 | Performance e Internals | NOV-JAN (ano 2)
  - Foco: medir, diagnosticar e otimizar com pprof.
  - LeetCode: Medium/Hard, 4-5x/semana.
  - Conceitos a dominar:
    - CPU profiling (flame graphs, hot paths)
    - Memory profiling (heap, GC pressure, leaks)
    - Tracing distribuído (trace tool)
    - Benchmarking Go (testing.B, comparação de alocações)
    - Garbage collector (mark-and-sweep, GC tuning)
    - Cache patterns (locality, hit ratio, TTL)
    - Backpressure e rate limiting
    - WebSocket protocol
    - B-tree estrutura e WAL (Write-Ahead Logging)
  - Atividades para validar:
    - Profile uma função lenta e otimizar
    - Comparar alocação de 3 implementações
    - Ver flame graph de aplicação real
    - Implementar cache com hit/miss rate
    - Resolver backpressure em goroutines
    - Escrever benchmark com B.ReportMetric
    - Demonstrar GC pause antes e depois de otimização
    - Implementar WebSocket echo server
  - Projetos: profiling real, connection pool, crawler com backpressure, chat websocket, benchmark comparativo, mini banco em disco.
  - Marco: resolver gargalo real com evidencia tecnica.

- Fase 04 | Distribuicao e Escala | FEV-MAI (ano 2)
  - Foco: microservicos, resiliência e processamento por eventos.
  - LeetCode: Hard + system design.
  - Conceitos a dominar:
    - gRPC e protocol buffers
    - Message queues (Kafka, pub/sub)
    - Idempotência e deduplicação
    - Dead letter queues (DLQ)
    - Distributed transactions (saga pattern)
    - Circuit breaker e retry policies
    - Service discovery e load balancing
    - Eventual consistency vs strong consistency
    - Event sourcing e CQRS
    - CAP theorem
  - Atividades para validar:
    - Definir .proto e gerar stubs
    - Produtor/consumidor Kafka com retry
    - Implementar idempotência com banco
    - Usar DLQ para falhas
    - Implementar circuit breaker com estado
    - Discutir CAP trade-offs em 3 cenários
    - Implementar saga distribuída
    - Event store com rebuild de estado
    - Fazer mock interview de system design
  - Projetos: gRPC, cache em camadas, Kafka + DLQ, distributed lock, circuit breaker, event sourcing.
  - Marco: projetar sistema para 1 milhao de usuarios com trade-offs claros.

- Fase 05 | Big Tech Stack | JUN-DEZ+ (ano 2+)
  - Foco: cloud-native completo e preparo de entrevista.
  - LeetCode: Hard + mock interviews.
  - Conceitos a dominar:
    - Kubernetes (deployments, services, ingress, statefulsets)
    - Helm charts e GitOps
    - OpenTelemetry (traces, metrics, logs)
    - Jaeger para observabilidade distribuída
    - Prometheus e Grafana
    - Service mesh (Istio basics)
    - Multi-region deployment
    - Security (TLS, RBAC, secrets management)
    - Infrastructure as Code (Terraform)
    - System design patterns (sharding, partitioning, consensus)
  - Atividades para validar:
    - Deploy app em K8s com 3+ replicas e service
    - Configurar ingress e HTTPS
    - Implementar OpenTelemetry traces
    - Correlacionar trace entre 3 serviços
    - Criar Grafana dashboard com métricas
    - Fazer helm chart funcional
    - Demonstrar auto-scaling horizontal
    - Fazer mock interview técnica de 1h
    - Documentar sistema para 1M usuários
    - Contribuir com PR real em projeto Go OSS
  - Projetos: deploy em Kubernetes, observabilidade distribuida, docs de system design, contribuicao open source, SaaS completo.
  - Marco: pronto para entrevista tecnica de Big Tech.

## Metas de carreira

- 12-18 meses: Junior/Pleno (produto real em Go)
- 24-30 meses: Senior (sistemas distribuidos e decisoes tecnicas)
- 36+ meses: Big Tech/Staff (escala real e impacto)

## Materiais de estudo

- Fundacao CS
  - Computer Science Distilled
  - How Linux Works
  - The Linux Command Line

- Go e Backend
  - Learning Go
  - 100 Go Mistakes
  - Let's Go / Let's Go Further
  - Learn Go with Tests

- Performance e Distribuicao
  - Hands-On High Performance with Go
  - Database Internals
  - Designing Data-Intensive Applications

- Escala e Cloud Native
  - Building Microservices with Go
  - Distributed Services with Go
  - Cloud Native Go

![Gopher em ação](gifs/go.gif)

