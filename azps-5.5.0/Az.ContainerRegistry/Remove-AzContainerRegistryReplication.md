---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166354"
---
# <span data-ttu-id="b764e-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b764e-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="b764e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b764e-102">SYNOPSIS</span></span>
<span data-ttu-id="b764e-103">Eltávolít egy tárolóadatbázis-replikációt.</span><span class="sxs-lookup"><span data-stu-id="b764e-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="b764e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b764e-104">SYNTAX</span></span>

### <span data-ttu-id="b764e-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b764e-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b764e-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b764e-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b764e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b764e-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b764e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b764e-108">DESCRIPTION</span></span>
<span data-ttu-id="b764e-109">A Remove-AzContainerRegistryReplication parancsmag eltávolítja a tároló beállításjegyzékének replikációját.</span><span class="sxs-lookup"><span data-stu-id="b764e-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="b764e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b764e-110">EXAMPLES</span></span>

### <span data-ttu-id="b764e-111">1. példa: Eltávolítja a tároló beállításjegyzékének replikációját.</span><span class="sxs-lookup"><span data-stu-id="b764e-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="b764e-112">Eltávolítja a tároló beállításjegyzékének replikációját.</span><span class="sxs-lookup"><span data-stu-id="b764e-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="b764e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b764e-113">PARAMETERS</span></span>

### <span data-ttu-id="b764e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b764e-114">-DefaultProfile</span></span>
<span data-ttu-id="b764e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b764e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b764e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b764e-116">-Name</span></span>
<span data-ttu-id="b764e-117">Container Registry Replikációs név.</span><span class="sxs-lookup"><span data-stu-id="b764e-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="b764e-118">A hely nevének alapértelmezett beállítása.</span><span class="sxs-lookup"><span data-stu-id="b764e-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b764e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b764e-119">-PassThru</span></span>
<span data-ttu-id="b764e-120">Azt jelzi, hogy ez a parancsmag igaz értéket ad vissza, ha az eltávolítás sikerült.</span><span class="sxs-lookup"><span data-stu-id="b764e-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="b764e-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b764e-121">-RegistryName</span></span>
<span data-ttu-id="b764e-122">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="b764e-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b764e-123">-Replikáció</span><span class="sxs-lookup"><span data-stu-id="b764e-123">-Replication</span></span>
<span data-ttu-id="b764e-124">Container Registry objektum.</span><span class="sxs-lookup"><span data-stu-id="b764e-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: Replicatoin

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b764e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b764e-125">-ResourceGroupName</span></span>
<span data-ttu-id="b764e-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b764e-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b764e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b764e-127">-ResourceId</span></span>
<span data-ttu-id="b764e-128">A tároló beállításjegyzékének replikációs erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b764e-128">The container registry replication resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b764e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b764e-129">-Confirm</span></span>
<span data-ttu-id="b764e-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b764e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b764e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b764e-131">-WhatIf</span></span>
<span data-ttu-id="b764e-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b764e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b764e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b764e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b764e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b764e-134">CommonParameters</span></span>
<span data-ttu-id="b764e-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b764e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b764e-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b764e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b764e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b764e-137">INPUTS</span></span>

### <span data-ttu-id="b764e-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b764e-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="b764e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b764e-139">System.String</span></span>

## <span data-ttu-id="b764e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b764e-140">OUTPUTS</span></span>

### <span data-ttu-id="b764e-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b764e-141">System.Boolean</span></span>

## <span data-ttu-id="b764e-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b764e-142">NOTES</span></span>

## <span data-ttu-id="b764e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b764e-143">RELATED LINKS</span></span>

[<span data-ttu-id="b764e-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b764e-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="b764e-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b764e-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

