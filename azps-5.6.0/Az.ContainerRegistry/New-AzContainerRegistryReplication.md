---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: a446fe34ba29789e93e8907d3155af654a93ff21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941282"
---
# <span data-ttu-id="e640d-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e640d-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="e640d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e640d-102">SYNOPSIS</span></span>
<span data-ttu-id="e640d-103">Létrehoz egy tárolóadatbázis-replikációt.</span><span class="sxs-lookup"><span data-stu-id="e640d-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="e640d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e640d-104">SYNTAX</span></span>

### <span data-ttu-id="e640d-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e640d-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e640d-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e640d-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e640d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e640d-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e640d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e640d-108">DESCRIPTION</span></span>
<span data-ttu-id="e640d-109">A New-AzContainerRegistryReplication parancsmag létrehoz egy új tárolóadatbázis-replikációt.</span><span class="sxs-lookup"><span data-stu-id="e640d-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="e640d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e640d-110">EXAMPLES</span></span>

### <span data-ttu-id="e640d-111">1. példa: Új tároló beállításjegyzék-replikáció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="e640d-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="e640d-112">Hozzon létre egy új tárolóadatbázis-replikációt.</span><span class="sxs-lookup"><span data-stu-id="e640d-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="e640d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e640d-113">PARAMETERS</span></span>

### <span data-ttu-id="e640d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e640d-114">-DefaultProfile</span></span>
<span data-ttu-id="e640d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e640d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e640d-116">-Location</span><span class="sxs-lookup"><span data-stu-id="e640d-116">-Location</span></span>
<span data-ttu-id="e640d-117">Container Registry Location.</span><span class="sxs-lookup"><span data-stu-id="e640d-117">Container Registry Location.</span></span>
<span data-ttu-id="e640d-118">Alapértelmezés szerint az erőforráscsoport helye.</span><span class="sxs-lookup"><span data-stu-id="e640d-118">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e640d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e640d-119">-Name</span></span>
<span data-ttu-id="e640d-120">Container Registry Replikációs név.</span><span class="sxs-lookup"><span data-stu-id="e640d-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="e640d-121">A hely nevének alapértelmezett beállítása.</span><span class="sxs-lookup"><span data-stu-id="e640d-121">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e640d-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="e640d-122">-Registry</span></span>
<span data-ttu-id="e640d-123">Container Registry objektum.</span><span class="sxs-lookup"><span data-stu-id="e640d-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e640d-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="e640d-124">-RegistryName</span></span>
<span data-ttu-id="e640d-125">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="e640d-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e640d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e640d-126">-ResourceGroupName</span></span>
<span data-ttu-id="e640d-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e640d-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e640d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e640d-128">-ResourceId</span></span>
<span data-ttu-id="e640d-129">A tároló beállításjegyzékének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e640d-129">The container registry resource id</span></span>

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

### <span data-ttu-id="e640d-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="e640d-130">-Tag</span></span>
<span data-ttu-id="e640d-131">Container Registry Tags.</span><span class="sxs-lookup"><span data-stu-id="e640d-131">Container Registry Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e640d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e640d-132">-Confirm</span></span>
<span data-ttu-id="e640d-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e640d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e640d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e640d-134">-WhatIf</span></span>
<span data-ttu-id="e640d-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e640d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e640d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e640d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e640d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e640d-137">CommonParameters</span></span>
<span data-ttu-id="e640d-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e640d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e640d-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e640d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e640d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e640d-140">INPUTS</span></span>

### <span data-ttu-id="e640d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e640d-141">System.String</span></span>

## <span data-ttu-id="e640d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e640d-142">OUTPUTS</span></span>

### <span data-ttu-id="e640d-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e640d-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="e640d-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e640d-144">NOTES</span></span>

## <span data-ttu-id="e640d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e640d-145">RELATED LINKS</span></span>

[<span data-ttu-id="e640d-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e640d-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="e640d-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e640d-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)