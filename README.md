Testes de Modelos de Reconhecimento de Fala para Dublagem de Vídeos do YouTube
Este projeto tem como objetivo avaliar diferentes modelos de reconhecimento de fala (Speech-to-Text - STT) para identificar a solução mais eficaz na dublagem de vídeos do YouTube em múltiplos idiomas, visando ampliar a acessibilidade do conteúdo.

Índice
Introdução
Objetivo
Modelos Avaliados
Instalação
Uso
Resultados
Contribuições
Licença
Agradecimentos
Introdução
A dublagem de vídeos em diversos idiomas é uma estratégia essencial para aumentar o alcance e promover a inclusão no YouTube. Com o avanço das tecnologias de reconhecimento de fala, é possível automatizar a transcrição e tradução de áudios, facilitando a criação de versões dubladas em diferentes línguas.

Objetivo
O objetivo deste projeto é testar e comparar diferentes modelos de STT para determinar qual oferece a melhor precisão e eficiência na transcrição de áudios, visando sua aplicação na dublagem automática de vídeos do YouTube.

Modelos Avaliados
OpenAI Whisper: Um modelo de reconhecimento de fala desenvolvido pela OpenAI, conhecido por sua precisão em diversas línguas.
Google Speech-to-Text: Serviço de transcrição de áudio para texto oferecido pelo Google Cloud, suportando múltiplos idiomas e dialetos.
Instalação
Pré-requisitos
Python 3.x: Certifique-se de ter o Python instalado em seu sistema.
Conta no Google Cloud: Necessária para utilizar o serviço Google Speech-to-Text.
Clonar o Repositório
bash
Copiar
Editar
git clone https://github.com/KaiqueCatarin/Testes_Transcript.git
cd Testes_Transcript
Instalar Dependências
bash
Copiar
Editar
pip install -r requirements.txt
Nota: O arquivo requirements.txt inclui pacotes necessários como google-cloud-speech para o Google STT e dependências para o Whisper.

Configurar o Google Speech-to-Text
Criar um Projeto no Google Cloud: Acesse o Google Cloud Console.
Ativar a API Speech-to-Text.
Criar Credenciais de Conta de Serviço:
Navegue até IAM & Admin > Contas de Serviço.

Crie uma nova conta de serviço e baixe o arquivo JSON da chave.

Defina a variável de ambiente:

bash
Copiar
Editar
export GOOGLE_APPLICATION_CREDENTIALS="caminho/para/suas/credenciais.json"
Configurar o OpenAI Whisper
Instalar o Whisper:

bash
Copiar
Editar
pip install git+https://github.com/openai/whisper.git
Instalar o FFmpeg: O Whisper requer o FFmpeg para processamento de áudio.

Para Windows: Baixe em FFmpeg.org e adicione ao PATH do sistema.

Para macOS: Use o Homebrew:

bash
Copiar
Editar
brew install ffmpeg
Para Linux: Instale via gerenciador de pacotes:

bash
Copiar
Editar
sudo apt-get install ffmpeg
Uso
Preparar Seus Arquivos de Áudio: Coloque suas amostras de áudio no diretório audio_samples.

Executar o Script de Comparação:

bash
Copiar
Editar
python compare_stt.py
Nota: O script compare_stt.py processa cada arquivo de áudio usando tanto o Whisper quanto o Google STT, e então salva as transcrições para análise.

Resultados
Após executar o script de comparação, os resultados serão armazenados no diretório results, incluindo:

Arquivos de Transcrição: Arquivos de texto contendo as transcrições de ambos os sistemas.
Métricas de Desempenho: Pontuações de precisão e tempos de processamento para cada amostra de áudio.
Para uma análise detalhada dos resultados, consulte o arquivo analysis_report.md.

Contribuições
Contribuições são bem-vindas! Por favor, faça um fork deste repositório e envie um pull request para quaisquer melhorias ou correções de bugs.

Licença
Este projeto está licenciado sob a Licença MIT. Consulte o arquivo LICENSE para mais detalhes.

Agradecimentos
OpenAI Whisper
Google Cloud Speech-to-Text
