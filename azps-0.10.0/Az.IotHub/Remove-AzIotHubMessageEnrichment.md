---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 5c30db1845fe135aad9ebb575a6b31f19e9598b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842201"
---
# <span data-ttu-id="0cc8e-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0cc8e-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="0cc8e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0cc8e-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc8e-103">Üzenet dúsításának törlése a IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="0cc8e-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="0cc8e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0cc8e-104">SYNTAX</span></span>

### <span data-ttu-id="0cc8e-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0cc8e-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cc8e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0cc8e-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cc8e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0cc8e-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cc8e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0cc8e-108">DESCRIPTION</span></span>
<span data-ttu-id="0cc8e-109">Az Azure IoT hub üzenet-dúsítási lehetőségeinek részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="0cc8e-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="0cc8e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0cc8e-110">EXAMPLES</span></span>

### <span data-ttu-id="0cc8e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0cc8e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="0cc8e-112">Törli a "newKey" üzenet dúsítását.</span><span class="sxs-lookup"><span data-stu-id="0cc8e-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="0cc8e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0cc8e-113">PARAMETERS</span></span>

### <span data-ttu-id="0cc8e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cc8e-114">-DefaultProfile</span></span>
<span data-ttu-id="0cc8e-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0cc8e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cc8e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cc8e-116">-InputObject</span></span>
<span data-ttu-id="0cc8e-117">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="0cc8e-117">IotHub object</span></span>

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

### <span data-ttu-id="0cc8e-118">-Kulcs</span><span class="sxs-lookup"><span data-stu-id="0cc8e-118">-Key</span></span>
<span data-ttu-id="0cc8e-119">A gazdagodás kulcsa.</span><span class="sxs-lookup"><span data-stu-id="0cc8e-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="0cc8e-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0cc8e-120">-Name</span></span>
<span data-ttu-id="0cc8e-121">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="0cc8e-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0cc8e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cc8e-122">-PassThru</span></span>
<span data-ttu-id="0cc8e-123">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="0cc8e-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="0cc8e-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0cc8e-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0cc8e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cc8e-125">-ResourceGroupName</span></span>
<span data-ttu-id="0cc8e-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0cc8e-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0cc8e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cc8e-127">-ResourceId</span></span>
<span data-ttu-id="0cc8e-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="0cc8e-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0cc8e-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0cc8e-129">-Confirm</span></span>
<span data-ttu-id="0cc8e-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0cc8e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cc8e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cc8e-131">-WhatIf</span></span>
<span data-ttu-id="0cc8e-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0cc8e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cc8e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0cc8e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cc8e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc8e-134">CommonParameters</span></span>
<span data-ttu-id="0cc8e-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0cc8e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc8e-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cc8e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc8e-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cc8e-137">INPUTS</span></span>

### <span data-ttu-id="0cc8e-138">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0cc8e-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0cc8e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0cc8e-139">System.String</span></span>

## <span data-ttu-id="0cc8e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cc8e-140">OUTPUTS</span></span>

### <span data-ttu-id="0cc8e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0cc8e-141">System.Boolean</span></span>

## <span data-ttu-id="0cc8e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0cc8e-142">NOTES</span></span>

## <span data-ttu-id="0cc8e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cc8e-143">RELATED LINKS</span></span>
