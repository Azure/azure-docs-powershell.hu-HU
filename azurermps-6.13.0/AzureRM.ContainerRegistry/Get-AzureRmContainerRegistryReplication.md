---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: d2cac696382f807a1fc4afe94f9d2d61ea65cece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93671977"
---
# <span data-ttu-id="39d90-101">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="39d90-101">Get-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="39d90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39d90-102">SYNOPSIS</span></span>
<span data-ttu-id="39d90-103">A tároló beállításjegyzékének replikálását kapja.</span><span class="sxs-lookup"><span data-stu-id="39d90-103">Gets a replication of a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39d90-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39d90-104">SYNTAX</span></span>

### <span data-ttu-id="39d90-105">ListReplicationByNameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39d90-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39d90-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="39d90-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39d90-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39d90-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39d90-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39d90-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39d90-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39d90-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39d90-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="39d90-110">DESCRIPTION</span></span>
<span data-ttu-id="39d90-111">A Get-AzureRmContainerRegistryReplication parancsmag a tároló beállításjegyzékének meghatározott replikálását vagy a tároló beállításjegyzékének összes replikálását kapja.</span><span class="sxs-lookup"><span data-stu-id="39d90-111">The Get-AzureRmContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="39d90-112">Példák</span><span class="sxs-lookup"><span data-stu-id="39d90-112">EXAMPLES</span></span>

### <span data-ttu-id="39d90-113">Példa 1: egy tároló rendszerleíró adatbázisának meghatározott replikálását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="39d90-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="39d90-114">A tároló beállításjegyzékének meghatározott replikálását kapja</span><span class="sxs-lookup"><span data-stu-id="39d90-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="39d90-115">2. példa: a tárolók rendszerleíró adatbázisának minden replikálását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="39d90-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="39d90-116">A tároló beállításjegyzékének minden replikálását kapja</span><span class="sxs-lookup"><span data-stu-id="39d90-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="39d90-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39d90-117">PARAMETERS</span></span>

### <span data-ttu-id="39d90-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d90-118">-DefaultProfile</span></span>
<span data-ttu-id="39d90-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39d90-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d90-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39d90-120">-Name</span></span>
<span data-ttu-id="39d90-121">A tároló beállításjegyzék-replikációs neve.</span><span class="sxs-lookup"><span data-stu-id="39d90-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="39d90-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="39d90-122">-Registry</span></span>
<span data-ttu-id="39d90-123">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="39d90-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="39d90-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="39d90-124">-RegistryName</span></span>
<span data-ttu-id="39d90-125">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="39d90-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="39d90-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39d90-126">-ResourceGroupName</span></span>
<span data-ttu-id="39d90-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="39d90-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="39d90-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39d90-128">-ResourceId</span></span>
<span data-ttu-id="39d90-129">A tároló beállításjegyzék-replikációs erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="39d90-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="39d90-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d90-130">CommonParameters</span></span>
<span data-ttu-id="39d90-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39d90-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d90-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39d90-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d90-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39d90-133">INPUTS</span></span>

### <span data-ttu-id="39d90-134">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="39d90-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="39d90-135">Paraméterek: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="39d90-135">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="39d90-136">System. String</span><span class="sxs-lookup"><span data-stu-id="39d90-136">System.String</span></span>

## <span data-ttu-id="39d90-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39d90-137">OUTPUTS</span></span>

### <span data-ttu-id="39d90-138">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="39d90-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="39d90-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39d90-139">NOTES</span></span>

## <span data-ttu-id="39d90-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39d90-140">RELATED LINKS</span></span>

[<span data-ttu-id="39d90-141">Új – AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="39d90-141">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="39d90-142">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="39d90-142">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
