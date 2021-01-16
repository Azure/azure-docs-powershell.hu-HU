---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325930"
---
# <span data-ttu-id="029a9-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="029a9-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="029a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="029a9-102">SYNOPSIS</span></span>
<span data-ttu-id="029a9-103">Eszközről felhőbe üzenetet küldhet.</span><span class="sxs-lookup"><span data-stu-id="029a9-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="029a9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="029a9-104">SYNTAX</span></span>

### <span data-ttu-id="029a9-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="029a9-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="029a9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="029a9-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="029a9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="029a9-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="029a9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="029a9-108">DESCRIPTION</span></span>
<span data-ttu-id="029a9-109">A parancs alkalmazás- és rendszertulajdonságokkal támogatja az üzenetek küldését.</span><span class="sxs-lookup"><span data-stu-id="029a9-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="029a9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="029a9-110">EXAMPLES</span></span>

### <span data-ttu-id="029a9-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="029a9-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="029a9-112">Eszköz küldése a felhőbeli üzenetbe alapértelmezett átviteli típus használatával.</span><span class="sxs-lookup"><span data-stu-id="029a9-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="029a9-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="029a9-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="029a9-114">Mqtt-eszköz küldése felhőbeli üzenetbe.</span><span class="sxs-lookup"><span data-stu-id="029a9-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="029a9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="029a9-115">PARAMETERS</span></span>

### <span data-ttu-id="029a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="029a9-116">-DefaultProfile</span></span>
<span data-ttu-id="029a9-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="029a9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="029a9-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="029a9-118">-DeviceId</span></span>
<span data-ttu-id="029a9-119">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="029a9-119">Target Device Id.</span></span>

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

### <span data-ttu-id="029a9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="029a9-120">-InputObject</span></span>
<span data-ttu-id="029a9-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="029a9-121">IotHub object</span></span>

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

### <span data-ttu-id="029a9-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="029a9-122">-IotHubName</span></span>
<span data-ttu-id="029a9-123">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="029a9-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="029a9-124">-Message</span><span class="sxs-lookup"><span data-stu-id="029a9-124">-Message</span></span>
<span data-ttu-id="029a9-125">Az IoT-központba küldenének üzenet törzse.</span><span class="sxs-lookup"><span data-stu-id="029a9-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="029a9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="029a9-126">-PassThru</span></span>
<span data-ttu-id="029a9-127">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="029a9-127">Allows to return the boolean object.</span></span> <span data-ttu-id="029a9-128">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="029a9-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="029a9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="029a9-129">-ResourceGroupName</span></span>
<span data-ttu-id="029a9-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="029a9-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="029a9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="029a9-131">-ResourceId</span></span>
<span data-ttu-id="029a9-132">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="029a9-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="029a9-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="029a9-133">-TransportType</span></span>
<span data-ttu-id="029a9-134">A használni használt átviteli típus.</span><span class="sxs-lookup"><span data-stu-id="029a9-134">Transport type to use.</span></span>
<span data-ttu-id="029a9-135">Az alapértelmezett érték az Amqp.</span><span class="sxs-lookup"><span data-stu-id="029a9-135">Default is Amqp.</span></span>

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

### <span data-ttu-id="029a9-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="029a9-136">-Confirm</span></span>
<span data-ttu-id="029a9-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="029a9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="029a9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="029a9-138">-WhatIf</span></span>
<span data-ttu-id="029a9-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="029a9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="029a9-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="029a9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="029a9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="029a9-141">CommonParameters</span></span>
<span data-ttu-id="029a9-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="029a9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="029a9-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="029a9-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="029a9-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="029a9-144">INPUTS</span></span>

### <span data-ttu-id="029a9-145">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="029a9-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="029a9-146">System.String</span><span class="sxs-lookup"><span data-stu-id="029a9-146">System.String</span></span>

## <span data-ttu-id="029a9-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="029a9-147">OUTPUTS</span></span>

### <span data-ttu-id="029a9-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="029a9-148">System.Boolean</span></span>

## <span data-ttu-id="029a9-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="029a9-149">NOTES</span></span>

## <span data-ttu-id="029a9-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="029a9-150">RELATED LINKS</span></span>
