---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 683d03537f410b38260b502bc25ed90c9da9b4d2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011423"
---
# <span data-ttu-id="f5390-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f5390-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="f5390-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5390-102">SYNOPSIS</span></span>
<span data-ttu-id="f5390-103">Üzenet dúsításának törlése a IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="f5390-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="f5390-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5390-104">SYNTAX</span></span>

### <span data-ttu-id="f5390-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5390-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5390-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f5390-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5390-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f5390-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5390-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5390-108">DESCRIPTION</span></span>
<span data-ttu-id="f5390-109">Az Azure IoT hub üzenet-dúsítási lehetőségeinek részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="f5390-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="f5390-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f5390-110">EXAMPLES</span></span>

### <span data-ttu-id="f5390-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f5390-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="f5390-112">Törli a "newKey" üzenet dúsítását.</span><span class="sxs-lookup"><span data-stu-id="f5390-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="f5390-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5390-113">PARAMETERS</span></span>

### <span data-ttu-id="f5390-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5390-114">-DefaultProfile</span></span>
<span data-ttu-id="f5390-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5390-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5390-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5390-116">-InputObject</span></span>
<span data-ttu-id="f5390-117">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="f5390-117">IotHub object</span></span>

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

### <span data-ttu-id="f5390-118">-Kulcs</span><span class="sxs-lookup"><span data-stu-id="f5390-118">-Key</span></span>
<span data-ttu-id="f5390-119">A gazdagodás kulcsa.</span><span class="sxs-lookup"><span data-stu-id="f5390-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="f5390-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5390-120">-Name</span></span>
<span data-ttu-id="f5390-121">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="f5390-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f5390-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5390-122">-PassThru</span></span>
<span data-ttu-id="f5390-123">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="f5390-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="f5390-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f5390-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f5390-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5390-125">-ResourceGroupName</span></span>
<span data-ttu-id="f5390-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f5390-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f5390-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5390-127">-ResourceId</span></span>
<span data-ttu-id="f5390-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="f5390-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f5390-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5390-129">-Confirm</span></span>
<span data-ttu-id="f5390-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5390-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5390-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5390-131">-WhatIf</span></span>
<span data-ttu-id="f5390-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f5390-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5390-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5390-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5390-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5390-134">CommonParameters</span></span>
<span data-ttu-id="f5390-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5390-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5390-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5390-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5390-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5390-137">INPUTS</span></span>

### <span data-ttu-id="f5390-138">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f5390-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f5390-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f5390-139">System.String</span></span>

## <span data-ttu-id="f5390-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5390-140">OUTPUTS</span></span>

### <span data-ttu-id="f5390-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5390-141">System.Boolean</span></span>

## <span data-ttu-id="f5390-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5390-142">NOTES</span></span>

## <span data-ttu-id="f5390-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5390-143">RELATED LINKS</span></span>
