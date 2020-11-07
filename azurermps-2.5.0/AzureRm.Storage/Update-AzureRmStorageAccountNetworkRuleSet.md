---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstorageaccountnetworkruleset
schema: 2.0.0
ms.openlocfilehash: beeaf374a261a30ad842aa9c0570ff544ec8ab68
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848974"
---
# <span data-ttu-id="013f0-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="013f0-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="013f0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="013f0-102">SYNOPSIS</span></span>
<span data-ttu-id="013f0-103">Tárolási fiók NetworkRule tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="013f0-103">Update the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="013f0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="013f0-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="013f0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="013f0-105">DESCRIPTION</span></span>
<span data-ttu-id="013f0-106">Az **Update-AzureRmStorageAccountNetworkRuleSet** parancsmag frissíti a tárolási fiók NetworkRule tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="013f0-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="013f0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="013f0-107">EXAMPLES</span></span>

### <span data-ttu-id="013f0-108">Példa 1: a NetworkRule összes tulajdonságának frissítése, beviteli szabályok a JSON-nal</span><span class="sxs-lookup"><span data-stu-id="013f0-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="013f0-109">Ez a parancs frissíti a NetworkRule összes tulajdonságát, valamint a JSON-szal való szövegbeviteli szabályokat.</span><span class="sxs-lookup"><span data-stu-id="013f0-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="013f0-110">2. példa: a NetworkRule frissítés megkerülése tulajdonsága</span><span class="sxs-lookup"><span data-stu-id="013f0-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="013f0-111">Ez a parancs frissíti a NetworkRule tulajdonságát (a többi tulajdonság nem változik).</span><span class="sxs-lookup"><span data-stu-id="013f0-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="013f0-112">3. példa: a NetworkRule szabályainak megtisztítása</span><span class="sxs-lookup"><span data-stu-id="013f0-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="013f0-113">Ez a parancs megtisztítja a NetworkRule szabályait (a többi tulajdonság nem változik).</span><span class="sxs-lookup"><span data-stu-id="013f0-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="013f0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="013f0-114">PARAMETERS</span></span>

### <span data-ttu-id="013f0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="013f0-115">-AsJob</span></span>
<span data-ttu-id="013f0-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="013f0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="013f0-117">-Kitérő</span><span class="sxs-lookup"><span data-stu-id="013f0-117">-Bypass</span></span>
<span data-ttu-id="013f0-118">A NetworkRule tulajdonságra való frissítés megkerülő értéke.</span><span class="sxs-lookup"><span data-stu-id="013f0-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="013f0-119">Az engedélyezett érték nincs vagy a következő kombinációk egyike: • naplózás • metrikák • Azureservices</span><span class="sxs-lookup"><span data-stu-id="013f0-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="013f0-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="013f0-120">-DefaultAction</span></span>
<span data-ttu-id="013f0-121">A DefaultAction érték a NetworkRule tulajdonságra való frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="013f0-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="013f0-122">Az engedélyezett beállítások: • Allow • deny</span><span class="sxs-lookup"><span data-stu-id="013f0-122">The allowed Options: • Allow • Deny</span></span>

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

### <span data-ttu-id="013f0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="013f0-123">-DefaultProfile</span></span>
<span data-ttu-id="013f0-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="013f0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="013f0-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="013f0-125">-IPRule</span></span>
<span data-ttu-id="013f0-126">A IpRule objektumok tömbje, amely a tárolási fiók NetworkRule tulajdonságára frissíthető.</span><span class="sxs-lookup"><span data-stu-id="013f0-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="013f0-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="013f0-127">-Name</span></span>
<span data-ttu-id="013f0-128">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="013f0-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="013f0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="013f0-129">-ResourceGroupName</span></span>
<span data-ttu-id="013f0-130">Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="013f0-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="013f0-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="013f0-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="013f0-132">A VirtualNetworkRule objektumok tömbje, amely a tárolási fiók NetworkRule tulajdonságára frissíthető.</span><span class="sxs-lookup"><span data-stu-id="013f0-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="013f0-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="013f0-133">-Confirm</span></span>
<span data-ttu-id="013f0-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="013f0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="013f0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="013f0-135">-WhatIf</span></span>
<span data-ttu-id="013f0-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="013f0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="013f0-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="013f0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="013f0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="013f0-138">CommonParameters</span></span>
<span data-ttu-id="013f0-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="013f0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="013f0-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="013f0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="013f0-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="013f0-141">INPUTS</span></span>

### <span data-ttu-id="013f0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="013f0-142">System.String</span></span>

### <span data-ttu-id="013f0-143">Microsoft. Azure. Command. Management. Storage. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="013f0-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="013f0-144">Paraméterek: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="013f0-144">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="013f0-145">Microsoft. Azure. Command. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="013f0-145">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="013f0-146">Paraméterek: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="013f0-146">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="013f0-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="013f0-147">OUTPUTS</span></span>

### <span data-ttu-id="013f0-148">Microsoft. Azure. Command. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="013f0-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="013f0-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="013f0-149">NOTES</span></span>

## <span data-ttu-id="013f0-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="013f0-150">RELATED LINKS</span></span>
