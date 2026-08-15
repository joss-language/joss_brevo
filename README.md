# Plugin joss_brevo

Plugin oficial para el envío de correos electrónicos transaccionales mediante la API REST de **Brevo (Sendinblue)** en el lenguaje **Joss**.

## Instalación

```bash
joss pub add joss_brevo
```

## Configuración (.env)

Configura tu API Key en tu archivo `.env`:

```ini
BREVO_API="xkeysib-..."
MAIL_FROM_ADDRESS="hi@joss.red"
MAIL_FROM_NAME="Mi Proyecto"
```

## Uso

```joss
$mailer = new BrevoClient()
$sent = $mailer->send("destinatario@example.com", "Asunto del Correo", "<h1>¡Hola desde Joss!</h1>")

($sent) ? {
    print("Correo enviado con éxito")
} : {
    print("Error: " . $mailer->lastError())
}
```
