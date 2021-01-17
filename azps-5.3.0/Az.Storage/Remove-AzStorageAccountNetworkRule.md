---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 1eeaf3a7c9d0c4b5715bc5b75e42e53a8fa98c5e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466920"
---
# <span data-ttu-id="bd2bb-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bd2bb-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="bd2bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd2bb-102">SYNOPSIS</span></span>
<span data-ttu-id="bd2bb-103">IpRules vagy VirtualNetworkRules eltávolítása egy tárfiók NetWorkRule tulajdonságában</span><span class="sxs-lookup"><span data-stu-id="bd2bb-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="bd2bb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd2bb-104">SYNTAX</span></span>

### <span data-ttu-id="bd2bb-105">NetWorkRuleString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd2bb-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd2bb-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="bd2bb-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd2bb-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="bd2bb-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd2bb-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="bd2bb-108">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd2bb-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd2bb-109">DESCRIPTION</span></span>
<span data-ttu-id="bd2bb-110">A **Remove-AzStorageAccountNetworkRule** parancsmag eltávolítja az IpRules vagy a VirtualNetworkRules tartományt egy tárfiók NetWorkRule tulajdonságában.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-110">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="bd2bb-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd2bb-111">EXAMPLES</span></span>

### <span data-ttu-id="bd2bb-112">1. példa: Több IpRules eltávolítása IPAddressOrRange-val</span><span class="sxs-lookup"><span data-stu-id="bd2bb-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="bd2bb-113">Ez a parancs eltávolít több IPRules ipAddressOrRange-t.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="bd2bb-114">2. példa: VirtualNetworkRule eltávolítása VirtualNetworkRule objektumbemenettel JSON-nal</span><span class="sxs-lookup"><span data-stu-id="bd2bb-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="bd2bb-115">Ez a parancs eltávolítja a VirtualNetworkRule-et VirtualNetworkRule objektum-bevitelsel JSON-nal.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="bd2bb-116">3. példa: Az első IpRule eltávolítása a prognózissal</span><span class="sxs-lookup"><span data-stu-id="bd2bb-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="bd2bb-117">Ez a parancs eltávolítja a prognózissal együtt az első IpRule-et.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="bd2bb-118">4. példa: Több VirtualNetworkRules eltávolítása VirtualNetworkResourceID értékekkel</span><span class="sxs-lookup"><span data-stu-id="bd2bb-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="bd2bb-119">Ez a parancs eltávolít több VirtualNetworkRulest VirtualNetworkResourceID értékekkel.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="bd2bb-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd2bb-120">PARAMETERS</span></span>

### <span data-ttu-id="bd2bb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd2bb-121">-AsJob</span></span>
<span data-ttu-id="bd2bb-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bd2bb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd2bb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd2bb-123">-DefaultProfile</span></span>
<span data-ttu-id="bd2bb-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd2bb-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="bd2bb-125">-IPAddressOrRange</span></span>
<span data-ttu-id="bd2bb-126">Az IpAddressOrRange tömb eltávolítja az azonos IpAddressOrRange ipRule értékeket a NetWorkRule tulajdonságból.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd2bb-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="bd2bb-127">-IPRule</span></span>
<span data-ttu-id="bd2bb-128">A NetWorkRule tulajdonságból eltávolítandó IpRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd2bb-129">-Name</span><span class="sxs-lookup"><span data-stu-id="bd2bb-129">-Name</span></span>
<span data-ttu-id="bd2bb-130">A Tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-130">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd2bb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd2bb-131">-ResourceGroupName</span></span>
<span data-ttu-id="bd2bb-132">A Tárfiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="bd2bb-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="bd2bb-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="bd2bb-134">A VirtualNetworkResourceId tömbje eltávolítja a VirtualNetworkRule értékeket ugyanazokkal a VirtualNetworkResourceId értékekkel a NetWorkRule tulajdonságból.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd2bb-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bd2bb-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="bd2bb-136">A NetWorkRule tulajdonságból eltávolítandó VirtualNetworkRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd2bb-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd2bb-137">-Confirm</span></span>
<span data-ttu-id="bd2bb-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd2bb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd2bb-139">-WhatIf</span></span>
<span data-ttu-id="bd2bb-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd2bb-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd2bb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd2bb-142">CommonParameters</span></span>
<span data-ttu-id="bd2bb-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd2bb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd2bb-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd2bb-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd2bb-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd2bb-145">INPUTS</span></span>

### <span data-ttu-id="bd2bb-146">System.String</span><span class="sxs-lookup"><span data-stu-id="bd2bb-146">System.String</span></span>

### <span data-ttu-id="bd2bb-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="bd2bb-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="bd2bb-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="bd2bb-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="bd2bb-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd2bb-149">OUTPUTS</span></span>

### <span data-ttu-id="bd2bb-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bd2bb-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="bd2bb-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="bd2bb-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="bd2bb-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd2bb-152">NOTES</span></span>

## <span data-ttu-id="bd2bb-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd2bb-153">RELATED LINKS</span></span>
