---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 52f929cea9f2017ad6a2c2ea16475ec7d5d8a5a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203413"
---
# <span data-ttu-id="e5704-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e5704-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="e5704-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5704-102">SYNOPSIS</span></span>
<span data-ttu-id="e5704-103">Ütemezés típusú objektumot hoz létre</span><span class="sxs-lookup"><span data-stu-id="e5704-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="e5704-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e5704-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5704-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e5704-105">DESCRIPTION</span></span>
<span data-ttu-id="e5704-106">Ütemezés típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e5704-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="e5704-107">Ezt az objektumot a naplóriasztás szabályát figyelő parancsnak kell átadódni.</span><span class="sxs-lookup"><span data-stu-id="e5704-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="e5704-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e5704-108">EXAMPLES</span></span>

### <span data-ttu-id="e5704-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="e5704-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="e5704-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5704-110">PARAMETERS</span></span>

### <span data-ttu-id="e5704-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5704-111">-DefaultProfile</span></span>
<span data-ttu-id="e5704-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5704-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5704-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="e5704-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="e5704-114">A riasztás gyakorisága</span><span class="sxs-lookup"><span data-stu-id="e5704-114">The alert frequency</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5704-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="e5704-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="e5704-116">A riasztási időkeret</span><span class="sxs-lookup"><span data-stu-id="e5704-116">The alert time window</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5704-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5704-117">CommonParameters</span></span>
<span data-ttu-id="e5704-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5704-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5704-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5704-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5704-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5704-120">INPUTS</span></span>

### <span data-ttu-id="e5704-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="e5704-121">None</span></span>

## <span data-ttu-id="e5704-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5704-122">OUTPUTS</span></span>

### <span data-ttu-id="e5704-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e5704-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="e5704-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e5704-124">NOTES</span></span>

## <span data-ttu-id="e5704-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5704-125">RELATED LINKS</span></span>
