---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: ef809acdf8b78eb0d1203a901b3b44028c79733e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467152"
---
# <span data-ttu-id="ecbfc-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ecbfc-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="ecbfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecbfc-102">SYNOPSIS</span></span>
<span data-ttu-id="ecbfc-103">Létrehoz egy Azure SQL-adatbázis felügyelt példányát.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="ecbfc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ecbfc-104">SYNTAX</span></span>

### <span data-ttu-id="ecbfc-105">NewByEditionAndComputeGenerációParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ecbfc-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecbfc-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecbfc-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecbfc-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecbfc-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecbfc-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="ecbfc-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecbfc-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ecbfc-109">DESCRIPTION</span></span>
<span data-ttu-id="ecbfc-110">A **New-AzSqlInstance** parancsmag létrehoz egy Azure SQL-adatbázis felügyelt példányát.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="ecbfc-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ecbfc-111">EXAMPLES</span></span>

### <span data-ttu-id="ecbfc-112">1. példa: Új példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="ecbfc-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="ecbfc-113">Ez a parancs új példányt hoz létre az SkuName paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="ecbfc-114">2. példa: Új példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="ecbfc-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="ecbfc-115">Ez a parancs új példányt hoz létre a Edition és a ComputeGeneráció paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="ecbfc-116">3. példa: Új példány létrehozása egy példánykészletben egy példánykészlet-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="ecbfc-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="ecbfc-117">Ez a parancs új példányt hoz létre egy példánykészletben egy példánykészlet-objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="ecbfc-118">4. példa: Új példány létrehozása egy példánykészletben egy példánykészlet erőforrás-azonosítójának használatával</span><span class="sxs-lookup"><span data-stu-id="ecbfc-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="ecbfc-119">Ez a parancs új példányt hoz létre egy példánykészletben a példánykészlet erőforrás-azonosítójának használatával.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="ecbfc-120">5. példa: Új példány létrehozása egy példánykészletben</span><span class="sxs-lookup"><span data-stu-id="ecbfc-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="ecbfc-121">Ez a parancs új példányt hoz létre egy példánykészletben, a név instancePool0 névvel</span><span class="sxs-lookup"><span data-stu-id="ecbfc-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="ecbfc-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecbfc-122">PARAMETERS</span></span>

### <span data-ttu-id="ecbfc-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="ecbfc-123">-AdministratorCredential</span></span>
<span data-ttu-id="ecbfc-124">A példány SQL-hitelesítési hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="ecbfc-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecbfc-125">-AsJob</span></span>
<span data-ttu-id="ecbfc-126">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ecbfc-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ecbfc-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ecbfc-127">-AssignIdentity</span></span>
<span data-ttu-id="ecbfc-128">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a Felügyelt példányhoz olyan kulcskezelési szolgáltatásokhoz, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ecbfc-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="ecbfc-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="ecbfc-130">Az Sql Azure Felügyelt példány biztonsági másolatának tárolásához használt biztonsági mentési tárterület redundancia.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="ecbfc-131">Beállítások: Helyi, Zóna és Földrajzi</span><span class="sxs-lookup"><span data-stu-id="ecbfc-131">Options are: Local, Zone and Geo</span></span>

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

### <span data-ttu-id="ecbfc-132">-Collation</span><span class="sxs-lookup"><span data-stu-id="ecbfc-132">-Collation</span></span>
<span data-ttu-id="ecbfc-133">A használt Azure SQL Felügyelt példány szétválogatása.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="ecbfc-134">-ComputeGeneráció</span><span class="sxs-lookup"><span data-stu-id="ecbfc-134">-ComputeGeneration</span></span>
<span data-ttu-id="ecbfc-135">A példány számítási generációja.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-135">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="ecbfc-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecbfc-136">-DefaultProfile</span></span>
<span data-ttu-id="ecbfc-137">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecbfc-138">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="ecbfc-138">-DnsZonePartner</span></span>
<span data-ttu-id="ecbfc-139">A Felügyelt kiszolgáló partner erőforrás-azonosítója, amely örökli a DnsZone tulajdonságot a Felügyelt példány létrehozásához</span><span class="sxs-lookup"><span data-stu-id="ecbfc-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="ecbfc-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="ecbfc-140">-Edition</span></span>
<span data-ttu-id="ecbfc-141">A példány kiadása.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-141">The edition for the instance.</span></span>

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

### <span data-ttu-id="ecbfc-142">-Force</span><span class="sxs-lookup"><span data-stu-id="ecbfc-142">-Force</span></span>
<span data-ttu-id="ecbfc-143">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="ecbfc-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ecbfc-144">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="ecbfc-144">-InstancePool</span></span>
<span data-ttu-id="ecbfc-145">A példánykészlet szülőobjektuma.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-145">The instance pool parent object.</span></span>

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

### <span data-ttu-id="ecbfc-146">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="ecbfc-146">-InstancePoolName</span></span>
<span data-ttu-id="ecbfc-147">Az a példánykészlet, amelybe ezt a példányt el kell helyezze.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-147">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="ecbfc-148">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="ecbfc-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="ecbfc-149">A példánykészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-149">The instance pool resource id.</span></span>

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

### <span data-ttu-id="ecbfc-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ecbfc-150">-LicenseType</span></span>
<span data-ttu-id="ecbfc-151">Meghatározza, hogy melyik licenctípust kell használni.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-151">Determines which License Type to use.</span></span> <span data-ttu-id="ecbfc-152">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="ecbfc-152">Possible values are:</span></span>
- <span data-ttu-id="ecbfc-153">BasePrice – Azure Hybrid Benefit (AHB) kedvezményes árazás érvényes a meglévő SQL Server-licenctulajdonosokra.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="ecbfc-154">A felügyelt példány szolgáltatására leszámítoljuk a meglévő SQL Server-licenctulajdonosok számára.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="ecbfc-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discounting for existing SQL Server license owners is not applied.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="ecbfc-156">A Felügyelt példány szolgáltatás ára tartalmazni fog egy új SQL Server-licencköltségeket.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="ecbfc-157">-Location</span><span class="sxs-lookup"><span data-stu-id="ecbfc-157">-Location</span></span>
<span data-ttu-id="ecbfc-158">A példány létrehozásának helye</span><span class="sxs-lookup"><span data-stu-id="ecbfc-158">The location in which to create the instance</span></span>

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

### <span data-ttu-id="ecbfc-159">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ecbfc-159">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="ecbfc-160">Az Sql Azure Felügyelt példány karbantartási konfigurációs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-160">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="ecbfc-161">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ecbfc-161">-MinimalTlsVersion</span></span>
<span data-ttu-id="ecbfc-162">A felügyelt példány minimális TLS-verziója</span><span class="sxs-lookup"><span data-stu-id="ecbfc-162">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="ecbfc-163">-Name</span><span class="sxs-lookup"><span data-stu-id="ecbfc-163">-Name</span></span>
<span data-ttu-id="ecbfc-164">Példány neve.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-164">Instance name.</span></span>

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

### <span data-ttu-id="ecbfc-165">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="ecbfc-165">-ProxyOverride</span></span>
<span data-ttu-id="ecbfc-166">A példányhoz való csatlakozáshoz használt kapcsolattípus.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-166">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="ecbfc-167">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="ecbfc-167">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="ecbfc-168">A nyilvános adatvégpont engedélyezett-e a példányban.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-168">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="ecbfc-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecbfc-169">-ResourceGroupName</span></span>
<span data-ttu-id="ecbfc-170">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-170">The name of the resource group.</span></span>

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

### <span data-ttu-id="ecbfc-171">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ecbfc-171">-SkuName</span></span>
<span data-ttu-id="ecbfc-172">A példány termékváltozatának neve, például "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="ecbfc-172">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="ecbfc-173">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="ecbfc-173">-StorageSizeInGB</span></span>
<span data-ttu-id="ecbfc-174">A példányhoz társítható tárterület méretét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-174">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="ecbfc-175">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ecbfc-175">-SubnetId</span></span>
<span data-ttu-id="ecbfc-176">A példány létrehozásához használt alhálózati azonosító</span><span class="sxs-lookup"><span data-stu-id="ecbfc-176">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="ecbfc-177">-Tag</span><span class="sxs-lookup"><span data-stu-id="ecbfc-177">-Tag</span></span>
<span data-ttu-id="ecbfc-178">A példányhoz társított címkék</span><span class="sxs-lookup"><span data-stu-id="ecbfc-178">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="ecbfc-179">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="ecbfc-179">-TimezoneId</span></span>
<span data-ttu-id="ecbfc-180">A beállított példány időzóna-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-180">The time zone id for the instance to set.</span></span> <span data-ttu-id="ecbfc-181">Az időzóna-azonosítók listája megjelenik a sys.time_zone_info (Transact-SQL) nézetben.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-181">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="ecbfc-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="ecbfc-182">-VCore</span></span>
<span data-ttu-id="ecbfc-183">A példányhoz társítható VCore-érték meghatározása</span><span class="sxs-lookup"><span data-stu-id="ecbfc-183">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="ecbfc-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecbfc-184">-Confirm</span></span>
<span data-ttu-id="ecbfc-185">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecbfc-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecbfc-186">-WhatIf</span></span>
<span data-ttu-id="ecbfc-187">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecbfc-188">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecbfc-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecbfc-189">CommonParameters</span></span>
<span data-ttu-id="ecbfc-190">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecbfc-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecbfc-191">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecbfc-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecbfc-192">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ecbfc-192">INPUTS</span></span>

### <span data-ttu-id="ecbfc-193">Nincs</span><span class="sxs-lookup"><span data-stu-id="ecbfc-193">None</span></span>

## <span data-ttu-id="ecbfc-194">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecbfc-194">OUTPUTS</span></span>

### <span data-ttu-id="ecbfc-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="ecbfc-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="ecbfc-196">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ecbfc-196">NOTES</span></span>

## <span data-ttu-id="ecbfc-197">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ecbfc-197">RELATED LINKS</span></span>
