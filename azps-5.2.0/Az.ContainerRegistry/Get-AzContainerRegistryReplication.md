---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351210"
---
# <span data-ttu-id="133ce-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="133ce-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="133ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="133ce-102">SYNOPSIS</span></span>
<span data-ttu-id="133ce-103">Egy tároló beállításjegyzékének replikációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="133ce-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="133ce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="133ce-104">SYNTAX</span></span>

### <span data-ttu-id="133ce-105">ListReplicationByNameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="133ce-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="133ce-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="133ce-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="133ce-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="133ce-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="133ce-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="133ce-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="133ce-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="133ce-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="133ce-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="133ce-110">DESCRIPTION</span></span>
<span data-ttu-id="133ce-111">A Get-AzContainerRegistryReplication parancsmag egy tároló beállításjegyzékének vagy a tárolóadatbázis összes replikációjának megadott replikációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="133ce-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="133ce-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="133ce-112">EXAMPLES</span></span>

### <span data-ttu-id="133ce-113">1. példa: Egy tárolóadatbázis megadott replikációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="133ce-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="133ce-114">Egy tároló beállításjegyzékének megadott replikációja</span><span class="sxs-lookup"><span data-stu-id="133ce-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="133ce-115">2. példa: Egy tároló beállításjegyzékének összes replikációját beveszi.</span><span class="sxs-lookup"><span data-stu-id="133ce-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="133ce-116">Egy tárolóadatbázis összes replikációjának lekérte</span><span class="sxs-lookup"><span data-stu-id="133ce-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="133ce-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="133ce-117">PARAMETERS</span></span>

### <span data-ttu-id="133ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="133ce-118">-DefaultProfile</span></span>
<span data-ttu-id="133ce-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="133ce-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="133ce-120">-Name</span><span class="sxs-lookup"><span data-stu-id="133ce-120">-Name</span></span>
<span data-ttu-id="133ce-121">Container Registry Replikációs név.</span><span class="sxs-lookup"><span data-stu-id="133ce-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="133ce-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="133ce-122">-Registry</span></span>
<span data-ttu-id="133ce-123">Container Registry objektum.</span><span class="sxs-lookup"><span data-stu-id="133ce-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="133ce-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="133ce-124">-RegistryName</span></span>
<span data-ttu-id="133ce-125">Tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="133ce-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="133ce-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="133ce-126">-ResourceGroupName</span></span>
<span data-ttu-id="133ce-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="133ce-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="133ce-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="133ce-128">-ResourceId</span></span>
<span data-ttu-id="133ce-129">A tároló beállításjegyzékének replikációs erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="133ce-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="133ce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133ce-130">CommonParameters</span></span>
<span data-ttu-id="133ce-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="133ce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133ce-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="133ce-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133ce-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="133ce-133">INPUTS</span></span>

### <span data-ttu-id="133ce-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="133ce-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="133ce-135">System.String</span><span class="sxs-lookup"><span data-stu-id="133ce-135">System.String</span></span>

## <span data-ttu-id="133ce-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="133ce-136">OUTPUTS</span></span>

### <span data-ttu-id="133ce-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="133ce-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="133ce-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="133ce-138">NOTES</span></span>

## <span data-ttu-id="133ce-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="133ce-139">RELATED LINKS</span></span>

[<span data-ttu-id="133ce-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="133ce-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="133ce-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="133ce-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)