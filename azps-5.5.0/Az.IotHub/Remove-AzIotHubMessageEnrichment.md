---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 683d03537f410b38260b502bc25ed90c9da9b4d2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159650"
---
# <span data-ttu-id="5d97d-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5d97d-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="5d97d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d97d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d97d-103">Törölje az üzenet gazdagítását az IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="5d97d-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="5d97d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5d97d-104">SYNTAX</span></span>

### <span data-ttu-id="5d97d-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d97d-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d97d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5d97d-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d97d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5d97d-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d97d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5d97d-108">DESCRIPTION</span></span>
<span data-ttu-id="5d97d-109">Az Azure IoT-központban az üzenetek gazdagításának részletes magyarázatát lásd: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="5d97d-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="5d97d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5d97d-110">EXAMPLES</span></span>

### <span data-ttu-id="5d97d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="5d97d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="5d97d-112">Törli az "újKulcs" üzenet gazdagítását.</span><span class="sxs-lookup"><span data-stu-id="5d97d-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="5d97d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d97d-113">PARAMETERS</span></span>

### <span data-ttu-id="5d97d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d97d-114">-DefaultProfile</span></span>
<span data-ttu-id="5d97d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d97d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d97d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d97d-116">-InputObject</span></span>
<span data-ttu-id="5d97d-117">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="5d97d-117">IotHub object</span></span>

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

### <span data-ttu-id="5d97d-118">-Key</span><span class="sxs-lookup"><span data-stu-id="5d97d-118">-Key</span></span>
<span data-ttu-id="5d97d-119">A gazdagodás kulcsa.</span><span class="sxs-lookup"><span data-stu-id="5d97d-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="5d97d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5d97d-120">-Name</span></span>
<span data-ttu-id="5d97d-121">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="5d97d-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5d97d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d97d-122">-PassThru</span></span>
<span data-ttu-id="5d97d-123">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="5d97d-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="5d97d-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5d97d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5d97d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d97d-125">-ResourceGroupName</span></span>
<span data-ttu-id="5d97d-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5d97d-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5d97d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d97d-127">-ResourceId</span></span>
<span data-ttu-id="5d97d-128">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="5d97d-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5d97d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d97d-129">-Confirm</span></span>
<span data-ttu-id="5d97d-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5d97d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d97d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d97d-131">-WhatIf</span></span>
<span data-ttu-id="5d97d-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5d97d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d97d-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d97d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d97d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d97d-134">CommonParameters</span></span>
<span data-ttu-id="5d97d-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d97d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d97d-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d97d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d97d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d97d-137">INPUTS</span></span>

### <span data-ttu-id="5d97d-138">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5d97d-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5d97d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5d97d-139">System.String</span></span>

## <span data-ttu-id="5d97d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d97d-140">OUTPUTS</span></span>

### <span data-ttu-id="5d97d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d97d-141">System.Boolean</span></span>

## <span data-ttu-id="5d97d-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5d97d-142">NOTES</span></span>

## <span data-ttu-id="5d97d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d97d-143">RELATED LINKS</span></span>
