---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156843"
---
# <span data-ttu-id="5ef58-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="5ef58-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="5ef58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ef58-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef58-103">Egy Azure IpAllocation törlése.</span><span class="sxs-lookup"><span data-stu-id="5ef58-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="5ef58-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5ef58-104">SYNTAX</span></span>

### <span data-ttu-id="5ef58-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ef58-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ef58-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ef58-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ef58-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ef58-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ef58-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5ef58-108">DESCRIPTION</span></span>
<span data-ttu-id="5ef58-109">Az **Remove-AzIpAllocation** parancsmag töröl egy Azure IpAllocation-t</span><span class="sxs-lookup"><span data-stu-id="5ef58-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="5ef58-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5ef58-110">EXAMPLES</span></span>

### <span data-ttu-id="5ef58-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="5ef58-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="5ef58-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ef58-112">PARAMETERS</span></span>

### <span data-ttu-id="5ef58-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ef58-113">-AsJob</span></span>
<span data-ttu-id="5ef58-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5ef58-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ef58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef58-115">-DefaultProfile</span></span>
<span data-ttu-id="5ef58-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ef58-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ef58-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5ef58-117">-Force</span></span>
<span data-ttu-id="5ef58-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ef58-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5ef58-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ef58-119">-InputObject</span></span>
<span data-ttu-id="5ef58-120">{{ Fill InputObject Description }}</span><span class="sxs-lookup"><span data-stu-id="5ef58-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef58-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5ef58-121">-Name</span></span>
<span data-ttu-id="5ef58-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5ef58-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef58-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ef58-123">-PassThru</span></span>
<span data-ttu-id="5ef58-124">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="5ef58-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5ef58-125">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5ef58-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5ef58-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ef58-126">-ResourceGroupName</span></span>
<span data-ttu-id="5ef58-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5ef58-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef58-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ef58-128">-ResourceId</span></span>
<span data-ttu-id="5ef58-129">IpAllocation resource id.</span><span class="sxs-lookup"><span data-stu-id="5ef58-129">IpAllocation resource id.</span></span>

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

### <span data-ttu-id="5ef58-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ef58-130">-Confirm</span></span>
<span data-ttu-id="5ef58-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5ef58-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ef58-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ef58-132">-WhatIf</span></span>
<span data-ttu-id="5ef58-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5ef58-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ef58-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ef58-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ef58-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef58-135">CommonParameters</span></span>
<span data-ttu-id="5ef58-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ef58-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef58-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ef58-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef58-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ef58-138">INPUTS</span></span>

### <span data-ttu-id="5ef58-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5ef58-139">System.String</span></span>

## <span data-ttu-id="5ef58-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ef58-140">OUTPUTS</span></span>

### <span data-ttu-id="5ef58-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ef58-141">System.Boolean</span></span>

## <span data-ttu-id="5ef58-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5ef58-142">NOTES</span></span>

## <span data-ttu-id="5ef58-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ef58-143">RELATED LINKS</span></span>
