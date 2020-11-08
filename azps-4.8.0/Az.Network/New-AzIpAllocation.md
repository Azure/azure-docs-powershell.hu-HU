---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181576"
---
# <span data-ttu-id="410e7-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="410e7-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="410e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="410e7-102">SYNOPSIS</span></span>
<span data-ttu-id="410e7-103">Azure-IpAllocation hoz létre.</span><span class="sxs-lookup"><span data-stu-id="410e7-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="410e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="410e7-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="410e7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="410e7-105">DESCRIPTION</span></span>
<span data-ttu-id="410e7-106">A **New-AzIpAllocation** parancsmag létrehoz egy Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="410e7-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="410e7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="410e7-107">EXAMPLES</span></span>

### <span data-ttu-id="410e7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="410e7-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="410e7-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="410e7-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="410e7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="410e7-110">PARAMETERS</span></span>

### <span data-ttu-id="410e7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="410e7-111">-AsJob</span></span>
<span data-ttu-id="410e7-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="410e7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="410e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="410e7-113">-DefaultProfile</span></span>
<span data-ttu-id="410e7-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="410e7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="410e7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="410e7-115">-Force</span></span>
<span data-ttu-id="410e7-116">Ha egy erőforrást felül szeretne bírálni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="410e7-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="410e7-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="410e7-117">-IpAllocationTag</span></span>
<span data-ttu-id="410e7-118">Az IP-kiosztás kiosztási címkéi</span><span class="sxs-lookup"><span data-stu-id="410e7-118">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="410e7-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="410e7-119">-IpAllocationType</span></span>
<span data-ttu-id="410e7-120">Az IP-kiosztás típusa</span><span class="sxs-lookup"><span data-stu-id="410e7-120">The type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hypernet, Undefined

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="410e7-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="410e7-121">-IpamAllocationId</span></span>
<span data-ttu-id="410e7-122">Az IP-kiosztás IPAM-allokációs azonosítója</span><span class="sxs-lookup"><span data-stu-id="410e7-122">The ipam allocation ID of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="410e7-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="410e7-123">-Location</span></span>
<span data-ttu-id="410e7-124">helyre.</span><span class="sxs-lookup"><span data-stu-id="410e7-124">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="410e7-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="410e7-125">-Name</span></span>
<span data-ttu-id="410e7-126">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="410e7-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="410e7-127">-Prefix</span><span class="sxs-lookup"><span data-stu-id="410e7-127">-Prefix</span></span>
<span data-ttu-id="410e7-128">Az IP-kiosztás előtagja</span><span class="sxs-lookup"><span data-stu-id="410e7-128">The prefix of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="410e7-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="410e7-129">-PrefixLength</span></span>
<span data-ttu-id="410e7-130">Az IP-kiosztás előtag-hossza</span><span class="sxs-lookup"><span data-stu-id="410e7-130">The prefix length of the IP allocation</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="410e7-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="410e7-131">-PrefixType</span></span>
<span data-ttu-id="410e7-132">Az IP-kiosztás előtag-típusa</span><span class="sxs-lookup"><span data-stu-id="410e7-132">The prefix type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPV4, IPV6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="410e7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="410e7-133">-ResourceGroupName</span></span>
<span data-ttu-id="410e7-134">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="410e7-134">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="410e7-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="410e7-135">-Tag</span></span>
<span data-ttu-id="410e7-136">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="410e7-136">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="410e7-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="410e7-137">-Confirm</span></span>
<span data-ttu-id="410e7-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="410e7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="410e7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="410e7-139">-WhatIf</span></span>
<span data-ttu-id="410e7-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="410e7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="410e7-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="410e7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="410e7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="410e7-142">CommonParameters</span></span>
<span data-ttu-id="410e7-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="410e7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="410e7-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="410e7-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="410e7-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="410e7-145">INPUTS</span></span>

### <span data-ttu-id="410e7-146">System. String</span><span class="sxs-lookup"><span data-stu-id="410e7-146">System.String</span></span>

### <span data-ttu-id="410e7-147">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="410e7-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="410e7-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="410e7-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="410e7-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="410e7-149">OUTPUTS</span></span>

### <span data-ttu-id="410e7-150">Microsoft. Azure. commands. Network. models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="410e7-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="410e7-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="410e7-151">NOTES</span></span>

## <span data-ttu-id="410e7-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="410e7-152">RELATED LINKS</span></span>
