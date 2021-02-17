---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
ms.openlocfilehash: c72573f467377a4ea16fd487a8cee5f0055a5cee
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401453"
---
# <span data-ttu-id="6b05e-101">New-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="6b05e-101">New-AzFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="6b05e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b05e-102">SYNOPSIS</span></span>
<span data-ttu-id="6b05e-103">FelügyeltRule-objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="6b05e-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="6b05e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b05e-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b05e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b05e-105">DESCRIPTION</span></span>
<span data-ttu-id="6b05e-106">FelügyeltRule-objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="6b05e-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="6b05e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b05e-107">EXAMPLES</span></span>

### <span data-ttu-id="6b05e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="6b05e-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="6b05e-109">ManagedRule-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="6b05e-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="6b05e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b05e-110">PARAMETERS</span></span>

### <span data-ttu-id="6b05e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b05e-111">-DefaultProfile</span></span>
<span data-ttu-id="6b05e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b05e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b05e-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="6b05e-113">-RuleGroupOverride</span></span>
<span data-ttu-id="6b05e-114">Az Azure felügyelt szolgáltató felülbírálási konfigurációjának listája</span><span class="sxs-lookup"><span data-stu-id="6b05e-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="6b05e-115">-Type</span><span class="sxs-lookup"><span data-stu-id="6b05e-115">-Type</span></span>
<span data-ttu-id="6b05e-116">A szabálykészlet típusa</span><span class="sxs-lookup"><span data-stu-id="6b05e-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="6b05e-117">-Version</span><span class="sxs-lookup"><span data-stu-id="6b05e-117">-Version</span></span>
<span data-ttu-id="6b05e-118">A szabálykészlet verziója</span><span class="sxs-lookup"><span data-stu-id="6b05e-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="6b05e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b05e-119">CommonParameters</span></span>
<span data-ttu-id="6b05e-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b05e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b05e-121">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b05e-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b05e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b05e-122">INPUTS</span></span>

### <span data-ttu-id="6b05e-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="6b05e-123">None</span></span>

## <span data-ttu-id="6b05e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b05e-124">OUTPUTS</span></span>

### <span data-ttu-id="6b05e-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="6b05e-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="6b05e-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b05e-126">NOTES</span></span>

## <span data-ttu-id="6b05e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b05e-127">RELATED LINKS</span></span>

<span data-ttu-id="6b05e-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="6b05e-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span></span>
