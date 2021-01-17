---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: bd12fd2067c931f05266ed1ed24fb5666ead59a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374680"
---
# <span data-ttu-id="f1ef5-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="f1ef5-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="f1ef5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ef5-103">Az Azure SQL Virtuális fürtről ad információkat.</span><span class="sxs-lookup"><span data-stu-id="f1ef5-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="f1ef5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f1ef5-104">SYNTAX</span></span>

### <span data-ttu-id="f1ef5-105">GetVirtualClusterByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1ef5-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1ef5-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f1ef5-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1ef5-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="f1ef5-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1ef5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f1ef5-108">DESCRIPTION</span></span>
<span data-ttu-id="f1ef5-109">A **Get-AzSqlVirtualCluster** parancsmag egy vagy több Azure SQL virtuális fürtről ad információkat.</span><span class="sxs-lookup"><span data-stu-id="f1ef5-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="f1ef5-110">Adja meg a virtuális fürt nevét, hogy csak az adott fürt adatait lássa.</span><span class="sxs-lookup"><span data-stu-id="f1ef5-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="f1ef5-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f1ef5-111">EXAMPLES</span></span>

### <span data-ttu-id="f1ef5-112">1. példa: Az erőforráscsoporthoz rendelt összes virtuális fürt lekérte</span><span class="sxs-lookup"><span data-stu-id="f1ef5-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
```powershell
PS C:> Get-AzSqlVirtualCluster -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster2
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster2
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name2

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster3
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster3
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name3
```

<span data-ttu-id="f1ef5-113">Ez a parancs információkat kap az Erőforráscsoport01 erőforráscsoporthoz rendelt összes virtuális fürtről.</span><span class="sxs-lookup"><span data-stu-id="f1ef5-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="f1ef5-114">2. példa: Információk lekérte egy adott virtuális fürtről</span><span class="sxs-lookup"><span data-stu-id="f1ef5-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="f1ef5-115">Ez a parancs információkat kap a VirtualCluster1 virtuális fürtről az ResourceGroup01 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="f1ef5-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f1ef5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1ef5-116">PARAMETERS</span></span>

### <span data-ttu-id="f1ef5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ef5-117">-DefaultProfile</span></span>
<span data-ttu-id="f1ef5-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1ef5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1ef5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f1ef5-119">-Name</span></span>
<span data-ttu-id="f1ef5-120">A virtuális fürt neve.</span><span class="sxs-lookup"><span data-stu-id="f1ef5-120">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1ef5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1ef5-121">-ResourceGroupName</span></span>
<span data-ttu-id="f1ef5-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f1ef5-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1ef5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1ef5-123">-ResourceId</span></span>
<span data-ttu-id="f1ef5-124">A lekért példányobjektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f1ef5-124">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ef5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ef5-125">CommonParameters</span></span>
<span data-ttu-id="f1ef5-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1ef5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ef5-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1ef5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ef5-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1ef5-128">INPUTS</span></span>

### <span data-ttu-id="f1ef5-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="f1ef5-129">None</span></span>

## <span data-ttu-id="f1ef5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1ef5-130">OUTPUTS</span></span>

### <span data-ttu-id="f1ef5-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="f1ef5-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="f1ef5-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f1ef5-132">NOTES</span></span>

## <span data-ttu-id="f1ef5-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1ef5-133">RELATED LINKS</span></span>
