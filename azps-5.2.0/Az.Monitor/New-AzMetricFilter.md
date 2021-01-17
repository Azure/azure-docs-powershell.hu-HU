---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331565"
---
# <span data-ttu-id="7e127-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="7e127-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="7e127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e127-102">SYNOPSIS</span></span>
<span data-ttu-id="7e127-103">Metrikus dimenziószűrőt hoz létre, amely használható a metrikák lekérdezéséhez.</span><span class="sxs-lookup"><span data-stu-id="7e127-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="7e127-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e127-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e127-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e127-105">DESCRIPTION</span></span>
<span data-ttu-id="7e127-106">A **New-AzMetricFilter** parancsmag létrehoz egy metrikus dimenziószűrőt, amely használható a metrikák lekérdezéséhez.</span><span class="sxs-lookup"><span data-stu-id="7e127-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="7e127-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e127-107">EXAMPLES</span></span>

### <span data-ttu-id="7e127-108">1. példa: Metrikus dimenziószűrő létrehozása</span><span class="sxs-lookup"><span data-stu-id="7e127-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="7e127-109">Ezzel a paranccsal metrikus dimenziószűrőt hoz létre a "Gyenes város" vagy a Város eq 'New York' formátumban.</span><span class="sxs-lookup"><span data-stu-id="7e127-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="7e127-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e127-110">PARAMETERS</span></span>

### <span data-ttu-id="7e127-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e127-111">-DefaultProfile</span></span>
<span data-ttu-id="7e127-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e127-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e127-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="7e127-113">-Dimension</span></span>
<span data-ttu-id="7e127-114">A metrikus dimenzió neve.</span><span class="sxs-lookup"><span data-stu-id="7e127-114">The name of the metric dimension.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e127-115">-Operátor</span><span class="sxs-lookup"><span data-stu-id="7e127-115">-Operator</span></span>
<span data-ttu-id="7e127-116">A metrikus dimenzió kiválasztásához használt operátor.</span><span class="sxs-lookup"><span data-stu-id="7e127-116">Specifies the operator used to select the metric dimension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e127-117">-Érték</span><span class="sxs-lookup"><span data-stu-id="7e127-117">-Value</span></span>
<span data-ttu-id="7e127-118">A metrikus dimenzióértékek tömbje.</span><span class="sxs-lookup"><span data-stu-id="7e127-118">Specifies the array of metric dimension values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e127-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e127-119">CommonParameters</span></span>
<span data-ttu-id="7e127-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e127-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e127-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e127-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e127-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e127-122">INPUTS</span></span>

### <span data-ttu-id="7e127-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7e127-123">System.String</span></span>

### <span data-ttu-id="7e127-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7e127-124">System.String[]</span></span>

## <span data-ttu-id="7e127-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e127-125">OUTPUTS</span></span>

### <span data-ttu-id="7e127-126">System.String</span><span class="sxs-lookup"><span data-stu-id="7e127-126">System.String</span></span>

## <span data-ttu-id="7e127-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e127-127">NOTES</span></span>

## <span data-ttu-id="7e127-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e127-128">RELATED LINKS</span></span>

<span data-ttu-id="7e127-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="7e127-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

