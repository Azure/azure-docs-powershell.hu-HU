---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 0f094ba8bdfa8dbf40f2af8495ee2f8cfa6fca16
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326812"
---
# <span data-ttu-id="a6787-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6787-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="a6787-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6787-102">SYNOPSIS</span></span>
<span data-ttu-id="a6787-103">Kognitív szolgáltatások fiók NetworkRule tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="a6787-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="a6787-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a6787-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6787-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a6787-105">DESCRIPTION</span></span>
<span data-ttu-id="a6787-106">Az **Update-AzCognitiveServicesAccountNetworkRuleSet** parancsmag frissíti a Kognitív szolgáltatások fiók NetworkRule tulajdonságát</span><span class="sxs-lookup"><span data-stu-id="a6787-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="a6787-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a6787-107">EXAMPLES</span></span>

### <span data-ttu-id="a6787-108">1. példa: A NetworkRule összes tulajdonságának frissítése, beviteli szabályok a JSON-nal</span><span class="sxs-lookup"><span data-stu-id="a6787-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="a6787-109">Ez a parancs frissíti a NetworkRule összes tulajdonságát, a beviteli szabályokat pedig JSON-nal.</span><span class="sxs-lookup"><span data-stu-id="a6787-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="a6787-110">2. példa: A NetworkRule megkerülő tulajdonságának frissítése</span><span class="sxs-lookup"><span data-stu-id="a6787-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="a6787-111">A NetworkRule ezen parancsfrissítésének Bypass tulajdonsága (más tulajdonságok nem változnak).</span><span class="sxs-lookup"><span data-stu-id="a6787-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="a6787-112">3. példa: A Kognitív szolgáltatások fiók networkrule-szabályainak megtisztíttatása</span><span class="sxs-lookup"><span data-stu-id="a6787-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="a6787-113">Ez a parancs megtisztítja a Kognitív Szolgáltatások-fiók NetworkRule szabályát (más tulajdonságok nem változnak).</span><span class="sxs-lookup"><span data-stu-id="a6787-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="a6787-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6787-114">PARAMETERS</span></span>

### <span data-ttu-id="a6787-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="a6787-115">-DefaultAction</span></span>
<span data-ttu-id="a6787-116">Cognitive Services Account NetworkRule DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="a6787-116">Cognitive Services Account NetworkRule DefaultAction.</span></span> <span data-ttu-id="a6787-117">Alapértelmezett `Deny` érték.</span><span class="sxs-lookup"><span data-stu-id="a6787-117">Default value `Deny`.</span></span>

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

### <span data-ttu-id="a6787-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6787-118">-DefaultProfile</span></span>
<span data-ttu-id="a6787-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6787-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6787-120">-IpRule</span><span class="sxs-lookup"><span data-stu-id="a6787-120">-IpRule</span></span>
<span data-ttu-id="a6787-121">Cognitive Services Account NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="a6787-121">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="a6787-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a6787-122">-Name</span></span>
<span data-ttu-id="a6787-123">Kognitív szolgáltatások fiókneve.</span><span class="sxs-lookup"><span data-stu-id="a6787-123">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="a6787-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6787-124">-ResourceGroupName</span></span>
<span data-ttu-id="a6787-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a6787-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a6787-126">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a6787-126">-VirtualNetworkRule</span></span>
<span data-ttu-id="a6787-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="a6787-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="a6787-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6787-128">-Confirm</span></span>
<span data-ttu-id="a6787-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a6787-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6787-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6787-130">-WhatIf</span></span>
<span data-ttu-id="a6787-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a6787-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6787-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6787-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6787-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6787-133">CommonParameters</span></span>
<span data-ttu-id="a6787-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6787-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6787-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6787-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6787-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6787-136">INPUTS</span></span>

### <span data-ttu-id="a6787-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a6787-137">System.String</span></span>

### <span data-ttu-id="a6787-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="a6787-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="a6787-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="a6787-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="a6787-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6787-140">OUTPUTS</span></span>

### <span data-ttu-id="a6787-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6787-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="a6787-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a6787-142">NOTES</span></span>

## <span data-ttu-id="a6787-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6787-143">RELATED LINKS</span></span>
