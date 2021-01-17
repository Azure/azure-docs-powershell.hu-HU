---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 2fdb5317504bb1bc08ed45e8224a30a61cca8e8c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477729"
---
# <span data-ttu-id="72509-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="72509-101">New-AzHostGroup</span></span>

## <span data-ttu-id="72509-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72509-102">SYNOPSIS</span></span>
<span data-ttu-id="72509-103">Állomáscsoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="72509-103">Creates a host group.</span></span>

## <span data-ttu-id="72509-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="72509-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72509-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="72509-105">DESCRIPTION</span></span>
<span data-ttu-id="72509-106">Ez a parancsmag gazdacsoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="72509-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="72509-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="72509-107">EXAMPLES</span></span>

### <span data-ttu-id="72509-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="72509-108">Example 1</span></span>
```
PS C:\> New-AzHostGroup -ResourceGroupName $resourceGroupName -Name $hostGroupName -Location $location -Zone $zone

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="72509-109">Ez a parancs létrehoz egy állomáscsoportot a megadott helyen és zónában.</span><span class="sxs-lookup"><span data-stu-id="72509-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="72509-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72509-110">PARAMETERS</span></span>

### <span data-ttu-id="72509-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72509-111">-AsJob</span></span>
<span data-ttu-id="72509-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="72509-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72509-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72509-113">-DefaultProfile</span></span>
<span data-ttu-id="72509-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72509-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72509-115">-Location</span><span class="sxs-lookup"><span data-stu-id="72509-115">-Location</span></span>
<span data-ttu-id="72509-116">Megadja a helyet.</span><span class="sxs-lookup"><span data-stu-id="72509-116">Specifies location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72509-117">-Name</span><span class="sxs-lookup"><span data-stu-id="72509-117">-Name</span></span>
<span data-ttu-id="72509-118">A gazdacsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72509-118">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72509-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="72509-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="72509-120">Megadja, hogy az állomáscsoport hány hibatartományt képes átfogni.</span><span class="sxs-lookup"><span data-stu-id="72509-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="72509-121">A minimális érték 1, a maximális érték pedig 3.</span><span class="sxs-lookup"><span data-stu-id="72509-121">The minimum value is 1 and the maximum value is 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72509-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72509-122">-ResourceGroupName</span></span>
<span data-ttu-id="72509-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="72509-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72509-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="72509-124">-Tag</span></span>
<span data-ttu-id="72509-125">Címkék megadása</span><span class="sxs-lookup"><span data-stu-id="72509-125">Specifies Tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72509-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="72509-126">-Zone</span></span>
<span data-ttu-id="72509-127">Az állomáscsoport zónáit adja meg.</span><span class="sxs-lookup"><span data-stu-id="72509-127">Specifies Zones of the host group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72509-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="72509-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="72509-129">Azt adja meg, hogy a HostGroup engedélyezi-e a virtuális gép automatikus elhelyezését.</span><span class="sxs-lookup"><span data-stu-id="72509-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="72509-130">Az automatikus elhelyezés azt jelenti, hogy ezek a virtuális gépek az Azure által kiválasztott dedikált állomásokon, a dedikált gazdacsoport alatt helyezték el őket.</span><span class="sxs-lookup"><span data-stu-id="72509-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="72509-131">Ha nincs megadva, az alapértelmezett érték igaz lesz.</span><span class="sxs-lookup"><span data-stu-id="72509-131">If not specified, default value will be true.</span></span>

```yaml
Type: bool
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="72509-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72509-132">-Confirm</span></span>
<span data-ttu-id="72509-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="72509-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72509-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72509-134">-WhatIf</span></span>
<span data-ttu-id="72509-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="72509-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72509-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="72509-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72509-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72509-137">CommonParameters</span></span>
<span data-ttu-id="72509-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72509-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72509-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72509-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72509-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72509-140">INPUTS</span></span>

### <span data-ttu-id="72509-141">System.String</span><span class="sxs-lookup"><span data-stu-id="72509-141">System.String</span></span>

## <span data-ttu-id="72509-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72509-142">OUTPUTS</span></span>

### <span data-ttu-id="72509-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="72509-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="72509-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="72509-144">NOTES</span></span>

## <span data-ttu-id="72509-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72509-145">RELATED LINKS</span></span>
