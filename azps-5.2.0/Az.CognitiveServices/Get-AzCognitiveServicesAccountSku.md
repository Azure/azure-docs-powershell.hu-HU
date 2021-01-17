---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: 3c632e6ffbf26e3aaacb725e9b663ffafbc49ec2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369191"
---
# <span data-ttu-id="77748-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="77748-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="77748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77748-102">SYNOPSIS</span></span>
<span data-ttu-id="77748-103">Egy fiókhoz elérhető SKUs-okat kap.</span><span class="sxs-lookup"><span data-stu-id="77748-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="77748-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="77748-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77748-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="77748-105">DESCRIPTION</span></span>
<span data-ttu-id="77748-106">A **Get-AzCognitiveServicesAccountSku** parancsmag a kognitív szolgáltatásokhoz elérhető termékváltozatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="77748-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="77748-107">Az SKU egy fiók tier csomagja.</span><span class="sxs-lookup"><span data-stu-id="77748-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="77748-108">Meghatározza a fiók árát, híváskorlátját és díját.</span><span class="sxs-lookup"><span data-stu-id="77748-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="77748-109">Az F0 termékváltozat egy ingyenes szint.</span><span class="sxs-lookup"><span data-stu-id="77748-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="77748-110">A fizetős szintek közé tartozik az S0, S1, S2 stb.</span><span class="sxs-lookup"><span data-stu-id="77748-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="77748-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="77748-111">EXAMPLES</span></span>

### <span data-ttu-id="77748-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="77748-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="77748-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77748-113">PARAMETERS</span></span>

### <span data-ttu-id="77748-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77748-114">-DefaultProfile</span></span>
<span data-ttu-id="77748-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="77748-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77748-116">-Location</span><span class="sxs-lookup"><span data-stu-id="77748-116">-Location</span></span>
<span data-ttu-id="77748-117">Kognitív szolgáltatások fiókjának helye.</span><span class="sxs-lookup"><span data-stu-id="77748-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="77748-118">-Type</span><span class="sxs-lookup"><span data-stu-id="77748-118">-Type</span></span>
<span data-ttu-id="77748-119">Kognitív szolgáltatások fióktípusa.</span><span class="sxs-lookup"><span data-stu-id="77748-119">Cognitive Services Account Type.</span></span>

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

### <span data-ttu-id="77748-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77748-120">CommonParameters</span></span>
<span data-ttu-id="77748-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77748-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77748-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77748-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77748-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77748-123">INPUTS</span></span>

### <span data-ttu-id="77748-124">System.String</span><span class="sxs-lookup"><span data-stu-id="77748-124">System.String</span></span>

## <span data-ttu-id="77748-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77748-125">OUTPUTS</span></span>

### <span data-ttu-id="77748-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span><span class="sxs-lookup"><span data-stu-id="77748-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="77748-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="77748-127">NOTES</span></span>

## <span data-ttu-id="77748-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77748-128">RELATED LINKS</span></span>
