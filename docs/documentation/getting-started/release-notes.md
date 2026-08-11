---
title: Release notes
deprecated: false
hidden: false
icon: fad fa-info
metadata:
  robots: index
---
# Release Notes

# **v6.7.5 - Nov. 6, 2025**

### **Bug**

- PN-3975 Backoffice - Onboarding simple - Proceso de Onboarding no inserta el logo por default.
- PN-3982 AgilPay API- ACH transactions are allowing `"HoldFunds": true"`
- PN-3998 Backoffice - Merchant Name Not Updating in DB After Edit

### **New Feature**

- PN-3924 WebPay - New parameter to load check Save Wallet marked by default

# **v6.7.4 - Oct. 30, 2025**

### **Epic**

- PN-4019 AgilPay - v6.7.4

### **Bug**

- PN-3996 Settlements - Pre-Auth transactions capture process is loggin sensitive data
- PN-4000 WebPay - Register token logs show raw sensitive data
- PN-4001 WebAPI - RegisterToken: The response returned when card valdiation fail has an invalid structure
- PN-4002 WebPay - "Object Reference Not Set" when the user try to register a new card on WebPay Register Card Mode
- PN-4007 Commissions - round amount issue

### **Improvement**

- PN-3935 Webpay - Query parameters dynamically with Internal API

# **v6.7.3 - Oct. 08, 2025**

### **New Feature**

- PN-3813 ACheck21 Onboarding maintenance on Backoffice

### **Improvement**

- PN-3954 Webpay Click2Pay - new flow for transactions with cards already saved in Click2Pay without ZipCode
- PN-3990 WebPay - Delete "Your click 2 pay cards" label from payment page
- PN-3902 AgilPay Portal: Default invoice due date configurable
- PN-3804 Api Interno - Migrate notification methods that already exists in WSV5
- PN-3823 Api Interno - New method ChangePassword
- PN-3973 Move Diskeys to Azure Vault using KEK/DEK
- PN-3909 Security improvement requested by Payroc team

### **Bug**

- PN-3957 Pay2Link - Invoice pagination lose data if the user change the page size
- PN-3979 WebAPI - ZipCode is sent empty if the length is greater than 5 characters
- PN-3984 WSV5 - Error executing GetNextSequence while transaction with BridgePay is processing
- PN-3991 Pay2Link - Edit invoice is not updating min. amount field
- PN-3992 WebPay - Mastercard Click2Pay init() fail by an invalid dpLocation value
- PN-3993 WebPay - Payment Page: The transactions processed with click2Pay cause an error on AgilPay portal transaction detail

# **v6.7.2 - Sep. 11, 2025**

### **Bug**

- PN-3890 CS General – Edit Payment Plan: The recurrence projection does not display data
- PN-3894 CS General – Pay2Link: The query for all invoices created by users uses the incorrect privilege
- PN-3896 CS General: Error on screens when accessing them without the required privilege
- PN-3906 CS General – Configuration: Users can update the default environment logo by modifying the merchant's logo
- PN-3929 Pay2Link: Error on Configuration page when merchant has no logo configured
- PN-3974 CS General: "Currency" field is disabled when creating a new agreemen

### **User Story**

- PN-3884 CS General – Batch History: Process closures through the settlements queue

### **Improvement**

- PN-3891 CS General – Payment Plan: Do not display recurrence projection if the status is not "Active"
- PN-3922 CS General: Typing a page name in the address bar allows access regardless of lacking permission
- PN-3937 Pay2Link Security Requirement: Invoices – add, edit, view, duplicate
- PN-3939 Pay2Link Security Requirement: Customer, Invoice Tracking, Service, Suppliers, Invoice Balance, Configuration
- PN-3940 User Security Requirement
- PN-3970 AgilPay Devices Api - New db field IoT ConString to migrate devices
- PN-3971 AgilPay Terminal Manager Api - Verify IoT ConString before send terminal commands

# **v6.7.1 - Aug. 07, 2025**

### **Historia**

- PN-3925 WebPay - Payment Page: Renombrar label del check que permite guardar los metodos de pago

# **v6.7 - Jul. 31, 2025**

### **Mejora**

- PN-3883 Guardar el Request y Response obtenido de los cierres
- PN-3910 Pay2link List Invoice - Permite acceso a facturas via QueryString (caso VL1)
- PN-3911 Virtual Terminal - Permite modificar los parametros en el request
- PN-3918 Pay2link Invoice  - Al visualizar el detalle de una transaccion se puede manipuar el Id en el Querystring
- PN-3919 Pay2Link Invoice - Controlar Cross Site Scripting (XSS)
- PN-3921 Recurrencia - Permite manipular los request a /api/Recurrent/GetLocations/ por querystring
- PN-3923 Black List - Permite visualizar la lista de tarjetas bloqueadas de otro merchant manipulando el ID

### **Nueva Función**

- PN-3871 ACollect - Ejecuciones por grupos

# **v6.6.24 - Jul. 15, 2025**

### **Error**

- PN-3898 La pantalla de creacion de comercios Pay2Link en Backoffice permite crear comercios sin correo
- PN-3899 Backoffice - Compañias pay2link - dropdowns no permiten filtrar las opciones
- PN-3903 Backoffice - Compañias pay2link - Error al crear comercio P2L

### **Mejoras**

- PN-3882 CS General - Batch Detail: Agregar columna \<Transaction\_Type> al detalle de los cierres y limitar tipo de transacciones
- PN-3885 CS General - Batch History: Agregar exportacion a excel
- PN-3886 CS General - Batch Detail: Agregar exportación a Excel

# **v6.6.23 - Jul. 3, 2025**

### **Historia**

- PN-3729 CS General - Recurrent Reports: Reemplazar logo de Dynamics Payments por el logo de AgilPay

### **Nueva función**

- PN-3878 WebAPI - Modificar metodos RefundById para realizar refunds parciales
- PN-3880 CS General - Agregar campo \<Detalle\_Transaccion> a la exportación y al detalle de las transacciones
- PN-3887 CS General - Settlements Reports: Agregar reportes por batchs
- PN-3723 CS GENERAL - Agregar funcionalidad que permita visualizar detalle de factura en el Portal

### **Mejora**

- PN-3559 CS General - Virtual Terminal: Controlar metodo de notificacion al procesar pago
- PN-3802 CS General - Mover operaciones de transacciones al WebAPI de Paynet
- PN-3877 CS General - Correcciones UI y de texto

# **v6.6.22 - Jun. 23, 2025**

### **Mejora**

- PN-3599 Backoffice - Routing Numbers: Actualizar mantenimiento con el campo OrderBy

### **Nueva Función**

- PN-3872 Integración 3D Secure con adquirente Azul

# **v6.6.21 - Jun. 12, 2025**

### **Error**

- PN-3868 Backoffice - Onboarding: Error al crear el comercio sin completar el campo Descripcion del usuario

### **Mejora**

- PN-3869 WebApi - GetTransactionByReference: Agregar filtros \<Transaction\_Type> y <Status>

# **v6.6.20 - Jun. 5, 2025**

### **Error**

- PN-3866 Paynet - WSV5: El correo electronico del usuario no esta siendo grabado en transaccion\_tc
- PN-3867 CS General - Payment Plan: El icono de nuevo payment plan esta pegado al texto
- PN-3870 CS Claro PR - Modal de notificaciones: El telefono y el email del cliente no vienen pre-cargados

### **Historia**

- PN-3585 CS General - Add Invoice/Edit Invoice: Agregar campo monto minimo

### **Change**

- PN-3863 Paynet - Mostrar numero de telefono de la localidad en la notificacion de pago

### **Mejora**

- PN-3825 Payment Plan - Actualización de labels y manejo de data en cache
- PN-3864 CS General - Add Invoice: Reorganizar campos  para reducir tamaño del formulario

# **v6.6.19 - May. 29, 2025**

### **Error**

- PN-3855 CS General - Barra de menú: El nombre del comercio desaparece al cambiar de pantalla
- PN-3861 CS General - Edit Payment Plan: Error al editar asignando un Plan Number existente
- PN-3862 WebAPI - AuthorizeToken: Error al intentar procesar una transaccion ACH con un EffectiveDate invalido
- PN-3077 WebPay - Payment Page: El correo de la localidad sale pegada al texto "Any Question" si la pantalla se sube en espanol

### **Historia**

- PN-3691 CS General - Transaction Detail: Cambiar de posicion el historico de eventos y paneles request/response

### **Change**

- PN-3859 WebApi - Modificar etiqueta <NoNotificate> del ExtData

### **Mejora**

- PN-3858 Paynet - Nuevo parametro para controlar notificaciones de pago
- PN-3860 CS General - Copiar invoice link sin mostrar la url en el modal

# **v6.6.18 - May. 22, 2025**

### **Mejora**

- PN-3857 WebPay - Grabar transacciones con create\_user “WebPay“
- PN-3442 Transactional Reports: Nuevo <Date Type> "Return ACH" para los reportes ACH Return Detail y ACH Return Detail Extended

# **v6.6.17 - May. 15, 2025**

### **Error**

- PN-3827 CS General - Payment Plan: El boton para exportar a excel no funciona
- PN-3852 Web API - GetTransactionByReference: Solo filtra por invoice y transacciones cerradas

### **Nueva función**

- PN-3666 CS GENERAL - Implementar multi compania para Pay2link

### **Mejora**

- PN-2707 CS Triple S - Pantalla de cierres: Adecuaciones
- PN-2708 CS ClaroPR - Pantalla de cierres: Adecuaciones
- PN-2987 CS General - Modal de clientes: Ajustar estetica del modal
- PN-2988 CS General - Modal de clientes: Mejorar metodo de consulta
- PN-3419 CS General - Edicion y Detalle de factura: Agregar botones de operaciones
- PN-3493 CS General - New Payment Plan: Reorganizacion de campos en metodos de pago Credit Card
- PN-3834 CS General - Configuration: Colocar el campo <Email> como solo lectura
- PN-3816 CS General - Advanced Search: Agregar filtro <Customer Number>
- PN-3831 GRAL CS - Agregar informacion de Factura y descripcion al Sumary Payment de Virtual Terminal y la confirmacion de pago enviada por email
- PN-3846 Backoffice - Usuarios: Modificar mensaje mostrado al insertar un perfil con un comercio que no esta en pay2link
- PN-3406 CS General - Pay2Link Configuration: Mejoras UX/UI en el campo <Logo>

# **v6.6.16 - May. 07, 2025**

### **Error**

- PN-3219 Back Office - Transsaciones: Al anular una transaccion por el backOffice el estatus solo cambia en transaccion\_tc, transacciones\_canal se queda igual.

### **Change**

- PN-3588 Paynet - Renombrar los parametros tipo servicio de ClaroPR

### **Mejora**

- PN-2804 WebPay - Boton de Pago BPD: Procesar la transaccion al recibir el mensaje MPOUT
- PN-3603 Paynet - Transacciones complementarias: Insertar Pament\_Type de la transaccion original en la nueva transaccion
- PN-3845 Mejoras UX/UI en el componente Click2Pay integrado en WebPay
- PN-3457 Cierre Azure - Notificacion de cierres: Enviar resumen de cierres procesados
- PN-3841 Backoffice - Afiliados: Mostrar el campo hora de cierre para todos los afiliados cuyo adquirente permite cierre automatico
- PN-3835 Backoffice - Afiliados: Actualizar la hora de cierre en BatchProcessSchedule
- PN-2196 PayNet WebAPI / WSV5: Mostrar en graylog request y response del proceso de notificacion
- PN-2198 PayNet DB - Agregar campo "Correlation\_Id" a Transacciones\_Canal
- PN-1733 Funcionalidad lista negra para backoffice

# **v6.6.15 - Apr. 10, 2025**

### **Error**

- PN-3515 Error en transacciones cuando alguna entidad esta inactiva
- PN-3829 WebPay - Click2Pay: El formulario de metodos de pagos se queda en blanco

### **Mejora**

- PN-3222 Backoffices - Transacciones: Dar espacio entre las columnas ID Transaccion y Fecha Transaccion
- PN-3266 CS General - Virtual Terminal: Enviar create\_user de la transaccion en el parametro ExtData del API
- PN-3268 CS General - Edit Invoice: No permitir editar el monto si la factura tiene un pago aplicado
- PN-3303 CS General - LogOut: Borrar los datos de las pantallas de consultas de la cache del navegador
- PN-3407 CS General - Virtual Terminal /  Payment Plan: Agregar botones \[Edit Customer] y \[New Customer]
- PN-3408 CS General - Add Invoice: Agregar botones \[Edit] y \[New]
- PN-3721 BACK OFFICE - Agregar indicador de Card Not Presente (CNP) y Card Present (CP) en Canal
- PN-3805 Crear un proyecto que unifique los asmx de WSV5, apayment.asmx, speedpay, speedpayTS
- PN-3046 customer service - General - Advanced Search: Conservar filtros al notificar
- PN-3053 Customer Service - General - Advanced Search: Concatenar moneda al monto
- PN-3435 CS General - Add Invoice: Cambiar labels "Field Required" por "\*" rojos
- PN-3437 CS General - Transactional Reports: Eliminar filtro <User Group>
- PN-3497 CS General - Advanced Search: Mostrar nombre del producto en la consulta
- PN-3506 Backoffice - Usuarios: Crear usuarios en BD Pay2Link

# **v6.6.14 - Mar. 31, 2025**

### **Error**

- PN-3446 Manejo de monto en registro de transacciones y monto secreto
- PN-3760 CS General - Payment History: La moneda de las transacciones cambian al modificar el idioma del portal
- PN-3765 CS General - Transactional Reports: El campo <Users> muestra los usuarios de todos los comercios a los usuarios multi-comercio
- PN-3779 Paynet - Response de Webhooks: No se graba la respuesta negativa recibida desde el WebHook del cliente
- PN-3809 CS General - Payment Plan: El formulario permite ingresar una tarjeta nueva con la fecha XX/XXXX
- PN-3821 Paynet WebAPI - Error al procesar pago

### **Historia**

- PN-3432 CS General - Invoice View/Edit: Agregar titulo "Payments" al card que lista los pagos de la factura
- PN-3433 CS General - Invoice View/Edit: Mostrar estatus con el mismo estilo que se utiliza en el listado de facturas
- PN-3728 CS General - Transactional Reports: Reemplazar logo de Dynamics Payments por el logo de AgilPay

### **Nueva función**

- PN-3719 WebPay - Mover la pagina ShowInvoice del site de Pay2Link al Site de WebPay.

### **Mejora**

- PN-2553 CS General - Transaction Detail: Ofuscar las credenciales Merchant\_Code / Terminal\_Code (BridgePay / Profit Stars)
- PN-3128 P2L/CS - Las facturas con estatus pendiente que se encuentre vencida debe mostrar "Overdue" en el estatus.
- PN-3249 Customer Service - General - Menú: Cambiar la imagen de Dynamics Payments por el logo de Agilpay.
- PN-3253 CS General - Barra de menu superior: Adecuacion del campo para el cambio de idioma
- PN-3267 CS General - AddInvoice: Mostrar grid con los pagos aplicados si la factura esta pendiente
- PN-3814 CS General - Transaction Detail: Habilitar boton \[Void] para el tipo de transaccion Auth con estatus PreAuth
- PN-3826 CS General - Transaction Detail: Agregar campo <Invoice> y la moneda al monto en la seccion Transaction Information

# **v6.6.13 - Mar. 13, 2025**

### **Error**

- PN-3751 CS Claro PR - Pantallas de recurrencias: Las opciones de recurrencias del menú no estan siendo validadas por privilegio
- PN-3775 WebPay - Payment Page: Error de redireccion lanzado por el navegador al pagar factura pay2link con wallet
- PN-3778 CS General - Virtual Terminal: Si se consulta un cliente con wallets, el listado no se muestra automáticamente

### **Historia**

- PN-3547 WebPay - Payment Page: Modificar validacion de cuenta ACH

### **Mejora**

- PN-3415 CS CLARO - Agregar Consulta de Recurrencia (Acuerdo Autorizado y Acuerdo Ejecutado)
- PN-3491 CS General - Import Invoices: Validaciones para el numero de factura
- PN-3763 Paynet - Transacciones Eventos: Insertar un evento para las transacciones tipo consulta
- PN-3776 Backoffice - Agregar parametro para configurar cuales adquirentes permiten ser insertados en BatchsProcessSchedule
- PN-3784 WebAPI - VoidById: Recibir usuario para insertarlo en los campos de auditoria
- PN-3785 WebAPI - Captures: Recibir usaurio para insertarlo en los campos de auditoria
- PN-3786 WebAPI - RefundById: Recibir usuario para insertarlo en los campos de auditoria
- PN-3799 Paynet - Insertar fecha de vencimiento de las tarjetas en los campos Mes\_Vencimiento y Ano\_Vencimiento

# **v6.6.12 - Feb. 11, 2025**

### **Error**

- PN-3625 La Informacion de Refunds a partir de una transaccion previa es incorrecta
- PN-3774 WebPay - Click2Pay Payment Page: El boton \[Pay Now] desaparece si el usuario con wallets cierra el modal OTP y paga con una nueva tarjeta
- PN-3781 WebPay - Payment Page: Error de conexion para consumir endpoint 3DS
- PN-3782 WebPay - Payment Page: Los Routing Numbers no cargan si la pantalla solo permite pagos ACH

### **Historia**

- PN-3050 Customer Service - General - Advanced Search:  Reorganizar el orden de los filtros
- PN-3762 API Interno - Consulta de parametros: Incluir parámetros de tipo servicio y tipo canal

### **Nueva función**

- PN-3567 Paynet - Captura de transacciones: Insertar transaccion\_evento de captura para la nueva transaccion generada por los capture
- PN-3771 WSV5 - Recurring.asmx: Reactivar acuerdo preautorizado

### **Mejora**

- PN-3747 WebPay - Payment Page: Mejorar CSS de los radios que permiten seleccionar el producto

# **v6.6.11 - Jan. 28, 2025**

### **Historia**

- PN-3685 CS General - Transaction Detail: Cambiar el color de los badges para las transacciones Auth capturadas
- PN-3724 CS General - Transaction Detail: Asignar color y estatus a tipo de transaccion balance

### **Error**

- PN-3467 WebAPI - CloseBatchResumen: El cierre exitoso de ProfitStars retorna el ResponseCode = null
- PN-3611 Paynet - Bitacora de transacciones: Los voids automaticos se insertar con Result Failed
- PN-3613 WSV5 - ReenviarNotificacion: Al reenviar la notificacion de una transaccion capturada, se envia con el monto de la preautorizacion
- PN-3640 AgilPay Mobile - Detail Trasaction: Error a intentar realizar refund a transaccion ACH
- PN-3642 AgilPay Mobile - Manual Entry: Al colocar una tarjeta Amex o Discovery, la aplicacion no muestra su template
- PN-3643 AgilPay Mobile - Manual Entry: El formulario permite que el usuario pueda someter un pago con tarjetas expiradas
- PN-3644 AgilPay Mobile - Manual Entry: La aplicacion muestra las respuesas negativas del api en formato json al usuario
- PN-3646 AgilPay Mobile - Transaction Reports: Las transacciones tipo refund no se muestran con monto negativo
- PN-3648 AgilPay Mobile - Settings: La validacion de seguridad retorna invalid password cuando se ingresa el password valido
- PN-3649 AgilPay Mobile - Manual Entry: El campo CVV solo permite 3 caracteres
- PN-3650 AgilPay Mobile - Pay2Link: El scroll de la pantalla pay2link no es fluido
- PN-3652 AgilPay Mobile - Manual Entry: La longitud del campo Card Number se reduce
- PN-3703 WSV5 - Security.asmx: El cambio de contraseña no valida el formato de la contraseña
- PN-3739 PAYNET WEBAPI - Cuando colocamos en el campo 'exdata' que no envie la notificación al correo, tampoco llega al SMS
- PN-3740 WebAPI - RegisterToken: Los clientes grabados por este metodo estan insertando el campo Numero\_identificacion con un prefijo
- PN-3752 WebAPI - Recurring Schedule Add: Los clientes grabados por este metodo estan insertando el campo Codigo\_Cliente con un prefijo en Acuerdo\_Preautorizado
- PN-3766 Paynet WebAPI - Recurring Controller: Metodos Get y Update no encuentran el acuerdo

### **Nueva función**

- PN-2993 WebPay / WebApi - Implementacion Click2Pay

### **Mejora**

- PN-3635 AgilPay Mobile - Transactions: Agregar tipo de transaccion a los registros de la consulta
- PN-3636 AgilPay Mobile - Detail Transactions: Agregar fecha de cierre y datos del batch
- PN-3637 AgilPay Mobile - Transactions: Mostrar filtros de fecha Custom ocupando todo el panel
- PN-3638 AgilPay Mobile - Pay2Link: Agregar funcionalidad Copy Invoice
- PN-3651 AgilPay Mobile - Pay2Link: Mejorar experiencia de usuario con campos requeridos

# **v6.6.10 - Jan. 13, 2025**

### **Error**

- PN-3597 WebPay - Payment Page: Pantalla de error 500 al pagar con una marca de tarjeta que no tiene ruta de pago
- PN-3726 CS General- Al crear un usuario con el valor "ALL" en el campo "services" nos da error al intentar eliminar y editar
- PN-3727 CS General- editar users- campo ''services''  mapea el valor 'ALL' independientemente del valor selerccionado en la pantalla editar
- PN-3736 Payment Controller: Las transacciones procesadas con Paynet.GenericV3 envian el mismo valor en dos parametros
- PN-3744 CS GENERAL Virtual Terminal- Al buscar un cliente por el codigo si hay un error no despliega el mensaje.
- PN-3745 CS General - Transaction Detail: La captura de transacciones no se procesa
- PN-3748 WebPay - Payment Page: Error 500 al pagar con un routing number invalido

### **Nueva función**

- PN-3568 Backoffice - Onboarding: Excluir afiliados de terminales fisicas en la insercion a la tabla  BatchProcessSchedule
- PN-3558 Paynet - WebAPI:  Agregar etiqueta que acepte indicadores para no notificar

### **Mejora**

- PN-3738 Backoffice - Afiliado: Convertir inputs \<Merchant\_Code> y \<Terminal\_Code> en alfanumericos
- PN-3742 CS General - Virtual Terminal: Realizar validacion de metodos de pagos consumiendo el api interno
- PN-3743 CS GENERAL - Remover el Logo de Dynamics a los reportes de General.

# **v6.6.9 - Dec. 12, 2024**

### **Error**

- PN-3735 CS General - al intentar visualizar el pago de una factura desde la pantalla de Invoice de Pay2link se genera un error

### **Historia**

- PN-3693 CS General - Transaction Detail: Mover campo de Transaction Result a Transaction Information

### **Nueva función**

- PN-3731 WebPay / WebAPI - Nuevo parámetro para cancelar redirección automática

# **v6.6.8 - Dec. 10, 2024**

### **Error**

- PN-3682 CS General - Transaction Detail: El label "Propinas" esta incorrecto cuando el portal esta en ingles
- PN-3683 CS General - Transaction Detail: El boton \[Void Payment] permanece visible
- PN-3704 CS General - Creacion de usuarios: El campo <Services>/<Servicio> no carga los servicios

### **Historia**

- PN-3472 Customer Services - Advanced Search y Transactional Reports: Agregar control de filtrado por rango de fecha
- PN-3712 CS General - Payment Plan: Renombrar el boton \[Cancel this Schedule]
- PN-3725 CS General - Transactional Reports: Traducir nombre de los reportes.

### **Mejora**

- PN-3694 CS Mejora de obtencion de privilegios de usuario

# **v6.6.7 - Nov. 28, 2024**

### **Mejora**

- PN-3612 CS General - Transactional Reports: Agregar columna tipo de transaccion a los reportes
- PN-3695 CS General - Payment Plan Edit: Mostrar la data del producto en claro
- PN-3689 Paynet WebAPI/WS - Registrar response de los validations en el campo response de transacciones\_canal

### **Error**

- PN-3447 Backoffice - Onboarding: Campo correo y número deben ser obligatorios
- PN-3668 Backoffice - Transacciones: Timeout al acceder a la pantalla con 3 recolectores o mas configurados (Produccion)
- PN-3681 CS General - Los contadores de paginas de las pantallas pay2link alteran el diseño de la pantalla
- PN-3702 CS General - Virtual Terminal: Error procesando un Refund con ACH
- PN-3696 WebApi - Bitacora de eventos: Las transacciones via PagaTodo se insertan como FAILED en transacciones\_evento

# **v6.6.6 - Nov. 21, 2024**

### **Error**

- PN-3667 CS General - Payment Plan: La pantalla se queda "Loading" al consultar un cliente sin completar el campo
- PN-3674 CS Triple S - Payment Scheduled: Mensaje de error al guardar un plan de pago con un nombre muy largo
- PN-3700 CS GENERAL - Al autenticar con usuarios de AD cuelga la base de datos

# **v6.6.5 - Nov. 11, 2024**

### **Historia**

- PN-3592 API Interno - Login: Modificar para retornar listado de comercios
- PN-3593 CS General - Login: Consumir api interno para hacer login
- PN-3594 CS General - Seguridad: Realizar consulta de canales y servicios consumiendo el API Interno

### **Error**

- PN-3672 Paynet - Error con captura de transacciones PreAuth durante el cierre

### **Nueva función**

- PN-3663 WSV5 - Recurring.asmx: Modificar metodo GetAcuerdoPreautorizado para retornar tarjetas en claro
- PN-3664 GS GENERAL - Modificar el proceso de Refund para poder modificar el monto a reembolsar

# **v6.6.4 - Oct. 24, 2024**

### **Error**

- PN-3428 CS General - Payment History: Error al reenviar la notificacion de pago
- PN-3595 Backoffice - Afiliados: Al presionar **Guardar** la pantalla hace un refresh y el afiliado no es guardado

### **Nueva función**

- PN-3564 WSV5 - Wallet.asmx: Modificar metodo GetCustomerTokens para retornar tarjetas en claro

# **v6.6.3 - Oct. 17, 2024**

### **Mejora**

- PN-3654 Correccion de template cuando la empresa tiene un estilo personalizado
- PN-3618 Mejoras en la experiencia de usuario con el manejo de adjuntos en las facturas Pay2Link

# **v6.6.2 - Oct. 10, 2024**

### **Error**

- PN-3127 P2L/CS - Invoice Review: Mostrar unicamente los metodos de pago que la empresa tenga habilitados
- PN-3476 Validacion de fecha de efectividad (EfectiveDate) para ACH via API
- PN-3571 CS General - Payment Plan: La pantalla no filtra por el campo <Servicio>
- PN-3586 CS General - Pay2Link: El menu no se colapsa en las pantallas Customer e Invoice
- PN-3590 CS General - Transaction Detail: Traducir titulo del modal Add Black List
- PN-3609 CS Triple S / CS ClaroPR: Transactional Reports: Error al exportar como PDF  buscando fuentes de texto
- PN-3610 CS GENERAL - Al llamar la pagina de cambio de clave esta pasando el usuario por QueryString
- PN-3624 CS General - Virtual Terminal: La pantalla se queda consultando las rutas de pagos al cambiar de servicio
- PN-3627 WSV5 - WSPaynetv1.asmx - El metodo ConsultaServicio no retorna el parametro Fecha\_Factura
- PN-3630 WebPay - BotonBHD: Error al someter pago o cancelar el pago desde BHD

### **Historia**

- PN-3604 CS GENERAL - Agregar la columna Codigo\_Cliente de la tabla Clientes en los reportes Details de CS

### **Nueva función**

- PN-3187 CS GENERAL - Autenticar Customer Services contra Azure Active Directory
- PN-3565 WSV5 - Security.asmx: Agregar nuevo metodo para consultar las empresas vinculadas al usuario

### **Mejora**

- PN-3615 WSV5 - Recurring.asmx: Cancelar ejecuciones pendientes del acuerdo
- PN-3616 WSV5 - Recurring.asmx: Actualizar monto de las ejecuciones pendientes del acuerdo

# **v6.6.1 - Sep. 12, 2024**

### **Error**

- PN-3606 CS General - Invoices: La moneda de las facturas se establece como pesos si el portal esta en español

### **Historia**

- PN-3561 CS General - Advanced Search: Renombrar columnas de la consulta
- PN-3576 CS General - Advanced Search: Agregar columna "Payment Type"

### **Change**

- PN-3600 Paynet - ProfitStars: Crear batchs Profitstars con fecha de cierre para dos dias luego de la creacion

### **Nueva función**

- PN-3511 Nuevo adquirente de pagos: ACheck21

# **v6.6.0 - Sep. 06, 2024**

### **Épica**

- PN-3490 Paynet - Mejoras en los tipos de transacción

### **Error**

- PN-2788 WebAPI - No se esta registrando el RunId en los logs.
- PN-3508 CS General - Black Listed Cards: La tarjeta no pasa a lista negra si se ingresa una justificacion con mas de 300 caracteres
- PN-3577 PAYNET - Los pagos con Boton popular estan fallando

### **Change**

- PN-3474 CS General - Transactional Reports: Excluir transacciones con estatus 158 de los totales y subtotales REFUNDED

### **Mejora**

- PN-3293 CS General - Transaction Detail: Mas detalles sobre la transacción

# **v6.5.19 - Ago. 29, 2024**

### **Historia**

- PN-3471 CS General - Pay2Link Add Invoice / Update Invoice: Crear facturas con pagos abiertos

### **Nueva función**

- PN-2836 Agregar funcionalidad multiidioma para customer service

# **v6.5.18 - Ago. 22, 2024**

### **Historia**

- PN-3434 CS General - Add Invoice: Crear facturas con fecha factura futura o pasada
- PN-3542 CS General - Consulta de Routing Numbers

### **Error**

- PN-3420 CS General - Advanced Search: El resultado de los voids, refund y resend notification no se oculta al cambiar de pantalla o cerrar sesion
- PN-3501 CS General - Payment Plan: La recurrencia ach no es guardada con número de producto que digita el usuario en pantalla
- PN-3522 CS General - Add Invoice: La factura elimina los guiones del invoice number cuando registra la factura
- PN-3541 CS General - Payment Plan: La opcion copiar acuerdo no funciona
- PN-3548 Cierre - Error al intentar autorizar las transacciones ACH Offline
- PN-3557 CS General - Advanced Search: Los filtros no se muestran si se coloca la pantalla con dimensiones mobile
- PN-3563 CS General - Payment Plan: La descripcion del RegEx no se muestra al editar un acuerdo con customer number invalido

### **Mejora**

- PN-2794 Conector ClaroPR - Leer las credenciales de consulta y  notificacion de pago desde los parametros tipo servicio
- PN-3360 Reemplazar dependencias locales en proyecto paynet-functions
- PN-3554 Implementacion de OAuth Bearer token fijos para autenticacion de Webhooks
- PN-3555 Paynet - Registrar transacciones identificando el tipo de producto en un nuevo campo

# **v6.5.17 - Ago. 01, 2024**

### **Error**

- PN-3535 Paynet - Transacciones Pagatodo: Error al intentar una transaccion con el conector PagaTodo
- PN-3536 CS General - Payment Plan: Correcciones ortograficas
- PN-3537 WSV5 - WSPaynetv1 y WSPaynetv2: Error de Entity al intentar procesar un pago sin enviar Numero\_Medio\_Pago
- PN-3543 WSV5 - ReenviarNotificacion: La notificacion no es enviada con el conector con Paynet.GenericV3

### **Historia**

- PN-2549 Oportunidades de mejoras aplicar al API y webpay

### **Mejora**

- PN-2558 Gray log - Registrar en el Graylog los llamados a Bridgepay y profitstars.
- PN-3104 Paynet - Conector Triple S: Mover lectura de credenciales a la tabla Parametros
- PN-3364 CS/P2L: Marcar los check box de los metodos de pagos por default
- PN-3539 Paynet Cierre - ProfitStars: Crear batchs con fecha de cierre automatico para el mismo dia de apertura
- PN-3546 Envio de campo Impuesto en los recibos por email de notificacion

# **v6.5.16 - Jul. 24, 2024**

### **Error**

- PN-3503 Agilpay - Filtro estatus no esta mostrando correctamente los resultados al seleccionar todos
- PN-3518 CS GENERAL - ADD INVOICE: El boton \[Save] se deshabilita si se inserta un invoice number con mas 10 caracteres
- PN-3520 CS General - Add Invoice: El boton \[Save] se habilita al ingresar un invoice number invalido
- PN-3524 CS General - New Payment Plan: El campo currency muestra la moneda USD de forma fija
- PN-3525 WebAPI - Transacciones en efectivo: Las transacciones en efectivo de AccountType = 4 retornan un response incompleto
- PN-3526 Paynet - Transacciones tipo efectivo: Las transacciones procesadas como efectivo solo se registran en transacciones\_canal
- PN-3530 WSV5 - Recurring.asmx: No se esta actualizando el campo Codigo\_Cliente de la tabla acuerdo\_preautorizado
- PN-3531 WSV5 - Recurring.asmx: Retornar mensaje de acuerdo duplicado al crear y editar

### **Historia**

- PN-3480 Backoffice - Mantenimiento de Routing Numbers
- PN-3489 Paynet - Transacciones PreAuth: Registrar transacciones PreAuth con su propio tipo de transaccion
- PN-3496 Paynet - Enviar NameOnAccount hasta el adquirente
- PN-3529 CS General - Edit Payment Plan: Los campos <Customer Number> y <Plan Number> deben ser editables

### **Change**

- PN-3532 Backoffice - Onboarding: Crear un solo servicio por comercio y dejar de insertar parametros de notificacion

### **Nueva función**

- PN-3461 Implementar ReCaptcha en Webpay
- PN-3507 WebPay aceptar multiples facturas a pagar

### **Mejora**

- PN-1931 Validar balance de BAN antes de realizar cobro de Direct Deposit
- PN-3430 Creacion de conector de servicios PaynetGenericV3 que integre Pay2Link y Webhooks
- PN-3504 Agilpay - Agregar filtros de metodo de pago y marca
- PN-3505 Backoffice - Cierres Host: Agregar columna servicio al detalle

# **v6.5.15 - Jul. 10, 2024**

### **Historia**

- PN-3519 CS General - Configurar email y telefono como no requeridos

### **Error**

- PN-3516 CS General - Add Invoice: El account number es requerido para la factura aunque la configuracion del comercio lo tiene como no requerido
- PN-3517 CS General - Add Invoice: El telefono es requerido para la factura aunque la configuracion del comercio lo tiene como no requerido

# **v6.5.14 - Jul. 04, 2024**

### **Error**

- PN-3483 Backoffice - Onboarding: Las validaciones no permiten crear un comercio con credenciales que no sean TC o ACH
- PN-3502 WSV5 - WSPaynetv1 y WSPaynetv2: El metodo AplicaPago no permite procesar transacciones como efectivo

### **Historia**

- PN-3421 CS General - Advanced Search: Mostrar transacciones Refund en negativo
- PN-3438 CS General - Transactional Reports: Agregar filtro <Transaction Type>
- PN-3439 CS General - Advanced Search: Agregar filtro <Transaction Type>
- PN-3473 CS General - Advanced Search: Colocar badges a la data de la columna <Type>
- PN-3477 Paynet - RefundById / ReembolsaTransaccion: Insertar la transaccion originada con su propio numero de autorizacion
- PN-3478 Paynet - Reemplazar estatus de transaccion 145
- PN-3479 Paynet - Mover Routings Numbers a una tabla
- PN-3487 CS General - Add Invoice: La moneda de la factura debe ser tomada desde el configuration
- PN-3492 Paynet - SpeedPay WS: Mover los .asmx del proyecto SpeedPay al proyecto WSV5
- PN-3495 Paynet - Agregar campo NameOnAccount a la tabla transaccion\_tc

### **Mejora**

- PN-3304 Paynet - Transaccion\_Evento: Insertar el resultado de la notificacion de pago a los conectores
- PN-3459 CS General - Transaction Details By User: Restar transacciones Refund del total y no considerar los voids
- PN-3460 Configurar Layout para el cliente PREMIER INSURANCE

# **v6.5.13 - Jun. 24, 2024**

### **Error**

- PN-3470 Error de timeouts para libreria ProfitStars Common
- PN-3475 WebAPI - RefundToken: La transaccion ACH tipo refund no es insertada en transaccion\_tc
- PN-2811 CS- P2L - Al acceder a un lote descartado, la pantalla se muestra en blanco.
- PN-2826 CS General - Transaction Detail: El boton \[Resend Notification] se muestra si la transaccion tiene estatus Voided
- PN-3136 CS General - New Payment Plan: La descripcion del tipo de servicio no se actualiza al cambiar de servicio
- PN-3463 CS General – Edit Payment Plan: No cancela recurrencia
- PN-3468 CS General - Batch: No se elimina las fechas al momento de tocar el boton clear
- PN-3469 CS General - Batch: Estatus incorrectos en el filtro
- PN-3485 CS General - New Payment Plan: Los campos <Retry> y <Number> no estan siendo llenados al acceder en modo edit
- PN-3488 WSV5 - Los clientes se duplican al crear una acuerdo preautorizado

### **Mejora**

- PN-3484 CS General - New Payment Plan: Agregar campo <Numero de Plan> / <Plan Number>
- PN-3436 WebAPI - Refund / RefundToken: Aplicar flujo ApplyCredit para las transacciones ACH Profitstars
- PN-3486 CS General - New Payment Plan: Colocar PaymentType "Credit Card" como default en el campo

# **v6.5.12 - Jun. 5, 2024**

### **Error**

- PN-3035 customer service - General - Batch History: El dropdown merchat muestra todos los afiliados.
- PN-3037 customer service - General - TRANSACTIONAL REPORTS: Lo reportes por canales muestran un mensaje de error al exportar  a excel.
- PN-3038 customer service - General - SETTLEMENTS - Batch Details: Al acceder a la pantalla de detalle de un lote descartado esta se muestra en blanco.
- PN-3126 P2L/CS - Eliminar texto "Create Invoice?" del footer del modal de confirmacion
- PN-3150 CS General - Payment Plan: La recurrencia no es guardada con la tarjeta que digita el usuario en pantalla
- PN-3399 CS General - Transactional reportes: La exportacion PDF ocasiona un error al primer intento
- PN-3443 Backoffice - Localidad: La pantalla se queda cargando al tratar de acceder desde el resumen de onboarding
- PN-3445 Cuando se registra un token y se envia un nuevo registro no se actualiza la informacion de Zipcode y nombre
- PN-3448 WebPay - Boton BPD: Error en el flujo de pago y salida

### **Mejora**

- PN-3152 WebPay - Payment Page: Validar el formato de la fecha de expiracion
- PN-3462 Unificar metodos Refund y RefundToken con ApplyCredit y ApplyCreditToken

# **v6.5.11 - May. 23, 2024**

### **Historia**

- PN-3422 Backoffice - Transacciones: Mostrar transacciones de tipo consulta
- PN-3440 Paynet - Void de transacciones Pre-Auth: Capturar transaccion antes de aplicar el void

### **Error**

- PN-3373 WebPay - Graylog Logs: Todos los logs se estan registrando con el mismo RunId
- PN-3378 Problema que no controla cuando el resultado de 3DS es fallido

### **Nueva función**

- PN-3414 Paynet - Reembolso de transacciones por ID: Crear transaccion tipo refund al realizar un refund con transaccion previa

### **Mejora**

- PN-3292 Paynet - Transaccion\_evento: Insertar registro de void aplicado por error al notificar via el conector
- PN-3424 Poder definir una Imagen de logo por defecto para empresas que no tengan uno asignado
- PN-3460 Configurar Layout para el cliente PREMIER INSURANCE

# **v6.5.10 - May. 22, 2024**

### **Historia**

- PN-3338 Backoffice - Adquirente: Aumentar el MaxLength del campo Host\_IP hasta 150
- PN-3417 Backoffice - Onboarding Simple: Insertar parametros EmailFrom y EmailTemplate para las notificaciones
- PN-3418 Backoffice - Onboarding Simple - Insertar parametros de notificacion con el servicio Pay2Link

### **Error**

- PN-3148 CS General - Batch Details: Las anulaciones no estan siendo contabilizadas en el resumen
- PN-3149 CS General - Batch Details: Los estatus mostrados en el detalle no corresponden a los estatus de advanced search
- PN-3151 CS General - Virtual Terminal: No se toma el servicio seleccionado en pantalla para hacer la consulta de cliente
- PN-3289 CS General - Virtual Terminal: El boton \[Submit Payment] se deshabilita al modificar el customer number
- PN-3412 Backoffice - Transacciones: El filtro \<Empresa / Servicio> no carga filtrando por el Partner del usuario
- PN-3425 PAYNET API/WS - Refund de transacciones ach: Error con codigo 6

### **Change**

- PN-3287 Paynet - Registros de clientes: Los metodos Autorize solo deben reigstrar el nombre del cliente en tarjeta\_registrada

### **Mejora**

- PN-2881 CS General - Ajustar la pantalla de pago segun configuracion.
- PN-3181 Backoffice - Comercios Pay2Link: Enviar notificacion de cambio de password al registrar el comercio
- PN-3404 Backoffice - Onboarding: Agregar campo para subir logo de la empresa
- PN-3410 Backoffice - Onboarding Simple: Activar metodo de pago en Pay2Link segun el afiliado
- PN-3429 Paynet - Conector: Enviar notificacion al WebHook del cliente con el conector Paynet.GenericV2
- PN-3444 CS Triple S / CS Claro PR - Login: Parametrizar la expiracion de la cache que almacena la data de los usuarios

# **v6.5.9 - May. 2, 2024**

### **Error**

- PN-3306 CS General - Vaidacion de sesion: Pantalla de error al presionar cualquier boton de la aplicacion con la sesion del usuario vencida
- PN-3307 CS General - Vaidacion de sesion: Pantalla de error al intentar acceder a una pantalla por la URL sin haber iniciado sesion
- PN-3336 Backoffice - Onboarding: Las empresas se duplican si se recarga la pagina al finalizar el proceso
- PN-3340 ACollect - Ejecucion de acuerdo: El proceso esta agregando la palabra "Email" al campo Correo\_Electronico
- PN-3398 Backoffice - Recuperacion de password: El usuario no esta siendo redireccionado al Customer Services
- PN-3411 Backoffice - Onboarding Simple: El proceso de creacion duplica los parametros de notificacion si se utiliza una empresa existente

### **Nueva función**

- PN-3394 Backoffice - Onboarding Simple: Registrar dispositivo en Azure IoT

### **Mejora**

- PN-3383 Implementar uso de cola de emails desde Customer Service

# **v6.5.8 - May. 2, 2024**

### **Épica**

- PN-3135 Migrar las funcionalidades de seguridad de WSV5 a un nuevo API REST

### **Historia**

- PN-3318 Migrar el Controller Merchant de WebApi al BackEndApi
- PN-3334 CS General - Virtual Terminal: Enviar propiedad NameOnAccount hasta el WebAPI

### **Error**

- PN-2870 WSV5 - WSPaynet.asmx: Error Log4Net al enviar un CloseBatch y consumir otros metodos
- PN-2894 CS - Virtual Terminal - No se habilita el compo routing si se selecciona other.
- PN-3182 Backoffice - Comercios Pay2Link: La pantalla edit no esta mostrando los datos correctos.
- PN-3387 QA CS General - Forgot Password: Pantalla de error al realizar el flujo mas de una vez
- PN-3391 CS General - Add Invoice: Los attachments de las facturas no se pueden visualizar en el navegador
- PN-3393 CS General - Customer: La exportacion a excel se acciona con el boton \[Enter]
- PN-3396 CS Ajustes de idioma
- PN-3397 CS en pantalla de confirmacion de facturas quitar medios de pago no disponibles

### **Nueva función**

- PN-3227 Backoffice - Busqueda de opciones dentro de los filtros
- PN-3290 Paynet - Actualizacion para manejar campo IDRecolector en tabla Clientes
- PN-3395 Backoffice - Terminal/Canal: Agregar campos <Serial> y <Conexion Azure IoT>

### **Mejora**

- PN-3281 Backoffice - Onboarding Simple: Mejoras para la creacion de comercios
- PN-3305 Customer Services - Transactional Reports: Restar transacciones Refund del total y no considerar los voids
- PN-3377 WebAPI - Controller 6: Agregar metodo GetBiller
- PN-3390 CS General - Configuration: Reorganizacion de la interfaz de usuario

# **v6.5.7 - Apr. 18, 2024**

### **Error**

- PN-3255 WebPay - Payment BHD: WebPay envia el monto mas el indicador de la moneda hasta el endpoint BHD si al leer el culture del navegador, se le agrega un indicador de moneda la monto
- PN-3367 WSV5 - WSPaynetv1.asmx: No se esta incluyendo la fecha de expiracion en la validacion del hash

### **Subtarea**

- PN-2929 Verificación de validación 3DS, manejo de errores y registro de respuesta en autenticación aprobada.

### **Mejora**

- PN-3375 WebAPI - GetBalance PagaTodo: Llenar propiedades TotalAmount, MaxAmount y MinAmount
- PN-3376 WebAPI - Autorize: Leer Validador y Cobro\_id desde ExtData

# **v6.5.6 - Apr. 11, 2024**

### **Historia**

- PN-3363 CS General - Add Invoice: Mostrar metodos de pagos seleccionados por default

### **Error**

- PN-3015 customer service - General - En la pantalla New Payment Plan no funciona el boton clear form
- PN-3362 Backoffice - Edicion de usuarios: Al editar el campo Partner a "Todos" se dejan de visualizar los recolectores

### **Mejora**

- PN-3300 Backoffices - Recaudador: Resumen de comercio

# **v6.5.5 - Apr. 8, 2024**

### **Error**

- PN-3341 WebPay - PaymentPage: La pantalla esta enviando un valor incorrecto como monto si la pantalla esta en español

### **Historia**

- PN-3277 WSV5 - WSPaynetv1.asmx: Ajustar diferencia de referencias en el WSDL
- PN-3278 WSV5 - WSPaynetv2.asmx: Ajustar diferencia de referencias en el WSDL
- PN-3329 WebPay - PaymentPage: Permitir acceso a la pantalla de pago con un PayLoad que no tiene CustomerId
- PN-3333 WebPay - PaymentPage: Enviar propiedad NameOnAccount al WebAPI
- PN-3349 WebPay - Actualizacion de la descripcion de los bancos

### **Nueva función**

- PN-3319 nuevo parametro iframe\_target para hacer overrride del target cuando se usa IFRAME

### **Mejora**

- PN-3302 Paynet - Adquirentes: Mover endpoint de conexion a la tabla adquirentes
- PN-3320 Mapeo de respuestas bridgepay a codigos ISO-8583 mejorado
- PN-3328 WebAPI - Agregar parametro "NameOnAccount"
- PN-3348 Reordenar la lista de bancos de Webpay alfabeticamente, adicional colocar Oriental Bank en la primera posicion.

# **v6.5.4 - Mar 21, 2024**

### **Historia**

- PN-3323 Backoffice - Onboarding Simple: El campo <Seleccione Empresa> debe venir filtrado por el Partner
- PN-3337 Backoffice - Onboarding Simple: Registrar el comercio con el IDPartner del usuario creador

### **Error**

- PN-3230 Backoffice - Onboarding: Al presionar el boton \[Finish] mas de una vez, se duplica el comercio
- PN-3339 WebAPI - Autorize: El API valida la longitud del AccountNumber cuando es un pago en efectivo

### **Nueva función**

- PN-3224 Backoffice - Agregar nueva entidad Partner
- PN-3225 Backoffice - Usuario\_Rol: Configuracion de Partners
- PN-3273 Backoffice - Mantenimiento de perfiles de usuarios - filtro de Partner

### **Mejora**

- PN-3327 WebAPI - GetTransactionById: Agregar parametro <Invoice> al response del metodo

# **v6.5.3 - Mar 7, 2024**

### **Error**

- PN-2815 CS- P2L - En la pantalla Scheduled Payments se deben mostrar los estatus que están en el grid  en el filtro status.
- PN-2847 CS Triple S - Advanced Search: La exportacion a excel no retorna data
- PN-2848 CS Claro PR - Advanced Search: La exportacion excel no esta utilizando los filtros de la pantalla
- PN-3291 WebPay - Payment Page: El culture leido por el navegador modifica la moneda del monto
- PN-3295 CS General - Recurrent Agreement: El label <Channel> no se visualiza correctamente

### **Mejora**

- PN-3280 Backoffice - Modificar campos tipo select por un control que permita filtrar las opciones
- PN-3308 parametrizacion de TDPU y NII para transacciones AMEX

# **v6.5.2 - Feb 22, 2024**

### **Error**

- PN-3091 Cierre - Cuotas Cardnet: No se esta enviando el indicardor de cuotas cuando ocurre un BatchUpload
- PN-3282 Backoffice - Edit Clientes Pay2Link: Los campos tipo select no se llenan correctamente
- PN-3283 CS General - Login: La Propiedad IsAdmin no se asigna si el usuario tiene un solo comercio configurado

### **Mejora**

- PN-3226 Backoffice - Usuarios: Enviar notificacion de reset password al forzar cambio de password
- PN-3285 WebPay - Payment Page: Control en reintentos de pagos con validacion de IP

# **v6.5.1 - Feb 12, 2024**

### **Error**

- PN-3020 customer service - General - Pantallas Profile, Users y Users Details: Mensaje de error al acceder a las pantallas.
- PN-3021 customer service - General - Gray List: El boton clear no limpia los campos de fecha.
- PN-3147 CS General - Transaction Detail: El boton \[Resend Notification] se muestra si la transaccion esta anulada
- PN-3251 API - ApplyCredit: Mensaje de error Object reference not set to an instance of an object.
- PN-3258 CS General - AddInvoice: El grid con los pagos realizados se muestra al duplicar una factura
- PN-3262 SpeedPayWS - TripleS.asmx: El campo Numero\_Identificacion de la tabla clientes es afectado por los metodos InsertPayment, InsertRecurringSchedule y UpdateRecurringSchedule
- PN-3263 CS Triple S - Edit Recurrent Payment: No se esta enviando el Numero\_Identificacion del cliente hasta el WSV5
- PN-3269 Paynet WebAPI - Metodos Autorize: No se esta validando el valor del campo AccountType

### **Nueva función**

- PN-2912 CS GENERAL - Replicar clientes creados en Customer Services a la base de datos de Pay2Link

### **Mejora**

- PN-3216 Customer Services - Advanced Search: Mostrar descripcion de errores si falla la consulta
- PN-3264 CS Triple S - Create / Edit Recurrent Agreement: Ajustar envio de parametros Numero\_Identificacion y Codigo\_Cliente
- PN-3265 Paynet WebAPI - Autorize y AutorizeToken: Recibir el create\_user de la transaccion por ExtData

# **v6.5 - Dec 31, 2024**

### **Error**

- PN-2949 Backoffice - Roles: La pantalla edit no carga el check del campo "Publico/Privado"
- PN-3207 WebAPI - Incongruencias en el guardado de los datos en la tabla Clientes.
- PN-3208 WebAPI - AutorizeToken: El primer nombre del cliente es actualizado con el que fue registrado el token
- PN-3217 Customer Service - General - Virtual Terminal: Mensaje de error al realizar un pago duplicado (ACH-CC).
- PN-3218 Backoffice - Transsaciones: En el campo servivio se muestra el tipo de transaccion en lugar del servivio.
- PN-3220 Backoffice - Transsaciones: Si se selecciona un recaudador en especifico el campo localidad no muestra la opcion todos.
- PN-3233 WebAPI - Refund: El metodo Refund registra la tarjeta del cliente en el wallet
- PN-3239 WebAPI - Actualizacion de clientes: No se esta actualizando los campos TelCasa y Referencia

### **Change**

- PN-3234 Backoffices - Perfiles: Leer campo "Publico" de la tabla Roles, en lugar del campo "EsPublico"

### **Mejora**

- PN-3154 Cambio de mensajeria de SMS de triple S Propiedad a Twilio
- PN-3223 Backoffices - Transacciones: Dar espacio entre las columnas Localidad y Monto
- PN-3235 Back Office - Cambiar logo por el de agilpay.
- PN-3254 Mejora de parametros de envio de emails para Seguros Multiples

# **v6.4.8 - Dec 31, 2024**

### **Error**

- PN-3039 SpeedPayWS - TripleS.asmx: Error al intentar crear una recurrencia
- PN-3142 WebAPI - Notificacion a Pay2Link: Se esta enviando el numero de cuenta en claro, al notificar un pago ACH a P2L
- PN-3146 CS General - Virtual Terminal: El campo <First Name> carga con el nombre y el apellido del cliente
- PN-3176 CS General - Virtual Terminal: El modal de confirmacion muestra el mensaje "Approved" si la transaccion falla
- PN-3183 Customer Service - Pay2Link - Users: Los usuarios creados con credenciales de P2L no se estan registrando en la base de datos de pay2link.
- PN-3197 CS General - Virtual Terminal: Error al pagar con una cuenta ACH
- PN-3199 CS General - Virtual Terminal: No se esta enviando el valor digitado en el campo FirstName
- PN-3204 CS General - Pantallas presentan mensaje de error al ingresar
- PN-3206 CS General - Virtual Terminal: La data del cliente no se actualiza al pagar con una nueva tarjeta
- PN-3211 CS General - Advanced Search: Los headers de Advanced Search no contemplan el Tipo de transaccion
- PN-3212 CS General - Advanced Search: Al cambiar de canal el campo <Service> no se llena con un default
- PN-3213 CS General - Virtual Terminal: Error al pagar con AMEX guardando el metodo de pago como predeterminado
- PN-3214 CS General - Virtual Terminal: Las tarjetas amex guardadas no muestran el icono de la marca
- PN-3215 CS General - Virtual Terminal: La aplicacion guarda el metodo de pago sin que se haya seleccionado \[Save Wallet] al procesar una transaccion refund con tarjeta digitada manual
- PN-3221 WebAPI - No esta escribiendo los archivos logs
- PN-3231 P2L/CS - Cambiar nombre de "Invoice number" a Service
- PN-3237 P2L/CS - Mensaje de error al crear un usuario
- PN-3238 CS General - Reset Password: Las notificaciones de nuevo usuario y recuperacion de password no se estan enviando
- PN-3240 CS General - Virtual Terminal: El portal no esta enviando el telefono del cliente hasta el WebAPI de Paynet.
- PN-3241 CS General - Pay2Link: Los pagos parciales duplican la factura en la pantalla "Invoice"
- PN-3243 CS General - Virtual Terminal: Las notificaciones de pago no estan siendo enviadas
- PN-3244 CS - P2L - Botón de reset no está habilitando
- PN-3246 CS - P2L - Mensaje de path no encontrado al intentar generar un reporte
- PN-3250 P2L - Customer Service: Las facturas se muestran vencidas al dia siguente de ser creadas
- PN-3257 CS General - Virtual Terminal: Errores ortograficos y de espacios
- PN-3261 CS - General - USERS MANAGEMENT: Al intentar eliminar el usuario en muestra el mensaje de exito pero no elimina el usuario y cambia el recolector.

### **Historia**

- PN-2687 CS General - Security: Validar si el password del usuario esta expirado al acceder a las pantallas.
- PN-3169 CS General - Transaction Detail: Mostrar el modal capture payment con el monto original de la transaccion
- PN-3170 CS General - Mostrar Label "Refund" o "Pre-Auth" en el modal Review
- PN-3178 CS General - Advanced Search: Ocultar botones \[Void], \[Refund] y \[Resend Notification] si la transaccion es tipo Refund
- PN-3179 CS General - Transaction Detail: Ocultar botones \[Void], \[Refund], \[Capture] y \[Resend Notification] si la transaccion es tipo Refund
- PN-3180 CS General - Virtual Terminal: Enviar el customerid hasta el nuget del WebAPI al utilizar AutorizeToken
- PN-3229 CS General - Virtual Terminal: Eliminar campo <Middle Name>
- PN-3242 CS General - Virtal Terminal: Ajustar perdida del branch PN-2971 en la version v6.4.8

### **Mejora**

- PN-3109 Agregar un radio button que permita realizar Sales, Pre-Auth y Refund
- PN-3110 Implementar las funcionalidades de sales
- PN-3111 Implementar las funcionalidades de Pre-Auth y Capture
- PN-3112 Implementar la funcionalidad Repetir transacciones
- PN-3177 CS General - Virtual Terminal: Utilizar el metodo RegisterToken para guardar los wallets
- PN-3200 ApaymentWeb: Agregar la opción de buscar transacciones por empresa y filtrar la localidad deseada
- PN-3201 ApaymentWeb: Agregar la opción de buscar por número de autorización
- PN-3202 Apayment:  mejorar formato archivo Excel
- PN-3205 ApaymenWS - WSV5: Configurar los metodos Process\_Sale, Process\_Sale2 y AutorizeToken para que registren el usuario que realiza la trasaccion.

# **v6.4.7 - Dec 14, 2023**

### **Épica**

- PN-2989 CS General - Payment History: Adecuaciones

### **Historia**

- PN-2704 Poner a funcionar el modulo de seguridad de Customer Services General
- PN-2990 CS General - Payment History: Modificar el estilo del grid para que sea igual a Advanced Search
- PN-2991 CS General - Payment History: Agregar comportamiento fail/success al proceso de notifiacion
- PN-3140 CS General - Virtual Terminal: Retoques UI al panel de los metodos de pago

### **Error**

- PN-3022 WSV5 - ConsultaHistorico - No muestra las transacciones que se realizaron enviando el campo ivoice por el CS.
- PN-3161 Paynet - Transacciones PreAuth: Las transacciones PreAuth se guardan con estatus 57 en transacciones\_canal

### **Change**

- PN-3143 Paynet - Notificacion de pago al endpoint del cliente Pay2Link

### **Nueva función**

- PN-3144 Crear un proceso de Cierre similar a CloseBatchResumen que permita cerrar por Terminal.

### **Mejora**

- PN-2992 CS General - Payment History: Mostrar load mientras la pantalla procesa la carga de la data
- PN-3108 Bajar el selector de canal a la pantalla de virtual terminal como dropdown
- PN-3141 WSV5 - ConsultaHistorico: Agregar el parametro: Numero\_Factura
- PN-3156 Modificar el metodo de Crear Refund de Paynet para que envie Tipo de Transaccion "Refund"

# **v6.4.6 - Nov 20, 2023**

### **Error**

- PN-2773 PaynetWS11 VisaNet - AplicaPago: Las transacciones MTT no registran el monto y el porciento aplicado al total de la transaccion en la tabla transaccion\_servicio
- PN-2543 Customer Service - General - Al exportar a Excel el campo email se está guardando el idTransaccion.
- PN-2682 WebApi - Recurring Controller: El metodo Update deja el campo Tipo\_Producto igual a null
- PN-2760 CS- General - Virtual Terminal: La pantalla se queda loading al consultar un account number sin ingresarlo en el campo
- PN-2871 API - CloseBatchResumen - No esta ejecutando el cierre
- PN-2873 WebPay - No esta funcionando el redireccionamiento de Pay2Link
- PN-2882 WebAPI- Validar que la fecha de expiración no está vencida cuando se envían 4 dígitos.
- PN-3087 customer service - General - New Payment Plan: El mensaje de la fecha se muestra antes de terminar de insertar la fecha cuando se coloca el tipo de ejecución como until.
- PN-3105 customer service - General - New User: Al crear un usuario no se esta guardando el email en el campo email de la tabla usuario.
- PN-3131 CS General - Add Services P2L: Los servicios se estan registrando con el create\_user egarcia  hardcoded
- PN-3162 CS General - Virtual Terminal: El campo <Service> muestra servicios que no tienen acceso a la pantalla

### **Historia**

- PN-2183 Agregar funcionalidades de Validacion Monto Secreto en PayNet
- PN-2857 Crear privilegios para la pantalla de cierre y la ejecución de este desde el customer services.
- PN-2939 WebApi - Merchant: Agregar propiedad RequireTokenCVV al response del metodo GetMerchant
- PN-2973 CS General - Virtual Terminal: Eliminar label "Mailing Address"
- PN-2974 CS General - Virtual Terminal: Mover cambio de canal a un DropDown
- PN-2977 CS General - Virtual Terminal: Agregar mascara e icono de tarjetas al campo Credit Card Number
- PN-2978 CS General - Virtual Terminal: Normalizar tipo de letras para los campos de metodos de pago
- PN-2979 CS General - Virtual Terminal: Colocar los campos <Name Of Account> y <Zip Code> en una sola linea

### **Nueva función**

- PN-2938 WebAPI - AutorizeToken: Recibir CVV como parametro opcional
- PN-2940 WebPay - Pantalla de pago: Validar parametro RequireTokenCVV
- PN-3157 Crear metodos de Agregar, Editar y Remover Clientes que consuman los metodos de PayNet para estas funciones.

### **Mejora**

- PN-2972 CS General - Virtual Terminal: La descripcion del customer number depende del servicio
- PN-2975 CS General - Virtual Terminal: Agregar scroll al panel de los metodos de pago si el listado es largo
- PN-2976 CS General - Virtual Terminal: Modificar radiobuttons de los metodos de pagos por checkboxs
- PN-3132 Paynet - Conector Paynet.Generic: Implementar notificacion de pago de factura al endpoint del cliente

# **v6.4.2 - Sept 8, 2023**

### **Historia**

- PN-2877 Customer Service - Consultar los canales y servicios disponibles para cargar los campos
- PN-2886 Customer Service - Menu Principal: Reorganizar secciones
- PN-2935 Archivos NACHA - Oriental Bank: Modificación de archivos para la cuenta de la nueva implementación
- PN-3033 Customer Service - Validación de privilegios: Validar acceso a las pantallas por recolector
- PN-2740 Customer Service - Crear una opción para poder consultar, crear, editar y eliminar usuarios
- PN-2741 Customer Service - Replicar usuarios creados en customer service en pay2link
- PN-2743 Customer Service - Crear funcionalidad para recuperación de contraseña

### **Improvement**

- PN-2739 Mejoras modulo seguridad Customer Service, funcionalidades de pay2link
- PN-2852 Customer Service - Change Password: Cerrar la sesión del usuario luego de cambiar el password
- PN-2866 Customer Service - Agregar botón de back to list en las pantallas New User y Edit User
- PN-2999 Customer Service - Pay2Link Configuration: Agregar campos State, City, Zip Code, Address 2
- PN-3036 Customer Service - Virtual Terminal: El canal seleccionado por default debe ser uno de los canales que tengan acceso a la pantalla.

<br />