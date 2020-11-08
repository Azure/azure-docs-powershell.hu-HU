---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bb9ae3ba225c67a98b6c3588e1dc0c63f02170ae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024355"
---
# <span data-ttu-id="3eb72-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3eb72-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="3eb72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3eb72-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb72-103">Azure SQL-adatbázishoz tartozó felügyelt példány létrehozása.</span><span class="sxs-lookup"><span data-stu-id="3eb72-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="3eb72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3eb72-104">SYNTAX</span></span>

### <span data-ttu-id="3eb72-105">NewByEditionAndComputeGenerationParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3eb72-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eb72-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3eb72-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eb72-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3eb72-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eb72-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="3eb72-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eb72-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="3eb72-109">DESCRIPTION</span></span>
<span data-ttu-id="3eb72-110">A **New-AzSqlInstance** parancsmag létrehoz egy Azure SQL-adatbázis felügyelt példányát.</span><span class="sxs-lookup"><span data-stu-id="3eb72-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="3eb72-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3eb72-111">EXAMPLES</span></span>

### <span data-ttu-id="3eb72-112">Példa 1: új példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="3eb72-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="3eb72-113">Ez a parancs új példányt hoz létre a SkuName paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="3eb72-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="3eb72-114">2. példa: új példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="3eb72-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="3eb72-115">Ezzel a paranccsal új példányt hozhat létre a kiadási és az ComputeGeneration paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="3eb72-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="3eb72-116">3. példa: új példány létrehozása egy példányban egy példány Pool-objektummal</span><span class="sxs-lookup"><span data-stu-id="3eb72-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="3eb72-117">Ez a parancs egy új példányt hoz létre egy példányban egy példány Pool-objektummal.</span><span class="sxs-lookup"><span data-stu-id="3eb72-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="3eb72-118">Példa 4: új példány létrehozása egy példányban egy példány erőforráskészlet-erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="3eb72-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="3eb72-119">Ez a parancs egy új példányt hoz létre egy példányban a példány-alkalmazáskészlet erőforrás-azonosítójának használatával.</span><span class="sxs-lookup"><span data-stu-id="3eb72-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="3eb72-120">Példa 5: új példány létrehozása egy példány-készletben</span><span class="sxs-lookup"><span data-stu-id="3eb72-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="3eb72-121">A parancs új példányt hoz létre egy instancePool0 nevű példányban.</span><span class="sxs-lookup"><span data-stu-id="3eb72-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="3eb72-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3eb72-122">PARAMETERS</span></span>

### <span data-ttu-id="3eb72-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="3eb72-123">-AdministratorCredential</span></span>
<span data-ttu-id="3eb72-124">A példány SQL-hitelesítési hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="3eb72-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="3eb72-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3eb72-125">-AsJob</span></span>
<span data-ttu-id="3eb72-126">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3eb72-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3eb72-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3eb72-127">-AssignIdentity</span></span>
<span data-ttu-id="3eb72-128">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást ehhez a felügyelt példányhoz, amely a kulcskezelő szolgáltatásokhoz (például Azure-tároló) használható.</span><span class="sxs-lookup"><span data-stu-id="3eb72-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="3eb72-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="3eb72-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="3eb72-130">Az SQL Azure-alapú felügyelt példány biztonsági másolatainak tárolásához használt biztonsági másolat.</span><span class="sxs-lookup"><span data-stu-id="3eb72-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="3eb72-131">A beállítások: helyi, zóna és geo</span><span class="sxs-lookup"><span data-stu-id="3eb72-131">Options are: Local, Zone and Geo</span></span>

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

### <span data-ttu-id="3eb72-132">-Szétválogatás</span><span class="sxs-lookup"><span data-stu-id="3eb72-132">-Collation</span></span>
<span data-ttu-id="3eb72-133">A használni kívánt Azure SQL-példány egybevetése.</span><span class="sxs-lookup"><span data-stu-id="3eb72-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="3eb72-134">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="3eb72-134">-ComputeGeneration</span></span>
<span data-ttu-id="3eb72-135">A példány számítási generációja.</span><span class="sxs-lookup"><span data-stu-id="3eb72-135">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="3eb72-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb72-136">-DefaultProfile</span></span>
<span data-ttu-id="3eb72-137">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3eb72-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eb72-138">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="3eb72-138">-DnsZonePartner</span></span>
<span data-ttu-id="3eb72-139">A felügyelt példány létrehozásakor örökölt DnsZone tulajdonságot örökölő erőforráspartner-kiszolgáló erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3eb72-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="3eb72-140">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="3eb72-140">-Edition</span></span>
<span data-ttu-id="3eb72-141">A példány kiadását.</span><span class="sxs-lookup"><span data-stu-id="3eb72-141">The edition for the instance.</span></span>

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

### <span data-ttu-id="3eb72-142">-Force</span><span class="sxs-lookup"><span data-stu-id="3eb72-142">-Force</span></span>
<span data-ttu-id="3eb72-143">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="3eb72-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3eb72-144">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="3eb72-144">-InstancePool</span></span>
<span data-ttu-id="3eb72-145">A példány Pool szülő objektuma.</span><span class="sxs-lookup"><span data-stu-id="3eb72-145">The instance pool parent object.</span></span>

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

### <span data-ttu-id="3eb72-146">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="3eb72-146">-InstancePoolName</span></span>
<span data-ttu-id="3eb72-147">A példány, ahová a példányt be szeretné szúrni.</span><span class="sxs-lookup"><span data-stu-id="3eb72-147">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="3eb72-148">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="3eb72-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="3eb72-149">A példány-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3eb72-149">The instance pool resource id.</span></span>

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

### <span data-ttu-id="3eb72-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3eb72-150">-LicenseType</span></span>
<span data-ttu-id="3eb72-151">Meghatározza, hogy melyik licenc-típust szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="3eb72-151">Determines which License Type to use.</span></span> <span data-ttu-id="3eb72-152">A lehetséges értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="3eb72-152">Possible values are:</span></span>
- <span data-ttu-id="3eb72-153">BasePrice – Azure hibrid haszon (AHB) a meglévő SQL Server-licenccel rendelkező tulajdonosok kedvezményes árait alkalmazzák.</span><span class="sxs-lookup"><span data-stu-id="3eb72-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="3eb72-154">A felügyelt példányok szolgáltatási ára a meglévő SQL Server-licenccel rendelkező tulajdonosok esetében diszkontálva lesz.</span><span class="sxs-lookup"><span data-stu-id="3eb72-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="3eb72-155">A LicenseIncluded-Azure Hybrid haszon (AHB) árengedménye nem érvényes a meglévő SQL Server-licenccel rendelkező tulajdonosok esetében.</span><span class="sxs-lookup"><span data-stu-id="3eb72-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="3eb72-156">A felügyelt példány szolgáltatás ára tartalmazni fog egy új SQL Server-licenc költségeit.</span><span class="sxs-lookup"><span data-stu-id="3eb72-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="3eb72-157">-Hely</span><span class="sxs-lookup"><span data-stu-id="3eb72-157">-Location</span></span>
<span data-ttu-id="3eb72-158">A példány létrehozásának helye</span><span class="sxs-lookup"><span data-stu-id="3eb72-158">The location in which to create the instance</span></span>

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

### <span data-ttu-id="3eb72-159">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3eb72-159">-MinimalTlsVersion</span></span>
<span data-ttu-id="3eb72-160">A felügyelt példány érvényesítéséhez szükséges minimális TLS-verzió</span><span class="sxs-lookup"><span data-stu-id="3eb72-160">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="3eb72-161">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3eb72-161">-Name</span></span>
<span data-ttu-id="3eb72-162">Példány neve.</span><span class="sxs-lookup"><span data-stu-id="3eb72-162">Instance name.</span></span>

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

### <span data-ttu-id="3eb72-163">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="3eb72-163">-ProxyOverride</span></span>
<span data-ttu-id="3eb72-164">A példányhoz való csatlakozáshoz használt kapcsolattípus.</span><span class="sxs-lookup"><span data-stu-id="3eb72-164">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="3eb72-165">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="3eb72-165">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="3eb72-166">Megadja, hogy engedélyezve van-e a nyilvános adatvégpont a példányhoz.</span><span class="sxs-lookup"><span data-stu-id="3eb72-166">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="3eb72-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb72-167">-ResourceGroupName</span></span>
<span data-ttu-id="3eb72-168">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3eb72-168">The name of the resource group.</span></span>

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

### <span data-ttu-id="3eb72-169">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3eb72-169">-SkuName</span></span>
<span data-ttu-id="3eb72-170">A példány SKU-neve (például "GP_Gen4", "BC_Gen4").</span><span class="sxs-lookup"><span data-stu-id="3eb72-170">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="3eb72-171">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="3eb72-171">-StorageSizeInGB</span></span>
<span data-ttu-id="3eb72-172">Azt határozza meg, hogy mekkora tárterületet társíthat a példányhoz</span><span class="sxs-lookup"><span data-stu-id="3eb72-172">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="3eb72-173">– NetI</span><span class="sxs-lookup"><span data-stu-id="3eb72-173">-SubnetId</span></span>
<span data-ttu-id="3eb72-174">A példány létrehozásához használandó alhálózat-azonosító</span><span class="sxs-lookup"><span data-stu-id="3eb72-174">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="3eb72-175">-Címke</span><span class="sxs-lookup"><span data-stu-id="3eb72-175">-Tag</span></span>
<span data-ttu-id="3eb72-176">A példánnyal társítani kívánt Címkék</span><span class="sxs-lookup"><span data-stu-id="3eb72-176">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="3eb72-177">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="3eb72-177">-TimezoneId</span></span>
<span data-ttu-id="3eb72-178">A beállítani kívánt példány időzóna-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3eb72-178">The time zone id for the instance to set.</span></span> <span data-ttu-id="3eb72-179">Az időzóna-azonosítók listája a sys.time_zone_info (Transact-SQL) nézetben van kitéve.</span><span class="sxs-lookup"><span data-stu-id="3eb72-179">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="3eb72-180">-VCore</span><span class="sxs-lookup"><span data-stu-id="3eb72-180">-VCore</span></span>
<span data-ttu-id="3eb72-181">Meghatározza, hogy mennyi VCore társítson a példányhoz</span><span class="sxs-lookup"><span data-stu-id="3eb72-181">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="3eb72-182">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3eb72-182">-Confirm</span></span>
<span data-ttu-id="3eb72-183">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3eb72-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eb72-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb72-184">-WhatIf</span></span>
<span data-ttu-id="3eb72-185">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3eb72-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eb72-186">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3eb72-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eb72-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb72-187">CommonParameters</span></span>
<span data-ttu-id="3eb72-188">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3eb72-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb72-189">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3eb72-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb72-190">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3eb72-190">INPUTS</span></span>

### <span data-ttu-id="3eb72-191">Nincs</span><span class="sxs-lookup"><span data-stu-id="3eb72-191">None</span></span>

## <span data-ttu-id="3eb72-192">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3eb72-192">OUTPUTS</span></span>

### <span data-ttu-id="3eb72-193">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="3eb72-193">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="3eb72-194">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3eb72-194">NOTES</span></span>

## <span data-ttu-id="3eb72-195">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3eb72-195">RELATED LINKS</span></span>
