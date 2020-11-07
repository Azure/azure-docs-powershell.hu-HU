---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 1878a1ccbdc60ebe4df52dbb762de2436d10086b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844049"
---
# <span data-ttu-id="76287-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="76287-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="76287-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76287-102">SYNOPSIS</span></span>
<span data-ttu-id="76287-103">Az adatmező szélén lévő eszköz eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="76287-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="76287-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76287-104">SYNTAX</span></span>

### <span data-ttu-id="76287-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76287-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76287-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76287-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76287-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76287-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76287-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="76287-108">DESCRIPTION</span></span>
<span data-ttu-id="76287-109">A **Remove-AzDataBoxEdgeDevice** parancsmag eltávolítja az adatmező peremhálózati eszközének konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="76287-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="76287-110">Fontos tudni, hogy az eszköz csak akkor törölhető, ha a megrendelés elhelyezése után a Microsoft a Microsoft által készített szállításhoz készült.</span><span class="sxs-lookup"><span data-stu-id="76287-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="76287-111">A [parancsmag](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource) használata előtt olvassa el az erőforrás törlésével kapcsolatos dokumentációt.</span><span class="sxs-lookup"><span data-stu-id="76287-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="76287-112">Példák</span><span class="sxs-lookup"><span data-stu-id="76287-112">EXAMPLES</span></span>

### <span data-ttu-id="76287-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="76287-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="76287-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76287-114">PARAMETERS</span></span>

### <span data-ttu-id="76287-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76287-115">-AsJob</span></span>
<span data-ttu-id="76287-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="76287-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76287-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76287-117">-DefaultProfile</span></span>
<span data-ttu-id="76287-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76287-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76287-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76287-119">-InputObject</span></span>
<span data-ttu-id="76287-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="76287-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76287-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76287-121">-Name</span></span>
<span data-ttu-id="76287-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="76287-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76287-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76287-123">-PassThru</span></span>
<span data-ttu-id="76287-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="76287-124">returns true if successful</span></span>

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

### <span data-ttu-id="76287-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76287-125">-ResourceGroupName</span></span>
<span data-ttu-id="76287-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="76287-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76287-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76287-127">-ResourceId</span></span>
<span data-ttu-id="76287-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="76287-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="76287-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="76287-129">-Confirm</span></span>
<span data-ttu-id="76287-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="76287-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76287-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76287-131">-WhatIf</span></span>
<span data-ttu-id="76287-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="76287-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76287-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="76287-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76287-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76287-134">CommonParameters</span></span>
<span data-ttu-id="76287-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76287-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76287-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="76287-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76287-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76287-137">INPUTS</span></span>

### <span data-ttu-id="76287-138">System. String</span><span class="sxs-lookup"><span data-stu-id="76287-138">System.String</span></span>

### <span data-ttu-id="76287-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="76287-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="76287-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76287-140">OUTPUTS</span></span>

### <span data-ttu-id="76287-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="76287-141">System.Boolean</span></span>

## <span data-ttu-id="76287-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76287-142">NOTES</span></span>

## <span data-ttu-id="76287-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76287-143">RELATED LINKS</span></span>
