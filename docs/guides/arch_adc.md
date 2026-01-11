cat <<EOF > .env.example
# Configuración del Sistema
APP_NAME="SCV Empresarial"
APP_ENV=local
APP_DEBUG=true

# Seguridad y GPG
GPG_KEY_ID=tu_llave_aqui
SIGNING_ENABLED=true

# API Keys (Ejemplo)
DATABASE_URL="postgresql://user:password@localhost:5432/db"
EOF