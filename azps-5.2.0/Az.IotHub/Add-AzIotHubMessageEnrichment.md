---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 04c65bf74d6c32dcaf93d2183936f9c0980aae4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364446"
---
# <span data-ttu-id="277d7-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="277d7-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="277d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="277d7-102">SYNOPSIS</span></span>
<span data-ttu-id="277d7-103">Egy üzenet gazdagítását hozza létre a kiválasztott végpontok számára az IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="277d7-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="277d7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="277d7-104">SYNTAX</span></span>

### <span data-ttu-id="277d7-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="277d7-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="277d7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="277d7-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="277d7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="277d7-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="277d7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="277d7-108">DESCRIPTION</span></span>
<span data-ttu-id="277d7-109">IoT-központonként akár 10 üzenetgazdagítást is hozzáadhat.</span><span class="sxs-lookup"><span data-stu-id="277d7-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="277d7-110">Ezek alkalmazástulajdonságként kerülnek be a kiválasztott végpont(ak)nak küldött üzenetekbe.</span><span class="sxs-lookup"><span data-stu-id="277d7-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="277d7-111">További tudnivalókért lásd: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="277d7-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="277d7-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="277d7-112">EXAMPLES</span></span>

### <span data-ttu-id="277d7-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="277d7-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="277d7-114">Új gazdagítás hozzáadása az "újKulcs" billentyűvel és az "újÉrték" értékkel.</span><span class="sxs-lookup"><span data-stu-id="277d7-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="277d7-115">Ez az új gazdagítás a "végpont1" és a "végpont2" végpontokra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="277d7-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="277d7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="277d7-116">PARAMETERS</span></span>

### <span data-ttu-id="277d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="277d7-117">-DefaultProfile</span></span>
<span data-ttu-id="277d7-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="277d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="277d7-119">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="277d7-119">-Endpoint</span></span>
<span data-ttu-id="277d7-120">Végpont(ak) a gazdagítások alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="277d7-120">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="277d7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="277d7-121">-InputObject</span></span>
<span data-ttu-id="277d7-122">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="277d7-122">IotHub object</span></span>

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

### <span data-ttu-id="277d7-123">-Key</span><span class="sxs-lookup"><span data-stu-id="277d7-123">-Key</span></span>
<span data-ttu-id="277d7-124">A gazdagodás kulcsa.</span><span class="sxs-lookup"><span data-stu-id="277d7-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="277d7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="277d7-125">-Name</span></span>
<span data-ttu-id="277d7-126">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="277d7-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="277d7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="277d7-127">-ResourceGroupName</span></span>
<span data-ttu-id="277d7-128">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="277d7-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="277d7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="277d7-129">-ResourceId</span></span>
<span data-ttu-id="277d7-130">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="277d7-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="277d7-131">-Érték</span><span class="sxs-lookup"><span data-stu-id="277d7-131">-Value</span></span>
<span data-ttu-id="277d7-132">A gazdagodás értéke.</span><span class="sxs-lookup"><span data-stu-id="277d7-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="277d7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="277d7-133">-Confirm</span></span>
<span data-ttu-id="277d7-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="277d7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="277d7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="277d7-135">-WhatIf</span></span>
<span data-ttu-id="277d7-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="277d7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="277d7-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="277d7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="277d7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="277d7-138">CommonParameters</span></span>
<span data-ttu-id="277d7-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="277d7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="277d7-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="277d7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="277d7-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="277d7-141">INPUTS</span></span>

### <span data-ttu-id="277d7-142">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="277d7-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="277d7-143">System.String</span><span class="sxs-lookup"><span data-stu-id="277d7-143">System.String</span></span>

## <span data-ttu-id="277d7-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="277d7-144">OUTPUTS</span></span>

### <span data-ttu-id="277d7-145">Microsoft.Azure.Commands.Management.iotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="277d7-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="277d7-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="277d7-146">NOTES</span></span>

## <span data-ttu-id="277d7-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="277d7-147">RELATED LINKS</span></span>
