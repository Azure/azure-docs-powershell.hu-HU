---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: a2a6dafe9aedfc41200e12bb3c583ad1b5fb02b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927874"
---
# <span data-ttu-id="53808-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="53808-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="53808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53808-102">SYNOPSIS</span></span>
<span data-ttu-id="53808-103">Create Spatial Anchors Account</span><span class="sxs-lookup"><span data-stu-id="53808-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="53808-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53808-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53808-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53808-105">DESCRIPTION</span></span>
<span data-ttu-id="53808-106">Hozzon létre egy új térbeli horgonyfiókot bizonyos Előfizetés, Erőforráscsoport és Régió területen.</span><span class="sxs-lookup"><span data-stu-id="53808-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="53808-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53808-107">EXAMPLES</span></span>

### <span data-ttu-id="53808-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="53808-108">Example 1</span></span>
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

<span data-ttu-id="53808-109">Hozzon létre egy új térbeli horgonyfiókot "példa" az aktuális Előfizetésben, az Erőforráscsoport "rg1" és a Közép-US verzióban.</span><span class="sxs-lookup"><span data-stu-id="53808-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="53808-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53808-110">PARAMETERS</span></span>

### <span data-ttu-id="53808-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53808-111">-Confirm</span></span>
<span data-ttu-id="53808-112">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="53808-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53808-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53808-113">-DefaultProfile</span></span>
<span data-ttu-id="53808-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53808-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53808-115">-Location</span><span class="sxs-lookup"><span data-stu-id="53808-115">-Location</span></span>
<span data-ttu-id="53808-116">Térbeli horgonyok fiók helye.</span><span class="sxs-lookup"><span data-stu-id="53808-116">Spatial Anchors Account Location.</span></span>

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

### <span data-ttu-id="53808-117">-Name</span><span class="sxs-lookup"><span data-stu-id="53808-117">-Name</span></span>
<span data-ttu-id="53808-118">Térbeli horgonyok fiókneve.</span><span class="sxs-lookup"><span data-stu-id="53808-118">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="53808-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53808-119">-ResourceGroupName</span></span>
<span data-ttu-id="53808-120">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="53808-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="53808-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53808-121">-WhatIf</span></span>
<span data-ttu-id="53808-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="53808-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53808-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53808-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53808-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53808-124">CommonParameters</span></span>
<span data-ttu-id="53808-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53808-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="53808-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53808-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53808-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53808-127">INPUTS</span></span>

### <span data-ttu-id="53808-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="53808-128">None</span></span>

## <span data-ttu-id="53808-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53808-129">OUTPUTS</span></span>

### <span data-ttu-id="53808-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="53808-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="53808-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53808-131">NOTES</span></span>

## <span data-ttu-id="53808-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53808-132">RELATED LINKS</span></span>
