---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: 9f8d098cb27532980b01cf46da6c83d4da30ed48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673090"
---
# <span data-ttu-id="5ea94-101">Add-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5ea94-101">Add-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="5ea94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ea94-102">SYNOPSIS</span></span>
 <span data-ttu-id="5ea94-103">IpRules vagy VirtualNetworkRules hozzáadása a NetworkRule tulajdonságához</span><span class="sxs-lookup"><span data-stu-id="5ea94-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ea94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ea94-104">SYNTAX</span></span>

### <span data-ttu-id="5ea94-105">NetWorkRuleString (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ea94-105">NetWorkRuleString (Default)</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ea94-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="5ea94-106">IpRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ea94-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="5ea94-107">NetworkRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ea94-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="5ea94-108">IpRuleString</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ea94-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ea94-109">DESCRIPTION</span></span>
<span data-ttu-id="5ea94-110">A **Add-AzureRmStorageAccountNetworkRule** parancsmag IpRules vagy VirtualNetworkRules ad az NetworkRule tulajdonsághoz.</span><span class="sxs-lookup"><span data-stu-id="5ea94-110">The **Add-AzureRmStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="5ea94-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5ea94-111">EXAMPLES</span></span>

### <span data-ttu-id="5ea94-112">1. példa: több IpRules hozzáadása a IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5ea94-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="5ea94-113">Ez a parancs több IpRules adhat hozzá a IPAddressOrRange-hoz.</span><span class="sxs-lookup"><span data-stu-id="5ea94-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="5ea94-114">2. példa: VirtualNetworkRule hozzáadása a VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="5ea94-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzureRmVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzureRmVirtualNetworkSubnetConfig
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="5ea94-115">Ezzel a paranccsal VirtualNetworkRule adhat hozzá a VirtualNetworkResourceID-hoz.</span><span class="sxs-lookup"><span data-stu-id="5ea94-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="5ea94-116">3. példa: VirtualNetworkRules felvétele más fiókból származó VirtualNetworkRule-objektumokkal</span><span class="sxs-lookup"><span data-stu-id="5ea94-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzureRMStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount1"
PS C:\> Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="5ea94-117">Ezzel a paranccsal VirtualNetworkRules adhat hozzá a VirtualNetworkRule-objektumokból egy másik fiókból.</span><span class="sxs-lookup"><span data-stu-id="5ea94-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="5ea94-118">4. példa: több IpRule hozzáadása IpRule-objektumokhoz, JSON-bevitel</span><span class="sxs-lookup"><span data-stu-id="5ea94-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="5ea94-119">Ez a parancs több IpRule adhat hozzá IpRule objektumokkal, a JSON-szal.</span><span class="sxs-lookup"><span data-stu-id="5ea94-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="5ea94-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ea94-120">PARAMETERS</span></span>

### <span data-ttu-id="5ea94-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5ea94-121">-IPAddressOrRange</span></span>
<span data-ttu-id="5ea94-122">A IpAddressOrRange tömbje, a beviteli IpAddressOrRange és az alapértelmezett művelettel IpRules adja hozzá az NetworkRule tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="5ea94-122">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="5ea94-123">-IPRule</span><span class="sxs-lookup"><span data-stu-id="5ea94-123">-IPRule</span></span>
<span data-ttu-id="5ea94-124">A NetworkRule tulajdonságba felvenni kívánt IpRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="5ea94-124">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="5ea94-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ea94-125">-Name</span></span>
<span data-ttu-id="5ea94-126">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ea94-126">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="5ea94-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea94-127">-ResourceGroupName</span></span>
<span data-ttu-id="5ea94-128">Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="5ea94-128">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="5ea94-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5ea94-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="5ea94-130">A VirtualNetworkResourceId tömbje hozzáadja a VirtualNetworkRule a beviteli VirtualNetworkResourceId és az alapértelmezett művelettel NetworkRule tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="5ea94-130">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="5ea94-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5ea94-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="5ea94-132">A NetworkRule tulajdonságba felvenni kívánt VirtualNetworkRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="5ea94-132">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="5ea94-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ea94-133">-Confirm</span></span>
<span data-ttu-id="5ea94-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ea94-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ea94-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ea94-135">-WhatIf</span></span>
<span data-ttu-id="5ea94-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ea94-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ea94-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ea94-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ea94-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea94-138">-DefaultProfile</span></span>
<span data-ttu-id="5ea94-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ea94-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ea94-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea94-140">CommonParameters</span></span>
<span data-ttu-id="5ea94-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ea94-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea94-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ea94-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea94-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ea94-143">INPUTS</span></span>

### <span data-ttu-id="5ea94-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5ea94-144">System.String</span></span>
<span data-ttu-id="5ea94-145">Microsoft. Azure. Command. Management. Storage. models. PSIpRule [] Microsoft. Azure. commands. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="5ea94-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="5ea94-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ea94-146">OUTPUTS</span></span>

### <span data-ttu-id="5ea94-147">Microsoft. Azure. Command. Management. Storage. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5ea94-147">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>
<span data-ttu-id="5ea94-148">Microsoft. Azure. Command. Management. Storage. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="5ea94-148">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="5ea94-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ea94-149">NOTES</span></span>

## <span data-ttu-id="5ea94-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ea94-150">RELATED LINKS</span></span>

