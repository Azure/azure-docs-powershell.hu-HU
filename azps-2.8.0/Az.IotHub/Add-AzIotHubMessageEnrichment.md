---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: fa3e46db14c7bba17ba87813285d0f7b119dc6c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666291"
---
# <span data-ttu-id="dd876-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dd876-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="dd876-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd876-102">SYNOPSIS</span></span>
<span data-ttu-id="dd876-103">Az IoT-központban kiválasztott végpontokra mutató üzenet dúsítását hozza létre.</span><span class="sxs-lookup"><span data-stu-id="dd876-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="dd876-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd876-104">SYNTAX</span></span>

### <span data-ttu-id="dd876-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd876-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd876-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dd876-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd876-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dd876-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd876-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd876-108">DESCRIPTION</span></span>
<span data-ttu-id="dd876-109">A IoT-hub-ra legfeljebb 10 üzenet gazdagodhat.</span><span class="sxs-lookup"><span data-stu-id="dd876-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="dd876-110">Ezek az alkalmazások a kijelölt végpont (ok) ba küldött üzenetekhez kerülnek hozzáadásra.</span><span class="sxs-lookup"><span data-stu-id="dd876-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="dd876-111">További információ: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="dd876-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="dd876-112">Példák</span><span class="sxs-lookup"><span data-stu-id="dd876-112">EXAMPLES</span></span>

### <span data-ttu-id="dd876-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dd876-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="dd876-114">Új gazdagodás hozzáadása a "newKey" és a "Újérték" értékkel.</span><span class="sxs-lookup"><span data-stu-id="dd876-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="dd876-115">Ezt az új gazdagodás a "endpoint1" és a "endpoint2" végpontokra alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="dd876-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="dd876-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd876-116">PARAMETERS</span></span>

### <span data-ttu-id="dd876-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd876-117">-DefaultProfile</span></span>
<span data-ttu-id="dd876-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd876-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd876-119">-Végpont</span><span class="sxs-lookup"><span data-stu-id="dd876-119">-Endpoint</span></span>
<span data-ttu-id="dd876-120">Végpont (ok) az alkoholtartalom-NÖVELÉSEK alkalmazásához.</span><span class="sxs-lookup"><span data-stu-id="dd876-120">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd876-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd876-121">-InputObject</span></span>
<span data-ttu-id="dd876-122">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="dd876-122">IotHub object</span></span>

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

### <span data-ttu-id="dd876-123">-Kulcs</span><span class="sxs-lookup"><span data-stu-id="dd876-123">-Key</span></span>
<span data-ttu-id="dd876-124">A gazdagodás kulcsa.</span><span class="sxs-lookup"><span data-stu-id="dd876-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="dd876-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dd876-125">-Name</span></span>
<span data-ttu-id="dd876-126">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="dd876-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dd876-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd876-127">-ResourceGroupName</span></span>
<span data-ttu-id="dd876-128">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="dd876-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dd876-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd876-129">-ResourceId</span></span>
<span data-ttu-id="dd876-130">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="dd876-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="dd876-131">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="dd876-131">-Value</span></span>
<span data-ttu-id="dd876-132">A gazdagodás értéke.</span><span class="sxs-lookup"><span data-stu-id="dd876-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="dd876-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dd876-133">-Confirm</span></span>
<span data-ttu-id="dd876-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dd876-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd876-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd876-135">-WhatIf</span></span>
<span data-ttu-id="dd876-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dd876-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd876-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd876-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd876-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd876-138">CommonParameters</span></span>
<span data-ttu-id="dd876-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd876-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd876-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd876-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd876-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd876-141">INPUTS</span></span>

### <span data-ttu-id="dd876-142">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dd876-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="dd876-143">System. String</span><span class="sxs-lookup"><span data-stu-id="dd876-143">System.String</span></span>

## <span data-ttu-id="dd876-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd876-144">OUTPUTS</span></span>

### <span data-ttu-id="dd876-145">Microsoft. Azure. Command. Management. IotHub. models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="dd876-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="dd876-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd876-146">NOTES</span></span>

## <span data-ttu-id="dd876-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd876-147">RELATED LINKS</span></span>
