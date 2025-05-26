# InkTrackAnalyzer

Este projeto realiza a análise automática do crescimento de uma mancha de tinta em vídeo, utilizando OpenCV e Python. O usuário calibra a escala e seleciona a região de interesse (ROI) no vídeo, e o script extrai o raio e a área da mancha ao longo do tempo, salvando os dados em um arquivo CSV.

## Como funciona

1. **Calibração da régua:**
    - O usuário seleciona dois pontos sobre uma régua visível no vídeo para definir a escala (pixels por unidade real).
2. **Seleção da ROI:**
    - O usuário seleciona a área do vídeo onde a mancha será analisada.
3. **Calibração do threshold:**
    - O usuário ajusta o limiar para binarização da imagem, facilitando a detecção da mancha.
4. **Processamento:**
    - O script processa todos os frames do vídeo, detecta a mancha, calcula o raio e a área, e salva os resultados em CSV.

## Requisitos

-   Python 3.8+
-   [uv](https://github.com/astral-sh/uv) (gerenciador de dependências ultrarrápido)

## Instalação das dependências

Com a ferramenta [uv](https://github.com/astral-sh/uv) instalada, basta rodar:

```bash
uv sync
```

## Como usar

1. Coloque o vídeo a ser analisado na pasta `videos/`.
2. Execute o script principal:
    ```bash
    uv run track.py
    ```
3. Siga as instruções na tela para calibrar e processar o vídeo.
4. Os resultados serão salvos em `data/` como um arquivo CSV.

## Estrutura do projeto

-   `track.py` — Script principal de análise.
-   `videos/` — Coloque aqui seus vídeos.
-   `data/` — Resultados em CSV serão salvos aqui.
-   `README.md` — Este arquivo.
-   `pyproject.toml` e `uv.lock` — Gerenciamento de dependências com uv.

## Observações

-   O script requer ambiente gráfico para exibir as janelas do OpenCV.
-   Para vídeos grandes, o processamento pode demorar.
-   O código é orientado a objetos e fácil de adaptar para outros experimentos.

---

Desenvolvido para fins acadêmicos na Unicamp.
