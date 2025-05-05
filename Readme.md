# WhatsApp Web Version Tracker

Repositório colaborativo para rastrear a versão mais recente do WhatsApp Web (Phone Version) usada pela Evolution API.

## 🔄 Como Atualizar a Versão

1. **Faça um fork** deste repositório
2. Edite o arquivo [`version.txt`](version.txt) (apenas a linha `phone_version=X.X.X.X`)
3. **Abra um Pull Request** para a branch `main`
4. Após aprovação e merge, o GitHub Actions atualizará automaticamente:
   - `metadata.json` (com data/hora e autor)
   - Histórico de versões

[📝 **Clique aqui para editar diretamente**](https://github.com/VelterGarcias/LATEST-WHATSAPP-SESSION_PHONE_VERSION/edit/main/version.txt) (sugere-se usar PR)

## 📡 Como Consultar a Versão

### Via API Pública (JSON)
```bash
curl https://raw.githubusercontent.com/VelterGarcias/LATEST-WHATSAPP-SESSION_PHONE_VERSION/main/metadata.json
```

### JavaScript (Node.js/Frontend)
```javascript
fetch('https://raw.githubusercontent.com/VelterGarcias/LATEST-WHATSAPP-SESSION_PHONE_VERSION/main/metadata.json')
  .then(response => response.json())
  .then(data => {
    console.log('Versão atual:', data.phone_version);
    console.log('Última atualização:', data.last_updated);
  });
```

### Python
```python
import requests
url = "https://raw.githubusercontent.com/VelterGarcias/LATEST-WHATSAPP-SESSION_PHONE_VERSION/main/metadata.json"
data = requests.get(url).json()
print("Versão:", data["phone_version"])
```

### PHP
```php
$json = file_get_contents('https://raw.githubusercontent.com/VelterGarcias/LATEST-WHATSAPP-SESSION_PHONE_VERSION/main/metadata.json');
$data = json_decode($json, true);
echo $data['phone_version'];
```

## 📊 Histórico de Versões
Veja todas as alterações no [CHANGELOG.md](CHANGELOG.md) (gerado automaticamente pelo GitHub Actions).

## 🤝 Contribuição
1. Garanta que a versão é compatível com a [Evolution API](https://github.com/EvolutionAPI/evolution-api)
2. Não inclua outros campos no `version.txt`
3. Atualize apenas quando necessário

[![Update Version](https://img.shields.io/badge/Atualizar_Versão-Open_in_GitHub-blue?style=for-the-badge)](https://github.com/VelterGarcias/LATEST-WHATSAPP-SESSION_PHONE_VERSION/edit/main/version.txt)

