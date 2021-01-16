---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 41ce3c066651cb2bc6ea13ddd0a7a3bb15d28879
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331541"
---
# <span data-ttu-id="4dfc3-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="4dfc3-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="4dfc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dfc3-102">SYNOPSIS</span></span>
<span data-ttu-id="4dfc3-103">Riasztási művelet típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4dfc3-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="4dfc3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4dfc3-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dfc3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4dfc3-105">DESCRIPTION</span></span>
<span data-ttu-id="4dfc3-106">Riasztási művelet típusú objektumot hoz létre. Ezt az objektumot a naplóriasztás szabályát figyelő parancsnak kell átadódni.</span><span class="sxs-lookup"><span data-stu-id="4dfc3-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="4dfc3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4dfc3-107">EXAMPLES</span></span>

### <span data-ttu-id="4dfc3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="4dfc3-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="4dfc3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dfc3-109">PARAMETERS</span></span>

### <span data-ttu-id="4dfc3-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="4dfc3-110">-AznsAction</span></span>
<span data-ttu-id="4dfc3-111">Az AzNS művelet részletei</span><span class="sxs-lookup"><span data-stu-id="4dfc3-111">The AzNS action details</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dfc3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dfc3-112">-DefaultProfile</span></span>
<span data-ttu-id="4dfc3-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4dfc3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dfc3-114">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="4dfc3-114">-Severity</span></span>
<span data-ttu-id="4dfc3-115">A riasztás súlyossága</span><span class="sxs-lookup"><span data-stu-id="4dfc3-115">The severity for this alert</span></span>

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

### <span data-ttu-id="4dfc3-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="4dfc3-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="4dfc3-117">Az az időtartam percben, amelynél a riasztást le kell szabályozásnak ki kell elégedni</span><span class="sxs-lookup"><span data-stu-id="4dfc3-117">The duration in minutes for which alert should be throttled</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dfc3-118">-Trigger</span><span class="sxs-lookup"><span data-stu-id="4dfc3-118">-Trigger</span></span>
<span data-ttu-id="4dfc3-119">A riasztási eseményindító feltétele</span><span class="sxs-lookup"><span data-stu-id="4dfc3-119">The alert trigger condition</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dfc3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dfc3-120">CommonParameters</span></span>
<span data-ttu-id="4dfc3-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dfc3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dfc3-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dfc3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dfc3-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4dfc3-123">INPUTS</span></span>

### <span data-ttu-id="4dfc3-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="4dfc3-124">None</span></span>

## <span data-ttu-id="4dfc3-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dfc3-125">OUTPUTS</span></span>

### <span data-ttu-id="4dfc3-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="4dfc3-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="4dfc3-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4dfc3-127">NOTES</span></span>

## <span data-ttu-id="4dfc3-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4dfc3-128">RELATED LINKS</span></span>
