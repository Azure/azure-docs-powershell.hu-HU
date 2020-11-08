---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183574"
---
# <span data-ttu-id="0ca3d-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="0ca3d-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="0ca3d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ca3d-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca3d-103">Felügyelt szabály létrehozása objektum felülírása</span><span class="sxs-lookup"><span data-stu-id="0ca3d-103">Create managed rule override object</span></span>

## <span data-ttu-id="0ca3d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ca3d-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ca3d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ca3d-105">DESCRIPTION</span></span>
<span data-ttu-id="0ca3d-106">PSAzureManagedRuleOverride objektum létrehozása a felügyelt WAF szabályok csoportjának objektum létrehozása felülbírálása.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="0ca3d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0ca3d-107">EXAMPLES</span></span>

### <span data-ttu-id="0ca3d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0ca3d-108">Example 1</span></span>
<span data-ttu-id="0ca3d-109">Felügyelt szabály létrehozása: annak az objektumnak a létrehozása, amely a 942250 szabályhoz van (ez a SQLI csoportban található).</span><span class="sxs-lookup"><span data-stu-id="0ca3d-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="0ca3d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ca3d-110">PARAMETERS</span></span>

### <span data-ttu-id="0ca3d-111">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="0ca3d-111">-Action</span></span>
<span data-ttu-id="0ca3d-112">Művelet felülírása</span><span class="sxs-lookup"><span data-stu-id="0ca3d-112">Override Action</span></span>

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

### <span data-ttu-id="0ca3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca3d-113">-DefaultProfile</span></span>
<span data-ttu-id="0ca3d-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ca3d-115">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="0ca3d-115">-Disabled</span></span>
<span data-ttu-id="0ca3d-116">Letiltott állapot</span><span class="sxs-lookup"><span data-stu-id="0ca3d-116">Disabled state</span></span>

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

### <span data-ttu-id="0ca3d-117">– Kizárás</span><span class="sxs-lookup"><span data-stu-id="0ca3d-117">-Exclusion</span></span>
<span data-ttu-id="0ca3d-118">Kirekesztés</span><span class="sxs-lookup"><span data-stu-id="0ca3d-118">Exclusion</span></span>

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

### <span data-ttu-id="0ca3d-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="0ca3d-119">-RuleId</span></span>
<span data-ttu-id="0ca3d-120">Szabály azonosítója</span><span class="sxs-lookup"><span data-stu-id="0ca3d-120">Rule ID</span></span>

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

### <span data-ttu-id="0ca3d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca3d-121">CommonParameters</span></span>
<span data-ttu-id="0ca3d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ca3d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca3d-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0ca3d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca3d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ca3d-124">INPUTS</span></span>

### <span data-ttu-id="0ca3d-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="0ca3d-125">None</span></span>

## <span data-ttu-id="0ca3d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ca3d-126">OUTPUTS</span></span>

### <span data-ttu-id="0ca3d-127">Microsoft. Azure. Command. FrontDoor. models. PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="0ca3d-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="0ca3d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ca3d-128">NOTES</span></span>

## <span data-ttu-id="0ca3d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ca3d-129">RELATED LINKS</span></span>

[<span data-ttu-id="0ca3d-130">Új – AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="0ca3d-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)