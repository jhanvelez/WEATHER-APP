# Nuevo Proyecto

Este proyecto incluye dos submódulos: un frontend en React y un backend en Laravel. A continuación se proporcionan instrucciones sobre cómo consumir los endpoints desde el frontend y cómo probar el proyecto en un entorno local.

## Submódulos

- [Frontend](frontend): Proyecto de React.
- [Backend](backend): Proyecto de Laravel.

## Cómo Consumir los Endpoints desde el Frontend

1. **Configurar el Backend:**
   - Asegúrate de que el backend esté corriendo en `http://localhost:8000`.
   - Puedes cambiar la URL base en el archivo de configuración del frontend si es necesario.

2. **Ejemplo de Consumo de Endpoint en el Frontend:**

    ```jsx
    import axios from 'axios';

    const getWeather = async (city, countryCode) => {
        try {
            const response = await axios.get('http://localhost:8000/api/weather/current', {
                params: { city, countryCode }
            });
            console.log(response.data);
        } catch (error) {
            console.error(error);
        }
    };

    getWeather('Pereira', 'CO');
    ```

## Instrucciones sobre Cómo Probar el Proyecto en un Entorno Local

### Backend (Laravel)

1. **Clonar el Repositorio:**

    ```bash
    git clone https://github.com/tu-usuario/nuevo-repositorio.git
    cd nuevo-repositorio/backend
    ```

2. **Instalar Dependencias:**

    ```bash
    composer install
    ```

3. **Configurar el Archivo .env:**

    ```bash
    cp .env.example .env
    ```

    - Configura las variables de entorno en el archivo [.env](http://_vscodecontentref_/#%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2FUsers%2Fpysti%2FProyectos%2FPySTI%2FTechnicalTest%2Fweather-app-backend%2F.env%22%2C%22path%22%3A%22%2FUsers%2Fpysti%2FProyectos%2FPySTI%2FTechnicalTest%2Fweather-app-backend%2F.env%22%2C%22scheme%22%3A%22file%22%7D%7D).

4. **Generar la Clave de la Aplicación:**

    ```bash
    php artisan key:generate
    ```

5. **Ejecutar las Migraciones:**

    ```bash
    php artisan migrate
    ```

6. **Iniciar el Servidor de Desarrollo:**

    ```bash
    php artisan serve
    ```

### Frontend (React)

1. **Navegar al Directorio del Frontend:**

    ```bash
    cd ../frontend
    ```

2. **Instalar Dependencias:**

    ```bash
    npm install
    ```

3. **Iniciar el Servidor de Desarrollo:**

    ```bash
    npm start
    ```

## Autor

El autor de este proyecto es @jhanvelez. Puedes encontrar más información sobre él en su [perfil de GitHub](https://github.com/jhanvelez).