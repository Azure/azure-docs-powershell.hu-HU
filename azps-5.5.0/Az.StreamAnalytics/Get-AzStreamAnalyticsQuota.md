---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: abce6b39b0dfa77ed4aa815ed9551b3ebff427ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150235"
---
# <span data-ttu-id="ad5d5-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="ad5d5-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="ad5d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad5d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ad5d5-103">Információkat kap a streamelési egység egy régióra vonatkozó kvótáról.</span><span class="sxs-lookup"><span data-stu-id="ad5d5-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="ad5d5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ad5d5-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad5d5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ad5d5-105">DESCRIPTION</span></span>
<span data-ttu-id="ad5d5-106">A **Get-AzStreamAnalyticsQuota** parancsmag információkat kap a streamelési egység egy régióra vonatkozó kvótáról.</span><span class="sxs-lookup"><span data-stu-id="ad5d5-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="ad5d5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ad5d5-107">EXAMPLES</span></span>

### <span data-ttu-id="ad5d5-108">1. PÉLDA: Információ a streamelési egység kvótáról egy régióhoz</span><span class="sxs-lookup"><span data-stu-id="ad5d5-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="ad5d5-109">Ez a parancs információkat ad vissza a streamelési egység kvótáról és használatról az Egyesült Államok nyugati régiójában.</span><span class="sxs-lookup"><span data-stu-id="ad5d5-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="ad5d5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad5d5-110">PARAMETERS</span></span>

### <span data-ttu-id="ad5d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad5d5-111">-DefaultProfile</span></span>
<span data-ttu-id="ad5d5-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad5d5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad5d5-113">-Location</span><span class="sxs-lookup"><span data-stu-id="ad5d5-113">-Location</span></span>
<span data-ttu-id="ad5d5-114">Annak az Azure-régiónak vagy adatközpontnak a nevét adja meg, amelynek a streamelési egység kvóta-információit le kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="ad5d5-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="ad5d5-115">A http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services támogatott Azure-régiók listáját itt láthatja.</span><span class="sxs-lookup"><span data-stu-id="ad5d5-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="ad5d5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad5d5-116">CommonParameters</span></span>
<span data-ttu-id="ad5d5-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad5d5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad5d5-118">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad5d5-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad5d5-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad5d5-119">INPUTS</span></span>

### <span data-ttu-id="ad5d5-120">System.String</span><span class="sxs-lookup"><span data-stu-id="ad5d5-120">System.String</span></span>

## <span data-ttu-id="ad5d5-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad5d5-121">OUTPUTS</span></span>

### <span data-ttu-id="ad5d5-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span><span class="sxs-lookup"><span data-stu-id="ad5d5-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="ad5d5-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ad5d5-123">NOTES</span></span>

## <span data-ttu-id="ad5d5-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad5d5-124">RELATED LINKS</span></span>

[<span data-ttu-id="ad5d5-125">Azure Stream Analytics-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ad5d5-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


