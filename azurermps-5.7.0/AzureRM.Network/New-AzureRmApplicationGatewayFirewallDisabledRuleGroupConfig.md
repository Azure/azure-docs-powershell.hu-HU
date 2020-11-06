---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 780e231f2ca512b5becf0ee068c004dd815cea89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496396"
---
# <span data-ttu-id="f5ef9-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="f5ef9-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="f5ef9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ef9-103">Új letiltott szabály-konfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f5ef9-103">Creates a new disabled rule group configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5ef9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5ef9-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5ef9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5ef9-105">DESCRIPTION</span></span>
<span data-ttu-id="f5ef9-106">A **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** parancsmag új letiltott szabály-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f5ef9-106">The **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="f5ef9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f5ef9-107">EXAMPLES</span></span>

### <span data-ttu-id="f5ef9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f5ef9-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="f5ef9-109">A parancs új, letiltott szabály-konfigurációt hoz létre a "Request-942-APPLICATION-ATTACK-SQLI" nevű szabály csoportjának a 942130 és a 942140-as szabály letiltásával.</span><span class="sxs-lookup"><span data-stu-id="f5ef9-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="f5ef9-110">Az új letiltott szabály csoport konfigurációját a program az 1 $disabledRuleGroup menti.</span><span class="sxs-lookup"><span data-stu-id="f5ef9-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="f5ef9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5ef9-111">PARAMETERS</span></span>

### <span data-ttu-id="f5ef9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ef9-112">-DefaultProfile</span></span>
<span data-ttu-id="f5ef9-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5ef9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ef9-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ef9-114">-RuleGroupName</span></span>
<span data-ttu-id="f5ef9-115">Annak a szabálynak a neve, amely le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="f5ef9-115">The name of the rule group that will be disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ef9-116">-Szabályok</span><span class="sxs-lookup"><span data-stu-id="f5ef9-116">-Rules</span></span>
<span data-ttu-id="f5ef9-117">A letiltani kívánt szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="f5ef9-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="f5ef9-118">Ha NULL, a szabály csoport minden szabálya le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="f5ef9-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ef9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ef9-119">CommonParameters</span></span>
<span data-ttu-id="f5ef9-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5ef9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ef9-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5ef9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ef9-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5ef9-122">INPUTS</span></span>

### <span data-ttu-id="f5ef9-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="f5ef9-123">None</span></span>

## <span data-ttu-id="f5ef9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5ef9-124">OUTPUTS</span></span>

### <span data-ttu-id="f5ef9-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="f5ef9-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="f5ef9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5ef9-126">NOTES</span></span>

## <span data-ttu-id="f5ef9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5ef9-127">RELATED LINKS</span></span>

[<span data-ttu-id="f5ef9-128">Új – AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5ef9-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="f5ef9-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5ef9-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

