# bergcastro-image-processing

Um pacote Python para processamento de imagens, incluindo funcionalidades para comparar imagens, transferir histogramas e redimensionar imagens.

## Descrição

O pacote `bergcastro-image-processing` oferece ferramentas para:

- Comparar imagens usando similaridade estrutural.
- Transferir histogramas entre imagens.
- Redimensionar imagens com diferentes proporções.

## Instalação

Use o gerenciador de pacotes [pip](https://pip.pypa.io/en/stable/) para instalar `bergcastro-image-processing`.

```bash
pip install bergcastro-image-processing
```

## Uso
### Comparando imagens

import numpy as np
from skimage import io
from bergcastro_image_processing.similarity import find_difference

### Carregue as imagens
image1 = io.imread('imagem1.png')
image2 = io.imread('imagem2.png')

### Encontre a diferença entre as imagens
difference_image = find_difference(image1, image2)

### Salve a imagem da diferença
io.imsave('diferenca.png', difference_image)

## Histograma

from skimage import io
from bergcastro_image_processing.histogram import transfer_histogram

## Carregue as imagens
image1 = io.imread('imagem1.png')
image2 = io.imread('imagem2.png')

## Transfira o histograma da imagem2 para a imagem1
matched_image = transfer_histogram(image1, image2)

## Salve a imagem resultante
io.imsave('histograma_transferido.png', matched_image)


## Autor

- Berg Castro - [https://github.com/BergCastro](https://github.com/BergCastro)

## Licença

Este projeto está licenciado sob a [Licença MIT](https://choosealicense.com/licenses/mit/) - veja o arquivo [LICENSE](LICENSE) para detalhes.