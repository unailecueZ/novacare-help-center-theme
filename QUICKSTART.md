# 🚀 Quick Start - NovaCare Health Theme

## ✅ Estado Actual

**El theme ya está importado en Zendesk**
- Theme ID: `ac49355b-7649-4408-9847-62e3109d4474`
- Estado: Importado (no publicado aún)
- Ubicación: Admin Center > Guide > Themes

## 📋 Pasos Siguientes

### 1. Publicar el Theme (5 minutos)

```bash
# Opción A: Desde la UI de Zendesk (Recomendado)
```

1. Ve a **Admin Center** → **Guide** → **Themes**
2. Busca "NovaCare Health Theme"
3. Click en **Customize** (opcional: personalizar colores/logo)
4. Click en **Publish**
5. Confirma la publicación

```bash
# Opción B: Desde CLI
zcli themes:publish ac49355b-7649-4408-9847-62e3109d4474
```

### 2. Subir Logo de NovaCare (2 minutos)

1. En **Customize** > **Brand** > **Logo**
2. Click **Choose file**
3. Sube logo PNG (recomendado: 40-60px de altura, fondo transparente)
4. Click **Save** y luego **Publish**

### 3. Crear Contenido de Ejemplo (15-20 minutos)

#### Categorías Recomendadas:
1. **Billing & Payments**
2. **Appointments**  
3. **Clinical Devices**
4. **Patient Portal**

#### Crear en Zendesk:
1. Admin Center > **Guide** > **Arrange content**
2. Click **Add category**
3. Nombre: "Billing & Payments"
4. Descripción: "Manage your bills and payment options"
5. Click **Save**
6. Repite para las otras categorías

#### Crear Sections (dentro de cada categoría):
- Billing & Payments → "Making Payments", "Understanding Your Bill"
- Appointments → "Scheduling", "Rescheduling", "Cancellations"
- Clinical Devices → "Glucose Monitors", "Blood Pressure Monitors"
- Patient Portal → "Account Setup", "Portal Features"

#### Crear Artículos:

**Artículo Ejemplo 1: "How to Pay Your Bill Online"**
```
Category: Billing & Payments
Section: Making Payments
Title: How to Pay Your Bill Online

Content:
# How to Pay Your Bill Online

Learn how to conveniently pay your medical bills through our online portal.

## Prerequisites
- Active NovaCare patient portal account
- Your account number from your billing statement

## Step-by-Step Instructions

1. **Log in to the Patient Portal**
   - Go to https://portal.novacare.com
   - Enter your username and password
   - Click "Sign In"

2. **Navigate to Billing**
   - Click "Billing" in the main menu
   - Select "View Bills"

3. **Select the Bill to Pay**
   - Review your outstanding bills
   - Click "Pay Now" on the bill you want to pay

4. **Enter Payment Information**
   - Choose payment method (Credit Card, Debit Card, or Bank Account)
   - Enter payment details
   - Review the amount

5. **Confirm Payment**
   - Review all information
   - Click "Submit Payment"
   - Save your confirmation number

## Troubleshooting

**Can't see your bill?**
- Bills appear 24-48 hours after service
- Check that you're logged into the correct account

**Payment not going through?**
- Verify your payment information is correct
- Check with your bank about transaction limits
- Try a different payment method

## Need Help?
Contact our billing department:
- Phone: (555) 123-4567
- Email: billing@novacare.com
- Hours: Monday-Friday, 8am-5pm EST
```

**Artículo Ejemplo 2: "How to Reschedule Your Appointment"**
**Artículo Ejemplo 3: "Pairing Your Glucose Monitor"**

### 4. Verificar que Todo Funciona (5 minutos)

1. **Visita tu Help Center**
   ```
   https://TU-SUBDOMAIN.zendesk.com/hc/en-us
   ```

2. **Prueba estas cosas:**
   - [ ] Header y footer se ven con colores NovaCare
   - [ ] Hero section tiene gradiente azul
   - [ ] Categorías aparecen como cards
   - [ ] Search box funciona
   - [ ] Click en un artículo muestra el contenido
   - [ ] Breadcrumbs funcionan
   - [ ] Mobile responsive (reduce ventana del navegador)

### 5. Configurar Campo Personalizado "Patient ID" (5 minutos)

Para la Parte 3 del ejercicio FDE (ZAF Sidebar App):

1. Admin Center > **Objects and rules** > **Tickets** > **Fields**
2. Click **Add field**
3. Configuración:
   - Field type: **Text**
   - Field name: **Patient ID**
   - Field key: `patient_id`
   - Required: Optional (para testing)
   - Visible to agents: Yes
4. Click **Save**

## 🎯 Checklist Completo para FDE

### Pre-Interview Setup
- [ ] Theme publicado en Zendesk
- [ ] Logo de NovaCare subido
- [ ] 4 categorías creadas
- [ ] 8-12 secciones creadas
- [ ] 10-15 artículos publicados (no drafts)
- [ ] Campo "Patient ID" creado
- [ ] Búsqueda probada
- [ ] Mobile testing completado

### Durante la Entrevista
- [ ] Parte 1: AI Agent con knowledge base funcional
- [ ] Parte 2: Action Flows con branding consistente
- [ ] Parte 3: ZAF App integrado con theme

## 🔧 Comandos Útiles

```bash
# Ver themes importados
zcli themes:list

# Actualizar theme después de cambios
zcli themes:update ac49355b-7649-4408-9847-62e3109d4474

# Preview theme antes de publicar
zcli themes:preview ac49355b-7649-4408-9847-62e3109d4474

# Ver detalles del theme
zcli themes:describe ac49355b-7649-4408-9847-62e3109d4474
```

## 📍 URLs Importantes

- **Help Center**: `https://TU-SUBDOMAIN.zendesk.com/hc/en-us`
- **Admin Center**: `https://TU-SUBDOMAIN.zendesk.com/admin`
- **Theme Customization**: Admin Center > Guide > Themes
- **Content Management**: Admin Center > Guide > Arrange content
- **GitHub Repo**: https://github.com/unailecueZ/novacare-help-center-theme

## 🆘 Problemas Comunes

### Theme no se ve después de publicar
```bash
# Limpia cache del navegador
Cmd+Shift+R (Mac) o Ctrl+Shift+R (Windows)

# O prueba en modo incógnito
Cmd+Shift+N (Mac) o Ctrl+Shift+N (Windows)
```

### Artículos no aparecen en búsqueda
1. Verifica que estén **Published** (no Draft)
2. Admin Center > Guide > Settings > **Rebuild search index**
3. Espera 5-10 minutos

### Colores no se ven correctamente
1. Verifica que el theme esté **Published** (no solo imported)
2. Ve a Customize > Colors y verifica que brand_color sea `#2C5F8D`
3. Si cambiaste style.css, ejecuta `zcli themes:update`

## 💡 Tips

1. **Contenido de Calidad**: Los artículos del FDE ejercicio serán evaluados. Usa el ejemplo arriba como guía.

2. **Estructura Clara**: Categorías → Sections → Articles. Mantén jerarquía lógica.

3. **SEO**: Usa títulos descriptivos. "How to Pay Your Bill Online" es mejor que "Online Payments".

4. **Imágenes**: Considera agregar screenshots a los artículos para mayor claridad.

5. **Testing**: Prueba SIEMPRE en mobile antes de la entrevista.

## ⏱️ Tiempo Estimado Total

- Publicar theme: **5 min**
- Subir logo: **2 min**  
- Crear categorías/sections: **10 min**
- Crear 10 artículos: **45-60 min**
- Testing: **10 min**
- Configurar campo Patient ID: **5 min**

**Total: ~75-90 minutos**

## ✅ Siguiente Paso

```bash
# 1. Publica el theme ahora
#    Admin Center > Guide > Themes > NovaCare Health Theme > Publish

# 2. Verifica que se vea bien
#    https://TU-SUBDOMAIN.zendesk.com/hc/en-us

# 3. Empieza a crear contenido
#    Admin Center > Guide > Arrange content > Add category
```

---

**Theme ID**: `ac49355b-7649-4408-9847-62e3109d4474`  
**Repository**: https://github.com/unailecueZ/novacare-help-center-theme  
**Status**: ✅ Ready to publish
