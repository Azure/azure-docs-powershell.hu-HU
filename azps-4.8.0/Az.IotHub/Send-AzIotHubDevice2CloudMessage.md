---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181902"
---
# <span data-ttu-id="2aa66-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="2aa66-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="2aa66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2aa66-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa66-103">Eszköz – Felhőbeli üzenet küldése</span><span class="sxs-lookup"><span data-stu-id="2aa66-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="2aa66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2aa66-104">SYNTAX</span></span>

### <span data-ttu-id="2aa66-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2aa66-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa66-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2aa66-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2aa66-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2aa66-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2aa66-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2aa66-108">DESCRIPTION</span></span>
<span data-ttu-id="2aa66-109">A parancs támogatja az üzenetküldést az alkalmazás és a rendszer tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="2aa66-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="2aa66-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2aa66-110">EXAMPLES</span></span>

### <span data-ttu-id="2aa66-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2aa66-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="2aa66-112">Eszköz küldése Felhőbeli üzenetbe alapértelmezett átviteli típus használatával.</span><span class="sxs-lookup"><span data-stu-id="2aa66-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="2aa66-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2aa66-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="2aa66-114">Mqtt eszköz küldése Felhőbeli üzenetbe</span><span class="sxs-lookup"><span data-stu-id="2aa66-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="2aa66-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2aa66-115">PARAMETERS</span></span>

### <span data-ttu-id="2aa66-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa66-116">-DefaultProfile</span></span>
<span data-ttu-id="2aa66-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2aa66-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa66-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2aa66-118">-DeviceId</span></span>
<span data-ttu-id="2aa66-119">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2aa66-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa66-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aa66-120">-InputObject</span></span>
<span data-ttu-id="2aa66-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="2aa66-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa66-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2aa66-122">-IotHubName</span></span>
<span data-ttu-id="2aa66-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="2aa66-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa66-124">-Üzenet</span><span class="sxs-lookup"><span data-stu-id="2aa66-124">-Message</span></span>
<span data-ttu-id="2aa66-125">Üzenet szövegtörzse, amelyet a IoT-hub-ba küld el.</span><span class="sxs-lookup"><span data-stu-id="2aa66-125">Message body to send to IoT Hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa66-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2aa66-126">-PassThru</span></span>
<span data-ttu-id="2aa66-127">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="2aa66-127">Allows to return the boolean object.</span></span> <span data-ttu-id="2aa66-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2aa66-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa66-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aa66-129">-ResourceGroupName</span></span>
<span data-ttu-id="2aa66-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2aa66-130">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa66-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2aa66-131">-ResourceId</span></span>
<span data-ttu-id="2aa66-132">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="2aa66-132">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa66-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="2aa66-133">-TransportType</span></span>
<span data-ttu-id="2aa66-134">A használandó átviteli típus.</span><span class="sxs-lookup"><span data-stu-id="2aa66-134">Transport type to use.</span></span>
<span data-ttu-id="2aa66-135">Az alapértelmezett érték a Amqp.</span><span class="sxs-lookup"><span data-stu-id="2aa66-135">Default is Amqp.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSTransportType
Parameter Sets: (All)
Aliases:
Accepted values: Amqp, Http1, Amqp_WebSocket_Only, Amqp_Tcp_Only, Mqtt, Mqtt_WebSocket_Only, Mqtt_Tcp_Only

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa66-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2aa66-136">-Confirm</span></span>
<span data-ttu-id="2aa66-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2aa66-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa66-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aa66-138">-WhatIf</span></span>
<span data-ttu-id="2aa66-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2aa66-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aa66-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2aa66-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa66-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa66-141">CommonParameters</span></span>
<span data-ttu-id="2aa66-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2aa66-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa66-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aa66-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa66-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2aa66-144">INPUTS</span></span>

### <span data-ttu-id="2aa66-145">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2aa66-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2aa66-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2aa66-146">System.String</span></span>

## <span data-ttu-id="2aa66-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2aa66-147">OUTPUTS</span></span>

### <span data-ttu-id="2aa66-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2aa66-148">System.Boolean</span></span>

## <span data-ttu-id="2aa66-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2aa66-149">NOTES</span></span>

## <span data-ttu-id="2aa66-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2aa66-150">RELATED LINKS</span></span>
