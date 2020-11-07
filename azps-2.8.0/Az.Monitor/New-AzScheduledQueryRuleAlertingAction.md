---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 382aa35b9967e016ce87da982b32c97148c9f3c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837759"
---
# <span data-ttu-id="4d015-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="4d015-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="4d015-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d015-102">SYNOPSIS</span></span>
<span data-ttu-id="4d015-103">Értesítés típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="4d015-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="4d015-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d015-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d015-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d015-105">DESCRIPTION</span></span>
<span data-ttu-id="4d015-106">Egy olyan objektum létrehozása, amely figyelmeztetést jelenít meg, ezt az objektumot a rendszer a naplózási riasztási szabályt létrehozó parancshoz továbbítja.</span><span class="sxs-lookup"><span data-stu-id="4d015-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="4d015-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4d015-107">EXAMPLES</span></span>

### <span data-ttu-id="4d015-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4d015-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="4d015-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d015-109">PARAMETERS</span></span>

### <span data-ttu-id="4d015-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="4d015-110">-AznsAction</span></span>
<span data-ttu-id="4d015-111">A AzNS műveletek részletei</span><span class="sxs-lookup"><span data-stu-id="4d015-111">The AzNS action details</span></span>

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

### <span data-ttu-id="4d015-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d015-112">-DefaultProfile</span></span>
<span data-ttu-id="4d015-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d015-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d015-114">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="4d015-114">-Severity</span></span>
<span data-ttu-id="4d015-115">Az értesítés súlyossága</span><span class="sxs-lookup"><span data-stu-id="4d015-115">The severity for this alert</span></span>

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

### <span data-ttu-id="4d015-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="4d015-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="4d015-117">Az időtartam percben, amelyre a riasztást szabályozni kell</span><span class="sxs-lookup"><span data-stu-id="4d015-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="4d015-118">-Trigger</span><span class="sxs-lookup"><span data-stu-id="4d015-118">-Trigger</span></span>
<span data-ttu-id="4d015-119">A riasztási indító feltétel</span><span class="sxs-lookup"><span data-stu-id="4d015-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="4d015-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d015-120">CommonParameters</span></span>
<span data-ttu-id="4d015-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d015-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d015-122">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4d015-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d015-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d015-123">INPUTS</span></span>

### <span data-ttu-id="4d015-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="4d015-124">None</span></span>

## <span data-ttu-id="4d015-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d015-125">OUTPUTS</span></span>

### <span data-ttu-id="4d015-126">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="4d015-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="4d015-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d015-127">NOTES</span></span>

## <span data-ttu-id="4d015-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d015-128">RELATED LINKS</span></span>
