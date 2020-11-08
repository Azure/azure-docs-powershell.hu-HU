---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: abce6b39b0dfa77ed4aa815ed9551b3ebff427ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195020"
---
# <span data-ttu-id="eb5e8-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="eb5e8-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="eb5e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="eb5e8-103">Információt kap egy régió streaming Unit kvótáról.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="eb5e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb5e8-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb5e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb5e8-105">DESCRIPTION</span></span>
<span data-ttu-id="eb5e8-106">A **Get-AzStreamAnalyticsQuota** parancsmag információkat kap egy adott terület adatfolyam-kvótáról.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="eb5e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eb5e8-107">EXAMPLES</span></span>

### <span data-ttu-id="eb5e8-108">1. példa: információk beszerzése egy régió streaming Unit kvótáról</span><span class="sxs-lookup"><span data-stu-id="eb5e8-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="eb5e8-109">Ez a parancs információt ad eredményül a folyó egység kvótáról és használatáról a Nyugat-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="eb5e8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb5e8-110">PARAMETERS</span></span>

### <span data-ttu-id="eb5e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb5e8-111">-DefaultProfile</span></span>
<span data-ttu-id="eb5e8-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb5e8-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="eb5e8-113">-Location</span></span>
<span data-ttu-id="eb5e8-114">Itt adhatja meg egy Azure-terület vagy adatközpont-hely nevét, amelyhez adatfolyam-kvóta adatait szeretne beszerezni.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="eb5e8-115">Lásd: http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services támogatott Azure-régiók listája.</span><span class="sxs-lookup"><span data-stu-id="eb5e8-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="eb5e8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb5e8-116">CommonParameters</span></span>
<span data-ttu-id="eb5e8-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb5e8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb5e8-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb5e8-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb5e8-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb5e8-119">INPUTS</span></span>

### <span data-ttu-id="eb5e8-120">System. String</span><span class="sxs-lookup"><span data-stu-id="eb5e8-120">System.String</span></span>

## <span data-ttu-id="eb5e8-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb5e8-121">OUTPUTS</span></span>

### <span data-ttu-id="eb5e8-122">Microsoft. Azure. Command. StreamAnalytics. models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="eb5e8-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="eb5e8-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb5e8-123">NOTES</span></span>

## <span data-ttu-id="eb5e8-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb5e8-124">RELATED LINKS</span></span>

[<span data-ttu-id="eb5e8-125">Azure stream Analytics-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="eb5e8-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


