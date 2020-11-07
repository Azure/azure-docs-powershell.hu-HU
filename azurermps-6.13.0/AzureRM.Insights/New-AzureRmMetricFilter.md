---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
ms.openlocfilehash: 783f5c780b0202ddb78666c2c7446ba07b5434e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680672"
---
# <span data-ttu-id="02f2b-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="02f2b-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="02f2b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="02f2b-103">A mérőszámok lekérdezéséhez használható metrikus dimenzió szűrőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="02f2b-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02f2b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02f2b-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02f2b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="02f2b-105">DESCRIPTION</span></span>
<span data-ttu-id="02f2b-106">A **New-AzureRmMetricFilter** parancsmag olyan metrikus dimenzióértéket hoz létre, amely a mérőszámok lekérdezéséhez használható.</span><span class="sxs-lookup"><span data-stu-id="02f2b-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="02f2b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="02f2b-107">EXAMPLES</span></span>

### <span data-ttu-id="02f2b-108">Példa 1: metrikus dimenzióérték létrehozása</span><span class="sxs-lookup"><span data-stu-id="02f2b-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="02f2b-109">Ez a parancs metrikus dimenzió szűrőt hoz létre a "város EQ" Seattle vagy a City EQ "New York" formátumhoz.</span><span class="sxs-lookup"><span data-stu-id="02f2b-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="02f2b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02f2b-110">PARAMETERS</span></span>

### <span data-ttu-id="02f2b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f2b-111">-DefaultProfile</span></span>
<span data-ttu-id="02f2b-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02f2b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02f2b-113">-Dimension (dimenzió)</span><span class="sxs-lookup"><span data-stu-id="02f2b-113">-Dimension</span></span>
<span data-ttu-id="02f2b-114">A mérőszám méretének neve.</span><span class="sxs-lookup"><span data-stu-id="02f2b-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="02f2b-115">-Operátor</span><span class="sxs-lookup"><span data-stu-id="02f2b-115">-Operator</span></span>
<span data-ttu-id="02f2b-116">A metrikus dimenzió kiválasztásához használt operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="02f2b-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="02f2b-117">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="02f2b-117">-Value</span></span>
<span data-ttu-id="02f2b-118">A metrikus dimenzió értékek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02f2b-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="02f2b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f2b-119">CommonParameters</span></span>
<span data-ttu-id="02f2b-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02f2b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f2b-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02f2b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f2b-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02f2b-122">INPUTS</span></span>

### <span data-ttu-id="02f2b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="02f2b-123">System.String</span></span>

### <span data-ttu-id="02f2b-124">System. string []</span><span class="sxs-lookup"><span data-stu-id="02f2b-124">System.String[]</span></span>

## <span data-ttu-id="02f2b-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02f2b-125">OUTPUTS</span></span>

### <span data-ttu-id="02f2b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="02f2b-126">System.String</span></span>

## <span data-ttu-id="02f2b-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02f2b-127">NOTES</span></span>

## <span data-ttu-id="02f2b-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02f2b-128">RELATED LINKS</span></span>

<span data-ttu-id="02f2b-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="02f2b-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

