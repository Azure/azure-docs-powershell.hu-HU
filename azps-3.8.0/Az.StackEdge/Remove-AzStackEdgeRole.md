---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013477"
---
# <span data-ttu-id="38beb-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="38beb-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="38beb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38beb-102">SYNOPSIS</span></span>
<span data-ttu-id="38beb-103">Eltávolítja az eszközhöz tartozó IoT szerepkört.</span><span class="sxs-lookup"><span data-stu-id="38beb-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="38beb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38beb-104">SYNTAX</span></span>

### <span data-ttu-id="38beb-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38beb-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38beb-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38beb-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38beb-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38beb-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38beb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="38beb-108">DESCRIPTION</span></span>
<span data-ttu-id="38beb-109">A **Remove-AzStackEdgeRole** parancsmag eltávolítja a kapcsolódó IoT szerepkört egy halom Edge-eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="38beb-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="38beb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="38beb-110">EXAMPLES</span></span>

### <span data-ttu-id="38beb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="38beb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="38beb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38beb-112">PARAMETERS</span></span>

### <span data-ttu-id="38beb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38beb-113">-AsJob</span></span>
<span data-ttu-id="38beb-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="38beb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38beb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38beb-115">-DefaultProfile</span></span>
<span data-ttu-id="38beb-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38beb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38beb-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="38beb-117">-DeviceName</span></span>
<span data-ttu-id="38beb-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="38beb-118">Device Name</span></span>

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

### <span data-ttu-id="38beb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38beb-119">-InputObject</span></span>
<span data-ttu-id="38beb-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="38beb-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38beb-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38beb-121">-Name</span></span>
<span data-ttu-id="38beb-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="38beb-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38beb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38beb-123">-PassThru</span></span>
<span data-ttu-id="38beb-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="38beb-124">returns true if successful</span></span>

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

### <span data-ttu-id="38beb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38beb-125">-ResourceGroupName</span></span>
<span data-ttu-id="38beb-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="38beb-126">Resource Group Name</span></span>

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

### <span data-ttu-id="38beb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38beb-127">-ResourceId</span></span>
<span data-ttu-id="38beb-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="38beb-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="38beb-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="38beb-129">-Confirm</span></span>
<span data-ttu-id="38beb-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="38beb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38beb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38beb-131">-WhatIf</span></span>
<span data-ttu-id="38beb-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="38beb-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38beb-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38beb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38beb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38beb-134">CommonParameters</span></span>
<span data-ttu-id="38beb-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38beb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38beb-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="38beb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38beb-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38beb-137">INPUTS</span></span>

### <span data-ttu-id="38beb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="38beb-138">System.String</span></span>

### <span data-ttu-id="38beb-139">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="38beb-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="38beb-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38beb-140">OUTPUTS</span></span>

### <span data-ttu-id="38beb-141">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="38beb-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="38beb-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38beb-142">NOTES</span></span>

## <span data-ttu-id="38beb-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38beb-143">RELATED LINKS</span></span>
