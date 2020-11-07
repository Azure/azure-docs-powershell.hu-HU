---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 0679f4281d9528a7124f4a9a5235d47dd8af107c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841949"
---
# <span data-ttu-id="9a635-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="9a635-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="9a635-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a635-102">SYNOPSIS</span></span>
<span data-ttu-id="9a635-103">Forrás típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="9a635-103">Creates an object of type Source</span></span>

## <span data-ttu-id="9a635-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a635-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a635-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a635-105">DESCRIPTION</span></span>
<span data-ttu-id="9a635-106">Egy forrás típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9a635-106">Creates an object of type Source.</span></span>
<span data-ttu-id="9a635-107">Ezt az objektumot a naplózási riasztási szabályt létrehozó parancsnak kell átadnia</span><span class="sxs-lookup"><span data-stu-id="9a635-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="9a635-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9a635-108">EXAMPLES</span></span>

### <span data-ttu-id="9a635-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9a635-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="9a635-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a635-110">PARAMETERS</span></span>

### <span data-ttu-id="9a635-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="9a635-111">-AuthorizedResource</span></span>
<span data-ttu-id="9a635-112">A riasztásra jogosult források listája</span><span class="sxs-lookup"><span data-stu-id="9a635-112">The list of authorized resources for this alert</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a635-113">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="9a635-113">-DataSourceId</span></span>
<span data-ttu-id="9a635-114">Az az adatforrás, amelyen a riasztás létrejött</span><span class="sxs-lookup"><span data-stu-id="9a635-114">The data source on which this alert is created</span></span>

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

### <span data-ttu-id="9a635-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a635-115">-DefaultProfile</span></span>
<span data-ttu-id="9a635-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a635-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a635-117">-Query</span><span class="sxs-lookup"><span data-stu-id="9a635-117">-Query</span></span>
<span data-ttu-id="9a635-118">A riasztási lekérdezés</span><span class="sxs-lookup"><span data-stu-id="9a635-118">The alert query</span></span>

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

### <span data-ttu-id="9a635-119">-QueryType</span><span class="sxs-lookup"><span data-stu-id="9a635-119">-QueryType</span></span>
<span data-ttu-id="9a635-120">Lekérdezés típusa – jelenleg támogatott értékek: ResultCount</span><span class="sxs-lookup"><span data-stu-id="9a635-120">Type of Query - currently supported values : ResultCount</span></span>

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

### <span data-ttu-id="9a635-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a635-121">CommonParameters</span></span>
<span data-ttu-id="9a635-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a635-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a635-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9a635-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a635-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a635-124">INPUTS</span></span>

### <span data-ttu-id="9a635-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="9a635-125">None</span></span>

## <span data-ttu-id="9a635-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a635-126">OUTPUTS</span></span>

### <span data-ttu-id="9a635-127">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="9a635-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="9a635-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a635-128">NOTES</span></span>

## <span data-ttu-id="9a635-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a635-129">RELATED LINKS</span></span>
