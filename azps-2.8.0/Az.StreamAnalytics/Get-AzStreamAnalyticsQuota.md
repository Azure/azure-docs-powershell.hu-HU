---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: dd36a1dcf5b23c26f0936b3adb0f692335c03c48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838705"
---
# <span data-ttu-id="5e72b-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="5e72b-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="5e72b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e72b-102">SYNOPSIS</span></span>
<span data-ttu-id="5e72b-103">Információt kap egy régió streaming Unit kvótáról.</span><span class="sxs-lookup"><span data-stu-id="5e72b-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="5e72b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e72b-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e72b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e72b-105">DESCRIPTION</span></span>
<span data-ttu-id="5e72b-106">A **Get-AzStreamAnalyticsQuota** parancsmag információkat kap egy adott terület adatfolyam-kvótáról.</span><span class="sxs-lookup"><span data-stu-id="5e72b-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="5e72b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5e72b-107">EXAMPLES</span></span>

### <span data-ttu-id="5e72b-108">1. példa: információk beszerzése egy régió streaming Unit kvótáról</span><span class="sxs-lookup"><span data-stu-id="5e72b-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="5e72b-109">Ez a parancs információt ad eredményül a folyó egység kvótáról és használatáról a Nyugat-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="5e72b-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="5e72b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e72b-110">PARAMETERS</span></span>

### <span data-ttu-id="5e72b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e72b-111">-DefaultProfile</span></span>
<span data-ttu-id="5e72b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e72b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e72b-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="5e72b-113">-Location</span></span>
<span data-ttu-id="5e72b-114">Itt adhatja meg egy Azure-terület vagy adatközpont-hely nevét, amelyhez adatfolyam-kvóta adatait szeretne beszerezni.</span><span class="sxs-lookup"><span data-stu-id="5e72b-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="5e72b-115">Lásd: https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services támogatott Azure-régiók listája.</span><span class="sxs-lookup"><span data-stu-id="5e72b-115">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="5e72b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e72b-116">CommonParameters</span></span>
<span data-ttu-id="5e72b-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e72b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e72b-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e72b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e72b-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e72b-119">INPUTS</span></span>

### <span data-ttu-id="5e72b-120">System. String</span><span class="sxs-lookup"><span data-stu-id="5e72b-120">System.String</span></span>

## <span data-ttu-id="5e72b-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e72b-121">OUTPUTS</span></span>

### <span data-ttu-id="5e72b-122">Microsoft. Azure. Command. StreamAnalytics. models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="5e72b-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="5e72b-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e72b-123">NOTES</span></span>

## <span data-ttu-id="5e72b-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e72b-124">RELATED LINKS</span></span>

[<span data-ttu-id="5e72b-125">Azure stream Analytics-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="5e72b-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


