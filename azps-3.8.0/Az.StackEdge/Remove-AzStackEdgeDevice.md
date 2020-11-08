---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 431726e1bcbc0045cb1b9958ce9513638259bd8f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012320"
---
# <span data-ttu-id="a036a-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a036a-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="a036a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a036a-102">SYNOPSIS</span></span>
<span data-ttu-id="a036a-103">Egy halom szélén álló eszköz eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a036a-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="a036a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a036a-104">SYNTAX</span></span>

### <span data-ttu-id="a036a-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a036a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a036a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a036a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a036a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a036a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a036a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a036a-108">DESCRIPTION</span></span>
<span data-ttu-id="a036a-109">A **Remove-AzStackEdgeDevice** parancsmag eltávolítja a halmozási eszköz konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a036a-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="a036a-110">Fontos tudni, hogy az eszköz csak akkor törölhető, ha a megrendelés elhelyezése után a Microsoft a Microsoft által készített szállításhoz készült.</span><span class="sxs-lookup"><span data-stu-id="a036a-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="a036a-111">A [parancsmag](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource) használata előtt olvassa el az erőforrás törlésével kapcsolatos dokumentációt.</span><span class="sxs-lookup"><span data-stu-id="a036a-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="a036a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a036a-112">EXAMPLES</span></span>

### <span data-ttu-id="a036a-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a036a-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="a036a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a036a-114">PARAMETERS</span></span>

### <span data-ttu-id="a036a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a036a-115">-AsJob</span></span>
<span data-ttu-id="a036a-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a036a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a036a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a036a-117">-DefaultProfile</span></span>
<span data-ttu-id="a036a-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a036a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a036a-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a036a-119">-DeviceObject</span></span>
<span data-ttu-id="a036a-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="a036a-120">Input Object</span></span>

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

### <span data-ttu-id="a036a-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a036a-121">-Name</span></span>
<span data-ttu-id="a036a-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="a036a-122">Resource Name</span></span>

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

### <span data-ttu-id="a036a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a036a-123">-PassThru</span></span>
<span data-ttu-id="a036a-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="a036a-124">returns true if successful</span></span>

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

### <span data-ttu-id="a036a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a036a-125">-ResourceGroupName</span></span>
<span data-ttu-id="a036a-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a036a-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a036a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a036a-127">-ResourceId</span></span>
<span data-ttu-id="a036a-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a036a-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="a036a-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a036a-129">-Confirm</span></span>
<span data-ttu-id="a036a-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a036a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a036a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a036a-131">-WhatIf</span></span>
<span data-ttu-id="a036a-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a036a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a036a-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a036a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a036a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a036a-134">CommonParameters</span></span>
<span data-ttu-id="a036a-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a036a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a036a-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a036a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a036a-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a036a-137">INPUTS</span></span>

### <span data-ttu-id="a036a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a036a-138">System.String</span></span>

### <span data-ttu-id="a036a-139">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a036a-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="a036a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a036a-140">OUTPUTS</span></span>

### <span data-ttu-id="a036a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a036a-141">System.Boolean</span></span>

## <span data-ttu-id="a036a-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a036a-142">NOTES</span></span>

## <span data-ttu-id="a036a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a036a-143">RELATED LINKS</span></span>
