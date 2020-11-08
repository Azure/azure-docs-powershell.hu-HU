---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 1eeaf3a7c9d0c4b5715bc5b75e42e53a8fa98c5e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195033"
---
# <span data-ttu-id="41535-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="41535-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="41535-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41535-102">SYNOPSIS</span></span>
<span data-ttu-id="41535-103">IpRules vagy VirtualNetworkRules eltávolítása a NetWorkRule tulajdonságból</span><span class="sxs-lookup"><span data-stu-id="41535-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="41535-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41535-104">SYNTAX</span></span>

### <span data-ttu-id="41535-105">NetWorkRuleString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41535-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41535-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="41535-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41535-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="41535-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41535-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="41535-108">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41535-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="41535-109">DESCRIPTION</span></span>
<span data-ttu-id="41535-110">A **Remove-AzStorageAccountNetworkRule** parancsmag eltávolítja a IpRules vagy a VirtualNetworkRules a NetWorkRule tulajdonságból.</span><span class="sxs-lookup"><span data-stu-id="41535-110">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="41535-111">Példák</span><span class="sxs-lookup"><span data-stu-id="41535-111">EXAMPLES</span></span>

### <span data-ttu-id="41535-112">1. példa: több IpRules eltávolítása a IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="41535-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="41535-113">Ez a parancs több IpRules távolít el a IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="41535-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="41535-114">2. példa: VirtualNetworkRule eltávolítása a VirtualNetworkRule objektum bevitelével JSON-val</span><span class="sxs-lookup"><span data-stu-id="41535-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="41535-115">Ez a parancs eltávolítja a VirtualNetworkRule a VirtualNetworkRule objektum bevitelével a JSON-szal.</span><span class="sxs-lookup"><span data-stu-id="41535-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="41535-116">3. példa: az első IpRule eltávolítása a csővezetéktel</span><span class="sxs-lookup"><span data-stu-id="41535-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="41535-117">Ez a parancs eltávolítja az első IpRule a futószalagról.</span><span class="sxs-lookup"><span data-stu-id="41535-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="41535-118">4. példa: több VirtualNetworkRules eltávolítása a VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="41535-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="41535-119">Ez a parancs több VirtualNetworkRules távolít el a VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="41535-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="41535-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41535-120">PARAMETERS</span></span>

### <span data-ttu-id="41535-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41535-121">-AsJob</span></span>
<span data-ttu-id="41535-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="41535-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41535-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41535-123">-DefaultProfile</span></span>
<span data-ttu-id="41535-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41535-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41535-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="41535-125">-IPAddressOrRange</span></span>
<span data-ttu-id="41535-126">A IpAddressOrRange tömbje eltávolítja a NetWorkRule tulajdonsággal azonos IpAddressOrRange IpRule.</span><span class="sxs-lookup"><span data-stu-id="41535-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="41535-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="41535-127">-IPRule</span></span>
<span data-ttu-id="41535-128">A NetWorkRule tulajdonságból eltávolítandó IpRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="41535-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="41535-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41535-129">-Name</span></span>
<span data-ttu-id="41535-130">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41535-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="41535-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41535-131">-ResourceGroupName</span></span>
<span data-ttu-id="41535-132">Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="41535-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="41535-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="41535-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="41535-134">A VirtualNetworkResourceId tömbje eltávolítja a NetWorkRule tulajdonsággal azonos VirtualNetworkResourceId VirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="41535-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="41535-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="41535-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="41535-136">A NetWorkRule tulajdonságból eltávolítandó VirtualNetworkRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="41535-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="41535-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="41535-137">-Confirm</span></span>
<span data-ttu-id="41535-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="41535-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41535-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41535-139">-WhatIf</span></span>
<span data-ttu-id="41535-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="41535-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41535-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41535-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41535-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41535-142">CommonParameters</span></span>
<span data-ttu-id="41535-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41535-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41535-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41535-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41535-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41535-145">INPUTS</span></span>

### <span data-ttu-id="41535-146">System. String</span><span class="sxs-lookup"><span data-stu-id="41535-146">System.String</span></span>

### <span data-ttu-id="41535-147">Microsoft. Azure. Command. Management. Storage. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="41535-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="41535-148">Microsoft. Azure. Command. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="41535-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="41535-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41535-149">OUTPUTS</span></span>

### <span data-ttu-id="41535-150">Microsoft. Azure. Command. Management. Storage. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="41535-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="41535-151">Microsoft. Azure. Command. Management. Storage. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="41535-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="41535-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41535-152">NOTES</span></span>

## <span data-ttu-id="41535-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41535-153">RELATED LINKS</span></span>