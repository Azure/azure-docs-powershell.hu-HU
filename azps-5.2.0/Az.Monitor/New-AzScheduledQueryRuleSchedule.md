---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 52f929cea9f2017ad6a2c2ea16475ec7d5d8a5a0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344861"
---
# <span data-ttu-id="fb963-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="fb963-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="fb963-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb963-102">SYNOPSIS</span></span>
<span data-ttu-id="fb963-103">Ütemezés típusú objektumot hoz létre</span><span class="sxs-lookup"><span data-stu-id="fb963-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="fb963-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fb963-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb963-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fb963-105">DESCRIPTION</span></span>
<span data-ttu-id="fb963-106">Ütemezés típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fb963-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="fb963-107">Ezt az objektumot a naplóriasztás szabályát figyelő parancsnak kell átadódni.</span><span class="sxs-lookup"><span data-stu-id="fb963-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="fb963-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fb963-108">EXAMPLES</span></span>

### <span data-ttu-id="fb963-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="fb963-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="fb963-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb963-110">PARAMETERS</span></span>

### <span data-ttu-id="fb963-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb963-111">-DefaultProfile</span></span>
<span data-ttu-id="fb963-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb963-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb963-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="fb963-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="fb963-114">A riasztás gyakorisága</span><span class="sxs-lookup"><span data-stu-id="fb963-114">The alert frequency</span></span>

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

### <span data-ttu-id="fb963-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="fb963-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="fb963-116">A riasztási időkeret</span><span class="sxs-lookup"><span data-stu-id="fb963-116">The alert time window</span></span>

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

### <span data-ttu-id="fb963-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb963-117">CommonParameters</span></span>
<span data-ttu-id="fb963-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb963-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb963-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb963-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb963-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb963-120">INPUTS</span></span>

### <span data-ttu-id="fb963-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="fb963-121">None</span></span>

## <span data-ttu-id="fb963-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb963-122">OUTPUTS</span></span>

### <span data-ttu-id="fb963-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="fb963-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="fb963-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fb963-124">NOTES</span></span>

## <span data-ttu-id="fb963-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb963-125">RELATED LINKS</span></span>
