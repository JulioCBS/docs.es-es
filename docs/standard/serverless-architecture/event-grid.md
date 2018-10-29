---
title: Azure Event Grid - aplicaciones sin servidor
description: Azure Event Grid es una solución sin servidor para la entrega de eventos confiable y el enrutamiento a gran escala en un modelo de pago por evento.
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: b2507da61cbea3b4bdc51c6eecfe4d784737e924
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/03/2018
ms.locfileid: "49370209"
---
# <a name="event-grid"></a><span data-ttu-id="549f8-103">Cuadrícula de eventos</span><span class="sxs-lookup"><span data-stu-id="549f8-103">Event Grid</span></span>

<span data-ttu-id="549f8-104">[Azure Event Grid](/azure-event-grid/overview) proporciona infraestructura sin servidor para las aplicaciones basadas en eventos.</span><span class="sxs-lookup"><span data-stu-id="549f8-104">[Azure Event Grid](/azure-event-grid/overview) provides serverless infrastructure for event-based applications.</span></span> <span data-ttu-id="549f8-105">Puede publicar en Event Grid desde cualquier origen y consumir mensajes desde cualquier plataforma.</span><span class="sxs-lookup"><span data-stu-id="549f8-105">You can publish to Event Grid from any source and consume messages from any platform.</span></span> <span data-ttu-id="549f8-106">Event Grid también tiene compatibilidad integrada para eventos de recursos de Azure para simplificar la integración con sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="549f8-106">Event Grid also has built-in support for events from Azure resources to streamline integration with your applications.</span></span> <span data-ttu-id="549f8-107">Por ejemplo, puede suscribirse a eventos para notificar a la aplicación cuando se carga un archivo de blob storage.</span><span class="sxs-lookup"><span data-stu-id="549f8-107">For example, you can subscribe to blob storage events to notify your app when a file is uploaded.</span></span> <span data-ttu-id="549f8-108">La aplicación, a continuación, puede publicar un mensaje de cuadrícula de eventos personalizados que se consume en otra nube o aplicaciones locales.</span><span class="sxs-lookup"><span data-stu-id="549f8-108">Your application can then publish a custom event grid message that is consumed by other cloud or on-premises applications.</span></span> <span data-ttu-id="549f8-109">Event Grid se creó para controlar de forma confiable escala masiva.</span><span class="sxs-lookup"><span data-stu-id="549f8-109">Event Grid was built to reliably handle massive scale.</span></span> <span data-ttu-id="549f8-110">Obtenga las ventajas de publicar y suscribirse a mensajes sin la sobrecarga de configurar la infraestructura necesaria.</span><span class="sxs-lookup"><span data-stu-id="549f8-110">You get the benefits of publishing and subscribing to messages without the overhead of setting up the necessary infrastructure.</span></span>

![Logotipo de la cuadrícula de eventos](./media/event-grid-logo.png)

<span data-ttu-id="549f8-112">Las principales características de event grid incluyen:</span><span class="sxs-lookup"><span data-stu-id="549f8-112">The major features of event grid include:</span></span>

* <span data-ttu-id="549f8-113">Enrutamiento de eventos totalmente administrado.</span><span class="sxs-lookup"><span data-stu-id="549f8-113">Fully managed event routing.</span></span>
* <span data-ttu-id="549f8-114">Cerca de la entrega de eventos en tiempo real a escala.</span><span class="sxs-lookup"><span data-stu-id="549f8-114">Near real-time event delivery at scale.</span></span>
* <span data-ttu-id="549f8-115">Amplia cobertura tanto dentro como fuera de Azure.</span><span class="sxs-lookup"><span data-stu-id="549f8-115">Broad coverage both inside and outside of Azure.</span></span>

## <a name="scenarios"></a><span data-ttu-id="549f8-116">Escenarios</span><span class="sxs-lookup"><span data-stu-id="549f8-116">Scenarios</span></span>

<span data-ttu-id="549f8-117">Event Grid aborda varios escenarios diferentes.</span><span class="sxs-lookup"><span data-stu-id="549f8-117">Event Grid addresses several different scenarios.</span></span> <span data-ttu-id="549f8-118">En esta sección se trata tres de las más comunes.</span><span class="sxs-lookup"><span data-stu-id="549f8-118">This section covers three of the most common ones.</span></span>

### <a name="ops-automation"></a><span data-ttu-id="549f8-119">Automatización de operaciones</span><span class="sxs-lookup"><span data-stu-id="549f8-119">Ops automation</span></span>

![Automatización de operaciones](./media/ops-automation.png)

<span data-ttu-id="549f8-121">Event Grid puede ayudar a la automatización de la velocidad y simplificar el cumplimiento de directivas mediante la notificación a [Azure Automation](https://docs.microsoft.com/azure/automation) cuando se aprovisiona la infraestructura.</span><span class="sxs-lookup"><span data-stu-id="549f8-121">Event Grid can help speed automation and simplify policy enforcement by notifying [Azure Automation](https://docs.microsoft.com/azure/automation) when infrastructure is provisioned.</span></span>

### <a name="application-integration"></a><span data-ttu-id="549f8-122">Integración de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="549f8-122">Application integration</span></span>

![Integración de aplicaciones](./media/app-integration.png)

<span data-ttu-id="549f8-124">Puede usar Event Grid para conectar la aplicación a otros servicios.</span><span class="sxs-lookup"><span data-stu-id="549f8-124">You can use Event Grid to connect your app to other services.</span></span> <span data-ttu-id="549f8-125">Mediante los protocolos HTTP estándar, las aplicaciones heredadas incluso pueden modificarse fácilmente para publicar mensajes de Event Grid.</span><span class="sxs-lookup"><span data-stu-id="549f8-125">Using standard HTTP protocols, even legacy apps can be easily modified to publish Event Grid messages.</span></span> <span data-ttu-id="549f8-126">Enlaces Web están disponibles para otros servicios y plataformas para consumir mensajes de Event Grid.</span><span class="sxs-lookup"><span data-stu-id="549f8-126">Web hooks are available for other services and platforms to consume Event Grid messages.</span></span>

### <a name="serverless-apps"></a><span data-ttu-id="549f8-127">Aplicaciones sin servidor</span><span class="sxs-lookup"><span data-stu-id="549f8-127">Serverless apps</span></span>

![Aplicaciones sin servidor](./media/serverless-apps.png)

<span data-ttu-id="549f8-129">Event Grid puede desencadenarse Azure Functions, Logic Apps o su propio código personalizado.</span><span class="sxs-lookup"><span data-stu-id="549f8-129">Event Grid can trigger Azure Functions, Logic Apps, or your own custom code.</span></span> <span data-ttu-id="549f8-130">Una ventaja importante del uso de Event Grid es que usa un *inserción* mecanismo para enviar mensajes cuando se producen eventos.</span><span class="sxs-lookup"><span data-stu-id="549f8-130">A major benefit of using Event Grid is that it uses a *push* mechanism to send messages when events occur.</span></span> <span data-ttu-id="549f8-131">La arquitectura de inserción consume menos recursos y se escala mejor que *sondeo* mecanismos.</span><span class="sxs-lookup"><span data-stu-id="549f8-131">The push architecture consumes fewer resources and scales better than *polling* mechanisms.</span></span> <span data-ttu-id="549f8-132">Sondeo debe comprobar si las actualizaciones de manera periódica.</span><span class="sxs-lookup"><span data-stu-id="549f8-132">Polling must check for updates on a regular interval.</span></span>

## <a name="event-grid-vs-other-azure-messaging-services"></a><span data-ttu-id="549f8-133">Cuadrícula de eventos frente a otros servicios de mensajes de Azure</span><span class="sxs-lookup"><span data-stu-id="549f8-133">Event Grid vs. other Azure messaging services</span></span>

<span data-ttu-id="549f8-134">Azure proporciona varios servicios de mensajes, como [Event Hubs](https://docs.microsoft.com/azure/event-hubs) y [Service Bus](https://docs.microsoft.com/azure/service-bus-messaging).</span><span class="sxs-lookup"><span data-stu-id="549f8-134">Azure provides several messaging services, including [Event Hubs](https://docs.microsoft.com/azure/event-hubs) and [Service Bus](https://docs.microsoft.com/azure/service-bus-messaging).</span></span> <span data-ttu-id="549f8-135">Cada uno está diseñado para abordar un conjunto específico de casos de uso.</span><span class="sxs-lookup"><span data-stu-id="549f8-135">Each is designed to address a specific set of use cases.</span></span> <span data-ttu-id="549f8-136">El diagrama siguiente proporciona una descripción general de las diferencias entre los servicios.</span><span class="sxs-lookup"><span data-stu-id="549f8-136">The following diagram provides a high-level overview of the differences between the services.</span></span>

![Comparación de mensajería de Azure](./media/azure-messaging-services.png)

<span data-ttu-id="549f8-138">Para obtener una comparación más detallada, consulte [Compare los servicios de mensajes](https://docs.microsoft.com/azure/event-grid/compare-messaging-services).</span><span class="sxs-lookup"><span data-stu-id="549f8-138">For a more in-depth comparison, see [Compare messaging services](https://docs.microsoft.com/azure/event-grid/compare-messaging-services).</span></span>

## <a name="performance-targets"></a><span data-ttu-id="549f8-139">Objetivos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="549f8-139">Performance targets</span></span>

<span data-ttu-id="549f8-140">Con Event Grid puede sacar partido del rendimiento de las siguiente garantías:</span><span class="sxs-lookup"><span data-stu-id="549f8-140">Using Event Grid you can take advantage of the following performance guarantees:</span></span>

* <span data-ttu-id="549f8-141">Latencia de extremo a otro en el percentil 99 de subsegundos.</span><span class="sxs-lookup"><span data-stu-id="549f8-141">Subsecond end-to-end latency in the 99th percentile.</span></span>
* <span data-ttu-id="549f8-142">disponibilidad del 99,99%.</span><span class="sxs-lookup"><span data-stu-id="549f8-142">99.99% availability.</span></span>
* <span data-ttu-id="549f8-143">10 millones de eventos por segundo por región.</span><span class="sxs-lookup"><span data-stu-id="549f8-143">10 million events per second per region.</span></span>
* <span data-ttu-id="549f8-144">suscripciones de 100 millones por región.</span><span class="sxs-lookup"><span data-stu-id="549f8-144">100 million subscriptions per region.</span></span>
* <span data-ttu-id="549f8-145">latencia de 50 ms. publisher.</span><span class="sxs-lookup"><span data-stu-id="549f8-145">50-ms publisher latency.</span></span>
* <span data-ttu-id="549f8-146">24 horas de reintento con retroceso exponencial para garantizar la entrega en la ventana de 1 día.</span><span class="sxs-lookup"><span data-stu-id="549f8-146">24-hour retry with exponential back-off for guaranteed delivery in the 1-day window.</span></span>
* <span data-ttu-id="549f8-147">Conmutación por error regional transparente.</span><span class="sxs-lookup"><span data-stu-id="549f8-147">Transparent regional failover.</span></span>

## <a name="event-grid-schema"></a><span data-ttu-id="549f8-148">Esquema de Event Grid</span><span class="sxs-lookup"><span data-stu-id="549f8-148">Event Grid schema</span></span>

<span data-ttu-id="549f8-149">Event Grid usa un esquema estándar para encapsular los eventos personalizados.</span><span class="sxs-lookup"><span data-stu-id="549f8-149">Event Grid uses a standard schema to wrap custom events.</span></span> <span data-ttu-id="549f8-150">El esquema es como un envolvente que contiene el elemento de datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="549f8-150">The schema is like an envelope that wraps your custom data element.</span></span> <span data-ttu-id="549f8-151">Este es un mensaje de Event Grid de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="549f8-151">Here is an example Event Grid message:</span></span>

```json
[{
    "id": "03e24f21-a955-43cc-8921-1f61a6081ce0",
    "eventType": "myCustomEvent",
    "subject": "foo/bar/12",
    "eventTime": "2018-09-22T10:36:01+00:00",
    "data": {
        "favoriteColor": "blue",
        "favoriteAnimal": "panther",
        "favoritePlanet": "Jupiter"
    },
    "dataVersion": "1.0"
}]
```

<span data-ttu-id="549f8-152">Todo lo relacionado con el mensaje es estándar, excepto el `data` propiedad.</span><span class="sxs-lookup"><span data-stu-id="549f8-152">Everything about the message is standard except the `data` property.</span></span> <span data-ttu-id="549f8-153">Puede inspeccionar el mensaje y utilizar el `eventType` y `dataVersion` para deserializar la parte de la carga personalizada.</span><span class="sxs-lookup"><span data-stu-id="549f8-153">You can inspect the message and use the `eventType` and `dataVersion` to de-serialize the custom portion of the payload.</span></span>

## <a name="azure-resources"></a><span data-ttu-id="549f8-154">recursos de Azure</span><span class="sxs-lookup"><span data-stu-id="549f8-154">Azure resources</span></span>

<span data-ttu-id="549f8-155">Una ventaja importante del uso de Event Grid es los mensajes automática generados por Azure.</span><span class="sxs-lookup"><span data-stu-id="549f8-155">A major benefit of using Event Grid is the automatic messages produced by Azure.</span></span> <span data-ttu-id="549f8-156">En Azure, recursos publican automáticamente en un *tema* que le permite suscribirse para varios eventos.</span><span class="sxs-lookup"><span data-stu-id="549f8-156">In Azure, resources automatically publish to a *topic* that allows you to subscribe for various events.</span></span> <span data-ttu-id="549f8-157">En la tabla siguiente se enumera los tipos de recursos, tipos de mensajes y eventos que están disponibles automáticamente.</span><span class="sxs-lookup"><span data-stu-id="549f8-157">The following table lists the resource types, message types, and events that are available automatically.</span></span>

| <span data-ttu-id="549f8-158">Recursos de Azure</span><span class="sxs-lookup"><span data-stu-id="549f8-158">Azure resource</span></span> | <span data-ttu-id="549f8-159">Tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="549f8-159">Event type</span></span> | <span data-ttu-id="549f8-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="549f8-160">Description</span></span> |
| -------------- | ---------- | ----------- |
| <span data-ttu-id="549f8-161">Suscripción a Azure</span><span class="sxs-lookup"><span data-stu-id="549f8-161">Azure subscription</span></span> | <span data-ttu-id="549f8-162">Microsoft.Resources.ResourceWriteSuccess</span><span class="sxs-lookup"><span data-stu-id="549f8-162">Microsoft.Resources.ResourceWriteSuccess</span></span> | <span data-ttu-id="549f8-163">Se genera cuando un recurso se crea o la operación de actualización se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="549f8-163">Raised when a resource create or update operation succeeds.</span></span> |
| | <span data-ttu-id="549f8-164">Microsoft.Resources.ResourceWriteFailure</span><span class="sxs-lookup"><span data-stu-id="549f8-164">Microsoft.Resources.ResourceWriteFailure</span></span> | <span data-ttu-id="549f8-165">Se genera al crear un recurso o se produce un error en la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="549f8-165">Raised when a resource create or update operation fails.</span></span> |
| | <span data-ttu-id="549f8-166">Microsoft.Resources.ResourceWriteCancel</span><span class="sxs-lookup"><span data-stu-id="549f8-166">Microsoft.Resources.ResourceWriteCancel</span></span> | <span data-ttu-id="549f8-167">Se genera cuando un recurso crear o actualizar la operación se cancela.</span><span class="sxs-lookup"><span data-stu-id="549f8-167">Raised when a resource create or update operation is canceled.</span></span> |
|  | <span data-ttu-id="549f8-168">Microsoft.Resources.ResourceDeleteSuccess</span><span class="sxs-lookup"><span data-stu-id="549f8-168">Microsoft.Resources.ResourceDeleteSuccess</span></span> | <span data-ttu-id="549f8-169">Se genera cuando se realiza correctamente una operación de eliminación de recursos.</span><span class="sxs-lookup"><span data-stu-id="549f8-169">Raised when a resource delete operation succeeds.</span></span> |
|  | <span data-ttu-id="549f8-170">Microsoft.Resources.ResourceDeleteFailure</span><span class="sxs-lookup"><span data-stu-id="549f8-170">Microsoft.Resources.ResourceDeleteFailure</span></span> | <span data-ttu-id="549f8-171">Se genera cuando se produce un error en una operación de eliminación de recursos.</span><span class="sxs-lookup"><span data-stu-id="549f8-171">Raised when a resource delete operation fails.</span></span> |
| | <span data-ttu-id="549f8-172">Microsoft.Resources.ResourceDeleteCancel</span><span class="sxs-lookup"><span data-stu-id="549f8-172">Microsoft.Resources.ResourceDeleteCancel</span></span> | <span data-ttu-id="549f8-173">Se genera cuando se cancela una operación de eliminación de recursos.</span><span class="sxs-lookup"><span data-stu-id="549f8-173">Raised when a resource delete operation is canceled.</span></span> <span data-ttu-id="549f8-174">Este evento se produce cuando se cancela una implementación de plantilla.</span><span class="sxs-lookup"><span data-stu-id="549f8-174">This event happens when a template deployment is canceled.</span></span> |
| <span data-ttu-id="549f8-175">Almacenamiento de blobs</span><span class="sxs-lookup"><span data-stu-id="549f8-175">Blob storage</span></span> | <span data-ttu-id="549f8-176">Microsoft.Storage.BlobCreated</span><span class="sxs-lookup"><span data-stu-id="549f8-176">Microsoft.Storage.BlobCreated</span></span> | <span data-ttu-id="549f8-177">Se genera cuando se crea un blob.</span><span class="sxs-lookup"><span data-stu-id="549f8-177">Raised when a blob is created.</span></span> |
| | <span data-ttu-id="549f8-178">Microsoft.Storage.BlobDeleted</span><span class="sxs-lookup"><span data-stu-id="549f8-178">Microsoft.Storage.BlobDeleted</span></span> | <span data-ttu-id="549f8-179">Se genera cuando se elimina un blob.</span><span class="sxs-lookup"><span data-stu-id="549f8-179">Raised when a blob is deleted.</span></span> |
| <span data-ttu-id="549f8-180">Centros de eventos</span><span class="sxs-lookup"><span data-stu-id="549f8-180">Event hubs</span></span> | <span data-ttu-id="549f8-181">Microsoft.EventHub.CaptureFileCreated</span><span class="sxs-lookup"><span data-stu-id="549f8-181">Microsoft.EventHub.CaptureFileCreated</span></span> | <span data-ttu-id="549f8-182">Se genera cuando se crea un archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="549f8-182">Raised when a capture file is created.</span></span>
| <span data-ttu-id="549f8-183">Centro de IoT</span><span class="sxs-lookup"><span data-stu-id="549f8-183">IoT Hub</span></span> | <span data-ttu-id="549f8-184">Microsoft.Devices.DeviceCreated</span><span class="sxs-lookup"><span data-stu-id="549f8-184">Microsoft.Devices.DeviceCreated</span></span> | <span data-ttu-id="549f8-185">Se publica cuando se registra un dispositivo a IoT hub.</span><span class="sxs-lookup"><span data-stu-id="549f8-185">Published when a device is registered to an IoT hub.</span></span> |
| | <span data-ttu-id="549f8-186">Microsoft.Devices.DeviceDeleted</span><span class="sxs-lookup"><span data-stu-id="549f8-186">Microsoft.Devices.DeviceDeleted</span></span> | <span data-ttu-id="549f8-187">Se publica cuando se elimina un dispositivo de IoT hub.</span><span class="sxs-lookup"><span data-stu-id="549f8-187">Published when a device is deleted from an IoT hub.</span></span> |
| <span data-ttu-id="549f8-188">Grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="549f8-188">Resource groups</span></span> | <span data-ttu-id="549f8-189">Microsoft.Resources.ResourceWriteSuccess</span><span class="sxs-lookup"><span data-stu-id="549f8-189">Microsoft.Resources.ResourceWriteSuccess</span></span> | <span data-ttu-id="549f8-190">Se genera cuando un recurso se crea o la operación de actualización se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="549f8-190">Raised when a resource create or update operation succeeds.</span></span> |
| | <span data-ttu-id="549f8-191">Microsoft.Resources.ResourceWriteFailure</span><span class="sxs-lookup"><span data-stu-id="549f8-191">Microsoft.Resources.ResourceWriteFailure</span></span> | <span data-ttu-id="549f8-192">Se genera al crear un recurso o se produce un error en la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="549f8-192">Raised when a resource create or update operation fails.</span></span> |
| | <span data-ttu-id="549f8-193">Microsoft.Resources.ResourceWriteCancel</span><span class="sxs-lookup"><span data-stu-id="549f8-193">Microsoft.Resources.ResourceWriteCancel</span></span> | <span data-ttu-id="549f8-194">Se genera cuando un recurso crear o actualizar la operación se cancela.</span><span class="sxs-lookup"><span data-stu-id="549f8-194">Raised when a resource create or update operation is canceled.</span></span> |
| | <span data-ttu-id="549f8-195">Microsoft.Resources.ResourceDeleteSuccess</span><span class="sxs-lookup"><span data-stu-id="549f8-195">Microsoft.Resources.ResourceDeleteSuccess</span></span> | <span data-ttu-id="549f8-196">Se genera cuando se realiza correctamente una operación de eliminación de recursos.</span><span class="sxs-lookup"><span data-stu-id="549f8-196">Raised when a resource delete operation succeeds.</span></span> |
| | <span data-ttu-id="549f8-197">Microsoft.Resources.ResourceDeleteFailure</span><span class="sxs-lookup"><span data-stu-id="549f8-197">Microsoft.Resources.ResourceDeleteFailure</span></span> | <span data-ttu-id="549f8-198">Se genera cuando se produce un error en una operación de eliminación de recursos.</span><span class="sxs-lookup"><span data-stu-id="549f8-198">Raised when a resource delete operation fails.</span></span> |
| | <span data-ttu-id="549f8-199">Microsoft.Resources.ResourceDeleteCancel</span><span class="sxs-lookup"><span data-stu-id="549f8-199">Microsoft.Resources.ResourceDeleteCancel</span></span> | <span data-ttu-id="549f8-200">Se genera cuando se cancela una operación de eliminación de recursos.</span><span class="sxs-lookup"><span data-stu-id="549f8-200">Raised when a resource delete operation is canceled.</span></span> <span data-ttu-id="549f8-201">Este evento se produce cuando se cancela una implementación de plantilla.</span><span class="sxs-lookup"><span data-stu-id="549f8-201">This event happens when a template deployment is canceled.</span></span> |

<span data-ttu-id="549f8-202">Para obtener más información, consulte [esquema de eventos de Azure Event Grid](https://docs.microsoft.com/azure/event-grid/event-schema).</span><span class="sxs-lookup"><span data-stu-id="549f8-202">For more information, see [Azure Event Grid event schema](https://docs.microsoft.com/azure/event-grid/event-schema).</span></span>

<span data-ttu-id="549f8-203">Event Grid puede tener acceso desde cualquier tipo de aplicación, incluso uno que se ejecuta en el entorno local.</span><span class="sxs-lookup"><span data-stu-id="549f8-203">You can access Event Grid from any type of application, even one that runs on-premises.</span></span>

## <a name="conclusion"></a><span data-ttu-id="549f8-204">Conclusión</span><span class="sxs-lookup"><span data-stu-id="549f8-204">Conclusion</span></span>

<span data-ttu-id="549f8-205">En este capítulo, aprendió sobre la plataforma Azure sin servidor que se compone de Azure Functions, Logic Apps y Event Grid.</span><span class="sxs-lookup"><span data-stu-id="549f8-205">In this chapter you learned about the Azure serverless platform that is composed of Azure Functions, Logic Apps, and Event Grid.</span></span> <span data-ttu-id="549f8-206">Puede usar estos recursos para crear una arquitectura de aplicación sin servidor completamente, o crear una solución híbrida que interactúa con otros recursos de nube y servidores locales.</span><span class="sxs-lookup"><span data-stu-id="549f8-206">You can use these resources to build an entirely serverless app architecture, or create a hybrid solution that interacts with other cloud resources and on-premises servers.</span></span> <span data-ttu-id="549f8-207">Combinado con una plataforma de datos sin servidor, como [SQL Azure](https://docs.microsoft.com/azure/sql-database) o [CosmosDB](https://docs.microsoft.com/azure/cosmos-db/introduction), puede compilar aplicaciones nativas en la nube totalmente administrado.</span><span class="sxs-lookup"><span data-stu-id="549f8-207">Combined with a serverless data platform such as [Azure SQL](https://docs.microsoft.com/azure/sql-database) or [CosmosDB](https://docs.microsoft.com/azure/cosmos-db/introduction), you can build fully managed cloud native applications.</span></span>

## <a name="recommended-resources"></a><span data-ttu-id="549f8-208">Recursos recomendados</span><span class="sxs-lookup"><span data-stu-id="549f8-208">Recommended resources</span></span>

* [<span data-ttu-id="549f8-209">Planes de App service</span><span class="sxs-lookup"><span data-stu-id="549f8-209">App service plans</span></span>](https://docs.microsoft.com/azure/app-service/azure-web-sites-web-hosting-plans-in-depth-overview)
* [<span data-ttu-id="549f8-210">Application Insights</span><span class="sxs-lookup"><span data-stu-id="549f8-210">Application Insights</span></span>](https://docs.microsoft.com/azure/application-insights)
* [<span data-ttu-id="549f8-211">Análisis de Application Insights</span><span class="sxs-lookup"><span data-stu-id="549f8-211">Application Insights Analytics</span></span>](https://docs.microsoft.com/azure/application-insights/app-insights-analytics)
* [<span data-ttu-id="549f8-212">Azure: Traiga su aplicación a la nube con Azure Functions sin servidor</span><span class="sxs-lookup"><span data-stu-id="549f8-212">Azure: Bring your app to the cloud with serverless Azure Functions</span></span>](https://channel9.msdn.com/events/Connect/2017/E102)
* [<span data-ttu-id="549f8-213">Azure Event Grid</span><span class="sxs-lookup"><span data-stu-id="549f8-213">Azure Event Grid</span></span>](https://docs.microsoft.com/azure/azure-event-grid/overview)
* [<span data-ttu-id="549f8-214">Esquema de eventos de Azure Event Grid</span><span class="sxs-lookup"><span data-stu-id="549f8-214">Azure Event Grid event schema</span></span>](https://docs.microsoft.com/azure/event-grid/event-schema)
* [<span data-ttu-id="549f8-215">Azure Event Hubs</span><span class="sxs-lookup"><span data-stu-id="549f8-215">Azure Event Hubs</span></span>](https://docs.microsoft.com/azure/event-hubs)
* [<span data-ttu-id="549f8-216">Documentación de Azure Functions</span><span class="sxs-lookup"><span data-stu-id="549f8-216">Azure Functions documentation</span></span>](https://docs.microsoft.com/azure/azure-functions)
* [<span data-ttu-id="549f8-217">Conceptos de enlaces y desencadenadores de Azure Functions</span><span class="sxs-lookup"><span data-stu-id="549f8-217">Azure Functions triggers and bindings concepts</span></span>](https://docs.microsoft.com/azure/azure-functions/functions-triggers-bindings)
* [<span data-ttu-id="549f8-218">Azure Logic Apps</span><span class="sxs-lookup"><span data-stu-id="549f8-218">Azure Logic Apps</span></span>](https://docs.microsoft.com/azure/logic-apps)
* [<span data-ttu-id="549f8-219">Azure Service Bus</span><span class="sxs-lookup"><span data-stu-id="549f8-219">Azure Service Bus</span></span>](https://docs.microsoft.com/azure/service-bus-messaging)
* [<span data-ttu-id="549f8-220">Azure Table Storage</span><span class="sxs-lookup"><span data-stu-id="549f8-220">Azure Table Storage</span></span>](https://docs.microsoft.com/azure/cosmos-db/table-storage-overview)
* [<span data-ttu-id="549f8-221">Comparación de functions 1.x y 2.x</span><span class="sxs-lookup"><span data-stu-id="549f8-221">Compare functions 1.x and 2.x</span></span>](https://docs.microsoft.com/azure/azure-functions/functions-versions)
* [<span data-ttu-id="549f8-222">Conectarse a orígenes de datos locales con puerta de enlace de datos de Azure local</span><span class="sxs-lookup"><span data-stu-id="549f8-222">Connecting to on-premises data sources with Azure On-premises Data Gateway</span></span>](https://docs.microsoft.com/azure/analysis-services/analysis-services-gateway)
* [<span data-ttu-id="549f8-223">Crear su primera función en Azure portal</span><span class="sxs-lookup"><span data-stu-id="549f8-223">Create your first function in the Azure portal</span></span>](https://docs.microsoft.com/azure/azure-functions/functions-create-first-azure-function)
* [<span data-ttu-id="549f8-224">Cree su primera función mediante la CLI de Azure</span><span class="sxs-lookup"><span data-stu-id="549f8-224">Create your first function using the Azure CLI</span></span>](https://docs.microsoft.com/azure/azure-functions/functions-create-first-azure-function-azure-cli)
* [<span data-ttu-id="549f8-225">Cree su primera función mediante Visual Studio</span><span class="sxs-lookup"><span data-stu-id="549f8-225">Create your first function using Visual Studio</span></span>](https://docs.microsoft.com/azure/azure-functions/functions-create-your-first-function-visual-studio)
* [<span data-ttu-id="549f8-226">Las funciones de idiomas admitidos</span><span class="sxs-lookup"><span data-stu-id="549f8-226">Functions supported languages</span></span>](https://docs.microsoft.com/azure/azure-functions/supported-languages)
* [<span data-ttu-id="549f8-227">Supervisar Azure Functions</span><span class="sxs-lookup"><span data-stu-id="549f8-227">Monitor Azure Functions</span></span>](https://docs.microsoft.com/azure/azure-functions/functions-monitoring)
* [<span data-ttu-id="549f8-228">Trabajar con Azure Functions Proxies</span><span class="sxs-lookup"><span data-stu-id="549f8-228">Work with Azure Functions Proxies</span></span>](https://docs.microsoft.com/azure/azure-functions/functions-proxies)

>[!div class="step-by-step"]
<span data-ttu-id="549f8-229">[Anterior](logic-apps.md)
[Siguiente](durable-azure-functions.md)</span><span class="sxs-lookup"><span data-stu-id="549f8-229">[Previous](logic-apps.md)
[Next](durable-azure-functions.md)</span></span>