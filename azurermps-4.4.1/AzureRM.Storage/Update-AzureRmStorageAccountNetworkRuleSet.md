---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 09619247f41acb60180a7d3045afdcd689d5c183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679911"
---
# <span data-ttu-id="ce3d5-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ce3d5-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="ce3d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce3d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ce3d5-103">Tárolási fiók NetworkRule tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="ce3d5-103">Update the NetworkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce3d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce3d5-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce3d5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce3d5-105">DESCRIPTION</span></span>
<span data-ttu-id="ce3d5-106">Az **Update-AzureRmStorageAccountNetworkRuleSet** parancsmag frissíti a tárolási fiók NetworkRule tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="ce3d5-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="ce3d5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ce3d5-107">EXAMPLES</span></span>

### <span data-ttu-id="ce3d5-108">Példa 1: a NetworkRule összes tulajdonságának frissítése, beviteli szabályok a JSON-nal</span><span class="sxs-lookup"><span data-stu-id="ce3d5-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="ce3d5-109">Ez a parancs frissíti a NetworkRule összes tulajdonságát, valamint a JSON-szal való szövegbeviteli szabályokat.</span><span class="sxs-lookup"><span data-stu-id="ce3d5-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="ce3d5-110">2. példa: a NetworkRule frissítés megkerülése tulajdonsága</span><span class="sxs-lookup"><span data-stu-id="ce3d5-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="ce3d5-111">Ez a parancs frissíti a NetworkRule tulajdonságát (a többi tulajdonság nem változik).</span><span class="sxs-lookup"><span data-stu-id="ce3d5-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="ce3d5-112">3. példa: a NetworkRule szabályainak megtisztítása</span><span class="sxs-lookup"><span data-stu-id="ce3d5-112">Example 3: Clean up rules of NetworkRule of a Storage Account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="ce3d5-113">Ez a parancs megtisztítja a NetworkRule szabályait (a többi tulajdonság nem változik).</span><span class="sxs-lookup"><span data-stu-id="ce3d5-113">This command clean up rules of NetworkRule of a Storage Account (other properties not change).</span></span>

## <span data-ttu-id="ce3d5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce3d5-114">PARAMETERS</span></span>

### <span data-ttu-id="ce3d5-115">-Kitérő</span><span class="sxs-lookup"><span data-stu-id="ce3d5-115">-Bypass</span></span>
<span data-ttu-id="ce3d5-116">A NetworkRule tulajdonságra való frissítés megkerülő értéke.</span><span class="sxs-lookup"><span data-stu-id="ce3d5-116">The Bypass value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="ce3d5-117">Az engedélyezett érték nincs vagy a következő kombinációk egyike: â € ̆ naplózási â € ¢ Metrics â € ¢ Azureservices</span><span class="sxs-lookup"><span data-stu-id="ce3d5-117">The allowed value are none or any combination of: â€¢ Logging â€¢ Metrics â€¢ Azureservices</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases: 
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3d5-118">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="ce3d5-118">-DefaultAction</span></span>
<span data-ttu-id="ce3d5-119">A DefaultAction érték a NetworkRule tulajdonságra való frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="ce3d5-119">The DefaultAction value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="ce3d5-120">Az engedélyezett beállítások: â € ¢ Allow â € ¢ deny</span><span class="sxs-lookup"><span data-stu-id="ce3d5-120">The allowed Options: â€¢ Allow â€¢ Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3d5-121">-IPRule</span><span class="sxs-lookup"><span data-stu-id="ce3d5-121">-IPRule</span></span>
<span data-ttu-id="ce3d5-122">A IpRule objektumok tömbje, amely a tárolási fiók NetworkRule tulajdonságára frissíthető.</span><span class="sxs-lookup"><span data-stu-id="ce3d5-122">The Array of IpRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce3d5-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ce3d5-123">-Name</span></span>
<span data-ttu-id="ce3d5-124">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce3d5-124">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="ce3d5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce3d5-125">-ResourceGroupName</span></span>
<span data-ttu-id="ce3d5-126">Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="ce3d5-126">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="ce3d5-127">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce3d5-127">-VirtualNetworkRule</span></span>
<span data-ttu-id="ce3d5-128">A VirtualNetworkRule objektumok tömbje, amely a tárolási fiók NetworkRule tulajdonságára frissíthető.</span><span class="sxs-lookup"><span data-stu-id="ce3d5-128">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce3d5-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ce3d5-129">-Confirm</span></span>
<span data-ttu-id="ce3d5-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce3d5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce3d5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce3d5-131">-WhatIf</span></span>
<span data-ttu-id="ce3d5-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ce3d5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce3d5-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ce3d5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce3d5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce3d5-134">-DefaultProfile</span></span>
<span data-ttu-id="ce3d5-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce3d5-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce3d5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce3d5-136">CommonParameters</span></span>
<span data-ttu-id="ce3d5-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce3d5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce3d5-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce3d5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce3d5-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce3d5-139">INPUTS</span></span>

### <span data-ttu-id="ce3d5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ce3d5-140">System.String</span></span>
<span data-ttu-id="ce3d5-141">Microsoft. Azure. Command. Management. Storage. models. PSIpRule [] Microsoft. Azure. commands. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="ce3d5-141">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="ce3d5-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce3d5-142">OUTPUTS</span></span>

### <span data-ttu-id="ce3d5-143">Microsoft. Azure. Command. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ce3d5-143">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="ce3d5-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce3d5-144">NOTES</span></span>

## <span data-ttu-id="ce3d5-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce3d5-145">RELATED LINKS</span></span>

