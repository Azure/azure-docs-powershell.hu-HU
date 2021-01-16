---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340302"
---
# <span data-ttu-id="21016-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="21016-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="21016-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21016-102">SYNOPSIS</span></span>
<span data-ttu-id="21016-103">Új letiltott szabálycsoport-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="21016-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="21016-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="21016-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21016-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="21016-105">DESCRIPTION</span></span>
<span data-ttu-id="21016-106">A **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** parancsmag létrehoz egy új letiltott szabálycsoport-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="21016-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="21016-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="21016-107">EXAMPLES</span></span>

### <span data-ttu-id="21016-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="21016-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="21016-109">A parancs létrehoz egy új letiltott szabálycsoport-konfigurációt a REQUEST-942-APPLICATION-ATTACK-SQLI nevű szabálycsoporthoz, a 942130-as és a 942140-es szabály letiltva.</span><span class="sxs-lookup"><span data-stu-id="21016-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="21016-110">Az új letiltott szabálycsoport-konfigurációt a $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="21016-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="21016-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21016-111">PARAMETERS</span></span>

### <span data-ttu-id="21016-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21016-112">-DefaultProfile</span></span>
<span data-ttu-id="21016-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21016-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21016-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="21016-114">-RuleGroupName</span></span>
<span data-ttu-id="21016-115">A letiltott szabálycsoport neve.</span><span class="sxs-lookup"><span data-stu-id="21016-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="21016-116">-Rules</span><span class="sxs-lookup"><span data-stu-id="21016-116">-Rules</span></span>
<span data-ttu-id="21016-117">A letiltott szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="21016-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="21016-118">Null érték esetén a szabálycsoport összes szabálya le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="21016-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="21016-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21016-119">CommonParameters</span></span>
<span data-ttu-id="21016-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21016-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21016-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21016-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21016-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21016-122">INPUTS</span></span>

### <span data-ttu-id="21016-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="21016-123">None</span></span>

## <span data-ttu-id="21016-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21016-124">OUTPUTS</span></span>

### <span data-ttu-id="21016-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="21016-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="21016-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="21016-126">NOTES</span></span>

## <span data-ttu-id="21016-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21016-127">RELATED LINKS</span></span>

[<span data-ttu-id="21016-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="21016-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="21016-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="21016-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

