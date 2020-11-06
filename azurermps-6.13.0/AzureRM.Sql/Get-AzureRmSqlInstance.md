---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
ms.openlocfilehash: 72e3b740a84a46da094208b941e8b68173133e46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499360"
---
# <span data-ttu-id="138e8-101">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="138e8-101">Get-AzureRmSqlInstance</span></span>

## <span data-ttu-id="138e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="138e8-102">SYNOPSIS</span></span>
<span data-ttu-id="138e8-103">Információt ad az Azure SQL felügyelt adatbázis-példányról.</span><span class="sxs-lookup"><span data-stu-id="138e8-103">Returns information about Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="138e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="138e8-104">SYNTAX</span></span>

### <span data-ttu-id="138e8-105">GetInstanceByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="138e8-105">GetInstanceByResourceGroup (Default)</span></span>
```
Get-AzureRmSqlInstance [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="138e8-106">GetInstanceByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="138e8-106">GetInstanceByNameAndResourceGroup</span></span>
```
Get-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="138e8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="138e8-107">DESCRIPTION</span></span>
<span data-ttu-id="138e8-108">A **Get-AzureRmSqlInstance** parancsmag információt ad egy vagy több Azure SQL-alapú felügyelt példányról.</span><span class="sxs-lookup"><span data-stu-id="138e8-108">The **Get-AzureRmSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="138e8-109">Adja meg a példány nevét úgy, hogy csak az adott példány adatait lássa.</span><span class="sxs-lookup"><span data-stu-id="138e8-109">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="138e8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="138e8-110">EXAMPLES</span></span>

### <span data-ttu-id="138e8-111">Példa 1: egy erőforráscsoport számára hozzárendelt összes példány beolvasása</span><span class="sxs-lookup"><span data-stu-id="138e8-111">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlInstance -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="138e8-112">Ez a parancs információt kap az erőforráscsoport ResourceGroup01 társított összes példányról.</span><span class="sxs-lookup"><span data-stu-id="138e8-112">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="138e8-113">2. példa: információk kérése egy példányról</span><span class="sxs-lookup"><span data-stu-id="138e8-113">Example 2: Get information about an  instance</span></span>
```
PS C:\>Get-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="138e8-114">Ez a parancs információkat kap a managedInstance1 nevű példányról.</span><span class="sxs-lookup"><span data-stu-id="138e8-114">This command gets information about the instance named managedInstance1.</span></span>

## <span data-ttu-id="138e8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="138e8-115">PARAMETERS</span></span>

### <span data-ttu-id="138e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="138e8-116">-DefaultProfile</span></span>
<span data-ttu-id="138e8-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="138e8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="138e8-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="138e8-118">-Name</span></span>
<span data-ttu-id="138e8-119">SQL-példány neve</span><span class="sxs-lookup"><span data-stu-id="138e8-119">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="138e8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="138e8-120">-ResourceGroupName</span></span>
<span data-ttu-id="138e8-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="138e8-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="138e8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="138e8-122">CommonParameters</span></span>
<span data-ttu-id="138e8-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="138e8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="138e8-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="138e8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="138e8-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="138e8-125">INPUTS</span></span>

### <span data-ttu-id="138e8-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="138e8-126">None</span></span>

## <span data-ttu-id="138e8-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="138e8-127">OUTPUTS</span></span>

### <span data-ttu-id="138e8-128">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="138e8-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="138e8-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="138e8-129">NOTES</span></span>

## <span data-ttu-id="138e8-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="138e8-130">RELATED LINKS</span></span>
