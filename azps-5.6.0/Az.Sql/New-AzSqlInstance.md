---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: 9f648f0e2ab15919f3caa849041846570d627df5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927714"
---
# <span data-ttu-id="ee299-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ee299-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="ee299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee299-102">SYNOPSIS</span></span>
<span data-ttu-id="ee299-103">Létrehoz egy Azure SQL-adatbázis felügyelt példányát.</span><span class="sxs-lookup"><span data-stu-id="ee299-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="ee299-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ee299-104">SYNTAX</span></span>

### <span data-ttu-id="ee299-105">NewByEditionAndComputeGenerációParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee299-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee299-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee299-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee299-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee299-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee299-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="ee299-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee299-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ee299-109">DESCRIPTION</span></span>
<span data-ttu-id="ee299-110">A **New-AzSqlInstance** parancsmag létrehoz egy Azure SQL-adatbázis felügyelt példányát.</span><span class="sxs-lookup"><span data-stu-id="ee299-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="ee299-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ee299-111">EXAMPLES</span></span>

### <span data-ttu-id="ee299-112">1. példa: Új példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="ee299-112">Example 1: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4 -DnsZonePartner "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/partnerServerForDnsZone"
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
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="ee299-113">Ez a parancs új példányt hoz létre az SkuName paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="ee299-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="ee299-114">2. példa: Új példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="ee299-114">Example 2: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="ee299-115">Ez a parancs új példányt hoz létre a Edition és a ComputeGeneráció paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="ee299-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="ee299-116">3. példa: Új példány létrehozása egy példánykészletben egy példánykészlet-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="ee299-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="ee299-117">Ez a parancs új példányt hoz létre egy példánykészletben egy példánykészlet-objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="ee299-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="ee299-118">4. példa: Új példány létrehozása egy példánykészletben egy példánykészlet erőforrás-azonosítójának használatával</span><span class="sxs-lookup"><span data-stu-id="ee299-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
```powershell
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="ee299-119">Ez a parancs új példányt hoz létre egy példánykészletben a példánykészlet erőforrás-azonosítójának használatával.</span><span class="sxs-lookup"><span data-stu-id="ee299-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="ee299-120">5. példa: Új példány létrehozása egy példánykészletben</span><span class="sxs-lookup"><span data-stu-id="ee299-120">Example 5: Create a new instance in an instance pool</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 32 -VCore 2 -ComputeGeneration Gen5 -Edition GeneralPurpose -InstancePoolName instancePool0
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
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 32
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="ee299-121">Ez a parancs új példányt hoz létre egy példánykészletben, a név instancePool0 névvel</span><span class="sxs-lookup"><span data-stu-id="ee299-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

### <span data-ttu-id="ee299-122">6. példa: Új példány létrehozása karbantartási konfigurációval</span><span class="sxs-lookup"><span data-stu-id="ee299-122">Example 6: Create a new instance with maintenance configuration</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourcegroup01 -Location "westus" -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -ComputeGeneration Gen5 -Edition GeneralPurpose -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
Location                   : westus
Id                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName          : resourcegroup01
ManagedInstanceName        : managedInstance1
Tags                       :
Identity                   :
Sku                        : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName   : managedInstance1.wusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin         : adminLogin1
AdministratorPassword      :
SubnetId                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType                : LicenseIncluded
VCores                     : 8
StorageSizeInGB            : 256
Collation                  : SQL_Latin1_General_CP1_CI_AS
PublicDataEndpointEnabled  : False
ProxyOverride              :
TimezoneId                 : UTC
DnsZonePartner             :
DnsZone                    : ad35cna0mw
InstancePoolName           :
MinimalTlsVersion          :
BackupStorageRedundancy    : Geo
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2
```

<span data-ttu-id="ee299-123">Ez a parancs egy új példányt hoz létre karbantartási konfigurációs MI_2</span><span class="sxs-lookup"><span data-stu-id="ee299-123">This command creates a new instance with maintenance configuration MI_2</span></span>

## <span data-ttu-id="ee299-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee299-124">PARAMETERS</span></span>

### <span data-ttu-id="ee299-125">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="ee299-125">-AdministratorCredential</span></span>
<span data-ttu-id="ee299-126">A példány SQL-hitelesítési hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="ee299-126">The SQL authentication credential of the instance.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee299-127">-AsJob</span></span>
<span data-ttu-id="ee299-128">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ee299-128">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ee299-129">-AssignIdentity</span></span>
<span data-ttu-id="ee299-130">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a Felügyelt példányhoz olyan kulcskezelési szolgáltatásokhoz, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ee299-130">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-131">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="ee299-131">-BackupStorageRedundancy</span></span>
<span data-ttu-id="ee299-132">Az Sql Azure Felügyelt példány biztonsági másolatának tárolásához használt biztonsági mentési tárterület redundancia.</span><span class="sxs-lookup"><span data-stu-id="ee299-132">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="ee299-133">Beállítások: Helyi, Zóna és Földrajzi</span><span class="sxs-lookup"><span data-stu-id="ee299-133">Options are: Local, Zone and Geo</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-134">-Collation</span><span class="sxs-lookup"><span data-stu-id="ee299-134">-Collation</span></span>
<span data-ttu-id="ee299-135">A használt Azure SQL Felügyelt példány szétválogatása.</span><span class="sxs-lookup"><span data-stu-id="ee299-135">The collation of the Azure SQL Managed Instance to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-136">-ComputeGeneráció</span><span class="sxs-lookup"><span data-stu-id="ee299-136">-ComputeGeneration</span></span>
<span data-ttu-id="ee299-137">A példány számítási generációja.</span><span class="sxs-lookup"><span data-stu-id="ee299-137">The compute generation for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee299-138">-DefaultProfile</span></span>
<span data-ttu-id="ee299-139">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee299-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee299-140">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="ee299-140">-DnsZonePartner</span></span>
<span data-ttu-id="ee299-141">A Felügyelt kiszolgáló partner erőforrás-azonosítója, amely örökli a DnsZone tulajdonságot a Felügyelt példány létrehozásához</span><span class="sxs-lookup"><span data-stu-id="ee299-141">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-142">-Edition</span><span class="sxs-lookup"><span data-stu-id="ee299-142">-Edition</span></span>
<span data-ttu-id="ee299-143">A példány kiadása.</span><span class="sxs-lookup"><span data-stu-id="ee299-143">The edition for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-144">-Force</span><span class="sxs-lookup"><span data-stu-id="ee299-144">-Force</span></span>
<span data-ttu-id="ee299-145">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="ee299-145">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-146">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="ee299-146">-InstancePool</span></span>
<span data-ttu-id="ee299-147">A példánykészlet szülőobjektuma.</span><span class="sxs-lookup"><span data-stu-id="ee299-147">The instance pool parent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: NewByInstancePoolParentObjectParameterSet
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-148">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="ee299-148">-InstancePoolName</span></span>
<span data-ttu-id="ee299-149">Az a példánykészlet, amelybe ezt a példányt el kell helyezze.</span><span class="sxs-lookup"><span data-stu-id="ee299-149">The instance pool to place this instance in.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-150">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="ee299-150">-InstancePoolResourceId</span></span>
<span data-ttu-id="ee299-151">A példánykészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee299-151">The instance pool resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByInstancePoolResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ee299-152">-LicenseType</span></span>
<span data-ttu-id="ee299-153">Meghatározza, hogy melyik licenctípust kell használni.</span><span class="sxs-lookup"><span data-stu-id="ee299-153">Determines which License Type to use.</span></span> <span data-ttu-id="ee299-154">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="ee299-154">Possible values are:</span></span>
- <span data-ttu-id="ee299-155">BasePrice – Azure Hybrid Benefit (AHB) kedvezményes árazás érvényes a meglévő SQL Server-licenctulajdonosokra.</span><span class="sxs-lookup"><span data-stu-id="ee299-155">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="ee299-156">A felügyelt példány szolgáltatására leszámítoljuk a meglévő SQL Server-licenctulajdonosok számára.</span><span class="sxs-lookup"><span data-stu-id="ee299-156">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="ee299-157">LicenseIncluded - Azure Hybrid Benefit (AHB) discounting for existing SQL Server license owners is not applied.</span><span class="sxs-lookup"><span data-stu-id="ee299-157">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="ee299-158">A Felügyelt példány szolgáltatás ára tartalmazni fog egy új SQL Server-licencköltségeket.</span><span class="sxs-lookup"><span data-stu-id="ee299-158">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-159">-Location</span><span class="sxs-lookup"><span data-stu-id="ee299-159">-Location</span></span>
<span data-ttu-id="ee299-160">A példány létrehozásának helye</span><span class="sxs-lookup"><span data-stu-id="ee299-160">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-161">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ee299-161">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="ee299-162">Az Sql Azure Felügyelt példány karbantartási konfigurációs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee299-162">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-163">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ee299-163">-MinimalTlsVersion</span></span>
<span data-ttu-id="ee299-164">A felügyelt példány minimális TLS-verziója</span><span class="sxs-lookup"><span data-stu-id="ee299-164">The minimal TLS version to enforce for Managed instance</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-165">-Name</span><span class="sxs-lookup"><span data-stu-id="ee299-165">-Name</span></span>
<span data-ttu-id="ee299-166">Példány neve.</span><span class="sxs-lookup"><span data-stu-id="ee299-166">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-167">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="ee299-167">-ProxyOverride</span></span>
<span data-ttu-id="ee299-168">A példányhoz való csatlakozáshoz használt kapcsolattípus.</span><span class="sxs-lookup"><span data-stu-id="ee299-168">The connection type used for connecting to the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-169">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="ee299-169">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="ee299-170">A nyilvános adatvégpont engedélyezett-e a példányban.</span><span class="sxs-lookup"><span data-stu-id="ee299-170">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee299-171">-ResourceGroupName</span></span>
<span data-ttu-id="ee299-172">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ee299-172">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-173">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ee299-173">-SkuName</span></span>
<span data-ttu-id="ee299-174">A példány termékváltozatának neve, például "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="ee299-174">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: System.String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-175">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="ee299-175">-StorageSizeInGB</span></span>
<span data-ttu-id="ee299-176">A példányhoz társítható tárterület méretét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ee299-176">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-177">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ee299-177">-SubnetId</span></span>
<span data-ttu-id="ee299-178">A példány létrehozásához használt alhálózati azonosító</span><span class="sxs-lookup"><span data-stu-id="ee299-178">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee299-179">-Tag</span></span>
<span data-ttu-id="ee299-180">A példányhoz társított címkék</span><span class="sxs-lookup"><span data-stu-id="ee299-180">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="ee299-181">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="ee299-181">-TimezoneId</span></span>
<span data-ttu-id="ee299-182">A beállított példány időzóna-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee299-182">The time zone id for the instance to set.</span></span> <span data-ttu-id="ee299-183">Az időzóna-azonosítók listája megjelenik a sys.time_zone_info (Transact-SQL) nézetben.</span><span class="sxs-lookup"><span data-stu-id="ee299-183">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="ee299-184">-VCore</span></span>
<span data-ttu-id="ee299-185">A példányhoz társítható VCore-érték meghatározása</span><span class="sxs-lookup"><span data-stu-id="ee299-185">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee299-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee299-186">-Confirm</span></span>
<span data-ttu-id="ee299-187">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ee299-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee299-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee299-188">-WhatIf</span></span>
<span data-ttu-id="ee299-189">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ee299-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee299-190">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee299-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee299-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee299-191">CommonParameters</span></span>
<span data-ttu-id="ee299-192">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee299-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee299-193">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee299-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee299-194">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee299-194">INPUTS</span></span>

### <span data-ttu-id="ee299-195">Nincs</span><span class="sxs-lookup"><span data-stu-id="ee299-195">None</span></span>

## <span data-ttu-id="ee299-196">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee299-196">OUTPUTS</span></span>

### <span data-ttu-id="ee299-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="ee299-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="ee299-198">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ee299-198">NOTES</span></span>

## <span data-ttu-id="ee299-199">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee299-199">RELATED LINKS</span></span>
