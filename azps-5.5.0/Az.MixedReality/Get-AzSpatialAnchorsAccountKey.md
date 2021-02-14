---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 81bce36cb1b8cd4737141e58ad3e220199e726cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161306"
---
# <span data-ttu-id="c183e-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="c183e-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="c183e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c183e-102">SYNOPSIS</span></span>
<span data-ttu-id="c183e-103">A térbeli horgonyok fiókjának billentyűinek lekérte</span><span class="sxs-lookup"><span data-stu-id="c183e-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="c183e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c183e-104">SYNTAX</span></span>

### <span data-ttu-id="c183e-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c183e-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c183e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c183e-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c183e-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="c183e-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c183e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c183e-108">DESCRIPTION</span></span>
<span data-ttu-id="c183e-109">Get developer keys of Spatial Anchors Account.</span><span class="sxs-lookup"><span data-stu-id="c183e-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="c183e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c183e-110">EXAMPLES</span></span>

### <span data-ttu-id="c183e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c183e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="c183e-112">A Térbeli horgonyok fiók "példa" fejlesztői kulcsait az aktuális Előfizetés és Erőforráscsoport "rg1" elemből szerezze be.</span><span class="sxs-lookup"><span data-stu-id="c183e-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="c183e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c183e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="c183e-114">A térbeli horgonyok fiók "példáját" a jelenlegi Előfizetés és Erőforráscsoport "rg1" fejlesztői kulcsával, pipázással.</span><span class="sxs-lookup"><span data-stu-id="c183e-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="c183e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c183e-115">PARAMETERS</span></span>

### <span data-ttu-id="c183e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c183e-116">-DefaultProfile</span></span>
<span data-ttu-id="c183e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c183e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c183e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c183e-118">-InputObject</span></span>
<span data-ttu-id="c183e-119">Az egyéni tartományobjektum.</span><span class="sxs-lookup"><span data-stu-id="c183e-119">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c183e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c183e-120">-Name</span></span>
<span data-ttu-id="c183e-121">Térbeli horgonyok fiókneve.</span><span class="sxs-lookup"><span data-stu-id="c183e-121">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c183e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c183e-122">-ResourceGroupName</span></span>
<span data-ttu-id="c183e-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c183e-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c183e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c183e-124">-ResourceId</span></span>
<span data-ttu-id="c183e-125">A térbeli horgonyok fiókja erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c183e-125">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c183e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c183e-126">CommonParameters</span></span>
<span data-ttu-id="c183e-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c183e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c183e-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c183e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c183e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c183e-129">INPUTS</span></span>

### <span data-ttu-id="c183e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c183e-130">System.String</span></span>

### <span data-ttu-id="c183e-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="c183e-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="c183e-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c183e-132">OUTPUTS</span></span>

### <span data-ttu-id="c183e-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c183e-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="c183e-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c183e-134">NOTES</span></span>

## <span data-ttu-id="c183e-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c183e-135">RELATED LINKS</span></span>
