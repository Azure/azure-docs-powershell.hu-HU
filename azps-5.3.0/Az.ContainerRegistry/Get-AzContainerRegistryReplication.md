---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477577"
---
# <span data-ttu-id="ae4a3-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ae4a3-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="ae4a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4a3-103">Egy tároló beállításjegyzékének replikációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ae4a3-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="ae4a3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ae4a3-104">SYNTAX</span></span>

### <span data-ttu-id="ae4a3-105">ListReplicationByNameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae4a3-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae4a3-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae4a3-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae4a3-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae4a3-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae4a3-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae4a3-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae4a3-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae4a3-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae4a3-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ae4a3-110">DESCRIPTION</span></span>
<span data-ttu-id="ae4a3-111">A Get-AzContainerRegistryReplication parancsmag egy tároló beállításjegyzékének vagy a tárolóadatbázis összes replikációjának megadott replikációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ae4a3-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="ae4a3-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ae4a3-112">EXAMPLES</span></span>

### <span data-ttu-id="ae4a3-113">1. példa: Egy tárolóadatbázis megadott replikációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ae4a3-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="ae4a3-114">Egy tároló beállításjegyzékének megadott replikációja</span><span class="sxs-lookup"><span data-stu-id="ae4a3-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="ae4a3-115">2. példa: Egy tároló beállításjegyzékének összes replikációját beveszi.</span><span class="sxs-lookup"><span data-stu-id="ae4a3-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="ae4a3-116">Egy tárolóadatbázis összes replikációjának lekérte</span><span class="sxs-lookup"><span data-stu-id="ae4a3-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="ae4a3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae4a3-117">PARAMETERS</span></span>

### <span data-ttu-id="ae4a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae4a3-118">-DefaultProfile</span></span>
<span data-ttu-id="ae4a3-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae4a3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae4a3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ae4a3-120">-Name</span></span>
<span data-ttu-id="ae4a3-121">Container Registry Replikációs név.</span><span class="sxs-lookup"><span data-stu-id="ae4a3-121">Container Registry Replication Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4a3-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="ae4a3-122">-Registry</span></span>
<span data-ttu-id="ae4a3-123">Container Registry objektum.</span><span class="sxs-lookup"><span data-stu-id="ae4a3-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae4a3-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ae4a3-124">-RegistryName</span></span>
<span data-ttu-id="ae4a3-125">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="ae4a3-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4a3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae4a3-126">-ResourceGroupName</span></span>
<span data-ttu-id="ae4a3-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ae4a3-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4a3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae4a3-128">-ResourceId</span></span>
<span data-ttu-id="ae4a3-129">A tároló beállításjegyzékének replikációs erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ae4a3-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="ae4a3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4a3-130">CommonParameters</span></span>
<span data-ttu-id="ae4a3-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae4a3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4a3-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae4a3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4a3-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae4a3-133">INPUTS</span></span>

### <span data-ttu-id="ae4a3-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ae4a3-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="ae4a3-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ae4a3-135">System.String</span></span>

## <span data-ttu-id="ae4a3-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae4a3-136">OUTPUTS</span></span>

### <span data-ttu-id="ae4a3-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ae4a3-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="ae4a3-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ae4a3-138">NOTES</span></span>

## <span data-ttu-id="ae4a3-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae4a3-139">RELATED LINKS</span></span>

[<span data-ttu-id="ae4a3-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ae4a3-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="ae4a3-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ae4a3-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)