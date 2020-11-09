---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302960"
---
# <span data-ttu-id="0e562-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0e562-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="0e562-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e562-102">SYNOPSIS</span></span>
 <span data-ttu-id="0e562-103">IpRules vagy VirtualNetworkRules hozzáadása a NetworkRule tulajdonságához</span><span class="sxs-lookup"><span data-stu-id="0e562-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="0e562-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e562-104">SYNTAX</span></span>

### <span data-ttu-id="0e562-105">NetWorkRuleString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0e562-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e562-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="0e562-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e562-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="0e562-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e562-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="0e562-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e562-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e562-109">DESCRIPTION</span></span>
<span data-ttu-id="0e562-110">A **Add-AzStorageAccountNetworkRule** parancsmag IpRules vagy VirtualNetworkRules ad az NetworkRule tulajdonsághoz.</span><span class="sxs-lookup"><span data-stu-id="0e562-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="0e562-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0e562-111">EXAMPLES</span></span>

### <span data-ttu-id="0e562-112">1. példa: több IpRules hozzáadása a IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="0e562-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="0e562-113">Ez a parancs több IpRules adhat hozzá a IPAddressOrRange-hoz.</span><span class="sxs-lookup"><span data-stu-id="0e562-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="0e562-114">2. példa: VirtualNetworkRule hozzáadása a VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="0e562-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="0e562-115">Ezzel a paranccsal VirtualNetworkRule adhat hozzá a VirtualNetworkResourceID-hoz.</span><span class="sxs-lookup"><span data-stu-id="0e562-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="0e562-116">3. példa: VirtualNetworkRules felvétele más fiókból származó VirtualNetworkRule-objektumokkal</span><span class="sxs-lookup"><span data-stu-id="0e562-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="0e562-117">Ezzel a paranccsal VirtualNetworkRules adhat hozzá a VirtualNetworkRule-objektumokból egy másik fiókból.</span><span class="sxs-lookup"><span data-stu-id="0e562-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="0e562-118">4. példa: több IpRule hozzáadása IpRule-objektumokhoz, JSON-bevitel</span><span class="sxs-lookup"><span data-stu-id="0e562-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="0e562-119">Ez a parancs több IpRule adhat hozzá IpRule objektumokkal, a JSON-szal.</span><span class="sxs-lookup"><span data-stu-id="0e562-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="0e562-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e562-120">PARAMETERS</span></span>

### <span data-ttu-id="0e562-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e562-121">-AsJob</span></span>
<span data-ttu-id="0e562-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0e562-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e562-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e562-123">-DefaultProfile</span></span>
<span data-ttu-id="0e562-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e562-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e562-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="0e562-125">-IPAddressOrRange</span></span>
<span data-ttu-id="0e562-126">A IpAddressOrRange tömbje, a beviteli IpAddressOrRange és az alapértelmezett művelettel IpRules adja hozzá az NetworkRule tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="0e562-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="0e562-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="0e562-127">-IPRule</span></span>
<span data-ttu-id="0e562-128">A NetworkRule tulajdonságba felvenni kívánt IpRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="0e562-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="0e562-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0e562-129">-Name</span></span>
<span data-ttu-id="0e562-130">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e562-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="0e562-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e562-131">-ResourceGroupName</span></span>
<span data-ttu-id="0e562-132">Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="0e562-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="0e562-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="0e562-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="0e562-134">A VirtualNetworkResourceId tömbje hozzáadja a VirtualNetworkRule a beviteli VirtualNetworkResourceId és az alapértelmezett művelettel NetworkRule tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="0e562-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="0e562-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0e562-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="0e562-136">A NetworkRule tulajdonságba felvenni kívánt VirtualNetworkRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="0e562-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="0e562-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0e562-137">-Confirm</span></span>
<span data-ttu-id="0e562-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0e562-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e562-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e562-139">-WhatIf</span></span>
<span data-ttu-id="0e562-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0e562-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e562-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e562-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e562-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e562-142">CommonParameters</span></span>
<span data-ttu-id="0e562-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e562-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e562-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e562-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e562-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e562-145">INPUTS</span></span>

### <span data-ttu-id="0e562-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0e562-146">System.String</span></span>

### <span data-ttu-id="0e562-147">Microsoft. Azure. Command. Management. Storage. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="0e562-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="0e562-148">Microsoft. Azure. Command. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="0e562-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="0e562-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e562-149">OUTPUTS</span></span>

### <span data-ttu-id="0e562-150">Microsoft. Azure. Command. Management. Storage. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0e562-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="0e562-151">Microsoft. Azure. Command. Management. Storage. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="0e562-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="0e562-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e562-152">NOTES</span></span>

## <span data-ttu-id="0e562-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e562-153">RELATED LINKS</span></span>
