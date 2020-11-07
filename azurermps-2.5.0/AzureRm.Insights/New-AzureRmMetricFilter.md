---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
ms.openlocfilehash: 42633beddee9e6681e68ce1ba61e71d276abf478
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849325"
---
# <span data-ttu-id="ca88d-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="ca88d-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="ca88d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca88d-102">SYNOPSIS</span></span>
<span data-ttu-id="ca88d-103">A mérőszámok lekérdezéséhez használható metrikus dimenzió szűrőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ca88d-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca88d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca88d-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca88d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca88d-105">DESCRIPTION</span></span>
<span data-ttu-id="ca88d-106">A **New-AzureRmMetricFilter** parancsmag olyan metrikus dimenzióértéket hoz létre, amely a mérőszámok lekérdezéséhez használható.</span><span class="sxs-lookup"><span data-stu-id="ca88d-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="ca88d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ca88d-107">EXAMPLES</span></span>

### <span data-ttu-id="ca88d-108">Példa 1: metrikus dimenzióérték létrehozása</span><span class="sxs-lookup"><span data-stu-id="ca88d-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="ca88d-109">Ez a parancs metrikus dimenzió szűrőt hoz létre a "város EQ" Seattle vagy a City EQ "New York" formátumhoz.</span><span class="sxs-lookup"><span data-stu-id="ca88d-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="ca88d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca88d-110">PARAMETERS</span></span>

### <span data-ttu-id="ca88d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca88d-111">-DefaultProfile</span></span>
<span data-ttu-id="ca88d-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca88d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca88d-113">-Dimension (dimenzió)</span><span class="sxs-lookup"><span data-stu-id="ca88d-113">-Dimension</span></span>
<span data-ttu-id="ca88d-114">A mérőszám méretének neve.</span><span class="sxs-lookup"><span data-stu-id="ca88d-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="ca88d-115">-Operátor</span><span class="sxs-lookup"><span data-stu-id="ca88d-115">-Operator</span></span>
<span data-ttu-id="ca88d-116">A metrikus dimenzió kiválasztásához használt operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca88d-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="ca88d-117">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="ca88d-117">-Value</span></span>
<span data-ttu-id="ca88d-118">A metrikus dimenzió értékek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca88d-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="ca88d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca88d-119">CommonParameters</span></span>
<span data-ttu-id="ca88d-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca88d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca88d-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca88d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca88d-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca88d-122">INPUTS</span></span>

### <span data-ttu-id="ca88d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ca88d-123">System.String</span></span>

### <span data-ttu-id="ca88d-124">System. string []</span><span class="sxs-lookup"><span data-stu-id="ca88d-124">System.String[]</span></span>

## <span data-ttu-id="ca88d-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca88d-125">OUTPUTS</span></span>

### <span data-ttu-id="ca88d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ca88d-126">System.String</span></span>

## <span data-ttu-id="ca88d-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca88d-127">NOTES</span></span>

## <span data-ttu-id="ca88d-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca88d-128">RELATED LINKS</span></span>

<span data-ttu-id="ca88d-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="ca88d-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

