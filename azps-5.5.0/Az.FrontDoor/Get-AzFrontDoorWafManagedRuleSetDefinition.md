---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209511"
---
# <span data-ttu-id="e02a9-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="e02a9-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="e02a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e02a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e02a9-103">A WAF felügyelt szabálykészlet-definícióinak lekérte</span><span class="sxs-lookup"><span data-stu-id="e02a9-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="e02a9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e02a9-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e02a9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e02a9-105">DESCRIPTION</span></span>
<span data-ttu-id="e02a9-106">Hivatkozásként használható waf felügyelt szabálykészlet-definíciók listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="e02a9-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="e02a9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e02a9-107">EXAMPLES</span></span>

### <span data-ttu-id="e02a9-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e02a9-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="e02a9-109">{{ Adja meg itt a példa leírását }}</span><span class="sxs-lookup"><span data-stu-id="e02a9-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e02a9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e02a9-110">PARAMETERS</span></span>

### <span data-ttu-id="e02a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02a9-111">-DefaultProfile</span></span>
<span data-ttu-id="e02a9-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e02a9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e02a9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02a9-113">CommonParameters</span></span>
<span data-ttu-id="e02a9-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e02a9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02a9-115">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e02a9-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02a9-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e02a9-116">INPUTS</span></span>

### <span data-ttu-id="e02a9-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="e02a9-117">None</span></span>

## <span data-ttu-id="e02a9-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e02a9-118">OUTPUTS</span></span>

### <span data-ttu-id="e02a9-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="e02a9-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="e02a9-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e02a9-120">NOTES</span></span>

## <span data-ttu-id="e02a9-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e02a9-121">RELATED LINKS</span></span>

<span data-ttu-id="e02a9-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="e02a9-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
