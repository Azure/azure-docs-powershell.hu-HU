---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: aadac0f7d408efd5f635d77d14f9afabfbd444d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166378"
---
# <span data-ttu-id="d2346-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d2346-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="d2346-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2346-102">SYNOPSIS</span></span>
<span data-ttu-id="d2346-103">Létrehoz egy tárolóadatbázis-replikációt.</span><span class="sxs-lookup"><span data-stu-id="d2346-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="d2346-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d2346-104">SYNTAX</span></span>

### <span data-ttu-id="d2346-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d2346-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2346-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2346-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2346-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2346-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2346-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d2346-108">DESCRIPTION</span></span>
<span data-ttu-id="d2346-109">A New-AzContainerRegistryReplication parancsmag létrehoz egy új tárolóadatbázis-replikációt.</span><span class="sxs-lookup"><span data-stu-id="d2346-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="d2346-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d2346-110">EXAMPLES</span></span>

### <span data-ttu-id="d2346-111">1. példa: Új tároló beállításjegyzék-replikáció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="d2346-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="d2346-112">Hozzon létre egy új tárolóadatbázis-replikációt.</span><span class="sxs-lookup"><span data-stu-id="d2346-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="d2346-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2346-113">PARAMETERS</span></span>

### <span data-ttu-id="d2346-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2346-114">-DefaultProfile</span></span>
<span data-ttu-id="d2346-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2346-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2346-116">-Location</span><span class="sxs-lookup"><span data-stu-id="d2346-116">-Location</span></span>
<span data-ttu-id="d2346-117">Container Registry Location.</span><span class="sxs-lookup"><span data-stu-id="d2346-117">Container Registry Location.</span></span>
<span data-ttu-id="d2346-118">Alapértelmezés szerint az erőforráscsoport helye.</span><span class="sxs-lookup"><span data-stu-id="d2346-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="d2346-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d2346-119">-Name</span></span>
<span data-ttu-id="d2346-120">Container Registry Replikációs név.</span><span class="sxs-lookup"><span data-stu-id="d2346-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="d2346-121">A hely nevének alapértelmezett beállítása.</span><span class="sxs-lookup"><span data-stu-id="d2346-121">Default to the location name.</span></span>

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

### <span data-ttu-id="d2346-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="d2346-122">-Registry</span></span>
<span data-ttu-id="d2346-123">Container Registry objektum.</span><span class="sxs-lookup"><span data-stu-id="d2346-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="d2346-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d2346-124">-RegistryName</span></span>
<span data-ttu-id="d2346-125">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="d2346-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="d2346-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2346-126">-ResourceGroupName</span></span>
<span data-ttu-id="d2346-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d2346-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="d2346-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2346-128">-ResourceId</span></span>
<span data-ttu-id="d2346-129">A tároló beállításjegyzékének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d2346-129">The container registry resource id</span></span>

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

### <span data-ttu-id="d2346-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="d2346-130">-Tag</span></span>
<span data-ttu-id="d2346-131">Container Registry Tags.</span><span class="sxs-lookup"><span data-stu-id="d2346-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="d2346-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2346-132">-Confirm</span></span>
<span data-ttu-id="d2346-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d2346-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2346-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2346-134">-WhatIf</span></span>
<span data-ttu-id="d2346-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d2346-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2346-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d2346-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2346-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2346-137">CommonParameters</span></span>
<span data-ttu-id="d2346-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2346-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2346-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2346-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2346-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2346-140">INPUTS</span></span>

### <span data-ttu-id="d2346-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d2346-141">System.String</span></span>

## <span data-ttu-id="d2346-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2346-142">OUTPUTS</span></span>

### <span data-ttu-id="d2346-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d2346-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="d2346-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d2346-144">NOTES</span></span>

## <span data-ttu-id="d2346-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2346-145">RELATED LINKS</span></span>

[<span data-ttu-id="d2346-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d2346-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="d2346-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d2346-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)