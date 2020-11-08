---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 431726e1bcbc0045cb1b9958ce9513638259bd8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183823"
---
# <span data-ttu-id="e95a4-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e95a4-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="e95a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e95a4-102">SYNOPSIS</span></span>
<span data-ttu-id="e95a4-103">Egy halom szélén álló eszköz eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e95a4-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="e95a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e95a4-104">SYNTAX</span></span>

### <span data-ttu-id="e95a4-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e95a4-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95a4-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95a4-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95a4-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95a4-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e95a4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e95a4-108">DESCRIPTION</span></span>
<span data-ttu-id="e95a4-109">A **Remove-AzStackEdgeDevice** parancsmag eltávolítja a halmozási eszköz konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="e95a4-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="e95a4-110">Fontos tudni, hogy az eszköz csak akkor törölhető, ha a megrendelés elhelyezése után a Microsoft a Microsoft által készített szállításhoz készült.</span><span class="sxs-lookup"><span data-stu-id="e95a4-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="e95a4-111">A [parancsmag](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource) használata előtt olvassa el az erőforrás törlésével kapcsolatos dokumentációt.</span><span class="sxs-lookup"><span data-stu-id="e95a4-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="e95a4-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e95a4-112">EXAMPLES</span></span>

### <span data-ttu-id="e95a4-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e95a4-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="e95a4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e95a4-114">PARAMETERS</span></span>

### <span data-ttu-id="e95a4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e95a4-115">-AsJob</span></span>
<span data-ttu-id="e95a4-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e95a4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e95a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95a4-117">-DefaultProfile</span></span>
<span data-ttu-id="e95a4-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e95a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e95a4-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e95a4-119">-DeviceObject</span></span>
<span data-ttu-id="e95a4-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="e95a4-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e95a4-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e95a4-121">-Name</span></span>
<span data-ttu-id="e95a4-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="e95a4-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95a4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e95a4-123">-PassThru</span></span>
<span data-ttu-id="e95a4-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="e95a4-124">returns true if successful</span></span>

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

### <span data-ttu-id="e95a4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e95a4-125">-ResourceGroupName</span></span>
<span data-ttu-id="e95a4-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e95a4-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95a4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e95a4-127">-ResourceId</span></span>
<span data-ttu-id="e95a4-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e95a4-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95a4-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e95a4-129">-Confirm</span></span>
<span data-ttu-id="e95a4-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e95a4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e95a4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e95a4-131">-WhatIf</span></span>
<span data-ttu-id="e95a4-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e95a4-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e95a4-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e95a4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e95a4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95a4-134">CommonParameters</span></span>
<span data-ttu-id="e95a4-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e95a4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95a4-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e95a4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95a4-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e95a4-137">INPUTS</span></span>

### <span data-ttu-id="e95a4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e95a4-138">System.String</span></span>

### <span data-ttu-id="e95a4-139">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e95a4-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="e95a4-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e95a4-140">OUTPUTS</span></span>

### <span data-ttu-id="e95a4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e95a4-141">System.Boolean</span></span>

## <span data-ttu-id="e95a4-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e95a4-142">NOTES</span></span>

## <span data-ttu-id="e95a4-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e95a4-143">RELATED LINKS</span></span>
