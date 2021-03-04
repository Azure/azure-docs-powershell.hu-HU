---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 295f79f48ffa966024561486745cdcf52ec8e38f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929281"
---
# <span data-ttu-id="c1457-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c1457-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="c1457-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1457-102">SYNOPSIS</span></span>
<span data-ttu-id="c1457-103">IpRules vagy VirtualNetworkRules eltávolítása egy tárfiók NetWorkRule tulajdonságában</span><span class="sxs-lookup"><span data-stu-id="c1457-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="c1457-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c1457-104">SYNTAX</span></span>

### <span data-ttu-id="c1457-105">NetWorkRuleString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1457-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1457-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="c1457-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1457-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="c1457-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1457-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="c1457-108">ResourceAccessRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1457-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="c1457-109">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1457-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="c1457-110">ResourceAccessRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1457-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c1457-111">DESCRIPTION</span></span>
<span data-ttu-id="c1457-112">A **Remove-AzStorageAccountNetworkRule** parancsmag eltávolítja az IpRules vagy a VirtualNetworkRules tartományt egy tárfiók NetWorkRule tulajdonságában.</span><span class="sxs-lookup"><span data-stu-id="c1457-112">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="c1457-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c1457-113">EXAMPLES</span></span>

### <span data-ttu-id="c1457-114">1. példa: Több IpRules eltávolítása IPAddressOrRange-val</span><span class="sxs-lookup"><span data-stu-id="c1457-114">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="c1457-115">Ez a parancs eltávolít több IPRules ipAddressOrRange-t.</span><span class="sxs-lookup"><span data-stu-id="c1457-115">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="c1457-116">2. példa: VirtualNetworkRule eltávolítása VirtualNetworkRule objektumbemenettel JSON-nal</span><span class="sxs-lookup"><span data-stu-id="c1457-116">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="c1457-117">Ez a parancs eltávolítja a VirtualNetworkRule-et VirtualNetworkRule objektum-bevitelsel JSON-nal.</span><span class="sxs-lookup"><span data-stu-id="c1457-117">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="c1457-118">3. példa: Az első IpRule eltávolítása a prognózissal</span><span class="sxs-lookup"><span data-stu-id="c1457-118">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="c1457-119">Ez a parancs eltávolítja a prognózissal együtt az első IpRule-et.</span><span class="sxs-lookup"><span data-stu-id="c1457-119">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="c1457-120">4. példa: Több VirtualNetworkRules eltávolítása VirtualNetworkResourceID értékekkel</span><span class="sxs-lookup"><span data-stu-id="c1457-120">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="c1457-121">Ez a parancs eltávolít több VirtualNetworkRulest VirtualNetworkResourceID értékekkel.</span><span class="sxs-lookup"><span data-stu-id="c1457-121">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="c1457-122">5. példa: Erőforrás-hozzáférési szabály eltávolítása a TenantId és az ResourceId fiókkal.</span><span class="sxs-lookup"><span data-stu-id="c1457-122">Example 5: Remove a resource access rule with TenantId and ResourceId.</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"  -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="c1457-123">Ez a parancs eltávolít egy erőforrás-hozzáférési szabályt a TenantId és az ResourceId használatával.</span><span class="sxs-lookup"><span data-stu-id="c1457-123">This command removes a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="c1457-124">6. példa: Az első 3 erőforrás-hozzáférési szabály eltávolítása egy tárfiókból</span><span class="sxs-lookup"><span data-stu-id="c1457-124">Example 6: Remove the first 3 resource access rules from a storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount").ResourceAccessRules | Select-Object -First 3 | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="c1457-125">Ez a parancs eltávolítja az első 3 erőforrás-hozzáférési szabályt egy tárfiókból.</span><span class="sxs-lookup"><span data-stu-id="c1457-125">This command removes the first 3 resource access rules from a storage account.</span></span>

## <span data-ttu-id="c1457-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1457-126">PARAMETERS</span></span>

### <span data-ttu-id="c1457-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1457-127">-AsJob</span></span>
<span data-ttu-id="c1457-128">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c1457-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1457-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1457-129">-DefaultProfile</span></span>
<span data-ttu-id="c1457-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1457-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1457-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c1457-131">-IPAddressOrRange</span></span>
<span data-ttu-id="c1457-132">Az IpAddressOrRange tömb eltávolítja az azonos IpAddressOrRange ipRule értékeket a NetWorkRule tulajdonságból.</span><span class="sxs-lookup"><span data-stu-id="c1457-132">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="c1457-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="c1457-133">-IPRule</span></span>
<span data-ttu-id="c1457-134">A NetWorkRule tulajdonságból eltávolítandó IpRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="c1457-134">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="c1457-135">-Name</span><span class="sxs-lookup"><span data-stu-id="c1457-135">-Name</span></span>
<span data-ttu-id="c1457-136">A Tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1457-136">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="c1457-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="c1457-137">-ResourceAccessRule</span></span>
<span data-ttu-id="c1457-138">Tárfiók NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="c1457-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: ResourceAccessRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1457-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1457-139">-ResourceGroupName</span></span>
<span data-ttu-id="c1457-140">A Tárfiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1457-140">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="c1457-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1457-141">-ResourceId</span></span>
<span data-ttu-id="c1457-142">Storage Account ResourceAccessRule ResourceId in string.</span><span class="sxs-lookup"><span data-stu-id="c1457-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1457-143">-TenantId</span><span class="sxs-lookup"><span data-stu-id="c1457-143">-TenantId</span></span>
<span data-ttu-id="c1457-144">Storage Account ResourceAccessRule TenantId in string.</span><span class="sxs-lookup"><span data-stu-id="c1457-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1457-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="c1457-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="c1457-146">A VirtualNetworkResourceId tömbje eltávolítja a VirtualNetworkRule értékeket ugyanazokkal a VirtualNetworkResourceId értékekkel a NetWorkRule tulajdonságból.</span><span class="sxs-lookup"><span data-stu-id="c1457-146">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="c1457-147">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c1457-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="c1457-148">A NetWorkRule tulajdonságból eltávolítandó VirtualNetworkRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="c1457-148">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="c1457-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1457-149">-Confirm</span></span>
<span data-ttu-id="c1457-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c1457-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1457-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1457-151">-WhatIf</span></span>
<span data-ttu-id="c1457-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c1457-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1457-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1457-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1457-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1457-154">CommonParameters</span></span>
<span data-ttu-id="c1457-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1457-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1457-156">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1457-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1457-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1457-157">INPUTS</span></span>

### <span data-ttu-id="c1457-158">System.String</span><span class="sxs-lookup"><span data-stu-id="c1457-158">System.String</span></span>

### <span data-ttu-id="c1457-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="c1457-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="c1457-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="c1457-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="c1457-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1457-161">OUTPUTS</span></span>

### <span data-ttu-id="c1457-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c1457-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="c1457-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="c1457-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="c1457-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c1457-164">NOTES</span></span>

## <span data-ttu-id="c1457-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1457-165">RELATED LINKS</span></span>
