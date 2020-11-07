---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: ce933affbe3b99854f1ce907c968f35645c1d777
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838704"
---
# <span data-ttu-id="1d19c-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="1d19c-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="1d19c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d19c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d19c-103">Információkat kap az adatfolyam-elemzésről.</span><span class="sxs-lookup"><span data-stu-id="1d19c-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="1d19c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d19c-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d19c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d19c-105">DESCRIPTION</span></span>
<span data-ttu-id="1d19c-106">A **Get-AzStreamAnalyticsTransformation** parancsmag információkat kap az adatfolyam-elemzési feladatokon meghatározott átalakításról.</span><span class="sxs-lookup"><span data-stu-id="1d19c-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="1d19c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1d19c-107">EXAMPLES</span></span>

### <span data-ttu-id="1d19c-108">1. példa: információk kérése az adatfolyam-elemzésről</span><span class="sxs-lookup"><span data-stu-id="1d19c-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="1d19c-109">Ez a parancs információt ad az StreamingJob nevű StreamingJob nevű átalakításról.</span><span class="sxs-lookup"><span data-stu-id="1d19c-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="1d19c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d19c-110">PARAMETERS</span></span>

### <span data-ttu-id="1d19c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d19c-111">-DefaultProfile</span></span>
<span data-ttu-id="1d19c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d19c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d19c-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="1d19c-113">-JobName</span></span>
<span data-ttu-id="1d19c-114">Annak az Azure stream Analytics-feladatnak a neve, amelyhez az Azure stream Analytics-transzformáció tartozik.</span><span class="sxs-lookup"><span data-stu-id="1d19c-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="1d19c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d19c-115">-Name</span></span>
<span data-ttu-id="1d19c-116">A lekérdezni kívánt Azure stream Analytics-transzformáció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d19c-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="1d19c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d19c-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d19c-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-transzformáció tartozik.</span><span class="sxs-lookup"><span data-stu-id="1d19c-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="1d19c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d19c-119">CommonParameters</span></span>
<span data-ttu-id="1d19c-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d19c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d19c-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d19c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d19c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d19c-122">INPUTS</span></span>

### <span data-ttu-id="1d19c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1d19c-123">System.String</span></span>

## <span data-ttu-id="1d19c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d19c-124">OUTPUTS</span></span>

### <span data-ttu-id="1d19c-125">Microsoft. Azure. Command. StreamAnalytics. models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="1d19c-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="1d19c-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d19c-126">NOTES</span></span>

## <span data-ttu-id="1d19c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d19c-127">RELATED LINKS</span></span>

[<span data-ttu-id="1d19c-128">Új – AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="1d19c-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


