---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: b6edc46131bac545d649e6ea3fe41b142d596850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493311"
---
# <span data-ttu-id="937c5-101">Get-AzureRmStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="937c5-101">Get-AzureRmStreamAnalyticsQuota</span></span>

## <span data-ttu-id="937c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="937c5-102">SYNOPSIS</span></span>
<span data-ttu-id="937c5-103">Információt kap egy régió streaming Unit kvótáról.</span><span class="sxs-lookup"><span data-stu-id="937c5-103">Gets information about the Streaming Unit quota for a region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="937c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="937c5-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="937c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="937c5-105">DESCRIPTION</span></span>
<span data-ttu-id="937c5-106">A **Get-AzureRmStreamAnalyticsQuota** parancsmag információkat kap egy adott terület adatfolyam-kvótáról.</span><span class="sxs-lookup"><span data-stu-id="937c5-106">The **Get-AzureRmStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="937c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="937c5-107">EXAMPLES</span></span>

### <span data-ttu-id="937c5-108">1. példa: információk beszerzése egy régió streaming Unit kvótáról</span><span class="sxs-lookup"><span data-stu-id="937c5-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="937c5-109">Ez a parancs információt ad eredményül a folyó egység kvótáról és használatáról a Nyugat-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="937c5-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="937c5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="937c5-110">PARAMETERS</span></span>

### <span data-ttu-id="937c5-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="937c5-111">-Location</span></span>
<span data-ttu-id="937c5-112">Itt adhatja meg egy Azure-terület vagy adatközpont-hely nevét, amelyhez adatfolyam-kvóta adatait szeretne beszerezni.</span><span class="sxs-lookup"><span data-stu-id="937c5-112">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="937c5-113">Lásd: https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services támogatott Azure-régiók listája.</span><span class="sxs-lookup"><span data-stu-id="937c5-113">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="937c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="937c5-114">-DefaultProfile</span></span>
<span data-ttu-id="937c5-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="937c5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="937c5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="937c5-116">CommonParameters</span></span>
<span data-ttu-id="937c5-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="937c5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="937c5-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="937c5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="937c5-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="937c5-119">INPUTS</span></span>

## <span data-ttu-id="937c5-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="937c5-120">OUTPUTS</span></span>

### <span data-ttu-id="937c5-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. StreamAnalytics. models. PSQuota, Microsoft. Azure. commands. StreamAnalytics]] Microsoft. Azure. Command. StreamAnalytics. models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="937c5-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="937c5-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="937c5-122">NOTES</span></span>

## <span data-ttu-id="937c5-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="937c5-123">RELATED LINKS</span></span>

[<span data-ttu-id="937c5-124">Azure stream Analytics-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="937c5-124">Azure Stream Analytics Cmdlets</span></span>](./AzureRM.StreamAnalytics.md)


