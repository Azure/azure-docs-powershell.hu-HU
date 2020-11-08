---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: a9b0d3565e2266373d3ba553be94ffd8a24707d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184183"
---
# <span data-ttu-id="ddb23-101">Remove-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="ddb23-101">Remove-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="ddb23-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ddb23-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb23-103">Eltávolít egy meglévő triggert az eszközön.</span><span class="sxs-lookup"><span data-stu-id="ddb23-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="ddb23-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ddb23-104">SYNTAX</span></span>

### <span data-ttu-id="ddb23-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ddb23-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddb23-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddb23-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddb23-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddb23-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-InputObject] <PSDataBoxEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddb23-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ddb23-108">DESCRIPTION</span></span>
<span data-ttu-id="ddb23-109">A **Remove-AzDataBoxEdgeTrigger** parancsmag egy meglévő triggert távolít el az adatmező szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="ddb23-109">The **Remove-AzDataBoxEdgeTrigger** cmdlet removes an existing trigger on the Data Box Edge device.</span></span>

## <span data-ttu-id="ddb23-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ddb23-110">EXAMPLES</span></span>

### <span data-ttu-id="ddb23-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ddb23-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="ddb23-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ddb23-112">PARAMETERS</span></span>

### <span data-ttu-id="ddb23-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddb23-113">-AsJob</span></span>
<span data-ttu-id="ddb23-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ddb23-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddb23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb23-115">-DefaultProfile</span></span>
<span data-ttu-id="ddb23-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ddb23-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddb23-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ddb23-117">-DeviceName</span></span>
<span data-ttu-id="ddb23-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="ddb23-118">Device Name</span></span>

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

### <span data-ttu-id="ddb23-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddb23-119">-InputObject</span></span>
<span data-ttu-id="ddb23-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="ddb23-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddb23-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ddb23-121">-Name</span></span>
<span data-ttu-id="ddb23-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="ddb23-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddb23-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddb23-123">-PassThru</span></span>
<span data-ttu-id="ddb23-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="ddb23-124">returns true if successful</span></span>

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

### <span data-ttu-id="ddb23-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddb23-125">-ResourceGroupName</span></span>
<span data-ttu-id="ddb23-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ddb23-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ddb23-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddb23-127">-ResourceId</span></span>
<span data-ttu-id="ddb23-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddb23-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddb23-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ddb23-129">-Confirm</span></span>
<span data-ttu-id="ddb23-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ddb23-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddb23-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddb23-131">-WhatIf</span></span>
<span data-ttu-id="ddb23-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ddb23-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddb23-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ddb23-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddb23-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb23-134">CommonParameters</span></span>
<span data-ttu-id="ddb23-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ddb23-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb23-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ddb23-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb23-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddb23-137">INPUTS</span></span>

### <span data-ttu-id="ddb23-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ddb23-138">System.String</span></span>

### <span data-ttu-id="ddb23-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="ddb23-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="ddb23-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddb23-140">OUTPUTS</span></span>

### <span data-ttu-id="ddb23-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ddb23-141">System.Boolean</span></span>

## <span data-ttu-id="ddb23-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ddb23-142">NOTES</span></span>

## <span data-ttu-id="ddb23-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ddb23-143">RELATED LINKS</span></span>
