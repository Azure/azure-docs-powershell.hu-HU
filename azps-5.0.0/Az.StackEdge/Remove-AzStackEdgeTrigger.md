---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
ms.openlocfilehash: ad2761e4e0fba3ef7dbb7a28b15477a649891042
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186359"
---
# <span data-ttu-id="adbb3-101">Remove-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="adbb3-101">Remove-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="adbb3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="adbb3-102">SYNOPSIS</span></span>
<span data-ttu-id="adbb3-103">Eltávolít egy meglévő triggert az eszközön.</span><span class="sxs-lookup"><span data-stu-id="adbb3-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="adbb3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="adbb3-104">SYNTAX</span></span>

### <span data-ttu-id="adbb3-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="adbb3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adbb3-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="adbb3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adbb3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adbb3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-InputObject] <PSStackEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adbb3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="adbb3-108">DESCRIPTION</span></span>
<span data-ttu-id="adbb3-109">A **Remove-AzStackEdgeTrigger** parancsmag eltávolítja a meglévő triggert a halom szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="adbb3-109">The **Remove-AzStackEdgeTrigger** cmdlet removes an existing trigger on the Stack Edge device.</span></span>

## <span data-ttu-id="adbb3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="adbb3-110">EXAMPLES</span></span>

### <span data-ttu-id="adbb3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="adbb3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="adbb3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="adbb3-112">PARAMETERS</span></span>

### <span data-ttu-id="adbb3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="adbb3-113">-AsJob</span></span>
<span data-ttu-id="adbb3-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="adbb3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="adbb3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adbb3-115">-DefaultProfile</span></span>
<span data-ttu-id="adbb3-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="adbb3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adbb3-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="adbb3-117">-DeviceName</span></span>
<span data-ttu-id="adbb3-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="adbb3-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adbb3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adbb3-119">-InputObject</span></span>
<span data-ttu-id="adbb3-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="adbb3-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Trigger

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adbb3-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="adbb3-121">-Name</span></span>
<span data-ttu-id="adbb3-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="adbb3-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adbb3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adbb3-123">-PassThru</span></span>
<span data-ttu-id="adbb3-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="adbb3-124">returns true if successful</span></span>

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

### <span data-ttu-id="adbb3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adbb3-125">-ResourceGroupName</span></span>
<span data-ttu-id="adbb3-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="adbb3-126">Resource Group Name</span></span>

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

### <span data-ttu-id="adbb3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adbb3-127">-ResourceId</span></span>
<span data-ttu-id="adbb3-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="adbb3-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="adbb3-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="adbb3-129">-Confirm</span></span>
<span data-ttu-id="adbb3-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="adbb3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adbb3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adbb3-131">-WhatIf</span></span>
<span data-ttu-id="adbb3-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="adbb3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="adbb3-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="adbb3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adbb3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adbb3-134">CommonParameters</span></span>
<span data-ttu-id="adbb3-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="adbb3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adbb3-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="adbb3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adbb3-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="adbb3-137">INPUTS</span></span>

### <span data-ttu-id="adbb3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="adbb3-138">System.String</span></span>

### <span data-ttu-id="adbb3-139">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="adbb3-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="adbb3-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adbb3-140">OUTPUTS</span></span>

### <span data-ttu-id="adbb3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="adbb3-141">System.Boolean</span></span>

## <span data-ttu-id="adbb3-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="adbb3-142">NOTES</span></span>

## <span data-ttu-id="adbb3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adbb3-143">RELATED LINKS</span></span>
