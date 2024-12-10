# Instrucciones CI/CD

Para minimizar el tiempo de despliegue desde el sincronizador, se puede realizar un commit rápido de solo-agregar de la siguiente manera:

    git clone --no-checkout --depth 1 --filter=blob:none git@github.com:clubestoril2/archivos-estaticos.git
    cd archivos-estaticos
    git sparse-checkout init --cone
    # Descarga únicamente el directorio raíz, sin subdirectorios
    git read-tree -mu HEAD

