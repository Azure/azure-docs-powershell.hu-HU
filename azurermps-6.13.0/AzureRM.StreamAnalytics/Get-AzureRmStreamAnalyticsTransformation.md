---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: d83038d521e562ec835324dd50740ec929fb5893
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491837"
---
# <span data-ttu-id="17200-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="17200-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="17200-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17200-102">SYNOPSIS</span></span>
<span data-ttu-id="17200-103">Információkat kap az adatfolyam-elemzésről.</span><span class="sxs-lookup"><span data-stu-id="17200-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17200-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17200-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17200-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="17200-105">DESCRIPTION</span></span>
<span data-ttu-id="17200-106">A **Get-AzureRmStreamAnalyticsTransformation** parancsmag információkat kap az adatfolyam-elemzési feladatokon meghatározott átalakításról.</span><span class="sxs-lookup"><span data-stu-id="17200-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="17200-107">Példák</span><span class="sxs-lookup"><span data-stu-id="17200-107">EXAMPLES</span></span>

### <span data-ttu-id="17200-108">1. példa: információk kérése az adatfolyam-elemzésről</span><span class="sxs-lookup"><span data-stu-id="17200-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="17200-109">Ez a parancs információt ad az StreamingJob nevű StreamingJob nevű átalakításról.</span><span class="sxs-lookup"><span data-stu-id="17200-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="17200-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17200-110">PARAMETERS</span></span>

### <span data-ttu-id="17200-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17200-111">-DefaultProfile</span></span>
<span data-ttu-id="17200-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17200-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17200-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="17200-113">-JobName</span></span>
<span data-ttu-id="17200-114">Annak az Azure stream Analytics-feladatnak a neve, amelyhez az Azure stream Analytics-transzformáció tartozik.</span><span class="sxs-lookup"><span data-stu-id="17200-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="17200-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="17200-115">-Name</span></span>
<span data-ttu-id="17200-116">A lekérdezni kívánt Azure stream Analytics-transzformáció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="17200-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17200-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17200-117">-ResourceGroupName</span></span>
<span data-ttu-id="17200-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-transzformáció tartozik.</span><span class="sxs-lookup"><span data-stu-id="17200-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="17200-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17200-119">CommonParameters</span></span>
<span data-ttu-id="17200-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17200-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17200-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17200-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17200-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17200-122">INPUTS</span></span>

### <span data-ttu-id="17200-123">System. String</span><span class="sxs-lookup"><span data-stu-id="17200-123">System.String</span></span>

## <span data-ttu-id="17200-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17200-124">OUTPUTS</span></span>

### <span data-ttu-id="17200-125">Microsoft. Azure. Command. StreamAnalytics. models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="17200-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="17200-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17200-126">NOTES</span></span>

## <span data-ttu-id="17200-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17200-127">RELATED LINKS</span></span>

[<span data-ttu-id="17200-128">Új – AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="17200-128">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


