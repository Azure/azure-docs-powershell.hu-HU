---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 04611df4dd315c972d9e32b280d635a6ecd0ed21
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180760"
---
# <span data-ttu-id="e794d-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e794d-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="e794d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e794d-102">SYNOPSIS</span></span>
<span data-ttu-id="e794d-103">Tárolási fiók NetworkRule tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="e794d-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="e794d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e794d-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e794d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e794d-105">DESCRIPTION</span></span>
<span data-ttu-id="e794d-106">Az **Update-AzStorageAccountNetworkRuleSet** parancsmag frissíti a tárolási fiók NetworkRule tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="e794d-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="e794d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e794d-107">EXAMPLES</span></span>

### <span data-ttu-id="e794d-108">Példa 1: a NetworkRule összes tulajdonságának frissítése, beviteli szabályok a JSON-nal</span><span class="sxs-lookup"><span data-stu-id="e794d-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="e794d-109">Ez a parancs frissíti a NetworkRule összes tulajdonságát, valamint a JSON-szal való szövegbeviteli szabályokat.</span><span class="sxs-lookup"><span data-stu-id="e794d-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="e794d-110">2. példa: a NetworkRule frissítés megkerülése tulajdonsága</span><span class="sxs-lookup"><span data-stu-id="e794d-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="e794d-111">Ez a parancs frissíti a NetworkRule tulajdonságát (a többi tulajdonság nem változik).</span><span class="sxs-lookup"><span data-stu-id="e794d-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="e794d-112">3. példa: a NetworkRule szabályainak megtisztítása</span><span class="sxs-lookup"><span data-stu-id="e794d-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="e794d-113">Ez a parancs megtisztítja a NetworkRule szabályait (a többi tulajdonság nem változik).</span><span class="sxs-lookup"><span data-stu-id="e794d-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="e794d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e794d-114">PARAMETERS</span></span>

### <span data-ttu-id="e794d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e794d-115">-AsJob</span></span>
<span data-ttu-id="e794d-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e794d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e794d-117">-Kitérő</span><span class="sxs-lookup"><span data-stu-id="e794d-117">-Bypass</span></span>
<span data-ttu-id="e794d-118">A NetworkRule tulajdonságra való frissítés megkerülő értéke.</span><span class="sxs-lookup"><span data-stu-id="e794d-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="e794d-119">Az engedélyezett érték nincs vagy a következő kombinációk egyike: • naplózás • metrikák • Azureservices</span><span class="sxs-lookup"><span data-stu-id="e794d-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="e794d-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="e794d-120">-DefaultAction</span></span>
<span data-ttu-id="e794d-121">A DefaultAction érték a NetworkRule tulajdonságra való frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="e794d-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="e794d-122">Az engedélyezett beállítások: • Allow • deny</span><span class="sxs-lookup"><span data-stu-id="e794d-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e794d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e794d-123">-DefaultProfile</span></span>
<span data-ttu-id="e794d-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e794d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e794d-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="e794d-125">-IPRule</span></span>
<span data-ttu-id="e794d-126">A IpRule objektumok tömbje, amely a tárolási fiók NetworkRule tulajdonságára frissíthető.</span><span class="sxs-lookup"><span data-stu-id="e794d-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="e794d-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e794d-127">-Name</span></span>
<span data-ttu-id="e794d-128">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e794d-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="e794d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e794d-129">-ResourceGroupName</span></span>
<span data-ttu-id="e794d-130">Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="e794d-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="e794d-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e794d-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="e794d-132">A VirtualNetworkRule objektumok tömbje, amely a tárolási fiók NetworkRule tulajdonságára frissíthető.</span><span class="sxs-lookup"><span data-stu-id="e794d-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="e794d-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e794d-133">-Confirm</span></span>
<span data-ttu-id="e794d-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e794d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e794d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e794d-135">-WhatIf</span></span>
<span data-ttu-id="e794d-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e794d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e794d-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e794d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e794d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e794d-138">CommonParameters</span></span>
<span data-ttu-id="e794d-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e794d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e794d-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e794d-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e794d-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e794d-141">INPUTS</span></span>

### <span data-ttu-id="e794d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e794d-142">System.String</span></span>

### <span data-ttu-id="e794d-143">Microsoft. Azure. Command. Management. Storage. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="e794d-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="e794d-144">Microsoft. Azure. Command. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="e794d-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="e794d-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e794d-145">OUTPUTS</span></span>

### <span data-ttu-id="e794d-146">Microsoft. Azure. Command. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e794d-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="e794d-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e794d-147">NOTES</span></span>

## <span data-ttu-id="e794d-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e794d-148">RELATED LINKS</span></span>
