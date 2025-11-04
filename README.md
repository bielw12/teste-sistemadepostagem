🗞️ Portal de Notícias - Django

Portal de notícias completo desenvolvido com Django + Python, incluindo:
Sistema de autenticação
Publicação de artigos
Comentários moderados
Curtidas dinâmicas
Geolocalização com mapas
API REST integrada

🚀 Como Começar
✅ 1. Criar um Superusuário (Administrador)
Para acessar o painel administrativo, crie um superusuário:

python manage.py createsuperuser

Siga as instruções do terminal:
Nome de usuário
Email (opcional)
Senha segura

✅ 2. Acessar o Painel Admin

Acesse:
/admin/
Permissões disponíveis:
Gerenciar usuários e perfis
Moderar comentários
Marcar artigos como destaque
Adicionar novas tags
Ver estatísticas de curtidas

✅ 3. Criar Sua Primeira Conta de Usuário

Acesse:
/register/
Perfis disponíveis:
Leitor → ler, comentar e curtir artigos
Jornalista → criar/editar artigos

⚠️ Perfis de Administrador só podem ser atribuídos no painel admin por segurança.

✅ 4. Criar Seu Primeiro Artigo
Faça login como Jornalista ou Admin
Clique em "Criar Artigo"
Preencha:
Título
Resumo
Conteúdo
Imagem (opcional)
Tags

Localização (opcional)

✅ Marque Publicar artigo

👥 Tipos de Perfil
Perfil	Permissões
Leitor	Visualiza, comenta, curte, exclui comentários próprios
Jornalista	Tudo do leitor + CRUD dos próprios artigos + upload de imagens
Administrador	Todas as permissões + destaque, moderação, gestão de usuários
🔧 Funcionalidades Principais
📰 Artigos

CRUD completo

Editor de texto rico (Summernote)
Upload de imagens
Tags dinâmicas
Geolocalização com mapas (Folium)
Contador de views
Destaques para Home

💬 Comentários

Moderação manual
Exclusão de comentários próprios

❤️ Curtidas
Curtir/Descurtir sem reload (AJAX)
Contador atualizado em tempo real

🗺️ Mapas
Marcadores interativos
Visualização da localização

🔌 API REST
Base: /api/

Artigos
Método	Endpoint	Descrição
GET	/api/articles/	Lista todos os artigos
GET	/api/articles/{slug}/	Detalhe
POST	/api/articles/	Criar (jornalista+)
PUT	/api/articles/{slug}/	Atualizar (autor/admin)
DELETE	/api/articles/{slug}/	Deletar (autor/admin)
Comentários
Método	Endpoint	Descrição
GET	/api/comments/	Comentários aprovados
POST	/api/comments/	Criar comentário (autenticado)
Filtros
?search=termo
?ordering=-created_at
?page=2

📁 Estrutura do Projeto
portal_noticias/
├── articles/        # App de artigos e curtidas
├── comments/        # App de comentários
├── users/           # App de autenticação e perfis
├── api/             # API REST (DRF)
├── templates/       # HTML
│   ├── base/
│   ├── articles/
│   └── users/
├── static/          # CSS/JS
├── media/           # Uploads
├── manage.py
└── requirements.txt

🛠️ Comandos Úteis
# Criar migrações após mudanças nos models
python manage.py makemigrations

# Aplicar migrações
python manage.py migrate

# Criar superusuário
python manage.py createsuperuser

# Executar servidor
python manage.py runserver

# Shell interativa do Django
python manage.py shell

# Coletar arquivos estáticos
python manage.py collectstatic

🔒 Segurança

✅ Proteção CSRF
✅ Roles e permissões bem definidas
✅ Moderação obrigatória para comentários
✅ Upload validado
✅ API protegida por permissões
✅ Evita auto-promoção para admin

📚 Tecnologias Utilizadas
Django 4.2.7
Django REST Framework
django-taggit
django-summernote
Pillow
Folium
psycopg2-binary
TailwindCSS

🎯 Próximos Passos

Personalizar layout
Novas funcionalidades
Notificações por email
Testes automatizados
Deploy em produção
Cache e otimizações

❓ Suporte

Caso encontre problemas:
Verifique os logs do Django
Confira o painel admin
Consulte a documentação em replit.md

🛠️ Desenvolvido com Django + Python 🐍
🔥 Projeto: teste-sistemadepostagem / teste-sistemadepostagem-V1.1
