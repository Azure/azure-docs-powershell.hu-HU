---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: b6ec1908af93642cf064b72b1a78a64641749409
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492981"
---
# <span data-ttu-id="60ad3-101">Add-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="60ad3-101">Add-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="60ad3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60ad3-102">SYNOPSIS</span></span>
 <span data-ttu-id="60ad3-103">IpRules vagy VirtualNetworkRules hozzáadása a NetworkRule tulajdonságához</span><span class="sxs-lookup"><span data-stu-id="60ad3-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60ad3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60ad3-104">SYNTAX</span></span>

### <span data-ttu-id="60ad3-105">NetWorkRuleString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="60ad3-105">NetWorkRuleString (Default)</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60ad3-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="60ad3-106">IpRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60ad3-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="60ad3-107">NetworkRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60ad3-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="60ad3-108">IpRuleString</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60ad3-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="60ad3-109">DESCRIPTION</span></span>
<span data-ttu-id="60ad3-110">A **Add-AzureRmStorageAccountNetworkRule** parancsmag IpRules vagy VirtualNetworkRules ad az NetworkRule tulajdonsághoz.</span><span class="sxs-lookup"><span data-stu-id="60ad3-110">The **Add-AzureRmStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="60ad3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="60ad3-111">EXAMPLES</span></span>

### <span data-ttu-id="60ad3-112">1. példa: több IpRules hozzáadása a IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="60ad3-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="60ad3-113">Ez a parancs több IpRules adhat hozzá a IPAddressOrRange-hoz.</span><span class="sxs-lookup"><span data-stu-id="60ad3-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="60ad3-114">2. példa: VirtualNetworkRule hozzáadása a VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="60ad3-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzureRmVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzureRmVirtualNetworkSubnetConfig
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="60ad3-115">Ezzel a paranccsal VirtualNetworkRule adhat hozzá a VirtualNetworkResourceID-hoz.</span><span class="sxs-lookup"><span data-stu-id="60ad3-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="60ad3-116">3. példa: VirtualNetworkRules felvétele más fiókból származó VirtualNetworkRule-objektumokkal</span><span class="sxs-lookup"><span data-stu-id="60ad3-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzureRMStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount1"
PS C:\> Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="60ad3-117">Ezzel a paranccsal VirtualNetworkRules adhat hozzá a VirtualNetworkRule-objektumokból egy másik fiókból.</span><span class="sxs-lookup"><span data-stu-id="60ad3-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="60ad3-118">4. példa: több IpRule hozzáadása IpRule-objektumokhoz, JSON-bevitel</span><span class="sxs-lookup"><span data-stu-id="60ad3-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="60ad3-119">Ez a parancs több IpRule adhat hozzá IpRule objektumokkal, a JSON-szal.</span><span class="sxs-lookup"><span data-stu-id="60ad3-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="60ad3-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60ad3-120">PARAMETERS</span></span>

### <span data-ttu-id="60ad3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60ad3-121">-AsJob</span></span>
<span data-ttu-id="60ad3-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="60ad3-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ad3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ad3-123">-DefaultProfile</span></span>
<span data-ttu-id="60ad3-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60ad3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ad3-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="60ad3-125">-IPAddressOrRange</span></span>
<span data-ttu-id="60ad3-126">A IpAddressOrRange tömbje, a beviteli IpAddressOrRange és az alapértelmezett művelettel IpRules adja hozzá az NetworkRule tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="60ad3-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

```yaml
Type: String[]
Parameter Sets: IpRuleString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ad3-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="60ad3-127">-IPRule</span></span>
<span data-ttu-id="60ad3-128">A NetworkRule tulajdonságba felvenni kívánt IpRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="60ad3-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: PSIpRule[]
Parameter Sets: IpRuleObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60ad3-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="60ad3-129">-Name</span></span>
<span data-ttu-id="60ad3-130">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="60ad3-130">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60ad3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60ad3-131">-ResourceGroupName</span></span>
<span data-ttu-id="60ad3-132">Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="60ad3-132">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60ad3-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="60ad3-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="60ad3-134">A VirtualNetworkResourceId tömbje hozzáadja a VirtualNetworkRule a beviteli VirtualNetworkResourceId és az alapértelmezett művelettel NetworkRule tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="60ad3-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

```yaml
Type: String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ad3-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="60ad3-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="60ad3-136">A NetworkRule tulajdonságba felvenni kívánt VirtualNetworkRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="60ad3-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60ad3-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="60ad3-137">-Confirm</span></span>
<span data-ttu-id="60ad3-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60ad3-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ad3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60ad3-139">-WhatIf</span></span>
<span data-ttu-id="60ad3-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="60ad3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60ad3-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60ad3-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ad3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ad3-142">CommonParameters</span></span>
<span data-ttu-id="60ad3-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60ad3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ad3-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60ad3-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ad3-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60ad3-145">INPUTS</span></span>

### <span data-ttu-id="60ad3-146">System. String</span><span class="sxs-lookup"><span data-stu-id="60ad3-146">System.String</span></span>
<span data-ttu-id="60ad3-147">Microsoft. Azure. Command. Management. Storage. models. PSIpRule [] Microsoft. Azure. commands. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="60ad3-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="60ad3-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60ad3-148">OUTPUTS</span></span>

### <span data-ttu-id="60ad3-149">Microsoft. Azure. Command. Management. Storage. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="60ad3-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>
<span data-ttu-id="60ad3-150">Microsoft. Azure. Command. Management. Storage. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="60ad3-150">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="60ad3-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60ad3-151">NOTES</span></span>

## <span data-ttu-id="60ad3-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60ad3-152">RELATED LINKS</span></span>

