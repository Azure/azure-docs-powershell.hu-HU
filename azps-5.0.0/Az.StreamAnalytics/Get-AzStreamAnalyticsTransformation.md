---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195015"
---
# <span data-ttu-id="b2ae6-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="b2ae6-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="b2ae6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="b2ae6-103">Információkat kap az adatfolyam-elemzésről.</span><span class="sxs-lookup"><span data-stu-id="b2ae6-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="b2ae6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2ae6-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2ae6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2ae6-105">DESCRIPTION</span></span>
<span data-ttu-id="b2ae6-106">A **Get-AzStreamAnalyticsTransformation** parancsmag információkat kap az adatfolyam-elemzési feladatokon meghatározott átalakításról.</span><span class="sxs-lookup"><span data-stu-id="b2ae6-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="b2ae6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b2ae6-107">EXAMPLES</span></span>

### <span data-ttu-id="b2ae6-108">1. példa: információk kérése az adatfolyam-elemzésről</span><span class="sxs-lookup"><span data-stu-id="b2ae6-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="b2ae6-109">Ez a parancs információt ad az StreamingJob nevű StreamingJob nevű átalakításról.</span><span class="sxs-lookup"><span data-stu-id="b2ae6-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="b2ae6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2ae6-110">PARAMETERS</span></span>

### <span data-ttu-id="b2ae6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2ae6-111">-DefaultProfile</span></span>
<span data-ttu-id="b2ae6-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2ae6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2ae6-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="b2ae6-113">-JobName</span></span>
<span data-ttu-id="b2ae6-114">Annak az Azure stream Analytics-feladatnak a neve, amelyhez az Azure stream Analytics-transzformáció tartozik.</span><span class="sxs-lookup"><span data-stu-id="b2ae6-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="b2ae6-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b2ae6-115">-Name</span></span>
<span data-ttu-id="b2ae6-116">A lekérdezni kívánt Azure stream Analytics-transzformáció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2ae6-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="b2ae6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2ae6-117">-ResourceGroupName</span></span>
<span data-ttu-id="b2ae6-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-transzformáció tartozik.</span><span class="sxs-lookup"><span data-stu-id="b2ae6-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="b2ae6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2ae6-119">CommonParameters</span></span>
<span data-ttu-id="b2ae6-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2ae6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2ae6-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2ae6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2ae6-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2ae6-122">INPUTS</span></span>

### <span data-ttu-id="b2ae6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b2ae6-123">System.String</span></span>

## <span data-ttu-id="b2ae6-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2ae6-124">OUTPUTS</span></span>

### <span data-ttu-id="b2ae6-125">Microsoft. Azure. Command. StreamAnalytics. models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="b2ae6-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="b2ae6-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2ae6-126">NOTES</span></span>

## <span data-ttu-id="b2ae6-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2ae6-127">RELATED LINKS</span></span>

[<span data-ttu-id="b2ae6-128">Új – AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="b2ae6-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


