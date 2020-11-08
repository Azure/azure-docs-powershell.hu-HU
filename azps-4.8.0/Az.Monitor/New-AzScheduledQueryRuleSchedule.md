---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 52f929cea9f2017ad6a2c2ea16475ec7d5d8a5a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024705"
---
# <span data-ttu-id="20854-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="20854-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="20854-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20854-102">SYNOPSIS</span></span>
<span data-ttu-id="20854-103">Az ütemterv típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="20854-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="20854-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20854-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20854-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20854-105">DESCRIPTION</span></span>
<span data-ttu-id="20854-106">Az ütemezés típusú objektumot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="20854-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="20854-107">Ezt az objektumot a naplózási riasztási szabályt létrehozó parancsnak kell átadnia.</span><span class="sxs-lookup"><span data-stu-id="20854-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="20854-108">Példák</span><span class="sxs-lookup"><span data-stu-id="20854-108">EXAMPLES</span></span>

### <span data-ttu-id="20854-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="20854-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="20854-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20854-110">PARAMETERS</span></span>

### <span data-ttu-id="20854-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20854-111">-DefaultProfile</span></span>
<span data-ttu-id="20854-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20854-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20854-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="20854-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="20854-114">Az értesítési gyakoriság</span><span class="sxs-lookup"><span data-stu-id="20854-114">The alert frequency</span></span>

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

### <span data-ttu-id="20854-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="20854-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="20854-116">A riasztási idő ablaka</span><span class="sxs-lookup"><span data-stu-id="20854-116">The alert time window</span></span>

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

### <span data-ttu-id="20854-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20854-117">CommonParameters</span></span>
<span data-ttu-id="20854-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20854-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20854-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="20854-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20854-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20854-120">INPUTS</span></span>

### <span data-ttu-id="20854-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="20854-121">None</span></span>

## <span data-ttu-id="20854-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20854-122">OUTPUTS</span></span>

### <span data-ttu-id="20854-123">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="20854-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="20854-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20854-124">NOTES</span></span>

## <span data-ttu-id="20854-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20854-125">RELATED LINKS</span></span>
