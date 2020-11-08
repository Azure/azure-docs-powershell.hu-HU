---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194485"
---
# <span data-ttu-id="9adea-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="9adea-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="9adea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9adea-102">SYNOPSIS</span></span>
<span data-ttu-id="9adea-103">Eltávolítja az eszközhöz tartozó IoT szerepkört.</span><span class="sxs-lookup"><span data-stu-id="9adea-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="9adea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9adea-104">SYNTAX</span></span>

### <span data-ttu-id="9adea-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9adea-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9adea-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9adea-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9adea-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9adea-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9adea-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9adea-108">DESCRIPTION</span></span>
<span data-ttu-id="9adea-109">A **Remove-AzStackEdgeRole** parancsmag eltávolítja a kapcsolódó IoT szerepkört egy halom Edge-eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="9adea-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="9adea-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9adea-110">EXAMPLES</span></span>

### <span data-ttu-id="9adea-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9adea-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="9adea-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9adea-112">PARAMETERS</span></span>

### <span data-ttu-id="9adea-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9adea-113">-AsJob</span></span>
<span data-ttu-id="9adea-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9adea-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9adea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9adea-115">-DefaultProfile</span></span>
<span data-ttu-id="9adea-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9adea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9adea-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9adea-117">-DeviceName</span></span>
<span data-ttu-id="9adea-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="9adea-118">Device Name</span></span>

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

### <span data-ttu-id="9adea-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9adea-119">-InputObject</span></span>
<span data-ttu-id="9adea-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="9adea-120">Input Object</span></span>

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

### <span data-ttu-id="9adea-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9adea-121">-Name</span></span>
<span data-ttu-id="9adea-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="9adea-122">Resource Name</span></span>

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

### <span data-ttu-id="9adea-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9adea-123">-PassThru</span></span>
<span data-ttu-id="9adea-124">eredménye igaz, ha sikeres</span><span class="sxs-lookup"><span data-stu-id="9adea-124">returns true if successful</span></span>

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

### <span data-ttu-id="9adea-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9adea-125">-ResourceGroupName</span></span>
<span data-ttu-id="9adea-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="9adea-126">Resource Group Name</span></span>

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

### <span data-ttu-id="9adea-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9adea-127">-ResourceId</span></span>
<span data-ttu-id="9adea-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9adea-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="9adea-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9adea-129">-Confirm</span></span>
<span data-ttu-id="9adea-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9adea-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9adea-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9adea-131">-WhatIf</span></span>
<span data-ttu-id="9adea-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9adea-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9adea-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9adea-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9adea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9adea-134">CommonParameters</span></span>
<span data-ttu-id="9adea-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9adea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9adea-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9adea-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9adea-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9adea-137">INPUTS</span></span>

### <span data-ttu-id="9adea-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9adea-138">System.String</span></span>

### <span data-ttu-id="9adea-139">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="9adea-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="9adea-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9adea-140">OUTPUTS</span></span>

### <span data-ttu-id="9adea-141">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="9adea-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="9adea-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9adea-142">NOTES</span></span>

## <span data-ttu-id="9adea-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9adea-143">RELATED LINKS</span></span>
