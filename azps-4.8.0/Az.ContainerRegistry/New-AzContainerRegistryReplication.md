---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: aadac0f7d408efd5f635d77d14f9afabfbd444d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182395"
---
# <span data-ttu-id="3aac7-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3aac7-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="3aac7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3aac7-102">SYNOPSIS</span></span>
<span data-ttu-id="3aac7-103">Tároló rendszerleíró adatbázis-replikációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3aac7-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="3aac7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3aac7-104">SYNTAX</span></span>

### <span data-ttu-id="3aac7-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3aac7-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3aac7-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aac7-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aac7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aac7-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3aac7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3aac7-108">DESCRIPTION</span></span>
<span data-ttu-id="3aac7-109">Az New-AzContainerRegistryReplication parancsmag létrehoz egy új tároló beállításjegyzék-replikálást.</span><span class="sxs-lookup"><span data-stu-id="3aac7-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="3aac7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3aac7-110">EXAMPLES</span></span>

### <span data-ttu-id="3aac7-111">Példa 1: új tároló rendszerleíróadatbázis-replikáció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="3aac7-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="3aac7-112">Új tároló rendszerleíró adatbázis-replikálás létrehozása</span><span class="sxs-lookup"><span data-stu-id="3aac7-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="3aac7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3aac7-113">PARAMETERS</span></span>

### <span data-ttu-id="3aac7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aac7-114">-DefaultProfile</span></span>
<span data-ttu-id="3aac7-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3aac7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3aac7-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="3aac7-116">-Location</span></span>
<span data-ttu-id="3aac7-117">A tároló beállításjegyzékének helye.</span><span class="sxs-lookup"><span data-stu-id="3aac7-117">Container Registry Location.</span></span>
<span data-ttu-id="3aac7-118">Alapértelmezett érték az erőforráscsoport helyére.</span><span class="sxs-lookup"><span data-stu-id="3aac7-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="3aac7-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3aac7-119">-Name</span></span>
<span data-ttu-id="3aac7-120">A tároló beállításjegyzék-replikációs neve.</span><span class="sxs-lookup"><span data-stu-id="3aac7-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="3aac7-121">A hely neve alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="3aac7-121">Default to the location name.</span></span>

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

### <span data-ttu-id="3aac7-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="3aac7-122">-Registry</span></span>
<span data-ttu-id="3aac7-123">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="3aac7-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="3aac7-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="3aac7-124">-RegistryName</span></span>
<span data-ttu-id="3aac7-125">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="3aac7-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="3aac7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aac7-126">-ResourceGroupName</span></span>
<span data-ttu-id="3aac7-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="3aac7-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="3aac7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3aac7-128">-ResourceId</span></span>
<span data-ttu-id="3aac7-129">A tároló beállításjegyzék-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="3aac7-129">The container registry resource id</span></span>

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

### <span data-ttu-id="3aac7-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="3aac7-130">-Tag</span></span>
<span data-ttu-id="3aac7-131">Tároló rendszerleíróadatbázis-címkék.</span><span class="sxs-lookup"><span data-stu-id="3aac7-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="3aac7-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3aac7-132">-Confirm</span></span>
<span data-ttu-id="3aac7-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3aac7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aac7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aac7-134">-WhatIf</span></span>
<span data-ttu-id="3aac7-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3aac7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3aac7-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3aac7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aac7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aac7-137">CommonParameters</span></span>
<span data-ttu-id="3aac7-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3aac7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aac7-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3aac7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aac7-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3aac7-140">INPUTS</span></span>

### <span data-ttu-id="3aac7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3aac7-141">System.String</span></span>

## <span data-ttu-id="3aac7-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3aac7-142">OUTPUTS</span></span>

### <span data-ttu-id="3aac7-143">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3aac7-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="3aac7-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3aac7-144">NOTES</span></span>

## <span data-ttu-id="3aac7-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3aac7-145">RELATED LINKS</span></span>

[<span data-ttu-id="3aac7-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3aac7-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="3aac7-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3aac7-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)