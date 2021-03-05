---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 0e9b26b4bd22d167dffbee4449aa811381960732
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004133"
---
# <span data-ttu-id="3070d-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3070d-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="3070d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3070d-102">SYNOPSIS</span></span>
<span data-ttu-id="3070d-103">Frissítse az üzenet gazdagítását az IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="3070d-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="3070d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3070d-104">SYNTAX</span></span>

### <span data-ttu-id="3070d-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3070d-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3070d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3070d-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3070d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3070d-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3070d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3070d-108">DESCRIPTION</span></span>
<span data-ttu-id="3070d-109">Az Azure IoT-központban az üzenetek gazdagításának részletes magyarázatát lásd: https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="3070d-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="3070d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3070d-110">EXAMPLES</span></span>

### <span data-ttu-id="3070d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="3070d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="3070d-112">Frissíti a gazdagítás értékét "updatedValue" értékre az "újKulcs" kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="3070d-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="3070d-113">Az Azure IoT-központban az üzenetek gazdagításának részletes magyarázatát lásd: https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="3070d-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="3070d-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="3070d-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="3070d-115">Frissíti a gazdagítás végpontját "endpoint1, endpoint2, endpoint3" (végpont1, végpont3) az "újKey" kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="3070d-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="3070d-116">Az Azure IoT-központban az üzenetek gazdagításának részletes magyarázatát lásd: https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="3070d-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="3070d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3070d-117">PARAMETERS</span></span>

### <span data-ttu-id="3070d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3070d-118">-DefaultProfile</span></span>
<span data-ttu-id="3070d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3070d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3070d-120">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="3070d-120">-Endpoint</span></span>
<span data-ttu-id="3070d-121">Végpont(ak) a gazdagítások alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="3070d-121">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="3070d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3070d-122">-InputObject</span></span>
<span data-ttu-id="3070d-123">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="3070d-123">IotHub Object</span></span>

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

### <span data-ttu-id="3070d-124">-Key</span><span class="sxs-lookup"><span data-stu-id="3070d-124">-Key</span></span>
<span data-ttu-id="3070d-125">A gazdagodás kulcsa.</span><span class="sxs-lookup"><span data-stu-id="3070d-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="3070d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3070d-126">-Name</span></span>
<span data-ttu-id="3070d-127">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="3070d-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3070d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3070d-128">-ResourceGroupName</span></span>
<span data-ttu-id="3070d-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3070d-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3070d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3070d-130">-ResourceId</span></span>
<span data-ttu-id="3070d-131">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="3070d-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3070d-132">-Érték</span><span class="sxs-lookup"><span data-stu-id="3070d-132">-Value</span></span>
<span data-ttu-id="3070d-133">A gazdagodás értéke.</span><span class="sxs-lookup"><span data-stu-id="3070d-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="3070d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3070d-134">-Confirm</span></span>
<span data-ttu-id="3070d-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3070d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3070d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3070d-136">-WhatIf</span></span>
<span data-ttu-id="3070d-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3070d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3070d-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3070d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3070d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3070d-139">CommonParameters</span></span>
<span data-ttu-id="3070d-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3070d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3070d-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3070d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3070d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3070d-142">INPUTS</span></span>

### <span data-ttu-id="3070d-143">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3070d-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3070d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3070d-144">System.String</span></span>

## <span data-ttu-id="3070d-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3070d-145">OUTPUTS</span></span>

### <span data-ttu-id="3070d-146">Microsoft.Azure.Commands.Management.iotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="3070d-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="3070d-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3070d-147">NOTES</span></span>

## <span data-ttu-id="3070d-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3070d-148">RELATED LINKS</span></span>
