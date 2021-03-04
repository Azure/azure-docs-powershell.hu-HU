---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 0c7325d43ca1e1aefa2ee4751cc90369e06beca6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928954"
---
# <span data-ttu-id="06d27-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="06d27-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="06d27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06d27-102">SYNOPSIS</span></span>
<span data-ttu-id="06d27-103">Létrehoz egy Azure IpAllocationt.</span><span class="sxs-lookup"><span data-stu-id="06d27-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="06d27-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="06d27-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06d27-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="06d27-105">DESCRIPTION</span></span>
<span data-ttu-id="06d27-106">A **New-AzIpAllocation** parancsmag létrehoz egy Azure IpAllocation-t</span><span class="sxs-lookup"><span data-stu-id="06d27-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="06d27-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="06d27-107">EXAMPLES</span></span>

### <span data-ttu-id="06d27-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="06d27-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="06d27-109">2. példa</span><span class="sxs-lookup"><span data-stu-id="06d27-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="06d27-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06d27-110">PARAMETERS</span></span>

### <span data-ttu-id="06d27-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06d27-111">-AsJob</span></span>
<span data-ttu-id="06d27-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="06d27-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06d27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d27-113">-DefaultProfile</span></span>
<span data-ttu-id="06d27-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06d27-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06d27-115">-Force</span><span class="sxs-lookup"><span data-stu-id="06d27-115">-Force</span></span>
<span data-ttu-id="06d27-116">Ne kérjen megerősítést, ha felül szeretne bírálni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="06d27-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="06d27-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="06d27-117">-IpAllocationTag</span></span>
<span data-ttu-id="06d27-118">Az IP-kiosztás hozzárendelési címkéi</span><span class="sxs-lookup"><span data-stu-id="06d27-118">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="06d27-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="06d27-119">-IpAllocationType</span></span>
<span data-ttu-id="06d27-120">Az IP-kiosztás típusa</span><span class="sxs-lookup"><span data-stu-id="06d27-120">The type of the IP allocation</span></span>

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

### <span data-ttu-id="06d27-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="06d27-121">-IpamAllocationId</span></span>
<span data-ttu-id="06d27-122">Az IP-kiosztás IPam-kiosztási azonosítója</span><span class="sxs-lookup"><span data-stu-id="06d27-122">The ipam allocation ID of the IP allocation</span></span>

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

### <span data-ttu-id="06d27-123">-Location</span><span class="sxs-lookup"><span data-stu-id="06d27-123">-Location</span></span>
<span data-ttu-id="06d27-124">helyére.</span><span class="sxs-lookup"><span data-stu-id="06d27-124">location.</span></span>

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

### <span data-ttu-id="06d27-125">-Name</span><span class="sxs-lookup"><span data-stu-id="06d27-125">-Name</span></span>
<span data-ttu-id="06d27-126">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="06d27-126">The resource name.</span></span>

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

### <span data-ttu-id="06d27-127">-Előtag</span><span class="sxs-lookup"><span data-stu-id="06d27-127">-Prefix</span></span>
<span data-ttu-id="06d27-128">Az IP-kiosztás előtagja</span><span class="sxs-lookup"><span data-stu-id="06d27-128">The prefix of the IP allocation</span></span>

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

### <span data-ttu-id="06d27-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="06d27-129">-PrefixLength</span></span>
<span data-ttu-id="06d27-130">Az IP-kiosztás előtaghossza</span><span class="sxs-lookup"><span data-stu-id="06d27-130">The prefix length of the IP allocation</span></span>

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

### <span data-ttu-id="06d27-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="06d27-131">-PrefixType</span></span>
<span data-ttu-id="06d27-132">Az IP-kiosztás előtagtípusa</span><span class="sxs-lookup"><span data-stu-id="06d27-132">The prefix type of the IP allocation</span></span>

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

### <span data-ttu-id="06d27-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d27-133">-ResourceGroupName</span></span>
<span data-ttu-id="06d27-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="06d27-134">The resource group name.</span></span>

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

### <span data-ttu-id="06d27-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="06d27-135">-Tag</span></span>
<span data-ttu-id="06d27-136">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="06d27-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="06d27-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06d27-137">-Confirm</span></span>
<span data-ttu-id="06d27-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="06d27-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06d27-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06d27-139">-WhatIf</span></span>
<span data-ttu-id="06d27-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="06d27-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06d27-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06d27-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06d27-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d27-142">CommonParameters</span></span>
<span data-ttu-id="06d27-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d27-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d27-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06d27-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d27-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06d27-145">INPUTS</span></span>

### <span data-ttu-id="06d27-146">System.String</span><span class="sxs-lookup"><span data-stu-id="06d27-146">System.String</span></span>

### <span data-ttu-id="06d27-147">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="06d27-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="06d27-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="06d27-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="06d27-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06d27-149">OUTPUTS</span></span>

### <span data-ttu-id="06d27-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="06d27-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="06d27-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="06d27-151">NOTES</span></span>

## <span data-ttu-id="06d27-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06d27-152">RELATED LINKS</span></span>
