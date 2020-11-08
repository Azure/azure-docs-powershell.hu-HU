---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194766"
---
# <span data-ttu-id="3be7a-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="3be7a-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="3be7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3be7a-102">SYNOPSIS</span></span>
<span data-ttu-id="3be7a-103">WAF felügyelt szabálykészlet-definíciók beszerzése</span><span class="sxs-lookup"><span data-stu-id="3be7a-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="3be7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3be7a-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3be7a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3be7a-105">DESCRIPTION</span></span>
<span data-ttu-id="3be7a-106">Beolvassa a WAF felügyelt szabálykészlet definícióját, amelyet hivatkozásként használhat.</span><span class="sxs-lookup"><span data-stu-id="3be7a-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="3be7a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3be7a-107">EXAMPLES</span></span>

### <span data-ttu-id="3be7a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3be7a-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="3be7a-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="3be7a-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="3be7a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3be7a-110">PARAMETERS</span></span>

### <span data-ttu-id="3be7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3be7a-111">-DefaultProfile</span></span>
<span data-ttu-id="3be7a-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3be7a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3be7a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be7a-113">CommonParameters</span></span>
<span data-ttu-id="3be7a-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3be7a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be7a-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3be7a-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be7a-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3be7a-116">INPUTS</span></span>

### <span data-ttu-id="3be7a-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="3be7a-117">None</span></span>

## <span data-ttu-id="3be7a-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3be7a-118">OUTPUTS</span></span>

### <span data-ttu-id="3be7a-119">Microsoft. Azure. Command. FrontDoor. models. PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="3be7a-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="3be7a-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3be7a-120">NOTES</span></span>

## <span data-ttu-id="3be7a-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3be7a-121">RELATED LINKS</span></span>

<span data-ttu-id="3be7a-122">[Új – AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [Új – AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [Új – AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="3be7a-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
