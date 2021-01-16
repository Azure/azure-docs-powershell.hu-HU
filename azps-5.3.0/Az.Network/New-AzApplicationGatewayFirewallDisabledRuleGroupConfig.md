---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468113"
---
# <span data-ttu-id="b6861-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="b6861-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="b6861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6861-102">SYNOPSIS</span></span>
<span data-ttu-id="b6861-103">Új letiltott szabálycsoport-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b6861-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="b6861-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b6861-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6861-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b6861-105">DESCRIPTION</span></span>
<span data-ttu-id="b6861-106">A **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** parancsmag létrehoz egy új letiltott szabálycsoport-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="b6861-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="b6861-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b6861-107">EXAMPLES</span></span>

### <span data-ttu-id="b6861-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b6861-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="b6861-109">A parancs létrehoz egy új letiltott szabálycsoport-konfigurációt a REQUEST-942-APPLICATION-ATTACK-SQLI nevű szabálycsoporthoz, a 942130-as és a 942140-es szabály letiltva.</span><span class="sxs-lookup"><span data-stu-id="b6861-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="b6861-110">Az új letiltott szabálycsoport-konfigurációt a $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="b6861-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="b6861-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6861-111">PARAMETERS</span></span>

### <span data-ttu-id="b6861-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6861-112">-DefaultProfile</span></span>
<span data-ttu-id="b6861-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6861-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6861-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="b6861-114">-RuleGroupName</span></span>
<span data-ttu-id="b6861-115">A letiltott szabálycsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b6861-115">The name of the rule group that will be disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6861-116">-Rules</span><span class="sxs-lookup"><span data-stu-id="b6861-116">-Rules</span></span>
<span data-ttu-id="b6861-117">A letiltott szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="b6861-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="b6861-118">Null érték esetén a szabálycsoport összes szabálya le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="b6861-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6861-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6861-119">CommonParameters</span></span>
<span data-ttu-id="b6861-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6861-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6861-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6861-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6861-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6861-122">INPUTS</span></span>

### <span data-ttu-id="b6861-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="b6861-123">None</span></span>

## <span data-ttu-id="b6861-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6861-124">OUTPUTS</span></span>

### <span data-ttu-id="b6861-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="b6861-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="b6861-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b6861-126">NOTES</span></span>

## <span data-ttu-id="b6861-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6861-127">RELATED LINKS</span></span>

[<span data-ttu-id="b6861-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6861-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="b6861-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6861-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

