---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376373"
---
# <span data-ttu-id="10754-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="10754-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="10754-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10754-102">SYNOPSIS</span></span>
 <span data-ttu-id="10754-103">IpRules vagy VirtualNetworkRules hozzáadása egy tárfiók NetworkRule tulajdonságához</span><span class="sxs-lookup"><span data-stu-id="10754-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="10754-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="10754-104">SYNTAX</span></span>

### <span data-ttu-id="10754-105">NetWorkRuleString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="10754-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10754-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="10754-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10754-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="10754-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10754-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="10754-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10754-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="10754-109">DESCRIPTION</span></span>
<span data-ttu-id="10754-110">Az **Add-AzStorageAccountNetworkRule** parancsmag hozzáadja az IpRules vagy a VirtualNetworkRules értéket egy tárfiók NetworkRule tulajdonságához.</span><span class="sxs-lookup"><span data-stu-id="10754-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="10754-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="10754-111">EXAMPLES</span></span>

### <span data-ttu-id="10754-112">1. példa: Több IpRules hozzáadása az IPAddressOrRange protokollhoz</span><span class="sxs-lookup"><span data-stu-id="10754-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="10754-113">Ez a parancs több IpRules-t is hozzáad az IPAddressOrRange protokollal.</span><span class="sxs-lookup"><span data-stu-id="10754-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="10754-114">2. példa: VirtualNetworkRule hozzáadása VirtualNetworkResourceID-val</span><span class="sxs-lookup"><span data-stu-id="10754-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="10754-115">Ez a parancs virtualnetworkRule-t ad hozzá VirtualNetworkResourceID-val.</span><span class="sxs-lookup"><span data-stu-id="10754-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="10754-116">3. példa: VirtualNetworkRules hozzáadása virtualnetworkrule-objektumokkal egy másik fiókból</span><span class="sxs-lookup"><span data-stu-id="10754-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="10754-117">Ez a parancs hozzáadja a VirtualNetworkRules-t egy másik fiók VirtualNetworkRule-objektumaihoz.</span><span class="sxs-lookup"><span data-stu-id="10754-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="10754-118">4. példa: Több IpRule hozzáadása IpRule-objektumokkal, bevitel JSON-nal</span><span class="sxs-lookup"><span data-stu-id="10754-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="10754-119">Ez a parancs több IpRule-et ad hozzá IpRule-objektumokkal, JSON-bemenettel.</span><span class="sxs-lookup"><span data-stu-id="10754-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="10754-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10754-120">PARAMETERS</span></span>

### <span data-ttu-id="10754-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10754-121">-AsJob</span></span>
<span data-ttu-id="10754-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="10754-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10754-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10754-123">-DefaultProfile</span></span>
<span data-ttu-id="10754-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10754-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10754-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="10754-125">-IPAddressOrRange</span></span>
<span data-ttu-id="10754-126">Az IpAddressOrRange tömbje adja hozzá az IpRules értéket a bemeneti IpAddressOrRange és az alapértelmezett Allow to NetworkRule tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="10754-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="10754-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="10754-127">-IPRule</span></span>
<span data-ttu-id="10754-128">A NetworkRule tulajdonsághoz hozzáadandó IpRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="10754-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="10754-129">-Name</span><span class="sxs-lookup"><span data-stu-id="10754-129">-Name</span></span>
<span data-ttu-id="10754-130">A Tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10754-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="10754-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10754-131">-ResourceGroupName</span></span>
<span data-ttu-id="10754-132">A Tárfiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10754-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="10754-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="10754-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="10754-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span><span class="sxs-lookup"><span data-stu-id="10754-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="10754-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="10754-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="10754-136">A NetworkRule tulajdonsághoz hozzáadandó VirtualNetworkRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="10754-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="10754-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10754-137">-Confirm</span></span>
<span data-ttu-id="10754-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="10754-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10754-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10754-139">-WhatIf</span></span>
<span data-ttu-id="10754-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="10754-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10754-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="10754-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10754-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10754-142">CommonParameters</span></span>
<span data-ttu-id="10754-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10754-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10754-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10754-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10754-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10754-145">INPUTS</span></span>

### <span data-ttu-id="10754-146">System.String</span><span class="sxs-lookup"><span data-stu-id="10754-146">System.String</span></span>

### <span data-ttu-id="10754-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="10754-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="10754-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="10754-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="10754-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10754-149">OUTPUTS</span></span>

### <span data-ttu-id="10754-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="10754-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="10754-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="10754-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="10754-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="10754-152">NOTES</span></span>

## <span data-ttu-id="10754-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10754-153">RELATED LINKS</span></span>
