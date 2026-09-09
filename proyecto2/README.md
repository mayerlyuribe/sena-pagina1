# Actividad
Diseñar una aplicación, donde se vea la siguiente informacion de los siguientes servicios

Foto de la fachada del espacio real en el centro (formato horizontal, tipo banner).
Nombre del servicio como título principal.
Descripción de qué ofrece (mínimo 3–4 líneas, redactadas por ustedes).
Horarios de atención (por día de la semana, tabla o lista clara).
Teléfono de contacto (con formato legible, ej. +57 607 724 8100 ext. 205).
Ficha del encargado de atención al cliente:
Foto del encargado. Si no la consiguen, usar un avatar alusivo
Nombre completo.
Cargo.
Correo institucional.

Servicios
- Enfermeria
- Bienestar
- Biblioteca
- Cafeteria
- Coordinacion
Diseñar una pagina llamada Acerca en donde va Info del centro y equipo desarrollador


    <q-page>
        <!-- Hero Banner con q-img -->
        <q-img src="https://picsum.photos/1920/1080" height="450px" fit="cover">
            <!-- Capa de superposición con oscurecimiento y texto centrado -->
            <div class="absolute-full flex flex-center bg-dark-transparent text-white">
                <div class="text-center q-px-md">
                    <h1 class="text-h2 text-weight-bolder q-mb-xs">
                        Título Principal Hero
                    </h1>
                    <p class="text-subtitle1 text-weight-light q-mb-md">
                        Un subtítulo descriptivo para captar la atención de los usuarios.
                    </p>
                    <q-btn color="primary" label="Comenzar ahora" size="lg" unelevated rounded />
                </div>
            </div>
        </q-img>
    </q-page>