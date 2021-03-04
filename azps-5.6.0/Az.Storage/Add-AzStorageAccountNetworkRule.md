---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 0104c64bf65acc945609f4e2e0ae78ff288b142d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930705"
---
# <span data-ttu-id="6beb9-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6beb9-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="6beb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6beb9-102">SYNOPSIS</span></span>
 <span data-ttu-id="6beb9-103">IpRules vagy VirtualNetworkRules hozzáadása egy tárfiók NetworkRule tulajdonságához</span><span class="sxs-lookup"><span data-stu-id="6beb9-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="6beb9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6beb9-104">SYNTAX</span></span>

### <span data-ttu-id="6beb9-105">NetWorkRuleString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6beb9-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6beb9-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="6beb9-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6beb9-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="6beb9-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6beb9-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="6beb9-108">ResourceAccessRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6beb9-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="6beb9-109">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6beb9-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="6beb9-110">ResourceAccessRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6beb9-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6beb9-111">DESCRIPTION</span></span>
<span data-ttu-id="6beb9-112">Az **Add-AzStorageAccountNetworkRule** parancsmag hozzáadja az IpRules vagy a VirtualNetworkRules értéket egy tárfiók NetworkRule tulajdonságához.</span><span class="sxs-lookup"><span data-stu-id="6beb9-112">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="6beb9-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6beb9-113">EXAMPLES</span></span>

### <span data-ttu-id="6beb9-114">1. példa: Több IpRules hozzáadása az IPAddressOrRange-val</span><span class="sxs-lookup"><span data-stu-id="6beb9-114">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="6beb9-115">Ez a parancs több IpRules-t is hozzáad az IPAddressOrRange protokollal.</span><span class="sxs-lookup"><span data-stu-id="6beb9-115">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="6beb9-116">2. példa: VirtualNetworkRule hozzáadása VirtualNetworkResourceID-val</span><span class="sxs-lookup"><span data-stu-id="6beb9-116">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="6beb9-117">Ez a parancs virtualnetworkRule-t ad hozzá VirtualNetworkResourceID-val.</span><span class="sxs-lookup"><span data-stu-id="6beb9-117">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="6beb9-118">3. példa: VirtualNetworkRules hozzáadása virtualnetworkrule-objektumokkal egy másik fiókból</span><span class="sxs-lookup"><span data-stu-id="6beb9-118">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="6beb9-119">Ez a parancs hozzáadja a VirtualNetworkRules-t egy másik fiók VirtualNetworkRule-objektumaihoz.</span><span class="sxs-lookup"><span data-stu-id="6beb9-119">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="6beb9-120">4. példa: Több IpRule hozzáadása IpRule-objektumokkal, bevitel JSON-nal</span><span class="sxs-lookup"><span data-stu-id="6beb9-120">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="6beb9-121">Ez a parancs több IpRule-et ad hozzá IpRule-objektumokkal, és JSON-t ad meg.</span><span class="sxs-lookup"><span data-stu-id="6beb9-121">This command add several IpRule with IpRule objects, input with JSON.</span></span>

### <span data-ttu-id="6beb9-122">5. példa: Erőforrás-hozzáférési szabály hozzáadása</span><span class="sxs-lookup"><span data-stu-id="6beb9-122">Example 5: Add a resource access rule</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="6beb9-123">Ez a parancs hozzáad egy erőforrás-hozzáférési szabályt a TenantId és az ResourceId beállítással.</span><span class="sxs-lookup"><span data-stu-id="6beb9-123">This command adds a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="6beb9-124">6. példa: Az egyik tárfiók összes erőforrás-hozzáférési szabályának hozzáadása egy másik tárfiókhoz</span><span class="sxs-lookup"><span data-stu-id="6beb9-124">Example 6: Add all resource access rules of one storage account to another storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1").ResourceAccessRules | Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2"
```

<span data-ttu-id="6beb9-125">Ez a parancs egy tárhelyfiók összes erőforrás-hozzáférési szabályát beveszi, és hozzáadja őket egy másik tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="6beb9-125">This command gets all resource access rules from one storage account, and adds them to another storage account.</span></span>

## <span data-ttu-id="6beb9-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6beb9-126">PARAMETERS</span></span>

### <span data-ttu-id="6beb9-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6beb9-127">-AsJob</span></span>
<span data-ttu-id="6beb9-128">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6beb9-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6beb9-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6beb9-129">-DefaultProfile</span></span>
<span data-ttu-id="6beb9-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6beb9-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6beb9-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="6beb9-131">-IPAddressOrRange</span></span>
<span data-ttu-id="6beb9-132">Az IpAddressOrRange tömbje adja hozzá az IpRules értéket a bemeneti IpAddressOrRange és az alapértelmezett Allow to NetworkRule tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="6beb9-132">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="6beb9-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="6beb9-133">-IPRule</span></span>
<span data-ttu-id="6beb9-134">A NetworkRule tulajdonsághoz hozzáadandó IpRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="6beb9-134">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="6beb9-135">-Name</span><span class="sxs-lookup"><span data-stu-id="6beb9-135">-Name</span></span>
<span data-ttu-id="6beb9-136">A Tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6beb9-136">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="6beb9-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="6beb9-137">-ResourceAccessRule</span></span>
<span data-ttu-id="6beb9-138">Tárfiók NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="6beb9-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

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

### <span data-ttu-id="6beb9-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6beb9-139">-ResourceGroupName</span></span>
<span data-ttu-id="6beb9-140">A Tárfiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6beb9-140">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="6beb9-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6beb9-141">-ResourceId</span></span>
<span data-ttu-id="6beb9-142">Storage Account ResourceAccessRule ResourceId in string.</span><span class="sxs-lookup"><span data-stu-id="6beb9-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

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

### <span data-ttu-id="6beb9-143">-TenantId</span><span class="sxs-lookup"><span data-stu-id="6beb9-143">-TenantId</span></span>
<span data-ttu-id="6beb9-144">Storage Account ResourceAccessRule TenantId in string.</span><span class="sxs-lookup"><span data-stu-id="6beb9-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

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

### <span data-ttu-id="6beb9-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="6beb9-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="6beb9-146">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span><span class="sxs-lookup"><span data-stu-id="6beb9-146">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="6beb9-147">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6beb9-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="6beb9-148">A NetworkRule tulajdonsághoz hozzáadandó VirtualNetworkRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="6beb9-148">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="6beb9-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6beb9-149">-Confirm</span></span>
<span data-ttu-id="6beb9-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6beb9-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6beb9-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6beb9-151">-WhatIf</span></span>
<span data-ttu-id="6beb9-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6beb9-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6beb9-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6beb9-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6beb9-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6beb9-154">CommonParameters</span></span>
<span data-ttu-id="6beb9-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6beb9-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6beb9-156">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6beb9-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6beb9-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6beb9-157">INPUTS</span></span>

### <span data-ttu-id="6beb9-158">System.String</span><span class="sxs-lookup"><span data-stu-id="6beb9-158">System.String</span></span>

### <span data-ttu-id="6beb9-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="6beb9-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="6beb9-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="6beb9-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="6beb9-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6beb9-161">OUTPUTS</span></span>

### <span data-ttu-id="6beb9-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6beb9-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="6beb9-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="6beb9-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="6beb9-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6beb9-164">NOTES</span></span>

## <span data-ttu-id="6beb9-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6beb9-165">RELATED LINKS</span></span>
