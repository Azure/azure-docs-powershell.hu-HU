---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2d164e08876b5489ec45ce146f4f3c7cee3ee6d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665884"
---
# <span data-ttu-id="43caa-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="43caa-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="43caa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43caa-102">SYNOPSIS</span></span>
<span data-ttu-id="43caa-103">Területi horgonyok fiók törlése</span><span class="sxs-lookup"><span data-stu-id="43caa-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="43caa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43caa-104">SYNTAX</span></span>

### <span data-ttu-id="43caa-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43caa-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43caa-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43caa-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43caa-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="43caa-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43caa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="43caa-108">DESCRIPTION</span></span>
<span data-ttu-id="43caa-109">Meghatározott térbeli horgonyok fiók törlése bizonyos előfizetésből és erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="43caa-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="43caa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="43caa-110">EXAMPLES</span></span>

### <span data-ttu-id="43caa-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="43caa-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="43caa-112">Területi horgonyok fiók törlése "példa" a jelenlegi előfizetés és erőforráscsoport "rg1".</span><span class="sxs-lookup"><span data-stu-id="43caa-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="43caa-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43caa-113">PARAMETERS</span></span>

### <span data-ttu-id="43caa-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43caa-114">-Confirm</span></span>
<span data-ttu-id="43caa-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43caa-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43caa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43caa-116">-DefaultProfile</span></span>
<span data-ttu-id="43caa-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43caa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43caa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43caa-118">-InputObject</span></span>
<span data-ttu-id="43caa-119">Az egyéni tartomány-objektum.</span><span class="sxs-lookup"><span data-stu-id="43caa-119">The custom domain object.</span></span>

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

### <span data-ttu-id="43caa-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43caa-120">-Name</span></span>
<span data-ttu-id="43caa-121">Térbeli horgonyok fiók neve.</span><span class="sxs-lookup"><span data-stu-id="43caa-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="43caa-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43caa-122">-PassThru</span></span>
<span data-ttu-id="43caa-123">Ha meg van adva a visszatérési objektum</span><span class="sxs-lookup"><span data-stu-id="43caa-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43caa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43caa-124">-ResourceGroupName</span></span>
<span data-ttu-id="43caa-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="43caa-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="43caa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43caa-126">-ResourceId</span></span>
<span data-ttu-id="43caa-127">A térbeli horgonyok fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="43caa-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="43caa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43caa-128">-WhatIf</span></span>
<span data-ttu-id="43caa-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43caa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43caa-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43caa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43caa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43caa-131">CommonParameters</span></span>
<span data-ttu-id="43caa-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43caa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="43caa-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43caa-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43caa-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43caa-134">INPUTS</span></span>

### <span data-ttu-id="43caa-135">System. String</span><span class="sxs-lookup"><span data-stu-id="43caa-135">System.String</span></span>

### <span data-ttu-id="43caa-136">Microsoft. Azure. Command. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="43caa-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="43caa-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="43caa-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="43caa-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43caa-138">OUTPUTS</span></span>

### <span data-ttu-id="43caa-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43caa-139">System.Boolean</span></span>

## <span data-ttu-id="43caa-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43caa-140">NOTES</span></span>

## <span data-ttu-id="43caa-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43caa-141">RELATED LINKS</span></span>
