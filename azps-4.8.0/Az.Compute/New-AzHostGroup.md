---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 2fdb5317504bb1bc08ed45e8224a30a61cca8e8c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024831"
---
# <span data-ttu-id="1c54d-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="1c54d-101">New-AzHostGroup</span></span>

## <span data-ttu-id="1c54d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c54d-102">SYNOPSIS</span></span>
<span data-ttu-id="1c54d-103">Egy állomás-csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1c54d-103">Creates a host group.</span></span>

## <span data-ttu-id="1c54d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c54d-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c54d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c54d-105">DESCRIPTION</span></span>
<span data-ttu-id="1c54d-106">Ezzel a parancsmaggal létrejön egy állomás-csoport.</span><span class="sxs-lookup"><span data-stu-id="1c54d-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="1c54d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1c54d-107">EXAMPLES</span></span>

### <span data-ttu-id="1c54d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1c54d-108">Example 1</span></span>
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

<span data-ttu-id="1c54d-109">Ez a parancs létrehoz egy állomás-csoportot az adott helyen és zónában.</span><span class="sxs-lookup"><span data-stu-id="1c54d-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="1c54d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c54d-110">PARAMETERS</span></span>

### <span data-ttu-id="1c54d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c54d-111">-AsJob</span></span>
<span data-ttu-id="1c54d-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1c54d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c54d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c54d-113">-DefaultProfile</span></span>
<span data-ttu-id="1c54d-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c54d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c54d-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="1c54d-115">-Location</span></span>
<span data-ttu-id="1c54d-116">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="1c54d-116">Specifies location.</span></span>

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

### <span data-ttu-id="1c54d-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1c54d-117">-Name</span></span>
<span data-ttu-id="1c54d-118">A Host csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c54d-118">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="1c54d-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="1c54d-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="1c54d-120">Annak a hibának a tartományát adja meg, amennyit a Host-csoport átterjedhet.</span><span class="sxs-lookup"><span data-stu-id="1c54d-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="1c54d-121">A minimális érték 1, a maximális érték pedig 3.</span><span class="sxs-lookup"><span data-stu-id="1c54d-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="1c54d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c54d-122">-ResourceGroupName</span></span>
<span data-ttu-id="1c54d-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1c54d-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="1c54d-124">-Címke</span><span class="sxs-lookup"><span data-stu-id="1c54d-124">-Tag</span></span>
<span data-ttu-id="1c54d-125">Címkéket ad meg</span><span class="sxs-lookup"><span data-stu-id="1c54d-125">Specifies Tags</span></span>

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

### <span data-ttu-id="1c54d-126">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="1c54d-126">-Zone</span></span>
<span data-ttu-id="1c54d-127">Az állomás csoport zónáit adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c54d-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="1c54d-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="1c54d-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="1c54d-129">Annak megadása, hogy a HostGroup engedélyezi-e a VM automatikus elhelyezését.</span><span class="sxs-lookup"><span data-stu-id="1c54d-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="1c54d-130">Automatikus elhelyezés: ezek a VMs az Azure által kiválasztott dedikált állomásokra kerülnek, a dedikált házigazda csoportban.</span><span class="sxs-lookup"><span data-stu-id="1c54d-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="1c54d-131">Ha nincs megadva, az alapértelmezett érték igaz lesz.</span><span class="sxs-lookup"><span data-stu-id="1c54d-131">If not specified, default value will be true.</span></span>

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


### <span data-ttu-id="1c54d-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1c54d-132">-Confirm</span></span>
<span data-ttu-id="1c54d-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1c54d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c54d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c54d-134">-WhatIf</span></span>
<span data-ttu-id="1c54d-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1c54d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c54d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1c54d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c54d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c54d-137">CommonParameters</span></span>
<span data-ttu-id="1c54d-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c54d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c54d-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1c54d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c54d-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c54d-140">INPUTS</span></span>

### <span data-ttu-id="1c54d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1c54d-141">System.String</span></span>

## <span data-ttu-id="1c54d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c54d-142">OUTPUTS</span></span>

### <span data-ttu-id="1c54d-143">Microsoft. Azure. commands. számítási. Automation. models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="1c54d-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="1c54d-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c54d-144">NOTES</span></span>

## <span data-ttu-id="1c54d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c54d-145">RELATED LINKS</span></span>
