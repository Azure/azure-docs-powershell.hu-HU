---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: f5e52938a6d0f618d53621a895aeb7037dc543ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668911"
---
# <span data-ttu-id="6c91a-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="6c91a-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="6c91a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c91a-102">SYNOPSIS</span></span>
<span data-ttu-id="6c91a-103">Információt ad az Azure SQL virtuális fürtökről.</span><span class="sxs-lookup"><span data-stu-id="6c91a-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="6c91a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c91a-104">SYNTAX</span></span>

### <span data-ttu-id="6c91a-105">GetVirtualClusterByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6c91a-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c91a-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6c91a-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c91a-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="6c91a-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c91a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c91a-108">DESCRIPTION</span></span>
<span data-ttu-id="6c91a-109">A **Get-AzSqlVirtualCluster** parancsmag információt ad egy vagy több Azure SQL-szektorcsoportról.</span><span class="sxs-lookup"><span data-stu-id="6c91a-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="6c91a-110">Adjon meg egy virtuális fürtöt, ha csak a fürt adatait szeretné látni.</span><span class="sxs-lookup"><span data-stu-id="6c91a-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="6c91a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6c91a-111">EXAMPLES</span></span>

### <span data-ttu-id="6c91a-112">Példa 1: egy erőforráscsoport számára hozzárendelt összes virtuális fürt beszerzése</span><span class="sxs-lookup"><span data-stu-id="6c91a-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
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

<span data-ttu-id="6c91a-113">Ez a parancs információkat kap az erőforráscsoport ResourceGroup01 társított összes virtuális fürtökről.</span><span class="sxs-lookup"><span data-stu-id="6c91a-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="6c91a-114">2. példa: információk beszerzése konkrét virtuális fürtökről</span><span class="sxs-lookup"><span data-stu-id="6c91a-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="6c91a-115">Ez a parancs információt kap a virtuális fürtök VirtualCluster1 az erőforráscsoport ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6c91a-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="6c91a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c91a-116">PARAMETERS</span></span>

### <span data-ttu-id="6c91a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c91a-117">-DefaultProfile</span></span>
<span data-ttu-id="6c91a-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c91a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c91a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6c91a-119">-Name</span></span>
<span data-ttu-id="6c91a-120">A virtuális fürt neve.</span><span class="sxs-lookup"><span data-stu-id="6c91a-120">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="6c91a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c91a-121">-ResourceGroupName</span></span>
<span data-ttu-id="6c91a-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6c91a-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="6c91a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c91a-123">-ResourceId</span></span>
<span data-ttu-id="6c91a-124">A beolvasott példány-objektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6c91a-124">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="6c91a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c91a-125">CommonParameters</span></span>
<span data-ttu-id="6c91a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c91a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c91a-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6c91a-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c91a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c91a-128">INPUTS</span></span>

### <span data-ttu-id="6c91a-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="6c91a-129">None</span></span>

## <span data-ttu-id="6c91a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c91a-130">OUTPUTS</span></span>

### <span data-ttu-id="6c91a-131">Microsoft. Azure. Command. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="6c91a-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="6c91a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c91a-132">NOTES</span></span>

## <span data-ttu-id="6c91a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c91a-133">RELATED LINKS</span></span>
