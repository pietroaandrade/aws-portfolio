# AWS Portfolio

Projetos práticos de cloud na AWS, construídos enquanto me preparo para a certificação **AWS Certified Cloud Practitioner (CLF-C02)** e para fundar o **AWS Student Builder Group da FIAP**.

Cada projeto parte de um design doc, é construído como infraestrutura como código (Terraform) e documenta as decisões de arquitetura e os custos.

## Projetos

| # | Projeto | Serviços | Status |
| --- | --- | --- | --- |
| 1 | Site estático com CDN e HTTPS | S3, CloudFront, Route 53, ACM | 🔜 Planejado |
| 2 | API serverless de inscrição em eventos | API Gateway, Lambda, DynamoDB | 🔜 Planejado |
| 3 | Projeto 2 como código + CI/CD | Terraform, GitHub Actions (OIDC), pytest | 🔜 Planejado |
| 4 | Aplicação containerizada | ECR, ECS Fargate, ALB, VPC | 🔜 Planejado |
| 5 | Chatbot com RAG | Amazon Bedrock, Lambda, S3 | 🔜 Planejado |

Status: 🔜 Planejado · 🚧 Em construção · ✅ Concluído

## Estrutura do repositório

```
.
├── 01-static-site/
├── 02-serverless-api/
├── 03-iac-cicd/
├── 04-containers/
├── 05-bedrock-rag/
└── docs/            # design docs e ADRs
```

Cada pasta de projeto terá o próprio README com diagrama, como fazer o deploy, como destruir os recursos e custo estimado.

## Ferramentas

- AWS CLI v2
- Terraform
- Git e GitHub Actions
- Python (Lambda e testes)

## Práticas de segurança e custo

- Nenhuma credencial, chave ou arquivo de estado é versionado (ver `.gitignore`).
- Deploys automatizados usam OIDC entre GitHub e AWS, sem chaves de acesso fixas.
- Permissões IAM seguem o princípio do menor privilégio.
- Orçamento com alertas configurado na conta; todos os recursos são destruídos (`terraform destroy`) após cada sessão de estudo.
- Os projetos usam apenas dados fictícios.

## Roadmap

- [ ] Certificação AWS Certified Cloud Practitioner (nov/2026)
- [ ] Projetos 1–3 concluídos e documentados (dez/2026)
- [ ] Candidatura a líder do AWS Student Builder Group FIAP (dez/2026)
- [ ] Projetos 4–5 (jan/2027)
- [ ] AWS Certified Solutions Architect – Associate (2027)

## Contato

- LinkedIn: [@pietroaandrade](https://www.linkedin.com/in/pietroaandrade/)
