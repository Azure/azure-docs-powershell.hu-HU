---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: e1bacc62ca7efc3bd453be93196e83b0b6d67853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500255"
---
# <span data-ttu-id="4ef47-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="4ef47-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="4ef47-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ef47-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef47-103">Megkapja az elérhető SKU-t egy fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="4ef47-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ef47-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ef47-104">SYNTAX</span></span>

### <span data-ttu-id="4ef47-105">GetSkusWithAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ef47-105">GetSkusWithAccount (Default)</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ef47-106">GetSkusWithFilter</span><span class="sxs-lookup"><span data-stu-id="4ef47-106">GetSkusWithFilter</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ef47-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ef47-107">DESCRIPTION</span></span>
<span data-ttu-id="4ef47-108">A **Get-AzureRmCognitiveServicesAccountSkus** parancsmag a kognitív Services-fiókhoz elérhető SKU-ket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4ef47-108">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="4ef47-109">Az SKU a fiók Tier Plane.</span><span class="sxs-lookup"><span data-stu-id="4ef47-109">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="4ef47-110">Meghatározza a fiók árát, a hívás korlátját és a díjalapot.</span><span class="sxs-lookup"><span data-stu-id="4ef47-110">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="4ef47-111">A F0 SKU egy ingyenes Tier.</span><span class="sxs-lookup"><span data-stu-id="4ef47-111">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="4ef47-112">A kifizetett szintek közé tartozik a S0, az S1, az S2 stb.</span><span class="sxs-lookup"><span data-stu-id="4ef47-112">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="4ef47-113">Példák</span><span class="sxs-lookup"><span data-stu-id="4ef47-113">EXAMPLES</span></span>

### <span data-ttu-id="4ef47-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4ef47-114">Example 1</span></span>
```powershell
PS C:\> (Get-AzureRmCognitiveServicesAccountSkus -ResourceGroupName cognitive-services-resource-group -Name myluis).Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="4ef47-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ef47-115">PARAMETERS</span></span>

### <span data-ttu-id="4ef47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef47-116">-DefaultProfile</span></span>
<span data-ttu-id="4ef47-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4ef47-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ef47-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="4ef47-118">-Location</span></span>
<span data-ttu-id="4ef47-119">A kognitív szolgáltatások fiók helye.</span><span class="sxs-lookup"><span data-stu-id="4ef47-119">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef47-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ef47-120">-Name</span></span>
<span data-ttu-id="4ef47-121">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ef47-121">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef47-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ef47-122">-ResourceGroupName</span></span>
<span data-ttu-id="4ef47-123">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="4ef47-123">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef47-124">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="4ef47-124">-Type</span></span>
<span data-ttu-id="4ef47-125">A kognitív szolgáltatások fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="4ef47-125">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef47-126">CommonParameters</span></span>
<span data-ttu-id="4ef47-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ef47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef47-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ef47-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef47-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ef47-129">INPUTS</span></span>

### <span data-ttu-id="4ef47-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4ef47-130">System.String</span></span>

## <span data-ttu-id="4ef47-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ef47-131">OUTPUTS</span></span>

### <span data-ttu-id="4ef47-132">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="4ef47-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="4ef47-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ef47-133">NOTES</span></span>

## <span data-ttu-id="4ef47-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ef47-134">RELATED LINKS</span></span>
