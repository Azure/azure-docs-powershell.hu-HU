---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 03e6169a9e69b9f2faa3dfaccba934428f7db4e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929258"
---
# <span data-ttu-id="3f630-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f630-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="3f630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f630-102">SYNOPSIS</span></span>
<span data-ttu-id="3f630-103">Tárfiók NetworkRule tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="3f630-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="3f630-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f630-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-ResourceAccessRule <PSResourceAccessRule[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f630-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f630-105">DESCRIPTION</span></span>
<span data-ttu-id="3f630-106">**AzStorageAccountNetworkRuleSet** parancsmag frissíti egy tárfiók NetworkRule tulajdonságát</span><span class="sxs-lookup"><span data-stu-id="3f630-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="3f630-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f630-107">EXAMPLES</span></span>

### <span data-ttu-id="3f630-108">1. példa: A NetworkRule összes tulajdonságának frissítése, beviteli szabályok a JSON-nal</span><span class="sxs-lookup"><span data-stu-id="3f630-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"}) -ResourceAccessRule (@{ResourceId=$ResourceId1;TenantId=$tenantId1},@{ResourceId=$ResourceId2;TenantId=$tenantId1})
```

<span data-ttu-id="3f630-109">Ez a parancs frissíti a NetworkRule összes tulajdonságát, a beviteli szabályokat pedig JSON-nal.</span><span class="sxs-lookup"><span data-stu-id="3f630-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="3f630-110">2. példa: A NetworkRule megkerülő tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="3f630-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="3f630-111">A NetworkRule ezen parancsfrissítésének Bypass tulajdonsága (más tulajdonságok nem változnak).</span><span class="sxs-lookup"><span data-stu-id="3f630-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="3f630-112">3. példa: Tárfiók NetworkRule-szabályainak tisztítása</span><span class="sxs-lookup"><span data-stu-id="3f630-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @() -ResourceAccessRule @()
```

<span data-ttu-id="3f630-113">Ez a parancs megtisztítja egy tárfiók NetworkRule szabályát (a többi tulajdonság nem változik).</span><span class="sxs-lookup"><span data-stu-id="3f630-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="3f630-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f630-114">PARAMETERS</span></span>

### <span data-ttu-id="3f630-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f630-115">-AsJob</span></span>
<span data-ttu-id="3f630-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3f630-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f630-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="3f630-117">-Bypass</span></span>
<span data-ttu-id="3f630-118">The Bypass value to update to the NetworkRule property of a Storage account.</span><span class="sxs-lookup"><span data-stu-id="3f630-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="3f630-119">Az engedélyezett érték a következő értékek egyike vagy kombinációja: • Naplózás • Metrikák • Azureservices</span><span class="sxs-lookup"><span data-stu-id="3f630-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="3f630-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="3f630-120">-DefaultAction</span></span>
<span data-ttu-id="3f630-121">A DefaultAction érték, amely egy tárfiók NetworkRule tulajdonságára frissít.</span><span class="sxs-lookup"><span data-stu-id="3f630-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="3f630-122">Az engedélyezett beállítások: • Allow • Deny</span><span class="sxs-lookup"><span data-stu-id="3f630-122">The allowed Options: • Allow • Deny</span></span>

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

### <span data-ttu-id="3f630-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f630-123">-DefaultProfile</span></span>
<span data-ttu-id="3f630-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f630-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f630-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="3f630-125">-IPRule</span></span>
<span data-ttu-id="3f630-126">A tárfiók NetworkRule tulajdonságára frissítendő IpRule-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="3f630-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="3f630-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3f630-127">-Name</span></span>
<span data-ttu-id="3f630-128">A Tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f630-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="3f630-129">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="3f630-129">-ResourceAccessRule</span></span>
<span data-ttu-id="3f630-130">Tárfiók NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="3f630-130">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f630-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f630-131">-ResourceGroupName</span></span>
<span data-ttu-id="3f630-132">A Tárfiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f630-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="3f630-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3f630-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="3f630-134">The Array of VirtualNetworkRule objects to update to the NetworkRule property of a Storage account.</span><span class="sxs-lookup"><span data-stu-id="3f630-134">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="3f630-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f630-135">-Confirm</span></span>
<span data-ttu-id="3f630-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3f630-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f630-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f630-137">-WhatIf</span></span>
<span data-ttu-id="3f630-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3f630-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f630-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f630-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f630-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f630-140">CommonParameters</span></span>
<span data-ttu-id="3f630-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f630-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f630-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f630-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f630-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f630-143">INPUTS</span></span>

### <span data-ttu-id="3f630-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3f630-144">System.String</span></span>

### <span data-ttu-id="3f630-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="3f630-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="3f630-146">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="3f630-146">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="3f630-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f630-147">OUTPUTS</span></span>

### <span data-ttu-id="3f630-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f630-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="3f630-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f630-149">NOTES</span></span>

## <span data-ttu-id="3f630-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f630-150">RELATED LINKS</span></span>
