---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379104"
---
# <span data-ttu-id="86deb-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="86deb-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="86deb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86deb-102">SYNOPSIS</span></span>
<span data-ttu-id="86deb-103">Létrehoz egy Azure IpAllocationt.</span><span class="sxs-lookup"><span data-stu-id="86deb-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="86deb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="86deb-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86deb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="86deb-105">DESCRIPTION</span></span>
<span data-ttu-id="86deb-106">A **New-AzIpAllocation** parancsmag létrehoz egy Azure IpAllocation-t</span><span class="sxs-lookup"><span data-stu-id="86deb-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="86deb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="86deb-107">EXAMPLES</span></span>

### <span data-ttu-id="86deb-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="86deb-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="86deb-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="86deb-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="86deb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86deb-110">PARAMETERS</span></span>

### <span data-ttu-id="86deb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86deb-111">-AsJob</span></span>
<span data-ttu-id="86deb-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="86deb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86deb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86deb-113">-DefaultProfile</span></span>
<span data-ttu-id="86deb-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86deb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86deb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="86deb-115">-Force</span></span>
<span data-ttu-id="86deb-116">Ne kérjen megerősítést, ha felül szeretne bírálni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="86deb-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="86deb-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="86deb-117">-IpAllocationTag</span></span>
<span data-ttu-id="86deb-118">Az IP-kiosztás hozzárendelési címkéi</span><span class="sxs-lookup"><span data-stu-id="86deb-118">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="86deb-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="86deb-119">-IpAllocationType</span></span>
<span data-ttu-id="86deb-120">Az IP-kiosztás típusa</span><span class="sxs-lookup"><span data-stu-id="86deb-120">The type of the IP allocation</span></span>

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

### <span data-ttu-id="86deb-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="86deb-121">-IpamAllocationId</span></span>
<span data-ttu-id="86deb-122">Az IP-kiosztás IPam-kiosztási azonosítója</span><span class="sxs-lookup"><span data-stu-id="86deb-122">The ipam allocation ID of the IP allocation</span></span>

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

### <span data-ttu-id="86deb-123">-Location</span><span class="sxs-lookup"><span data-stu-id="86deb-123">-Location</span></span>
<span data-ttu-id="86deb-124">helyére.</span><span class="sxs-lookup"><span data-stu-id="86deb-124">location.</span></span>

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

### <span data-ttu-id="86deb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="86deb-125">-Name</span></span>
<span data-ttu-id="86deb-126">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="86deb-126">The resource name.</span></span>

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

### <span data-ttu-id="86deb-127">-Előtag</span><span class="sxs-lookup"><span data-stu-id="86deb-127">-Prefix</span></span>
<span data-ttu-id="86deb-128">Az IP-kiosztás előtagja</span><span class="sxs-lookup"><span data-stu-id="86deb-128">The prefix of the IP allocation</span></span>

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

### <span data-ttu-id="86deb-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="86deb-129">-PrefixLength</span></span>
<span data-ttu-id="86deb-130">Az IP-kiosztás előtaghossza</span><span class="sxs-lookup"><span data-stu-id="86deb-130">The prefix length of the IP allocation</span></span>

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

### <span data-ttu-id="86deb-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="86deb-131">-PrefixType</span></span>
<span data-ttu-id="86deb-132">Az IP-kiosztás előtagtípusa</span><span class="sxs-lookup"><span data-stu-id="86deb-132">The prefix type of the IP allocation</span></span>

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

### <span data-ttu-id="86deb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86deb-133">-ResourceGroupName</span></span>
<span data-ttu-id="86deb-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="86deb-134">The resource group name.</span></span>

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

### <span data-ttu-id="86deb-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="86deb-135">-Tag</span></span>
<span data-ttu-id="86deb-136">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="86deb-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="86deb-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86deb-137">-Confirm</span></span>
<span data-ttu-id="86deb-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="86deb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86deb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86deb-139">-WhatIf</span></span>
<span data-ttu-id="86deb-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="86deb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86deb-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86deb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86deb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86deb-142">CommonParameters</span></span>
<span data-ttu-id="86deb-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86deb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86deb-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86deb-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86deb-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86deb-145">INPUTS</span></span>

### <span data-ttu-id="86deb-146">System.String</span><span class="sxs-lookup"><span data-stu-id="86deb-146">System.String</span></span>

### <span data-ttu-id="86deb-147">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="86deb-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="86deb-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="86deb-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="86deb-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86deb-149">OUTPUTS</span></span>

### <span data-ttu-id="86deb-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="86deb-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="86deb-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="86deb-151">NOTES</span></span>

## <span data-ttu-id="86deb-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86deb-152">RELATED LINKS</span></span>
