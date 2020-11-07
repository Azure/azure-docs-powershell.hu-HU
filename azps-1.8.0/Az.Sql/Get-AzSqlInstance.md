---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
ms.openlocfilehash: a21b2436f44cb2df5f9984e70ccecf6c1d9c306a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668979"
---
# <span data-ttu-id="be23c-101">Get-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="be23c-101">Get-AzSqlInstance</span></span>

## <span data-ttu-id="be23c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be23c-102">SYNOPSIS</span></span>
<span data-ttu-id="be23c-103">Információt ad az Azure SQL felügyelt adatbázis-példányról.</span><span class="sxs-lookup"><span data-stu-id="be23c-103">Returns information about Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="be23c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be23c-104">SYNTAX</span></span>

```
Get-AzSqlInstance [[-Name] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be23c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="be23c-105">DESCRIPTION</span></span>
<span data-ttu-id="be23c-106">A **Get-AzSqlInstance** parancsmag információt ad egy vagy több Azure SQL-alapú felügyelt példányról.</span><span class="sxs-lookup"><span data-stu-id="be23c-106">The **Get-AzSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="be23c-107">Adja meg a példány nevét úgy, hogy csak az adott példány adatait lássa.</span><span class="sxs-lookup"><span data-stu-id="be23c-107">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="be23c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="be23c-108">EXAMPLES</span></span>

### <span data-ttu-id="be23c-109">Példa 1: egy erőforráscsoport számára hozzárendelt összes példány beolvasása</span><span class="sxs-lookup"><span data-stu-id="be23c-109">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="be23c-110">Ez a parancs információt kap az erőforráscsoport ResourceGroup01 társított összes példányról.</span><span class="sxs-lookup"><span data-stu-id="be23c-110">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="be23c-111">2. példa: információk kérése egy példányról</span><span class="sxs-lookup"><span data-stu-id="be23c-111">Example 2: Get information about an  instance</span></span>
```
PS C:\> Get-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="be23c-112">Ez a parancs információkat kap a managedInstance1 nevű példányról.</span><span class="sxs-lookup"><span data-stu-id="be23c-112">This command gets information about the instance named managedInstance1.</span></span>

### <span data-ttu-id="be23c-113">3. példa: az erőforráscsoport minden előfordulásának beolvasása szűréssel</span><span class="sxs-lookup"><span data-stu-id="be23c-113">Example 3: Get all instances assigned to a resource group using filtering</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "managedInstance*"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="be23c-114">Ez a parancs a "managedInstance" kezdetű erőforráscsoport-ResourceGroup01 tartozó összes példányról információt kap.</span><span class="sxs-lookup"><span data-stu-id="be23c-114">This command gets information about all instances assigned to the resource group ResourceGroup01 that start with "managedInstance".</span></span>

## <span data-ttu-id="be23c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be23c-115">PARAMETERS</span></span>

### <span data-ttu-id="be23c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be23c-116">-DefaultProfile</span></span>
<span data-ttu-id="be23c-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be23c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be23c-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="be23c-118">-Name</span></span>
<span data-ttu-id="be23c-119">SQL-példány neve</span><span class="sxs-lookup"><span data-stu-id="be23c-119">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="be23c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be23c-120">-ResourceGroupName</span></span>
<span data-ttu-id="be23c-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="be23c-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="be23c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be23c-122">CommonParameters</span></span>
<span data-ttu-id="be23c-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be23c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be23c-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="be23c-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be23c-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be23c-125">INPUTS</span></span>

### <span data-ttu-id="be23c-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="be23c-126">None</span></span>

## <span data-ttu-id="be23c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be23c-127">OUTPUTS</span></span>

### <span data-ttu-id="be23c-128">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="be23c-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="be23c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be23c-129">NOTES</span></span>

## <span data-ttu-id="be23c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be23c-130">RELATED LINKS</span></span>
