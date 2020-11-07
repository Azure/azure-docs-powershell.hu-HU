---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 6813bf30da73f09f285151d6d309eb89b32acbb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670412"
---
# <span data-ttu-id="055b9-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="055b9-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="055b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="055b9-102">SYNOPSIS</span></span>
<span data-ttu-id="055b9-103">Egy alkalmazás-átjáró tűzfal-házirendjét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="055b9-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="055b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="055b9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="055b9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="055b9-105">DESCRIPTION</span></span>
<span data-ttu-id="055b9-106">A **New-AzApplicationGatewayFirewallPolicy** parancsmag egy alkalmazás-átjáró tűzfal-házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="055b9-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="055b9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="055b9-107">EXAMPLES</span></span>

### <span data-ttu-id="055b9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="055b9-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzureRmApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRules $customRule
```

<span data-ttu-id="055b9-109">Ezzel a paranccsal létrehoz egy új Azure Application gateway-tűzfal-házirendet "wafResource1" nevű erőforráscsoport "rg1" nevű erőforráscsoport "westus" nevű "" nevű "" nevű új, a $customRule változóban meghatározott egyéni szabályokkal.</span><span class="sxs-lookup"><span data-stu-id="055b9-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="055b9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="055b9-110">PARAMETERS</span></span>

### <span data-ttu-id="055b9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="055b9-111">-AsJob</span></span>
<span data-ttu-id="055b9-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="055b9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="055b9-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="055b9-113">-CustomRule</span></span>
<span data-ttu-id="055b9-114">A CustomRules listája</span><span class="sxs-lookup"><span data-stu-id="055b9-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="055b9-115">-DefaultProfile</span></span>
<span data-ttu-id="055b9-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="055b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="055b9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="055b9-117">-Force</span></span>
<span data-ttu-id="055b9-118">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="055b9-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="055b9-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="055b9-119">-Location</span></span>
<span data-ttu-id="055b9-120">helyre.</span><span class="sxs-lookup"><span data-stu-id="055b9-120">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055b9-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="055b9-121">-Name</span></span>
<span data-ttu-id="055b9-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="055b9-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="055b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="055b9-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="055b9-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055b9-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="055b9-125">-Tag</span></span>
<span data-ttu-id="055b9-126">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="055b9-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055b9-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="055b9-127">-Confirm</span></span>
<span data-ttu-id="055b9-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="055b9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="055b9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="055b9-129">-WhatIf</span></span>
<span data-ttu-id="055b9-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="055b9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="055b9-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="055b9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="055b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="055b9-132">CommonParameters</span></span>
<span data-ttu-id="055b9-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="055b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="055b9-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="055b9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="055b9-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="055b9-135">INPUTS</span></span>

### <span data-ttu-id="055b9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="055b9-136">System.String</span></span>

### <span data-ttu-id="055b9-137">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="055b9-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="055b9-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="055b9-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="055b9-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="055b9-139">OUTPUTS</span></span>

### <span data-ttu-id="055b9-140">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="055b9-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="055b9-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="055b9-141">NOTES</span></span>

## <span data-ttu-id="055b9-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="055b9-142">RELATED LINKS</span></span>
