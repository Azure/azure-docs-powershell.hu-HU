---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466112"
---
# <span data-ttu-id="12c68-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="12c68-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="12c68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12c68-102">SYNOPSIS</span></span>
<span data-ttu-id="12c68-103">Felügyelt szabály felülbírálási objektumának létrehozása</span><span class="sxs-lookup"><span data-stu-id="12c68-103">Create managed rule override object</span></span>

## <span data-ttu-id="12c68-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="12c68-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12c68-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="12c68-105">DESCRIPTION</span></span>
<span data-ttu-id="12c68-106">PSAzureManagedRuleOverride objektum létrehozása felügyelt WAF-szabálycsoport felülbírálása objektum létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="12c68-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="12c68-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="12c68-107">EXAMPLES</span></span>

### <span data-ttu-id="12c68-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="12c68-108">Example 1</span></span>
<span data-ttu-id="12c68-109">Felügyelt szabály felülbírálási objektumának létrehozása a 942250-es szabályhoz (amely az SQLI-csoportban van).</span><span class="sxs-lookup"><span data-stu-id="12c68-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="12c68-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12c68-110">PARAMETERS</span></span>

### <span data-ttu-id="12c68-111">-Művelet</span><span class="sxs-lookup"><span data-stu-id="12c68-111">-Action</span></span>
<span data-ttu-id="12c68-112">Felülbírálás művelet</span><span class="sxs-lookup"><span data-stu-id="12c68-112">Override Action</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c68-113">-DefaultProfile</span></span>
<span data-ttu-id="12c68-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12c68-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12c68-115">-Disabled</span><span class="sxs-lookup"><span data-stu-id="12c68-115">-Disabled</span></span>
<span data-ttu-id="12c68-116">Letiltott állapot</span><span class="sxs-lookup"><span data-stu-id="12c68-116">Disabled state</span></span>

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

### <span data-ttu-id="12c68-117">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="12c68-117">-Exclusion</span></span>
<span data-ttu-id="12c68-118">Kivétel</span><span class="sxs-lookup"><span data-stu-id="12c68-118">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c68-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="12c68-119">-RuleId</span></span>
<span data-ttu-id="12c68-120">Szabályazonosító</span><span class="sxs-lookup"><span data-stu-id="12c68-120">Rule ID</span></span>

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

### <span data-ttu-id="12c68-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c68-121">CommonParameters</span></span>
<span data-ttu-id="12c68-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12c68-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c68-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12c68-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c68-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12c68-124">INPUTS</span></span>

### <span data-ttu-id="12c68-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="12c68-125">None</span></span>

## <span data-ttu-id="12c68-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12c68-126">OUTPUTS</span></span>

### <span data-ttu-id="12c68-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="12c68-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="12c68-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="12c68-128">NOTES</span></span>

## <span data-ttu-id="12c68-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12c68-129">RELATED LINKS</span></span>

[<span data-ttu-id="12c68-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="12c68-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)