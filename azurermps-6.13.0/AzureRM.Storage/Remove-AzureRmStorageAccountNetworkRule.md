---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: 73f096c516bb285b89e45d90107ff6a3ad406dbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680298"
---
# <span data-ttu-id="5170c-101">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5170c-101">Remove-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="5170c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5170c-102">SYNOPSIS</span></span>
<span data-ttu-id="5170c-103">IpRules vagy VirtualNetworkRules eltávolítása a NetWorkRule tulajdonságból</span><span class="sxs-lookup"><span data-stu-id="5170c-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5170c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5170c-104">SYNTAX</span></span>

### <span data-ttu-id="5170c-105">NetWorkRuleString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5170c-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5170c-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="5170c-106">IpRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5170c-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="5170c-107">NetworkRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5170c-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="5170c-108">IpRuleString</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5170c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5170c-109">DESCRIPTION</span></span>
<span data-ttu-id="5170c-110">A **Remove-AzureRmStorageAccountNetworkRule** parancsmag eltávolítja a IpRules vagy a VirtualNetworkRules a NetWorkRule tulajdonságból.</span><span class="sxs-lookup"><span data-stu-id="5170c-110">The **Remove-AzureRmStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="5170c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5170c-111">EXAMPLES</span></span>

### <span data-ttu-id="5170c-112">1. példa: több IpRules eltávolítása a IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5170c-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="5170c-113">Ez a parancs több IpRules távolít el a IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="5170c-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="5170c-114">2. példa: VirtualNetworkRule eltávolítása a VirtualNetworkRule objektum bevitelével JSON-val</span><span class="sxs-lookup"><span data-stu-id="5170c-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="5170c-115">Ez a parancs eltávolítja a VirtualNetworkRule a VirtualNetworkRule objektum bevitelével a JSON-szal.</span><span class="sxs-lookup"><span data-stu-id="5170c-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="5170c-116">3. példa: az első IpRule eltávolítása a csővezetéktel</span><span class="sxs-lookup"><span data-stu-id="5170c-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="5170c-117">Ez a parancs eltávolítja az első IpRule a futószalagról.</span><span class="sxs-lookup"><span data-stu-id="5170c-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="5170c-118">4. példa: több VirtualNetworkRules eltávolítása a VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="5170c-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="5170c-119">Ez a parancs több VirtualNetworkRules távolít el a VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="5170c-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="5170c-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5170c-120">PARAMETERS</span></span>

### <span data-ttu-id="5170c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5170c-121">-AsJob</span></span>
<span data-ttu-id="5170c-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5170c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5170c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5170c-123">-DefaultProfile</span></span>
<span data-ttu-id="5170c-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5170c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5170c-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5170c-125">-IPAddressOrRange</span></span>
<span data-ttu-id="5170c-126">A IpAddressOrRange tömbje eltávolítja a NetWorkRule tulajdonsággal azonos IpAddressOrRange IpRule.</span><span class="sxs-lookup"><span data-stu-id="5170c-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="5170c-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="5170c-127">-IPRule</span></span>
<span data-ttu-id="5170c-128">A NetWorkRule tulajdonságból eltávolítandó IpRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="5170c-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="5170c-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5170c-129">-Name</span></span>
<span data-ttu-id="5170c-130">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5170c-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="5170c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5170c-131">-ResourceGroupName</span></span>
<span data-ttu-id="5170c-132">Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="5170c-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="5170c-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5170c-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="5170c-134">A VirtualNetworkResourceId tömbje eltávolítja a NetWorkRule tulajdonsággal azonos VirtualNetworkResourceId VirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="5170c-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="5170c-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5170c-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="5170c-136">A NetWorkRule tulajdonságból eltávolítandó VirtualNetworkRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="5170c-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="5170c-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5170c-137">-Confirm</span></span>
<span data-ttu-id="5170c-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5170c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5170c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5170c-139">-WhatIf</span></span>
<span data-ttu-id="5170c-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5170c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5170c-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5170c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5170c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5170c-142">CommonParameters</span></span>
<span data-ttu-id="5170c-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5170c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5170c-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5170c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5170c-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5170c-145">INPUTS</span></span>

### <span data-ttu-id="5170c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="5170c-146">System.String</span></span>

### <span data-ttu-id="5170c-147">Microsoft. Azure. Command. Management. Storage. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="5170c-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="5170c-148">Paraméterek: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5170c-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="5170c-149">Microsoft. Azure. Command. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="5170c-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="5170c-150">Paraméterek: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5170c-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="5170c-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5170c-151">OUTPUTS</span></span>

### <span data-ttu-id="5170c-152">Microsoft. Azure. Command. Management. Storage. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5170c-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="5170c-153">Microsoft. Azure. Command. Management. Storage. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="5170c-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="5170c-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5170c-154">NOTES</span></span>

## <span data-ttu-id="5170c-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5170c-155">RELATED LINKS</span></span>
