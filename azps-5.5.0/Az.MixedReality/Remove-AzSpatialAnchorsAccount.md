---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 5ba079a17dcfb0a263766237adbbec9beb4cc64c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203574"
---
# <span data-ttu-id="a37b5-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="a37b5-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="a37b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a37b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a37b5-103">Térbeli horgonyok fiók törlése</span><span class="sxs-lookup"><span data-stu-id="a37b5-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="a37b5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a37b5-104">SYNTAX</span></span>

### <span data-ttu-id="a37b5-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a37b5-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a37b5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a37b5-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a37b5-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="a37b5-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a37b5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a37b5-108">DESCRIPTION</span></span>
<span data-ttu-id="a37b5-109">Adott térbeli horgonyfiók törlése adott Előfizetés és Erőforrás csoportból.</span><span class="sxs-lookup"><span data-stu-id="a37b5-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="a37b5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a37b5-110">EXAMPLES</span></span>

### <span data-ttu-id="a37b5-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a37b5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="a37b5-112">Törölje a térbeli horgonyok fiók "példáját" az aktuális Előfizetés és Erőforráscsoport "rg1" csoportjából.</span><span class="sxs-lookup"><span data-stu-id="a37b5-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="a37b5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a37b5-113">PARAMETERS</span></span>

### <span data-ttu-id="a37b5-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a37b5-114">-Confirm</span></span>
<span data-ttu-id="a37b5-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a37b5-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a37b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a37b5-116">-DefaultProfile</span></span>
<span data-ttu-id="a37b5-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a37b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a37b5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a37b5-118">-InputObject</span></span>
<span data-ttu-id="a37b5-119">Az egyéni tartományobjektum.</span><span class="sxs-lookup"><span data-stu-id="a37b5-119">The custom domain object.</span></span>

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

### <span data-ttu-id="a37b5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a37b5-120">-Name</span></span>
<span data-ttu-id="a37b5-121">Térbeli horgonyok fiókneve.</span><span class="sxs-lookup"><span data-stu-id="a37b5-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="a37b5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a37b5-122">-PassThru</span></span>
<span data-ttu-id="a37b5-123">Visszatérési objektum, ha meg van adva.</span><span class="sxs-lookup"><span data-stu-id="a37b5-123">Return object if specified.</span></span>

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

### <span data-ttu-id="a37b5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a37b5-124">-ResourceGroupName</span></span>
<span data-ttu-id="a37b5-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a37b5-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a37b5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a37b5-126">-ResourceId</span></span>
<span data-ttu-id="a37b5-127">A térbeli horgonyok fiókja erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a37b5-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="a37b5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a37b5-128">-WhatIf</span></span>
<span data-ttu-id="a37b5-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a37b5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a37b5-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a37b5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a37b5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a37b5-131">CommonParameters</span></span>
<span data-ttu-id="a37b5-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a37b5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a37b5-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a37b5-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a37b5-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a37b5-134">INPUTS</span></span>

### <span data-ttu-id="a37b5-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a37b5-135">System.String</span></span>

### <span data-ttu-id="a37b5-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="a37b5-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="a37b5-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a37b5-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a37b5-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a37b5-138">OUTPUTS</span></span>

### <span data-ttu-id="a37b5-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a37b5-139">System.Boolean</span></span>

## <span data-ttu-id="a37b5-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a37b5-140">NOTES</span></span>

## <span data-ttu-id="a37b5-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a37b5-141">RELATED LINKS</span></span>
