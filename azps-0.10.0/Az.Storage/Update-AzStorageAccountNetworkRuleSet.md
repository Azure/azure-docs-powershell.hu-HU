---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: b92da8f6128ecc58a8e85d5e8f3f92347fd8dce1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842822"
---
# <span data-ttu-id="9a8da-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a8da-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="9a8da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a8da-102">SYNOPSIS</span></span>
<span data-ttu-id="9a8da-103">Tárolási fiók NetworkRule tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="9a8da-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="9a8da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a8da-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a8da-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a8da-105">DESCRIPTION</span></span>
<span data-ttu-id="9a8da-106">Az **Update-AzStorageAccountNetworkRuleSet** parancsmag frissíti a tárolási fiók NetworkRule tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="9a8da-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="9a8da-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9a8da-107">EXAMPLES</span></span>

### <span data-ttu-id="9a8da-108">Példa 1: a NetworkRule összes tulajdonságának frissítése, beviteli szabályok a JSON-nal</span><span class="sxs-lookup"><span data-stu-id="9a8da-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="9a8da-109">Ez a parancs frissíti a NetworkRule összes tulajdonságát, valamint a JSON-szal való szövegbeviteli szabályokat.</span><span class="sxs-lookup"><span data-stu-id="9a8da-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="9a8da-110">2. példa: a NetworkRule frissítés megkerülése tulajdonsága</span><span class="sxs-lookup"><span data-stu-id="9a8da-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="9a8da-111">Ez a parancs frissíti a NetworkRule tulajdonságát (a többi tulajdonság nem változik).</span><span class="sxs-lookup"><span data-stu-id="9a8da-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="9a8da-112">3. példa: a NetworkRule szabályainak megtisztítása</span><span class="sxs-lookup"><span data-stu-id="9a8da-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="9a8da-113">Ez a parancs megtisztítja a NetworkRule szabályait (a többi tulajdonság nem változik).</span><span class="sxs-lookup"><span data-stu-id="9a8da-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="9a8da-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a8da-114">PARAMETERS</span></span>

### <span data-ttu-id="9a8da-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a8da-115">-AsJob</span></span>
<span data-ttu-id="9a8da-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9a8da-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a8da-117">-Kitérő</span><span class="sxs-lookup"><span data-stu-id="9a8da-117">-Bypass</span></span>
<span data-ttu-id="9a8da-118">A NetworkRule tulajdonságra való frissítés megkerülő értéke.</span><span class="sxs-lookup"><span data-stu-id="9a8da-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="9a8da-119">Az engedélyezett érték nincs vagy a következő kombinációk egyike: • naplózás • metrikák • Azureservices</span><span class="sxs-lookup"><span data-stu-id="9a8da-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="9a8da-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="9a8da-120">-DefaultAction</span></span>
<span data-ttu-id="9a8da-121">A DefaultAction érték a NetworkRule tulajdonságra való frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="9a8da-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="9a8da-122">Az engedélyezett beállítások: • Allow • deny</span><span class="sxs-lookup"><span data-stu-id="9a8da-122">The allowed Options: • Allow • Deny</span></span>

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

### <span data-ttu-id="9a8da-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a8da-123">-DefaultProfile</span></span>
<span data-ttu-id="9a8da-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a8da-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a8da-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="9a8da-125">-IPRule</span></span>
<span data-ttu-id="9a8da-126">A IpRule objektumok tömbje, amely a tárolási fiók NetworkRule tulajdonságára frissíthető.</span><span class="sxs-lookup"><span data-stu-id="9a8da-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="9a8da-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9a8da-127">-Name</span></span>
<span data-ttu-id="9a8da-128">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a8da-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="9a8da-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a8da-129">-ResourceGroupName</span></span>
<span data-ttu-id="9a8da-130">Itt adhatja meg, hogy az erőforráscsoport neve tartalmazza-e a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="9a8da-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="9a8da-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9a8da-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="9a8da-132">A VirtualNetworkRule objektumok tömbje, amely a tárolási fiók NetworkRule tulajdonságára frissíthető.</span><span class="sxs-lookup"><span data-stu-id="9a8da-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="9a8da-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9a8da-133">-Confirm</span></span>
<span data-ttu-id="9a8da-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9a8da-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a8da-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a8da-135">-WhatIf</span></span>
<span data-ttu-id="9a8da-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9a8da-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a8da-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a8da-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a8da-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a8da-138">CommonParameters</span></span>
<span data-ttu-id="9a8da-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a8da-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a8da-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a8da-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a8da-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a8da-141">INPUTS</span></span>

### <span data-ttu-id="9a8da-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9a8da-142">System.String</span></span>

### <span data-ttu-id="9a8da-143">Microsoft. Azure. Command. Management. Storage. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="9a8da-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="9a8da-144">Paraméterek: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9a8da-144">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="9a8da-145">Microsoft. Azure. Command. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="9a8da-145">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="9a8da-146">Paraméterek: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9a8da-146">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="9a8da-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a8da-147">OUTPUTS</span></span>

### <span data-ttu-id="9a8da-148">Microsoft. Azure. Command. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a8da-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="9a8da-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a8da-149">NOTES</span></span>

## <span data-ttu-id="9a8da-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a8da-150">RELATED LINKS</span></span>
