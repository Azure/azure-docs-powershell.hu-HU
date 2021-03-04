---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: eb9865d69d51fffc7488379bada256a812503a24
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933226"
---
# <span data-ttu-id="c68e0-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="c68e0-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="c68e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c68e0-102">SYNOPSIS</span></span>
<span data-ttu-id="c68e0-103">Egy fiókhoz elérhető SKUs-okat kap.</span><span class="sxs-lookup"><span data-stu-id="c68e0-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="c68e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c68e0-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c68e0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c68e0-105">DESCRIPTION</span></span>
<span data-ttu-id="c68e0-106">A **Get-AzCognitiveServicesAccountSku** parancsmag a kognitív szolgáltatásokhoz elérhető termékváltozatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="c68e0-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="c68e0-107">Az SKU egy fiók tier csomagja.</span><span class="sxs-lookup"><span data-stu-id="c68e0-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="c68e0-108">Meghatározza a fiók árát, híváskorlátját és díját.</span><span class="sxs-lookup"><span data-stu-id="c68e0-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="c68e0-109">Az F0 termékváltozat egy ingyenes szint.</span><span class="sxs-lookup"><span data-stu-id="c68e0-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="c68e0-110">A fizetős szintek közé tartozik az S0, S1, S2 stb.</span><span class="sxs-lookup"><span data-stu-id="c68e0-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="c68e0-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c68e0-111">EXAMPLES</span></span>

### <span data-ttu-id="c68e0-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="c68e0-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="c68e0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c68e0-113">PARAMETERS</span></span>

### <span data-ttu-id="c68e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c68e0-114">-DefaultProfile</span></span>
<span data-ttu-id="c68e0-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c68e0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c68e0-116">-Location</span><span class="sxs-lookup"><span data-stu-id="c68e0-116">-Location</span></span>
<span data-ttu-id="c68e0-117">Kognitív szolgáltatások fiókjának helye.</span><span class="sxs-lookup"><span data-stu-id="c68e0-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="c68e0-118">-Type</span><span class="sxs-lookup"><span data-stu-id="c68e0-118">-Type</span></span>
<span data-ttu-id="c68e0-119">Kognitív szolgáltatások fióktípusa.</span><span class="sxs-lookup"><span data-stu-id="c68e0-119">Cognitive Services Account Type.</span></span>

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

### <span data-ttu-id="c68e0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68e0-120">CommonParameters</span></span>
<span data-ttu-id="c68e0-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c68e0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c68e0-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c68e0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68e0-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c68e0-123">INPUTS</span></span>

### <span data-ttu-id="c68e0-124">System.String</span><span class="sxs-lookup"><span data-stu-id="c68e0-124">System.String</span></span>

## <span data-ttu-id="c68e0-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c68e0-125">OUTPUTS</span></span>

### <span data-ttu-id="c68e0-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span><span class="sxs-lookup"><span data-stu-id="c68e0-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="c68e0-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c68e0-127">NOTES</span></span>

## <span data-ttu-id="c68e0-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c68e0-128">RELATED LINKS</span></span>
