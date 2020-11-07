---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: d80e6ddd7fa420b07a0df30c2718d9c4e96123fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839414"
---
# <span data-ttu-id="9b6f9-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9b6f9-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="9b6f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b6f9-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6f9-103">Azure SQL-adatbázishoz tartozó felügyelt példány létrehozása.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="9b6f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b6f9-104">SYNTAX</span></span>

### <span data-ttu-id="9b6f9-105">NewByEditionAndComputeGenerationParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b6f9-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b6f9-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b6f9-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b6f9-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b6f9-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b6f9-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="9b6f9-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b6f9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b6f9-109">DESCRIPTION</span></span>
<span data-ttu-id="9b6f9-110">A **New-AzSqlInstance** parancsmag létrehoz egy Azure SQL-adatbázis felügyelt példányát.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="9b6f9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9b6f9-111">EXAMPLES</span></span>

### <span data-ttu-id="9b6f9-112">Példa 1: új példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="9b6f9-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="9b6f9-113">Ez a parancs új példányt hoz létre a SkuName paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="9b6f9-114">2. példa: új példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="9b6f9-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="9b6f9-115">Ezzel a paranccsal új példányt hozhat létre a kiadási és az ComputeGeneration paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="9b6f9-116">3. példa: új példány létrehozása egy példányban egy példány Pool-objektummal</span><span class="sxs-lookup"><span data-stu-id="9b6f9-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="9b6f9-117">Ez a parancs egy új példányt hoz létre egy példányban egy példány Pool-objektummal.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="9b6f9-118">Példa 4: új példány létrehozása egy példányban egy példány erőforráskészlet-erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="9b6f9-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="9b6f9-119">Ez a parancs egy új példányt hoz létre egy példányban a példány-alkalmazáskészlet erőforrás-azonosítójának használatával.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="9b6f9-120">Példa 5: új példány létrehozása egy példány-készletben</span><span class="sxs-lookup"><span data-stu-id="9b6f9-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="9b6f9-121">A parancs új példányt hoz létre egy instancePool0 nevű példányban.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="9b6f9-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b6f9-122">PARAMETERS</span></span>

### <span data-ttu-id="9b6f9-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="9b6f9-123">-AdministratorCredential</span></span>
<span data-ttu-id="9b6f9-124">A példány SQL-hitelesítési hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="9b6f9-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b6f9-125">-AsJob</span></span>
<span data-ttu-id="9b6f9-126">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9b6f9-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b6f9-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9b6f9-127">-AssignIdentity</span></span>
<span data-ttu-id="9b6f9-128">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást ehhez a felügyelt példányhoz, amely a kulcskezelő szolgáltatásokhoz (például Azure-tároló) használható.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="9b6f9-129">-Szétválogatás</span><span class="sxs-lookup"><span data-stu-id="9b6f9-129">-Collation</span></span>
<span data-ttu-id="9b6f9-130">A használni kívánt Azure SQL-példány egybevetése.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-130">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="9b6f9-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="9b6f9-131">-ComputeGeneration</span></span>
<span data-ttu-id="9b6f9-132">A példány számítási generációja.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-132">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="9b6f9-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6f9-133">-DefaultProfile</span></span>
<span data-ttu-id="9b6f9-134">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b6f9-135">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="9b6f9-135">-DnsZonePartner</span></span>
<span data-ttu-id="9b6f9-136">A felügyelt példány létrehozásakor örökölt DnsZone tulajdonságot örökölő erőforráspartner-kiszolgáló erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="9b6f9-136">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="9b6f9-137">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="9b6f9-137">-Edition</span></span>
<span data-ttu-id="9b6f9-138">A példány kiadását.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-138">The edition for the instance.</span></span>

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

### <span data-ttu-id="9b6f9-139">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="9b6f9-139">-InstancePool</span></span>
<span data-ttu-id="9b6f9-140">A példány Pool szülő objektuma.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-140">The instance pool parent object.</span></span>

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

### <span data-ttu-id="9b6f9-141">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="9b6f9-141">-InstancePoolName</span></span>
<span data-ttu-id="9b6f9-142">A példány, ahová a példányt be szeretné szúrni.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-142">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="9b6f9-143">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="9b6f9-143">-InstancePoolResourceId</span></span>
<span data-ttu-id="9b6f9-144">A példány-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-144">The instance pool resource id.</span></span>

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

### <span data-ttu-id="9b6f9-145">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9b6f9-145">-LicenseType</span></span>
<span data-ttu-id="9b6f9-146">Meghatározza, hogy melyik licenc-típust szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-146">Determines which License Type to use.</span></span> <span data-ttu-id="9b6f9-147">A lehetséges értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="9b6f9-147">Possible values are:</span></span>
- <span data-ttu-id="9b6f9-148">BasePrice – Azure hibrid haszon (AHB) a meglévő SQL Server-licenccel rendelkező tulajdonosok kedvezményes árait alkalmazzák.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-148">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="9b6f9-149">A felügyelt példányok szolgáltatási ára a meglévő SQL Server-licenccel rendelkező tulajdonosok esetében diszkontálva lesz.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-149">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="9b6f9-150">A LicenseIncluded-Azure Hybrid haszon (AHB) árengedménye nem érvényes a meglévő SQL Server-licenccel rendelkező tulajdonosok esetében.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-150">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="9b6f9-151">A felügyelt példány szolgáltatás ára tartalmazni fog egy új SQL Server-licenc költségeit.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-151">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="9b6f9-152">-Hely</span><span class="sxs-lookup"><span data-stu-id="9b6f9-152">-Location</span></span>
<span data-ttu-id="9b6f9-153">A példány létrehozásának helye</span><span class="sxs-lookup"><span data-stu-id="9b6f9-153">The location in which to create the instance</span></span>

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

### <span data-ttu-id="9b6f9-154">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9b6f9-154">-Name</span></span>
<span data-ttu-id="9b6f9-155">Példány neve.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-155">Instance name.</span></span>

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

### <span data-ttu-id="9b6f9-156">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="9b6f9-156">-ProxyOverride</span></span>
<span data-ttu-id="9b6f9-157">A példányhoz való csatlakozáshoz használt kapcsolattípus.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-157">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="9b6f9-158">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="9b6f9-158">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="9b6f9-159">Megadja, hogy engedélyezve van-e a nyilvános adatvégpont a példányhoz.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-159">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="9b6f9-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b6f9-160">-ResourceGroupName</span></span>
<span data-ttu-id="9b6f9-161">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-161">The name of the resource group.</span></span>

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

### <span data-ttu-id="9b6f9-162">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9b6f9-162">-SkuName</span></span>
<span data-ttu-id="9b6f9-163">A példány SKU-neve (például "GP_Gen4", "BC_Gen4").</span><span class="sxs-lookup"><span data-stu-id="9b6f9-163">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="9b6f9-164">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="9b6f9-164">-StorageSizeInGB</span></span>
<span data-ttu-id="9b6f9-165">Azt határozza meg, hogy mekkora tárterületet társíthat a példányhoz</span><span class="sxs-lookup"><span data-stu-id="9b6f9-165">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="9b6f9-166">– NetI</span><span class="sxs-lookup"><span data-stu-id="9b6f9-166">-SubnetId</span></span>
<span data-ttu-id="9b6f9-167">A példány létrehozásához használandó alhálózat-azonosító</span><span class="sxs-lookup"><span data-stu-id="9b6f9-167">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="9b6f9-168">-Címke</span><span class="sxs-lookup"><span data-stu-id="9b6f9-168">-Tag</span></span>
<span data-ttu-id="9b6f9-169">A példánnyal társítani kívánt Címkék</span><span class="sxs-lookup"><span data-stu-id="9b6f9-169">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="9b6f9-170">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="9b6f9-170">-TimezoneId</span></span>
<span data-ttu-id="9b6f9-171">A beállítani kívánt példány időzóna-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-171">The time zone id for the instance to set.</span></span> <span data-ttu-id="9b6f9-172">Az időzóna-azonosítók listája a sys.time_zone_info (Transact-SQL) nézetben van kitéve.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-172">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="9b6f9-173">-VCore</span><span class="sxs-lookup"><span data-stu-id="9b6f9-173">-VCore</span></span>
<span data-ttu-id="9b6f9-174">Meghatározza, hogy mennyi VCore társítson a példányhoz</span><span class="sxs-lookup"><span data-stu-id="9b6f9-174">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="9b6f9-175">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9b6f9-175">-Confirm</span></span>
<span data-ttu-id="9b6f9-176">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b6f9-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b6f9-177">-WhatIf</span></span>
<span data-ttu-id="9b6f9-178">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b6f9-179">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b6f9-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6f9-180">CommonParameters</span></span>
<span data-ttu-id="9b6f9-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b6f9-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6f9-182">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9b6f9-182">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6f9-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b6f9-183">INPUTS</span></span>

### <span data-ttu-id="9b6f9-184">Nincs</span><span class="sxs-lookup"><span data-stu-id="9b6f9-184">None</span></span>

## <span data-ttu-id="9b6f9-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b6f9-185">OUTPUTS</span></span>

### <span data-ttu-id="9b6f9-186">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="9b6f9-186">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="9b6f9-187">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b6f9-187">NOTES</span></span>

## <span data-ttu-id="9b6f9-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b6f9-188">RELATED LINKS</span></span>
