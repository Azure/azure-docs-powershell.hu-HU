---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 3905249cde38fc00e2dd4996f4b3a52fcd65e446
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666235"
---
# <span data-ttu-id="dcd25-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dcd25-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="dcd25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dcd25-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd25-103">Frissítse az üzenet dúsítását a IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="dcd25-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="dcd25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dcd25-104">SYNTAX</span></span>

### <span data-ttu-id="dcd25-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dcd25-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd25-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dcd25-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd25-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dcd25-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcd25-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dcd25-108">DESCRIPTION</span></span>
<span data-ttu-id="dcd25-109">Az Azure IoT hub üzenet-dúsítási lehetőségeinek részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="dcd25-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="dcd25-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dcd25-110">EXAMPLES</span></span>

### <span data-ttu-id="dcd25-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dcd25-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="dcd25-112">Frissíti a gazdagodás értékét "updatedValue" értékre a "newKey" kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="dcd25-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="dcd25-113">Az Azure IoT hub üzenet-dúsítási lehetőségeinek részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="dcd25-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="dcd25-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="dcd25-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="dcd25-115">Frissíti a dúsítás végpontját "endpoint1, endpoint2, endpoint3" értékre a "newKey" kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="dcd25-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="dcd25-116">Az Azure IoT hub üzenet-dúsítási lehetőségeinek részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="dcd25-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="dcd25-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dcd25-117">PARAMETERS</span></span>

### <span data-ttu-id="dcd25-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd25-118">-DefaultProfile</span></span>
<span data-ttu-id="dcd25-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dcd25-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcd25-120">-Végpont</span><span class="sxs-lookup"><span data-stu-id="dcd25-120">-Endpoint</span></span>
<span data-ttu-id="dcd25-121">Végpont (ok) az alkoholtartalom-NÖVELÉSEK alkalmazásához.</span><span class="sxs-lookup"><span data-stu-id="dcd25-121">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd25-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcd25-122">-InputObject</span></span>
<span data-ttu-id="dcd25-123">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="dcd25-123">IotHub Object</span></span>

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

### <span data-ttu-id="dcd25-124">-Kulcs</span><span class="sxs-lookup"><span data-stu-id="dcd25-124">-Key</span></span>
<span data-ttu-id="dcd25-125">A gazdagodás kulcsa.</span><span class="sxs-lookup"><span data-stu-id="dcd25-125">The enrichment's key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd25-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dcd25-126">-Name</span></span>
<span data-ttu-id="dcd25-127">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="dcd25-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dcd25-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcd25-128">-ResourceGroupName</span></span>
<span data-ttu-id="dcd25-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="dcd25-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dcd25-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd25-130">-ResourceId</span></span>
<span data-ttu-id="dcd25-131">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="dcd25-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="dcd25-132">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="dcd25-132">-Value</span></span>
<span data-ttu-id="dcd25-133">A gazdagodás értéke.</span><span class="sxs-lookup"><span data-stu-id="dcd25-133">The enrichment's value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd25-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dcd25-134">-Confirm</span></span>
<span data-ttu-id="dcd25-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dcd25-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcd25-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcd25-136">-WhatIf</span></span>
<span data-ttu-id="dcd25-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dcd25-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcd25-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dcd25-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcd25-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd25-139">CommonParameters</span></span>
<span data-ttu-id="dcd25-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dcd25-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd25-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcd25-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd25-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcd25-142">INPUTS</span></span>

### <span data-ttu-id="dcd25-143">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dcd25-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="dcd25-144">System. String</span><span class="sxs-lookup"><span data-stu-id="dcd25-144">System.String</span></span>

## <span data-ttu-id="dcd25-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcd25-145">OUTPUTS</span></span>

### <span data-ttu-id="dcd25-146">Microsoft. Azure. Command. Management. IotHub. models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="dcd25-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="dcd25-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dcd25-147">NOTES</span></span>

## <span data-ttu-id="dcd25-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dcd25-148">RELATED LINKS</span></span>
