---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 0fe5684805dfc3047abb39040d80eb8a388cf5a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002837"
---
# <span data-ttu-id="bf495-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="bf495-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="bf495-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf495-102">SYNOPSIS</span></span>
<span data-ttu-id="bf495-103">Forrás típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="bf495-103">Creates an object of type Source</span></span>

## <span data-ttu-id="bf495-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf495-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf495-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf495-105">DESCRIPTION</span></span>
<span data-ttu-id="bf495-106">Egy forrás típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bf495-106">Creates an object of type Source.</span></span>
<span data-ttu-id="bf495-107">Ezt az objektumot a naplózási riasztási szabályt létrehozó parancsnak kell átadnia</span><span class="sxs-lookup"><span data-stu-id="bf495-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="bf495-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bf495-108">EXAMPLES</span></span>

### <span data-ttu-id="bf495-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bf495-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="bf495-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf495-110">PARAMETERS</span></span>

### <span data-ttu-id="bf495-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="bf495-111">-AuthorizedResource</span></span>
<span data-ttu-id="bf495-112">A riasztásra jogosult források listája</span><span class="sxs-lookup"><span data-stu-id="bf495-112">The list of authorized resources for this alert</span></span>

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

### <span data-ttu-id="bf495-113">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="bf495-113">-DataSourceId</span></span>
<span data-ttu-id="bf495-114">Az az adatforrás, amelyen a riasztás létrejött</span><span class="sxs-lookup"><span data-stu-id="bf495-114">The data source on which this alert is created</span></span>

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

### <span data-ttu-id="bf495-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf495-115">-DefaultProfile</span></span>
<span data-ttu-id="bf495-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf495-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf495-117">-Query</span><span class="sxs-lookup"><span data-stu-id="bf495-117">-Query</span></span>
<span data-ttu-id="bf495-118">A riasztási lekérdezés</span><span class="sxs-lookup"><span data-stu-id="bf495-118">The alert query</span></span>

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

### <span data-ttu-id="bf495-119">-QueryType</span><span class="sxs-lookup"><span data-stu-id="bf495-119">-QueryType</span></span>
<span data-ttu-id="bf495-120">Lekérdezés típusa – jelenleg támogatott értékek: ResultCount</span><span class="sxs-lookup"><span data-stu-id="bf495-120">Type of Query - currently supported values : ResultCount</span></span>

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

### <span data-ttu-id="bf495-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf495-121">CommonParameters</span></span>
<span data-ttu-id="bf495-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf495-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf495-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bf495-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf495-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf495-124">INPUTS</span></span>

### <span data-ttu-id="bf495-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="bf495-125">None</span></span>

## <span data-ttu-id="bf495-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf495-126">OUTPUTS</span></span>

### <span data-ttu-id="bf495-127">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="bf495-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="bf495-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf495-128">NOTES</span></span>

## <span data-ttu-id="bf495-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf495-129">RELATED LINKS</span></span>
