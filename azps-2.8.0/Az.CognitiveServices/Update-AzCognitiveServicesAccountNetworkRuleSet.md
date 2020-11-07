---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 114163bdae16d73f490f0110186ccd43bee7d43c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667534"
---
# <span data-ttu-id="64123-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="64123-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="64123-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64123-102">SYNOPSIS</span></span>
<span data-ttu-id="64123-103">A kognitív Services-fiók NetworkRule tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="64123-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="64123-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64123-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64123-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64123-105">DESCRIPTION</span></span>
<span data-ttu-id="64123-106">Az **Update-AzCognitiveServicesAccountNetworkRuleSet** parancsmag a kognitív Services-fiók NetworkRule tulajdonságát frissíti.</span><span class="sxs-lookup"><span data-stu-id="64123-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="64123-107">Példák</span><span class="sxs-lookup"><span data-stu-id="64123-107">EXAMPLES</span></span>

### <span data-ttu-id="64123-108">Példa 1: a NetworkRule összes tulajdonságának frissítése, beviteli szabályok a JSON-nal</span><span class="sxs-lookup"><span data-stu-id="64123-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="64123-109">Ez a parancs frissíti a NetworkRule összes tulajdonságát, valamint a JSON-szal való szövegbeviteli szabályokat.</span><span class="sxs-lookup"><span data-stu-id="64123-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="64123-110">2. példa: a NetworkRule frissítés megkerülése tulajdonsága</span><span class="sxs-lookup"><span data-stu-id="64123-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="64123-111">Ez a parancs frissíti a NetworkRule tulajdonságát (a többi tulajdonság nem változik).</span><span class="sxs-lookup"><span data-stu-id="64123-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="64123-112">3. példa: a kognitív Services-fiók NetworkRule szabályainak megtisztítása</span><span class="sxs-lookup"><span data-stu-id="64123-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="64123-113">Ez a parancs a kognitív Services-fiók NetworkRule (más tulajdonságok nem változnak) szabályainak megtisztítására</span><span class="sxs-lookup"><span data-stu-id="64123-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="64123-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64123-114">PARAMETERS</span></span>

### <span data-ttu-id="64123-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="64123-115">-DefaultAction</span></span>
<span data-ttu-id="64123-116">A kognitív szolgáltatások fiók NetworkRule DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="64123-116">Cognitive Services Account NetworkRule DefaultAction.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64123-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64123-117">-DefaultProfile</span></span>
<span data-ttu-id="64123-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64123-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64123-119">-IpRule</span><span class="sxs-lookup"><span data-stu-id="64123-119">-IpRule</span></span>
<span data-ttu-id="64123-120">A kognitív szolgáltatások fiók NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="64123-120">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64123-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64123-121">-Name</span></span>
<span data-ttu-id="64123-122">A kognitív szolgáltatások fiók neve.</span><span class="sxs-lookup"><span data-stu-id="64123-122">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64123-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64123-123">-ResourceGroupName</span></span>
<span data-ttu-id="64123-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="64123-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="64123-125">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="64123-125">-VirtualNetworkRule</span></span>
<span data-ttu-id="64123-126">A kognitív szolgáltatások fiók NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="64123-126">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64123-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64123-127">-Confirm</span></span>
<span data-ttu-id="64123-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64123-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64123-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64123-129">-WhatIf</span></span>
<span data-ttu-id="64123-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64123-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64123-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64123-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64123-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64123-132">CommonParameters</span></span>
<span data-ttu-id="64123-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64123-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64123-134">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="64123-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64123-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64123-135">INPUTS</span></span>

### <span data-ttu-id="64123-136">System. String</span><span class="sxs-lookup"><span data-stu-id="64123-136">System.String</span></span>

### <span data-ttu-id="64123-137">Microsoft. Azure. Command. Management. CognitiveServices. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="64123-137">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="64123-138">Microsoft. Azure. Command. Management. CognitiveServices. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="64123-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="64123-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64123-139">OUTPUTS</span></span>

### <span data-ttu-id="64123-140">Microsoft. Azure. Command. Management. CognitiveServices. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="64123-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="64123-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64123-141">NOTES</span></span>

## <span data-ttu-id="64123-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64123-142">RELATED LINKS</span></span>
