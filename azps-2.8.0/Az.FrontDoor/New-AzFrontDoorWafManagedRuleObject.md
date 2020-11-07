---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: bde2d2edd48edf83efaf7f548daf4f97d6cffbaa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666411"
---
# <span data-ttu-id="98f72-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="98f72-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="98f72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98f72-102">SYNOPSIS</span></span>
<span data-ttu-id="98f72-103">ManagedRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="98f72-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="98f72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98f72-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98f72-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98f72-105">DESCRIPTION</span></span>
<span data-ttu-id="98f72-106">ManagedRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="98f72-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="98f72-107">Példák</span><span class="sxs-lookup"><span data-stu-id="98f72-107">EXAMPLES</span></span>

### <span data-ttu-id="98f72-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="98f72-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="98f72-109">ManagedRule objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="98f72-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="98f72-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98f72-110">PARAMETERS</span></span>

### <span data-ttu-id="98f72-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f72-111">-DefaultProfile</span></span>
<span data-ttu-id="98f72-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98f72-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98f72-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="98f72-113">-RuleGroupOverride</span></span>
<span data-ttu-id="98f72-114">Az Azure felügyelt szolgáltatóinak listája felülbírálja a konfigurációt</span><span class="sxs-lookup"><span data-stu-id="98f72-114">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f72-115">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="98f72-115">-Type</span></span>
<span data-ttu-id="98f72-116">A szabályrendszert típusa</span><span class="sxs-lookup"><span data-stu-id="98f72-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="98f72-117">-Verzió</span><span class="sxs-lookup"><span data-stu-id="98f72-117">-Version</span></span>
<span data-ttu-id="98f72-118">A szabály verziószáma</span><span class="sxs-lookup"><span data-stu-id="98f72-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="98f72-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f72-119">CommonParameters</span></span>
<span data-ttu-id="98f72-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98f72-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f72-121">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="98f72-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f72-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98f72-122">INPUTS</span></span>

### <span data-ttu-id="98f72-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="98f72-123">None</span></span>

## <span data-ttu-id="98f72-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98f72-124">OUTPUTS</span></span>

### <span data-ttu-id="98f72-125">Microsoft. Azure. Command. FrontDoor. models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="98f72-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="98f72-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98f72-126">NOTES</span></span>

## <span data-ttu-id="98f72-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98f72-127">RELATED LINKS</span></span>

<span data-ttu-id="98f72-128">[Új – AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [Új – AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="98f72-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
