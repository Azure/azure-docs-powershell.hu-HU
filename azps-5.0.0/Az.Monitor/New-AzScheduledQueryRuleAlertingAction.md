---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 41ce3c066651cb2bc6ea13ddd0a7a3bb15d28879
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187294"
---
# <span data-ttu-id="19556-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="19556-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="19556-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19556-102">SYNOPSIS</span></span>
<span data-ttu-id="19556-103">Értesítés típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="19556-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="19556-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19556-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19556-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19556-105">DESCRIPTION</span></span>
<span data-ttu-id="19556-106">Egy olyan objektum létrehozása, amely figyelmeztetést jelenít meg, ezt az objektumot a rendszer a naplózási riasztási szabályt létrehozó parancshoz továbbítja.</span><span class="sxs-lookup"><span data-stu-id="19556-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="19556-107">Példák</span><span class="sxs-lookup"><span data-stu-id="19556-107">EXAMPLES</span></span>

### <span data-ttu-id="19556-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="19556-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="19556-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19556-109">PARAMETERS</span></span>

### <span data-ttu-id="19556-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="19556-110">-AznsAction</span></span>
<span data-ttu-id="19556-111">A AzNS műveletek részletei</span><span class="sxs-lookup"><span data-stu-id="19556-111">The AzNS action details</span></span>

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

### <span data-ttu-id="19556-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19556-112">-DefaultProfile</span></span>
<span data-ttu-id="19556-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19556-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19556-114">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="19556-114">-Severity</span></span>
<span data-ttu-id="19556-115">Az értesítés súlyossága</span><span class="sxs-lookup"><span data-stu-id="19556-115">The severity for this alert</span></span>

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

### <span data-ttu-id="19556-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="19556-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="19556-117">Az időtartam percben, amelyre a riasztást szabályozni kell</span><span class="sxs-lookup"><span data-stu-id="19556-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="19556-118">-Trigger</span><span class="sxs-lookup"><span data-stu-id="19556-118">-Trigger</span></span>
<span data-ttu-id="19556-119">A riasztási indító feltétel</span><span class="sxs-lookup"><span data-stu-id="19556-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="19556-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19556-120">CommonParameters</span></span>
<span data-ttu-id="19556-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19556-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19556-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="19556-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19556-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19556-123">INPUTS</span></span>

### <span data-ttu-id="19556-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="19556-124">None</span></span>

## <span data-ttu-id="19556-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19556-125">OUTPUTS</span></span>

### <span data-ttu-id="19556-126">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="19556-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="19556-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19556-127">NOTES</span></span>

## <span data-ttu-id="19556-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19556-128">RELATED LINKS</span></span>