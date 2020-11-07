---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 21e821a4575fb918599ad2315c569a7f270e0a84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671183"
---
# <span data-ttu-id="5ddc3-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="5ddc3-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="5ddc3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ddc3-102">SYNOPSIS</span></span>
<span data-ttu-id="5ddc3-103">A tároló beállításjegyzékének replikálását kapja.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="5ddc3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ddc3-104">SYNTAX</span></span>

### <span data-ttu-id="5ddc3-105">ListReplicationByNameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ddc3-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ddc3-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ddc3-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ddc3-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ddc3-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ddc3-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ddc3-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ddc3-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ddc3-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ddc3-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ddc3-110">DESCRIPTION</span></span>
<span data-ttu-id="5ddc3-111">A Get-AzContainerRegistryReplication parancsmag a tároló beállításjegyzékének meghatározott replikálását vagy a tároló beállításjegyzékének összes replikálását kapja.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="5ddc3-112">Példák</span><span class="sxs-lookup"><span data-stu-id="5ddc3-112">EXAMPLES</span></span>

### <span data-ttu-id="5ddc3-113">Példa 1: egy tároló rendszerleíró adatbázisának meghatározott replikálását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="5ddc3-114">A tároló beállításjegyzékének meghatározott replikálását kapja</span><span class="sxs-lookup"><span data-stu-id="5ddc3-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="5ddc3-115">2. példa: a tárolók rendszerleíró adatbázisának minden replikálását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="5ddc3-116">A tároló beállításjegyzékének minden replikálását kapja</span><span class="sxs-lookup"><span data-stu-id="5ddc3-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="5ddc3-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ddc3-117">PARAMETERS</span></span>

### <span data-ttu-id="5ddc3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ddc3-118">-DefaultProfile</span></span>
<span data-ttu-id="5ddc3-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ddc3-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ddc3-120">-Name</span></span>
<span data-ttu-id="5ddc3-121">A tároló beállításjegyzék-replikációs neve.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="5ddc3-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="5ddc3-122">-Registry</span></span>
<span data-ttu-id="5ddc3-123">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="5ddc3-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="5ddc3-124">-RegistryName</span></span>
<span data-ttu-id="5ddc3-125">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="5ddc3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ddc3-126">-ResourceGroupName</span></span>
<span data-ttu-id="5ddc3-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="5ddc3-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="5ddc3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ddc3-128">-ResourceId</span></span>
<span data-ttu-id="5ddc3-129">A tároló beállításjegyzék-replikációs erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="5ddc3-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="5ddc3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ddc3-130">CommonParameters</span></span>
<span data-ttu-id="5ddc3-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ddc3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ddc3-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ddc3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ddc3-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ddc3-133">INPUTS</span></span>

### <span data-ttu-id="5ddc3-134">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5ddc3-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="5ddc3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5ddc3-135">System.String</span></span>

## <span data-ttu-id="5ddc3-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ddc3-136">OUTPUTS</span></span>

### <span data-ttu-id="5ddc3-137">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="5ddc3-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="5ddc3-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ddc3-138">NOTES</span></span>

## <span data-ttu-id="5ddc3-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ddc3-139">RELATED LINKS</span></span>

[<span data-ttu-id="5ddc3-140">Új – AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="5ddc3-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="5ddc3-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="5ddc3-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)