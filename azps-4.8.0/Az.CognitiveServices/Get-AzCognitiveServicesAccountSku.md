---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: 3c632e6ffbf26e3aaacb725e9b663ffafbc49ec2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181765"
---
# <span data-ttu-id="047cf-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="047cf-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="047cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="047cf-102">SYNOPSIS</span></span>
<span data-ttu-id="047cf-103">Megkapja az elérhető SKU-t egy fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="047cf-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="047cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="047cf-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="047cf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="047cf-105">DESCRIPTION</span></span>
<span data-ttu-id="047cf-106">A **Get-AzCognitiveServicesAccountSku** parancsmag a kognitív Services-fiókhoz elérhető SKU-ket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="047cf-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="047cf-107">Az SKU a fiók Tier Plane.</span><span class="sxs-lookup"><span data-stu-id="047cf-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="047cf-108">Meghatározza a fiók árát, a hívás korlátját és a díjalapot.</span><span class="sxs-lookup"><span data-stu-id="047cf-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="047cf-109">A F0 SKU egy ingyenes Tier.</span><span class="sxs-lookup"><span data-stu-id="047cf-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="047cf-110">A kifizetett szintek közé tartozik a S0, az S1, az S2 stb.</span><span class="sxs-lookup"><span data-stu-id="047cf-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="047cf-111">Példák</span><span class="sxs-lookup"><span data-stu-id="047cf-111">EXAMPLES</span></span>

### <span data-ttu-id="047cf-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="047cf-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="047cf-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="047cf-113">PARAMETERS</span></span>

### <span data-ttu-id="047cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="047cf-114">-DefaultProfile</span></span>
<span data-ttu-id="047cf-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="047cf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="047cf-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="047cf-116">-Location</span></span>
<span data-ttu-id="047cf-117">A kognitív szolgáltatások fiók helye.</span><span class="sxs-lookup"><span data-stu-id="047cf-117">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047cf-118">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="047cf-118">-Type</span></span>
<span data-ttu-id="047cf-119">A kognitív szolgáltatások fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="047cf-119">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047cf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="047cf-120">CommonParameters</span></span>
<span data-ttu-id="047cf-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="047cf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="047cf-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="047cf-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="047cf-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="047cf-123">INPUTS</span></span>

### <span data-ttu-id="047cf-124">System. String</span><span class="sxs-lookup"><span data-stu-id="047cf-124">System.String</span></span>

## <span data-ttu-id="047cf-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="047cf-125">OUTPUTS</span></span>

### <span data-ttu-id="047cf-126">Microsoft. Azure. Management. CognitiveServices. models. ResourceSku</span><span class="sxs-lookup"><span data-stu-id="047cf-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="047cf-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="047cf-127">NOTES</span></span>

## <span data-ttu-id="047cf-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="047cf-128">RELATED LINKS</span></span>
