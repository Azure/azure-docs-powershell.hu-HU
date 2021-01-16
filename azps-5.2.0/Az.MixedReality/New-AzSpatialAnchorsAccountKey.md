---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 35c00fca10223a22d586efba8961dd9cab6b0faf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344525"
---
# <span data-ttu-id="fa843-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="fa843-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="fa843-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa843-102">SYNOPSIS</span></span>
<span data-ttu-id="fa843-103">A térbeli horgonyok fiók kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="fa843-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="fa843-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fa843-104">SYNTAX</span></span>

### <span data-ttu-id="fa843-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa843-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa843-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa843-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa843-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa843-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa843-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa843-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa843-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa843-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa843-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa843-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa843-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fa843-111">DESCRIPTION</span></span>
<span data-ttu-id="fa843-112">A térbeli horgonyok fiókjának elsődleges vagy másodlagos kulcsát újragenerálja.</span><span class="sxs-lookup"><span data-stu-id="fa843-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="fa843-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fa843-113">EXAMPLES</span></span>

### <span data-ttu-id="fa843-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="fa843-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="fa843-115">A térbeli horgonyok másodlagos kulcsának "példa" újragenerálása az "rg1" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="fa843-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="fa843-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="fa843-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="fa843-117">A térbeli horgonyok másodlagos kulcsának "példáját" újragenerálja az aktuális Előfizetés és Erőforráscsoport "rg1" és pipával.</span><span class="sxs-lookup"><span data-stu-id="fa843-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="fa843-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa843-118">PARAMETERS</span></span>

### <span data-ttu-id="fa843-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa843-119">-DefaultProfile</span></span>
<span data-ttu-id="fa843-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa843-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa843-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fa843-121">-Force</span></span>
<span data-ttu-id="fa843-122">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="fa843-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa843-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa843-123">-InputObject</span></span>
<span data-ttu-id="fa843-124">Az egyéni tartományobjektum.</span><span class="sxs-lookup"><span data-stu-id="fa843-124">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa843-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fa843-125">-Name</span></span>
<span data-ttu-id="fa843-126">Térbeli horgonyok fiókneve.</span><span class="sxs-lookup"><span data-stu-id="fa843-126">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa843-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="fa843-127">-Primary</span></span>
<span data-ttu-id="fa843-128">A térbeli horgonyok fiókjának elsődleges kulcsát újragenerálja.</span><span class="sxs-lookup"><span data-stu-id="fa843-128">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa843-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa843-129">-ResourceGroupName</span></span>
<span data-ttu-id="fa843-130">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fa843-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa843-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa843-131">-ResourceId</span></span>
<span data-ttu-id="fa843-132">A térbeli horgonyok fiókja erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fa843-132">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa843-133">-Secondary</span><span class="sxs-lookup"><span data-stu-id="fa843-133">-Secondary</span></span>
<span data-ttu-id="fa843-134">A térbeli horgonyok fiókjának elsődleges kulcsát újragenerálja.</span><span class="sxs-lookup"><span data-stu-id="fa843-134">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa843-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa843-135">-Confirm</span></span>
<span data-ttu-id="fa843-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fa843-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa843-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa843-137">-WhatIf</span></span>
<span data-ttu-id="fa843-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fa843-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa843-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa843-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa843-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa843-140">CommonParameters</span></span>
<span data-ttu-id="fa843-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa843-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fa843-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa843-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa843-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa843-143">INPUTS</span></span>

### <span data-ttu-id="fa843-144">System.String</span><span class="sxs-lookup"><span data-stu-id="fa843-144">System.String</span></span>

### <span data-ttu-id="fa843-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="fa843-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="fa843-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa843-146">OUTPUTS</span></span>

### <span data-ttu-id="fa843-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fa843-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="fa843-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fa843-148">NOTES</span></span>

## <span data-ttu-id="fa843-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa843-149">RELATED LINKS</span></span>
