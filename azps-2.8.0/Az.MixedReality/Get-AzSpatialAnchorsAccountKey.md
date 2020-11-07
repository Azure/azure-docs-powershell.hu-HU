---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: ec84b4def7b1dfd19b2c85c71dc6562fa4cae763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665888"
---
# <span data-ttu-id="4729b-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="4729b-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="4729b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4729b-102">SYNOPSIS</span></span>
<span data-ttu-id="4729b-103">A térbeli horgonyok fiók kulcsának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4729b-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="4729b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4729b-104">SYNTAX</span></span>

### <span data-ttu-id="4729b-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4729b-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4729b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4729b-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4729b-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="4729b-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4729b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4729b-108">DESCRIPTION</span></span>
<span data-ttu-id="4729b-109">A térbeli horgonyok fiók fejlesztői kulcsainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="4729b-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="4729b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4729b-110">EXAMPLES</span></span>

### <span data-ttu-id="4729b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4729b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="4729b-112">A "rg1" a jelenlegi előfizetésből és Erőforráscsoportből származó területi horgonyok fiók fejlesztői kulcsainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="4729b-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="4729b-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="4729b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="4729b-114">A "rg1" és a "" "az aktuális előfizetésből és az erőforráscsoport" (például a "") fejlesztői kulcsai</span><span class="sxs-lookup"><span data-stu-id="4729b-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="4729b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4729b-115">PARAMETERS</span></span>

### <span data-ttu-id="4729b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4729b-116">-DefaultProfile</span></span>
<span data-ttu-id="4729b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4729b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4729b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4729b-118">-InputObject</span></span>
<span data-ttu-id="4729b-119">Az egyéni tartomány-objektum.</span><span class="sxs-lookup"><span data-stu-id="4729b-119">The custom domain object.</span></span>

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

### <span data-ttu-id="4729b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4729b-120">-Name</span></span>
<span data-ttu-id="4729b-121">Térbeli horgonyok fiók neve.</span><span class="sxs-lookup"><span data-stu-id="4729b-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="4729b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4729b-122">-ResourceGroupName</span></span>
<span data-ttu-id="4729b-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="4729b-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="4729b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4729b-124">-ResourceId</span></span>
<span data-ttu-id="4729b-125">A térbeli horgonyok fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4729b-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="4729b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4729b-126">CommonParameters</span></span>
<span data-ttu-id="4729b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4729b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4729b-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4729b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4729b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4729b-129">INPUTS</span></span>

### <span data-ttu-id="4729b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4729b-130">System.String</span></span>

### <span data-ttu-id="4729b-131">Microsoft. Azure. Command. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="4729b-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="4729b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4729b-132">OUTPUTS</span></span>

### <span data-ttu-id="4729b-133">Microsoft. Azure. Command. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4729b-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="4729b-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4729b-134">NOTES</span></span>

## <span data-ttu-id="4729b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4729b-135">RELATED LINKS</span></span>
