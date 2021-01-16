---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 04611df4dd315c972d9e32b280d635a6ecd0ed21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375954"
---
# <span data-ttu-id="9438c-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9438c-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="9438c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9438c-102">SYNOPSIS</span></span>
<span data-ttu-id="9438c-103">Tárfiók NetworkRule tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="9438c-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="9438c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9438c-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9438c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9438c-105">DESCRIPTION</span></span>
<span data-ttu-id="9438c-106">Az **Update-AzStorageAccountNetworkRuleSet** parancsmag frissíti egy tárfiók NetworkRule tulajdonságát</span><span class="sxs-lookup"><span data-stu-id="9438c-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="9438c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9438c-107">EXAMPLES</span></span>

### <span data-ttu-id="9438c-108">1. példa: A NetworkRule összes tulajdonságának frissítése, beviteli szabályok a JSON-nal</span><span class="sxs-lookup"><span data-stu-id="9438c-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="9438c-109">Ez a parancs frissíti a NetworkRule összes tulajdonságát, a beviteli szabályokat pedig JSON-nal.</span><span class="sxs-lookup"><span data-stu-id="9438c-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="9438c-110">2. példa: A NetworkRule megkerülő tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="9438c-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="9438c-111">A NetworkRule ezen parancsfrissítési bypass tulajdonsága (más tulajdonságok nem változnak).</span><span class="sxs-lookup"><span data-stu-id="9438c-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="9438c-112">3. példa: Tárfiók NetworkRule-szabályainak tisztítása</span><span class="sxs-lookup"><span data-stu-id="9438c-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="9438c-113">Ez a parancs megtisztítja egy tárfiók NetworkRule szabályát (a többi tulajdonság nem változik).</span><span class="sxs-lookup"><span data-stu-id="9438c-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="9438c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9438c-114">PARAMETERS</span></span>

### <span data-ttu-id="9438c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9438c-115">-AsJob</span></span>
<span data-ttu-id="9438c-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9438c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9438c-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="9438c-117">-Bypass</span></span>
<span data-ttu-id="9438c-118">The Bypass value to update to the NetworkRule property of a Storage account.</span><span class="sxs-lookup"><span data-stu-id="9438c-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="9438c-119">Az engedélyezett érték a következő értékek egyike vagy kombinációja: • Naplózás • Metrikák • Azureservices</span><span class="sxs-lookup"><span data-stu-id="9438c-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="9438c-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="9438c-120">-DefaultAction</span></span>
<span data-ttu-id="9438c-121">A DefaultAction érték, amely egy tárfiók NetworkRule tulajdonságára frissít.</span><span class="sxs-lookup"><span data-stu-id="9438c-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="9438c-122">Az engedélyezett beállítások: • Allow • Deny</span><span class="sxs-lookup"><span data-stu-id="9438c-122">The allowed Options: • Allow • Deny</span></span>

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

### <span data-ttu-id="9438c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9438c-123">-DefaultProfile</span></span>
<span data-ttu-id="9438c-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9438c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9438c-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="9438c-125">-IPRule</span></span>
<span data-ttu-id="9438c-126">A tárfiók NetworkRule tulajdonságára frissítendő IpRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="9438c-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="9438c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="9438c-127">-Name</span></span>
<span data-ttu-id="9438c-128">A Tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9438c-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="9438c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9438c-129">-ResourceGroupName</span></span>
<span data-ttu-id="9438c-130">A Tárfiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9438c-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="9438c-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9438c-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="9438c-132">The Array of VirtualNetworkRule objects to update to the NetworkRule property of a Storage account.</span><span class="sxs-lookup"><span data-stu-id="9438c-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="9438c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9438c-133">-Confirm</span></span>
<span data-ttu-id="9438c-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9438c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9438c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9438c-135">-WhatIf</span></span>
<span data-ttu-id="9438c-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9438c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9438c-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9438c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9438c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9438c-138">CommonParameters</span></span>
<span data-ttu-id="9438c-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9438c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9438c-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9438c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9438c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9438c-141">INPUTS</span></span>

### <span data-ttu-id="9438c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9438c-142">System.String</span></span>

### <span data-ttu-id="9438c-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="9438c-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="9438c-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="9438c-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="9438c-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9438c-145">OUTPUTS</span></span>

### <span data-ttu-id="9438c-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9438c-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="9438c-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9438c-147">NOTES</span></span>

## <span data-ttu-id="9438c-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9438c-148">RELATED LINKS</span></span>
