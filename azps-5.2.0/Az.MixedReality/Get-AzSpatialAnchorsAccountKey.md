---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 81bce36cb1b8cd4737141e58ad3e220199e726cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365607"
---
# <span data-ttu-id="7f742-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="7f742-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="7f742-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f742-102">SYNOPSIS</span></span>
<span data-ttu-id="7f742-103">A térbeli horgonyok fiókjának billentyűinek lekérte</span><span class="sxs-lookup"><span data-stu-id="7f742-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="7f742-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7f742-104">SYNTAX</span></span>

### <span data-ttu-id="7f742-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f742-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f742-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f742-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f742-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f742-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f742-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7f742-108">DESCRIPTION</span></span>
<span data-ttu-id="7f742-109">A Térbeli horgonyok fiók fejlesztői kulcsának lekérte.</span><span class="sxs-lookup"><span data-stu-id="7f742-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="7f742-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7f742-110">EXAMPLES</span></span>

### <span data-ttu-id="7f742-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7f742-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="7f742-112">A Térbeli horgonyok fiók "példa" fejlesztői kulcsait az aktuális Előfizetés és Erőforráscsoport "rg1" elemből szerezze be.</span><span class="sxs-lookup"><span data-stu-id="7f742-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="7f742-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7f742-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="7f742-114">A térbeli horgonyok fiók "példáját" a jelenlegi Előfizetés és Erőforráscsoport "rg1" fejlesztői kulcsával, pipázással.</span><span class="sxs-lookup"><span data-stu-id="7f742-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="7f742-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f742-115">PARAMETERS</span></span>

### <span data-ttu-id="7f742-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f742-116">-DefaultProfile</span></span>
<span data-ttu-id="7f742-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f742-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f742-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f742-118">-InputObject</span></span>
<span data-ttu-id="7f742-119">Az egyéni tartományobjektum.</span><span class="sxs-lookup"><span data-stu-id="7f742-119">The custom domain object.</span></span>

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

### <span data-ttu-id="7f742-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7f742-120">-Name</span></span>
<span data-ttu-id="7f742-121">Térbeli horgonyok fiókneve.</span><span class="sxs-lookup"><span data-stu-id="7f742-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="7f742-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f742-122">-ResourceGroupName</span></span>
<span data-ttu-id="7f742-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7f742-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="7f742-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f742-124">-ResourceId</span></span>
<span data-ttu-id="7f742-125">A térbeli horgonyok fiókja erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7f742-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="7f742-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f742-126">CommonParameters</span></span>
<span data-ttu-id="7f742-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f742-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7f742-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f742-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f742-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f742-129">INPUTS</span></span>

### <span data-ttu-id="7f742-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7f742-130">System.String</span></span>

### <span data-ttu-id="7f742-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="7f742-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="7f742-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f742-132">OUTPUTS</span></span>

### <span data-ttu-id="7f742-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7f742-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="7f742-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7f742-134">NOTES</span></span>

## <span data-ttu-id="7f742-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f742-135">RELATED LINKS</span></span>
