````markdown
# Moodle Activity Module Template

Este repositório é um **modelo básico** para criar módulos de atividade (`mod`) no Moodle.

## 📁 Estrutura de Diretórios

- `backup/` – scripts de backup e restore
- `classes/` – suas classes PHP modernas com namespace
- `db/` – banco de dados, permissões, eventos
- `lang/` – strings de idioma
- `lib.php` – funções principais do módulo
- `mod_form.php` – formulário de criação/edição no curso
- `view.php` – o que o aluno vê
- `index.php` – lista todas as instâncias do módulo
- `version.php` – metadados do módulo

## 🛠️ Como criar um novo módulo

1. **Clone este repositório e renomeie:**

   ```bash
   git clone https://github.com/seuusuario/moodle-mod_template.git mod_seumodulo
````

2. **Renomeie os arquivos e strings:**

   * Substitua `template` por `seumodulo` em **nomes de arquivos, pastas e conteúdos**
   * Edite o idioma em `lang/en/mod_template.php`

3. **Registre o módulo no `version.php`:**
   Exemplo:

   ```php
   defined('MOODLE_INTERNAL') || die();

   $plugin->component = 'mod_seumodulo';
   $plugin->version = 2025052800;
   $plugin->requires = 2022041900; // Moodle 4.0 ou superior
   $plugin->maturity = MATURITY_ALPHA;
   $plugin->release = 'v0.1';
   ```

4. **Instale no Moodle:**

   * Copie a pasta `mod_seumodulo` para o diretório `/mod` da sua instalação Moodle
   * Acesse o Moodle como administrador e finalize a instalação do plugin

5. **Adapte a lógica no `view.php`, `lib.php`, `locallib.php`, etc.**

## 💡 Dicas

* Use a função `get_string('key', 'mod_seumodulo')` para suporte a múltiplos idiomas.
* Valide seu código com o [Code Checker do Moodle](https://moodle.org/plugins/local_codechecker).

## 📄 Licença

MIT – Use livremente para aprender, criar e compartilhar!
