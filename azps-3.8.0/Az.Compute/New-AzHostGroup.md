---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: f83a52281cbe244e91b22300b7f10582d6ca6349
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011459"
---
# <span data-ttu-id="1666f-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="1666f-101">New-AzHostGroup</span></span>

## <span data-ttu-id="1666f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1666f-102">SYNOPSIS</span></span>
<span data-ttu-id="1666f-103">Egy állomás-csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1666f-103">Creates a host group.</span></span>

## <span data-ttu-id="1666f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1666f-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1666f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1666f-105">DESCRIPTION</span></span>
<span data-ttu-id="1666f-106">Ezzel a parancsmaggal létrejön egy állomás-csoport.</span><span class="sxs-lookup"><span data-stu-id="1666f-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="1666f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1666f-107">EXAMPLES</span></span>

### <span data-ttu-id="1666f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1666f-108">Example 1</span></span>
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

<span data-ttu-id="1666f-109">Ez a parancs létrehoz egy állomás-csoportot az adott helyen és zónában.</span><span class="sxs-lookup"><span data-stu-id="1666f-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="1666f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1666f-110">PARAMETERS</span></span>

### <span data-ttu-id="1666f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1666f-111">-AsJob</span></span>
<span data-ttu-id="1666f-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1666f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1666f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1666f-113">-DefaultProfile</span></span>
<span data-ttu-id="1666f-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1666f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1666f-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="1666f-115">-Location</span></span>
<span data-ttu-id="1666f-116">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="1666f-116">Specifies location.</span></span>

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

### <span data-ttu-id="1666f-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1666f-117">-Name</span></span>
<span data-ttu-id="1666f-118">A Host csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1666f-118">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="1666f-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="1666f-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="1666f-120">Annak a hibának a tartományát adja meg, amennyit a Host-csoport átterjedhet.</span><span class="sxs-lookup"><span data-stu-id="1666f-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="1666f-121">A minimális érték 1, a maximális érték pedig 3.</span><span class="sxs-lookup"><span data-stu-id="1666f-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="1666f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1666f-122">-ResourceGroupName</span></span>
<span data-ttu-id="1666f-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1666f-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="1666f-124">-Címke</span><span class="sxs-lookup"><span data-stu-id="1666f-124">-Tag</span></span>
<span data-ttu-id="1666f-125">Címkéket ad meg</span><span class="sxs-lookup"><span data-stu-id="1666f-125">Specifies Tags</span></span>

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

### <span data-ttu-id="1666f-126">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="1666f-126">-Zone</span></span>
<span data-ttu-id="1666f-127">Az állomás csoport zónáit adja meg.</span><span class="sxs-lookup"><span data-stu-id="1666f-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="1666f-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1666f-128">-Confirm</span></span>
<span data-ttu-id="1666f-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1666f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1666f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1666f-130">-WhatIf</span></span>
<span data-ttu-id="1666f-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1666f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1666f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1666f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1666f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1666f-133">CommonParameters</span></span>
<span data-ttu-id="1666f-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1666f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1666f-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1666f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1666f-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1666f-136">INPUTS</span></span>

### <span data-ttu-id="1666f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1666f-137">System.String</span></span>

## <span data-ttu-id="1666f-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1666f-138">OUTPUTS</span></span>

### <span data-ttu-id="1666f-139">Microsoft. Azure. commands. számítási. Automation. models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="1666f-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="1666f-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1666f-140">NOTES</span></span>

## <span data-ttu-id="1666f-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1666f-141">RELATED LINKS</span></span>
