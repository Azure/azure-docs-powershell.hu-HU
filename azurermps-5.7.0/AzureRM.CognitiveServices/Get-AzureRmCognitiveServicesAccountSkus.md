---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: ed243f822817c223576fd3bbe0293a8cf18d7a51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493215"
---
# <span data-ttu-id="1e5d1-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="1e5d1-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="1e5d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e5d1-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5d1-103">Megkapja az elérhető SKU-t egy fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="1e5d1-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e5d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e5d1-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e5d1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e5d1-105">DESCRIPTION</span></span>
<span data-ttu-id="1e5d1-106">A **Get-AzureRmCognitiveServicesAccountSkus** parancsmag a kognitív Services-fiókhoz elérhető SKU-ket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1e5d1-106">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>

<span data-ttu-id="1e5d1-107">Az SKU a fiók Tier Plane.</span><span class="sxs-lookup"><span data-stu-id="1e5d1-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="1e5d1-108">Meghatározza a fiók árát, a hívás korlátját és a díjalapot.</span><span class="sxs-lookup"><span data-stu-id="1e5d1-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="1e5d1-109">A F0 SKU egy ingyenes Tier.</span><span class="sxs-lookup"><span data-stu-id="1e5d1-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="1e5d1-110">A kifizetett szintek közé tartozik a S0, az S1, az S2 stb.</span><span class="sxs-lookup"><span data-stu-id="1e5d1-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="1e5d1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1e5d1-111">EXAMPLES</span></span>

## <span data-ttu-id="1e5d1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e5d1-112">PARAMETERS</span></span>

### <span data-ttu-id="1e5d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e5d1-113">-DefaultProfile</span></span>
<span data-ttu-id="1e5d1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1e5d1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5d1-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e5d1-115">-Name</span></span>
<span data-ttu-id="1e5d1-116">A fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e5d1-116">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e5d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="1e5d1-118">Annak az erőforráscsoportnek a neve, amelyhez a fiók hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="1e5d1-118">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5d1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5d1-119">CommonParameters</span></span>
<span data-ttu-id="1e5d1-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e5d1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5d1-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e5d1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5d1-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e5d1-122">INPUTS</span></span>

### <span data-ttu-id="1e5d1-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="1e5d1-123">None</span></span>
<span data-ttu-id="1e5d1-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1e5d1-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1e5d1-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e5d1-125">OUTPUTS</span></span>

### <span data-ttu-id="1e5d1-126">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="1e5d1-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="1e5d1-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e5d1-127">NOTES</span></span>

## <span data-ttu-id="1e5d1-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e5d1-128">RELATED LINKS</span></span>

