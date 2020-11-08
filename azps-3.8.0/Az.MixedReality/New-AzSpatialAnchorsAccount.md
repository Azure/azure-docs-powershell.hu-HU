---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2e4379007b296467bf86adff7c46f654eee671e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014515"
---
# <span data-ttu-id="fc087-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="fc087-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="fc087-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc087-102">SYNOPSIS</span></span>
<span data-ttu-id="fc087-103">Területi horgonyokat létrehozó fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="fc087-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="fc087-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc087-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc087-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc087-105">DESCRIPTION</span></span>
<span data-ttu-id="fc087-106">Új területi hírszerző fiók létrehozása bizonyos előfizetésekben, erőforrás-csoportokban és-régiókban.</span><span class="sxs-lookup"><span data-stu-id="fc087-106">Create a new Spatial Intelligence Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="fc087-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fc087-107">EXAMPLES</span></span>

### <span data-ttu-id="fc087-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fc087-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSpatialAnchorsAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="fc087-109">Új területi horgonyokat tartalmazó fiók létrehozása "példa" a jelenlegi előfizetésben, erőforráscsoport "rg1" és Közép-amerikai.</span><span class="sxs-lookup"><span data-stu-id="fc087-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="fc087-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc087-110">PARAMETERS</span></span>

### <span data-ttu-id="fc087-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fc087-111">-Confirm</span></span>
<span data-ttu-id="fc087-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fc087-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc087-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc087-113">-DefaultProfile</span></span>
<span data-ttu-id="fc087-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc087-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc087-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="fc087-115">-Location</span></span>
<span data-ttu-id="fc087-116">Területi horgonyok fiók helye.</span><span class="sxs-lookup"><span data-stu-id="fc087-116">Spatial Anchors Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc087-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc087-117">-Name</span></span>
<span data-ttu-id="fc087-118">Térbeli horgonyok fiók neve.</span><span class="sxs-lookup"><span data-stu-id="fc087-118">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc087-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc087-119">-ResourceGroupName</span></span>
<span data-ttu-id="fc087-120">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="fc087-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc087-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc087-121">-WhatIf</span></span>
<span data-ttu-id="fc087-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fc087-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc087-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc087-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc087-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc087-124">CommonParameters</span></span>
<span data-ttu-id="fc087-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc087-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fc087-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc087-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc087-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc087-127">INPUTS</span></span>

### <span data-ttu-id="fc087-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="fc087-128">None</span></span>

## <span data-ttu-id="fc087-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc087-129">OUTPUTS</span></span>

### <span data-ttu-id="fc087-130">Microsoft. Azure. Command. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="fc087-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="fc087-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc087-131">NOTES</span></span>

## <span data-ttu-id="fc087-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc087-132">RELATED LINKS</span></span>
