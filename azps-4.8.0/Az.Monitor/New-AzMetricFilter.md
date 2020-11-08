---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181800"
---
# <span data-ttu-id="af68e-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="af68e-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="af68e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af68e-102">SYNOPSIS</span></span>
<span data-ttu-id="af68e-103">A mérőszámok lekérdezéséhez használható metrikus dimenzió szűrőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="af68e-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="af68e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af68e-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af68e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af68e-105">DESCRIPTION</span></span>
<span data-ttu-id="af68e-106">A **New-AzMetricFilter** parancsmag olyan metrikus dimenzióértéket hoz létre, amely a mérőszámok lekérdezéséhez használható.</span><span class="sxs-lookup"><span data-stu-id="af68e-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="af68e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="af68e-107">EXAMPLES</span></span>

### <span data-ttu-id="af68e-108">Példa 1: metrikus dimenzióérték létrehozása</span><span class="sxs-lookup"><span data-stu-id="af68e-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="af68e-109">Ez a parancs metrikus dimenzió szűrőt hoz létre a "város EQ" Seattle vagy a City EQ "New York" formátumhoz.</span><span class="sxs-lookup"><span data-stu-id="af68e-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="af68e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af68e-110">PARAMETERS</span></span>

### <span data-ttu-id="af68e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af68e-111">-DefaultProfile</span></span>
<span data-ttu-id="af68e-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af68e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af68e-113">-Dimension (dimenzió)</span><span class="sxs-lookup"><span data-stu-id="af68e-113">-Dimension</span></span>
<span data-ttu-id="af68e-114">A mérőszám méretének neve.</span><span class="sxs-lookup"><span data-stu-id="af68e-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="af68e-115">-Operátor</span><span class="sxs-lookup"><span data-stu-id="af68e-115">-Operator</span></span>
<span data-ttu-id="af68e-116">A metrikus dimenzió kiválasztásához használt operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="af68e-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="af68e-117">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="af68e-117">-Value</span></span>
<span data-ttu-id="af68e-118">A metrikus dimenzió értékek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af68e-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="af68e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af68e-119">CommonParameters</span></span>
<span data-ttu-id="af68e-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af68e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af68e-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="af68e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af68e-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af68e-122">INPUTS</span></span>

### <span data-ttu-id="af68e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="af68e-123">System.String</span></span>

### <span data-ttu-id="af68e-124">System. string []</span><span class="sxs-lookup"><span data-stu-id="af68e-124">System.String[]</span></span>

## <span data-ttu-id="af68e-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af68e-125">OUTPUTS</span></span>

### <span data-ttu-id="af68e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="af68e-126">System.String</span></span>

## <span data-ttu-id="af68e-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af68e-127">NOTES</span></span>

## <span data-ttu-id="af68e-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af68e-128">RELATED LINKS</span></span>

<span data-ttu-id="af68e-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="af68e-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

