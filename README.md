# SnapLoop — Rede Social

Projeto básico de rede social estilo Instagram com HTML, CSS, JS e PHP.

## 📁 Estrutura de Arquivos

```
social/
├── index.html          → Feed principal
├── login.html          → Login
├── register.html       → Cadastro
├── upload.html         → Nova publicação
├── profile.html        → Perfil do usuário
├── explore.html        → Explorar / busca
│
├── css/
│   └── style.css       → Estilos globais
│
├── js/
│   ├── app.js          → Feed + modal de posts
│   ├── auth.js         → Login e cadastro
│   ├── upload.js       → Upload de imagem
│   ├── profile.js      → Página de perfil
│   └── explore.js      → Explorar + busca
│
├── php/
│   ├── config.php      → Conexão PDO + helpers
│   ├── install.php     → Cria as tabelas no banco
│   ├── register.php    → Cadastro de usuário
│   ├── login.php       → Login
│   ├── logout.php      → Logout
│   ├── upload_post.php → Upload de post
│   ├── get_posts.php   → Listar posts (feed/explore)
│   ├── like_post.php   → Curtir / descurtir
│   ├── get_comments.php→ Buscar comentários
│   ├── add_comment.php → Adicionar comentário
│   ├── get_profile.php → Dados do perfil
│   ├── update_profile.php → Atualizar bio
│   └── search_users.php→ Buscar usuários
│
└── uploads/            → Imagens enviadas (criado automaticamente)
```

## ⚙️ Instalação

### Requisitos
- PHP 7.4+ com extensões: PDO, PDO_MySQL, fileinfo
- MySQL / MariaDB
- Servidor local: XAMPP, WAMP, Laragon ou similar

### Passos

1. **Copie a pasta** `social/` para dentro do `htdocs/` (XAMPP) ou `www/` (WAMP).

2. **Crie o banco de dados** no phpMyAdmin (ou via terminal):
   ```sql
   CREATE DATABASE snaploop CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
   ```

3. **Configure a conexão** em `php/config.php`:
   ```php
   define('DB_HOST', 'localhost');
   define('DB_NAME', 'snaploop');
   define('DB_USER', 'root');     // seu usuário MySQL
   define('DB_PASS', '');         // sua senha MySQL
   ```

4. **Crie as tabelas** acessando no navegador:
   ```
   http://localhost/social/php/install.php
   ```

5. **Acesse o site:**
   ```
   http://localhost/social/login.html
   ```

## ✨ Funcionalidades

- ✅ Cadastro e Login com sessão PHP
- ✅ Feed de posts com fotos
- ✅ Stories decorativos
- ✅ Upload de imagens com preview
- ✅ Curtidas (persistidas no banco)
- ✅ Comentários nos posts
- ✅ Perfil com grid de fotos e bio editável
- ✅ Explorar posts e buscar usuários
- ✅ Modal de visualização de post
- ✅ Modo demo (funciona sem PHP/banco para visualização)

## 🔮 Próximas melhorias sugeridas

- Sistema de seguidores funcional
- Notificações
- Stories reais com upload
- Avatar personalizado
- Mensagens diretas
- Hashtags
