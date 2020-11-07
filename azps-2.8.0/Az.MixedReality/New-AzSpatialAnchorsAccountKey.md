---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 19af1cf3ae051500a6515340b96792efa8dbbc17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665885"
---
# <span data-ttu-id="15443-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="15443-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="15443-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15443-102">SYNOPSIS</span></span>
<span data-ttu-id="15443-103">A térbeli horgonyok fiók kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="15443-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="15443-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15443-104">SYNTAX</span></span>

### <span data-ttu-id="15443-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="15443-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15443-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="15443-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15443-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="15443-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15443-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="15443-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15443-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="15443-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15443-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="15443-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15443-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="15443-111">DESCRIPTION</span></span>
<span data-ttu-id="15443-112">A térbeli horgonyok fiók elsődleges kulcsának vagy másodlagos kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="15443-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="15443-113">Példák</span><span class="sxs-lookup"><span data-stu-id="15443-113">EXAMPLES</span></span>

### <span data-ttu-id="15443-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="15443-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="15443-115">Regenerálódni a térbeli horgonyok fiók másodlagos kulcsát "példa" a "rg1" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="15443-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="15443-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="15443-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="15443-117">A "rg1" és a "" típusú "a térbeli horgonyok" fiók másodlagos kulcsának újragenerálására szolgáló "példa" a csővezetékekkel.</span><span class="sxs-lookup"><span data-stu-id="15443-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="15443-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15443-118">PARAMETERS</span></span>

### <span data-ttu-id="15443-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15443-119">-DefaultProfile</span></span>
<span data-ttu-id="15443-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15443-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15443-121">-Force</span><span class="sxs-lookup"><span data-stu-id="15443-121">-Force</span></span>
<span data-ttu-id="15443-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="15443-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="15443-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15443-123">-InputObject</span></span>
<span data-ttu-id="15443-124">Az egyéni tartomány-objektum.</span><span class="sxs-lookup"><span data-stu-id="15443-124">The custom domain object.</span></span>

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

### <span data-ttu-id="15443-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="15443-125">-Name</span></span>
<span data-ttu-id="15443-126">Térbeli horgonyok fiók neve.</span><span class="sxs-lookup"><span data-stu-id="15443-126">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="15443-127">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="15443-127">-Primary</span></span>
<span data-ttu-id="15443-128">A térbeli horgonyok fiók elsődleges kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="15443-128">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="15443-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15443-129">-ResourceGroupName</span></span>
<span data-ttu-id="15443-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="15443-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="15443-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15443-131">-ResourceId</span></span>
<span data-ttu-id="15443-132">A térbeli horgonyok fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="15443-132">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="15443-133">-Másodlagos</span><span class="sxs-lookup"><span data-stu-id="15443-133">-Secondary</span></span>
<span data-ttu-id="15443-134">A térbeli horgonyok fiók elsődleges kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="15443-134">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="15443-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="15443-135">-Confirm</span></span>
<span data-ttu-id="15443-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="15443-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15443-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15443-137">-WhatIf</span></span>
<span data-ttu-id="15443-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="15443-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15443-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15443-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15443-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15443-140">CommonParameters</span></span>
<span data-ttu-id="15443-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15443-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="15443-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15443-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15443-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15443-143">INPUTS</span></span>

### <span data-ttu-id="15443-144">System. String</span><span class="sxs-lookup"><span data-stu-id="15443-144">System.String</span></span>

### <span data-ttu-id="15443-145">Microsoft. Azure. Command. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="15443-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="15443-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15443-146">OUTPUTS</span></span>

### <span data-ttu-id="15443-147">Microsoft. Azure. Command. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="15443-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="15443-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15443-148">NOTES</span></span>

## <span data-ttu-id="15443-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15443-149">RELATED LINKS</span></span>
