---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: a6dd059b7fdab3c2670e3b8902def148d88124d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015862"
---
# <span data-ttu-id="35f5c-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="35f5c-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="35f5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="35f5c-103">Beállítja egy Azure SQL-adatbázis felügyelt példányának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="35f5c-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="35f5c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="35f5c-104">SYNTAX</span></span>

### <span data-ttu-id="35f5c-105">SetInstanceFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="35f5c-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35f5c-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="35f5c-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35f5c-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="35f5c-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35f5c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="35f5c-108">DESCRIPTION</span></span>
<span data-ttu-id="35f5c-109">A **Set-AzSqlInstance** parancsmag módosítja egy Azure SQL-adatbázis felügyelt példányának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="35f5c-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="35f5c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="35f5c-110">EXAMPLES</span></span>

### <span data-ttu-id="35f5c-111">1. példa: Meglévő példány beállítása a -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore és -Edition új értékekkel</span><span class="sxs-lookup"><span data-stu-id="35f5c-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition BusinessCritical
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
InstancePoolName         :
```

### <span data-ttu-id="35f5c-112">2. példa: A meglévő példány hardverének létrehozása a -Compute Generation új érték használatával</span><span class="sxs-lookup"><span data-stu-id="35f5c-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -ComputeGeneration Gen5
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
InstancePoolName         :
```

<span data-ttu-id="35f5c-113">Ez a parancs a -AdministratorPassword, -LicenseType, -StorageSizeInGB és -VCore új értékekkel állítja be a meglévő példányt</span><span class="sxs-lookup"><span data-stu-id="35f5c-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="35f5c-114">3. példa: Meglévő példány beállítása új értékekkel a -AdministratorPassword, -LicenseType, -StorageSizeInGB és -VCore értékekkel egy példánykészleten belül</span><span class="sxs-lookup"><span data-stu-id="35f5c-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolName instancePool0
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
StorageSizeInGB          : 1024
InstancePoolName         : instancePool0
```

<span data-ttu-id="35f5c-115">Ez a parancs a -AdministratorPassword, -LicenseType, -StorageSizeInGB és -VCore értéket használva állítja be a meglévő példányt egy példánykészleten belül</span><span class="sxs-lookup"><span data-stu-id="35f5c-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

### <span data-ttu-id="35f5c-116">4. példa: A meglévő példány karbantartási konfigurációjának frissítése</span><span class="sxs-lookup"><span data-stu-id="35f5c-116">Example 4: Update maintenance configuration for existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
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

<span data-ttu-id="35f5c-117">Ez a parancs karbantartási beállításokkal frissíti a meglévő példányt MI_2</span><span class="sxs-lookup"><span data-stu-id="35f5c-117">This command updates existing instance with maintenance configuration MI_2</span></span>

### <span data-ttu-id="35f5c-118">5. példa: A karbantartási konfiguráció eltávolítása a meglévő példányból</span><span class="sxs-lookup"><span data-stu-id="35f5c-118">Example 5: Remove maintenance configuration from existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managediInstance1" -ResourceGroupName "Resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default"
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
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default
```

<span data-ttu-id="35f5c-119">Ez a parancs alaphelyzetbe állítja a karbantartási konfigurációt a meglévő példány alapértelmezett beállítására</span><span class="sxs-lookup"><span data-stu-id="35f5c-119">This command resets maintenance configuration to default for existing instance</span></span>

## <span data-ttu-id="35f5c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35f5c-120">PARAMETERS</span></span>

### <span data-ttu-id="35f5c-121">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="35f5c-121">-AdministratorPassword</span></span>
<span data-ttu-id="35f5c-122">A példány új SQL-rendszergazdai jelszava.</span><span class="sxs-lookup"><span data-stu-id="35f5c-122">The new SQL administrator password for the instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f5c-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35f5c-123">-AsJob</span></span>
<span data-ttu-id="35f5c-124">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="35f5c-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35f5c-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="35f5c-125">-AssignIdentity</span></span>
<span data-ttu-id="35f5c-126">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a példányhoz olyan kulcskezelő szolgáltatásokhoz, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="35f5c-126">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="35f5c-127">-ComputeGeneráció</span><span class="sxs-lookup"><span data-stu-id="35f5c-127">-ComputeGeneration</span></span>
<span data-ttu-id="35f5c-128">A példány számítási generációja.</span><span class="sxs-lookup"><span data-stu-id="35f5c-128">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="35f5c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f5c-129">-DefaultProfile</span></span>
<span data-ttu-id="35f5c-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35f5c-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35f5c-131">-Edition</span><span class="sxs-lookup"><span data-stu-id="35f5c-131">-Edition</span></span>
<span data-ttu-id="35f5c-132">A példányhoz hozzárendelni megfelelő kiadás.</span><span class="sxs-lookup"><span data-stu-id="35f5c-132">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="35f5c-133">-Force</span><span class="sxs-lookup"><span data-stu-id="35f5c-133">-Force</span></span>
<span data-ttu-id="35f5c-134">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="35f5c-134">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="35f5c-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35f5c-135">-InputObject</span></span>
<span data-ttu-id="35f5c-136">Az eltávolítható AzureSqlManagedInstanceModel objektum</span><span class="sxs-lookup"><span data-stu-id="35f5c-136">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35f5c-137">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="35f5c-137">-InstancePoolName</span></span>
<span data-ttu-id="35f5c-138">A példánykészlet neve.</span><span class="sxs-lookup"><span data-stu-id="35f5c-138">The instance pool name.</span></span>

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

### <span data-ttu-id="35f5c-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="35f5c-139">-LicenseType</span></span>
<span data-ttu-id="35f5c-140">Meghatározza, hogy melyik licenctípust kell használni.</span><span class="sxs-lookup"><span data-stu-id="35f5c-140">Determines which License Type to use.</span></span> <span data-ttu-id="35f5c-141">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="35f5c-141">Possible values are:</span></span>
- <span data-ttu-id="35f5c-142">BasePrice – Azure Hybrid Benefit (AHB) kedvezményes árazás érvényes a meglévő SQL Server-licenctulajdonosokra.</span><span class="sxs-lookup"><span data-stu-id="35f5c-142">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="35f5c-143">A felügyelt példány szolgáltatására leszámítoljuk a meglévő SQL Server-licenctulajdonosok számára.</span><span class="sxs-lookup"><span data-stu-id="35f5c-143">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="35f5c-144">LicenseIncluded - Azure Hybrid Benefit (AHB) discounting for existing SQL Server license owners is not applied.</span><span class="sxs-lookup"><span data-stu-id="35f5c-144">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="35f5c-145">A Felügyelt példány szolgáltatás ára tartalmazni fog egy új SQL Server-licencköltségeket.</span><span class="sxs-lookup"><span data-stu-id="35f5c-145">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="35f5c-146">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="35f5c-146">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="35f5c-147">Az Sql Azure Felügyelt példány karbantartási konfigurációs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="35f5c-147">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="35f5c-148">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="35f5c-148">-MinimalTlsVersion</span></span>
<span data-ttu-id="35f5c-149">A felügyelt példány minimális TLS-verziója</span><span class="sxs-lookup"><span data-stu-id="35f5c-149">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="35f5c-150">-Name</span><span class="sxs-lookup"><span data-stu-id="35f5c-150">-Name</span></span>
<span data-ttu-id="35f5c-151">Példány neve.</span><span class="sxs-lookup"><span data-stu-id="35f5c-151">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f5c-152">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="35f5c-152">-ProxyOverride</span></span>
<span data-ttu-id="35f5c-153">A példányhoz való csatlakozáshoz használt kapcsolattípus.</span><span class="sxs-lookup"><span data-stu-id="35f5c-153">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="35f5c-154">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="35f5c-154">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="35f5c-155">A nyilvános adatvégpont engedélyezett-e a példányban.</span><span class="sxs-lookup"><span data-stu-id="35f5c-155">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f5c-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f5c-156">-ResourceGroupName</span></span>
<span data-ttu-id="35f5c-157">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="35f5c-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f5c-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35f5c-158">-ResourceId</span></span>
<span data-ttu-id="35f5c-159">Az eltávolítható példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="35f5c-159">The resource id of instance to remove</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f5c-160">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="35f5c-160">-StorageSizeInGB</span></span>
<span data-ttu-id="35f5c-161">A példányhoz társítható tárterület méretét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="35f5c-161">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f5c-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="35f5c-162">-Tag</span></span>
<span data-ttu-id="35f5c-163">A példányhoz társított címkék.</span><span class="sxs-lookup"><span data-stu-id="35f5c-163">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="35f5c-164">-VCore</span><span class="sxs-lookup"><span data-stu-id="35f5c-164">-VCore</span></span>
<span data-ttu-id="35f5c-165">A példányhoz társítható VCore-érték meghatározása</span><span class="sxs-lookup"><span data-stu-id="35f5c-165">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f5c-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35f5c-166">-Confirm</span></span>
<span data-ttu-id="35f5c-167">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="35f5c-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35f5c-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35f5c-168">-WhatIf</span></span>
<span data-ttu-id="35f5c-169">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="35f5c-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35f5c-170">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35f5c-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35f5c-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f5c-171">CommonParameters</span></span>
<span data-ttu-id="35f5c-172">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35f5c-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f5c-173">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35f5c-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f5c-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35f5c-174">INPUTS</span></span>

### <span data-ttu-id="35f5c-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="35f5c-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="35f5c-176">System.String</span><span class="sxs-lookup"><span data-stu-id="35f5c-176">System.String</span></span>

## <span data-ttu-id="35f5c-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35f5c-177">OUTPUTS</span></span>

### <span data-ttu-id="35f5c-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="35f5c-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="35f5c-179">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="35f5c-179">NOTES</span></span>

## <span data-ttu-id="35f5c-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35f5c-180">RELATED LINKS</span></span>
