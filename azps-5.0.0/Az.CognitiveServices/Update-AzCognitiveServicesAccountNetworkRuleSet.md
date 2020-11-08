---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 0f094ba8bdfa8dbf40f2af8495ee2f8cfa6fca16
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194799"
---
# <span data-ttu-id="689ac-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="689ac-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="689ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="689ac-102">SYNOPSIS</span></span>
<span data-ttu-id="689ac-103">A kognitív Services-fiók NetworkRule tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="689ac-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="689ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="689ac-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="689ac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="689ac-105">DESCRIPTION</span></span>
<span data-ttu-id="689ac-106">Az **Update-AzCognitiveServicesAccountNetworkRuleSet** parancsmag a kognitív Services-fiók NetworkRule tulajdonságát frissíti.</span><span class="sxs-lookup"><span data-stu-id="689ac-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="689ac-107">Példák</span><span class="sxs-lookup"><span data-stu-id="689ac-107">EXAMPLES</span></span>

### <span data-ttu-id="689ac-108">Példa 1: a NetworkRule összes tulajdonságának frissítése, beviteli szabályok a JSON-nal</span><span class="sxs-lookup"><span data-stu-id="689ac-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="689ac-109">Ez a parancs frissíti a NetworkRule összes tulajdonságát, valamint a JSON-szal való szövegbeviteli szabályokat.</span><span class="sxs-lookup"><span data-stu-id="689ac-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="689ac-110">2. példa: a NetworkRule frissítés megkerülése tulajdonsága</span><span class="sxs-lookup"><span data-stu-id="689ac-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="689ac-111">Ez a parancs frissíti a NetworkRule tulajdonságát (a többi tulajdonság nem változik).</span><span class="sxs-lookup"><span data-stu-id="689ac-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="689ac-112">3. példa: a kognitív Services-fiók NetworkRule szabályainak megtisztítása</span><span class="sxs-lookup"><span data-stu-id="689ac-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="689ac-113">Ez a parancs a kognitív Services-fiók NetworkRule (más tulajdonságok nem változnak) szabályainak megtisztítására</span><span class="sxs-lookup"><span data-stu-id="689ac-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="689ac-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="689ac-114">PARAMETERS</span></span>

### <span data-ttu-id="689ac-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="689ac-115">-DefaultAction</span></span>
<span data-ttu-id="689ac-116">A kognitív szolgáltatások fiók NetworkRule DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="689ac-116">Cognitive Services Account NetworkRule DefaultAction.</span></span> <span data-ttu-id="689ac-117">Alapértelmezett érték `Deny`</span><span class="sxs-lookup"><span data-stu-id="689ac-117">Default value `Deny`.</span></span>

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

### <span data-ttu-id="689ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="689ac-118">-DefaultProfile</span></span>
<span data-ttu-id="689ac-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="689ac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="689ac-120">-IpRule</span><span class="sxs-lookup"><span data-stu-id="689ac-120">-IpRule</span></span>
<span data-ttu-id="689ac-121">A kognitív szolgáltatások fiók NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="689ac-121">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="689ac-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="689ac-122">-Name</span></span>
<span data-ttu-id="689ac-123">A kognitív szolgáltatások fiók neve.</span><span class="sxs-lookup"><span data-stu-id="689ac-123">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="689ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="689ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="689ac-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="689ac-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="689ac-126">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="689ac-126">-VirtualNetworkRule</span></span>
<span data-ttu-id="689ac-127">A kognitív szolgáltatások fiók NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="689ac-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="689ac-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="689ac-128">-Confirm</span></span>
<span data-ttu-id="689ac-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="689ac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="689ac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="689ac-130">-WhatIf</span></span>
<span data-ttu-id="689ac-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="689ac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="689ac-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="689ac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="689ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689ac-133">CommonParameters</span></span>
<span data-ttu-id="689ac-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="689ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689ac-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="689ac-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689ac-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="689ac-136">INPUTS</span></span>

### <span data-ttu-id="689ac-137">System. String</span><span class="sxs-lookup"><span data-stu-id="689ac-137">System.String</span></span>

### <span data-ttu-id="689ac-138">Microsoft. Azure. Command. Management. CognitiveServices. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="689ac-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="689ac-139">Microsoft. Azure. Command. Management. CognitiveServices. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="689ac-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="689ac-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="689ac-140">OUTPUTS</span></span>

### <span data-ttu-id="689ac-141">Microsoft. Azure. Command. Management. CognitiveServices. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="689ac-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="689ac-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="689ac-142">NOTES</span></span>

## <span data-ttu-id="689ac-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="689ac-143">RELATED LINKS</span></span>