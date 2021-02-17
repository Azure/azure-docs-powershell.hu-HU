---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147018"
---
# <span data-ttu-id="7b0bb-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="7b0bb-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="7b0bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b0bb-102">SYNOPSIS</span></span>
<span data-ttu-id="7b0bb-103">Új letiltott szabálycsoport-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7b0bb-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="7b0bb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7b0bb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b0bb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7b0bb-105">DESCRIPTION</span></span>
<span data-ttu-id="7b0bb-106">A **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** parancsmag létrehoz egy új letiltott szabálycsoport-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="7b0bb-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="7b0bb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7b0bb-107">EXAMPLES</span></span>

### <span data-ttu-id="7b0bb-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7b0bb-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="7b0bb-109">A parancs létrehoz egy új letiltott szabálycsoport-konfigurációt a REQUEST-942-APPLICATION-ATTACK-SQLI nevű szabálycsoporthoz, a 942130-as és a 942140-es szabály letiltva.</span><span class="sxs-lookup"><span data-stu-id="7b0bb-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="7b0bb-110">Az új letiltott szabálycsoport-konfigurációt a $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="7b0bb-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="7b0bb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b0bb-111">PARAMETERS</span></span>

### <span data-ttu-id="7b0bb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b0bb-112">-DefaultProfile</span></span>
<span data-ttu-id="7b0bb-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b0bb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b0bb-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="7b0bb-114">-RuleGroupName</span></span>
<span data-ttu-id="7b0bb-115">A letiltott szabálycsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7b0bb-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="7b0bb-116">-Rules</span><span class="sxs-lookup"><span data-stu-id="7b0bb-116">-Rules</span></span>
<span data-ttu-id="7b0bb-117">A letiltott szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="7b0bb-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="7b0bb-118">Null érték esetén a szabálycsoport összes szabálya le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="7b0bb-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="7b0bb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b0bb-119">CommonParameters</span></span>
<span data-ttu-id="7b0bb-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b0bb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b0bb-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b0bb-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b0bb-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b0bb-122">INPUTS</span></span>

### <span data-ttu-id="7b0bb-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="7b0bb-123">None</span></span>

## <span data-ttu-id="7b0bb-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b0bb-124">OUTPUTS</span></span>

### <span data-ttu-id="7b0bb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="7b0bb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="7b0bb-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7b0bb-126">NOTES</span></span>

## <span data-ttu-id="7b0bb-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b0bb-127">RELATED LINKS</span></span>

[<span data-ttu-id="7b0bb-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b0bb-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="7b0bb-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b0bb-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

