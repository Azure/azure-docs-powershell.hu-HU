---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: f16e6f2dcbcf3ebd16926784ca84eef02740df7b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163195"
---
# <span data-ttu-id="4713b-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4713b-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="4713b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4713b-102">SYNOPSIS</span></span>
<span data-ttu-id="4713b-103">Beállítja egy Azure SQL-adatbázis felügyelt példányának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="4713b-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="4713b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4713b-104">SYNTAX</span></span>

### <span data-ttu-id="4713b-105">SetInstanceFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4713b-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4713b-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="4713b-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4713b-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="4713b-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4713b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4713b-108">DESCRIPTION</span></span>
<span data-ttu-id="4713b-109">A **Set-AzSqlInstance** parancsmag módosítja egy Azure SQL-adatbázis felügyelt példányának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="4713b-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="4713b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4713b-110">EXAMPLES</span></span>

### <span data-ttu-id="4713b-111">1. példa: Meglévő példány beállítása a -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore és -Edition új értékekkel</span><span class="sxs-lookup"><span data-stu-id="4713b-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="4713b-112">2. példa: A meglévő példány hardverének létrehozása a -Compute Generation új érték használatával</span><span class="sxs-lookup"><span data-stu-id="4713b-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="4713b-113">Ez a parancs a -AdministratorPassword, -LicenseType, -StorageSizeInGB és -VCore új értékekkel állítja be a meglévő példányt</span><span class="sxs-lookup"><span data-stu-id="4713b-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="4713b-114">3. példa: Meglévő példány beállítása új értékekkel a -AdministratorPassword, -LicenseType, -StorageSizeInGB és -VCore értékekkel egy példánykészleten belül</span><span class="sxs-lookup"><span data-stu-id="4713b-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="4713b-115">Ez a parancs a -AdministratorPassword, -LicenseType, -StorageSizeInGB és -VCore értéket használva állítja be a meglévő példányt egy példánykészleten belül</span><span class="sxs-lookup"><span data-stu-id="4713b-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="4713b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4713b-116">PARAMETERS</span></span>

### <span data-ttu-id="4713b-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="4713b-117">-AdministratorPassword</span></span>
<span data-ttu-id="4713b-118">A példány új SQL-rendszergazdai jelszava.</span><span class="sxs-lookup"><span data-stu-id="4713b-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="4713b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4713b-119">-AsJob</span></span>
<span data-ttu-id="4713b-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4713b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4713b-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4713b-121">-AssignIdentity</span></span>
<span data-ttu-id="4713b-122">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a példányhoz olyan kulcskezelő szolgáltatásokhoz, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="4713b-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="4713b-123">-ComputeGeneráció</span><span class="sxs-lookup"><span data-stu-id="4713b-123">-ComputeGeneration</span></span>
<span data-ttu-id="4713b-124">A példány számítási generációja.</span><span class="sxs-lookup"><span data-stu-id="4713b-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="4713b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4713b-125">-DefaultProfile</span></span>
<span data-ttu-id="4713b-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4713b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4713b-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="4713b-127">-Edition</span></span>
<span data-ttu-id="4713b-128">A példányhoz hozzárendelni megfelelő kiadás.</span><span class="sxs-lookup"><span data-stu-id="4713b-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="4713b-129">-Force</span><span class="sxs-lookup"><span data-stu-id="4713b-129">-Force</span></span>
<span data-ttu-id="4713b-130">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="4713b-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="4713b-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4713b-131">-InputObject</span></span>
<span data-ttu-id="4713b-132">Az eltávolítható AzureSqlManagedInstanceModel objektum</span><span class="sxs-lookup"><span data-stu-id="4713b-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="4713b-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="4713b-133">-InstancePoolName</span></span>
<span data-ttu-id="4713b-134">A példánykészlet neve.</span><span class="sxs-lookup"><span data-stu-id="4713b-134">The instance pool name.</span></span>

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

### <span data-ttu-id="4713b-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4713b-135">-LicenseType</span></span>
<span data-ttu-id="4713b-136">Meghatározza, hogy melyik licenctípust kell használni.</span><span class="sxs-lookup"><span data-stu-id="4713b-136">Determines which License Type to use.</span></span> <span data-ttu-id="4713b-137">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="4713b-137">Possible values are:</span></span>
- <span data-ttu-id="4713b-138">BasePrice – Azure Hybrid Benefit (AHB) kedvezményes árazás érvényes a meglévő SQL Server-licenctulajdonosokra.</span><span class="sxs-lookup"><span data-stu-id="4713b-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="4713b-139">A felügyelt példány szolgáltatására leszámítoljuk a meglévő SQL Server-licenctulajdonosok számára.</span><span class="sxs-lookup"><span data-stu-id="4713b-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="4713b-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discounting for existing SQL Server license owners is not applied.</span><span class="sxs-lookup"><span data-stu-id="4713b-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="4713b-141">A Felügyelt példány szolgáltatás ára tartalmazni fog egy új SQL Server-licencköltségeket.</span><span class="sxs-lookup"><span data-stu-id="4713b-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="4713b-142">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4713b-142">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="4713b-143">Az Sql Azure Felügyelt példány karbantartási konfigurációs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4713b-143">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="4713b-144">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="4713b-144">-MinimalTlsVersion</span></span>
<span data-ttu-id="4713b-145">A felügyelt példány minimális TLS-verziója</span><span class="sxs-lookup"><span data-stu-id="4713b-145">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="4713b-146">-Name</span><span class="sxs-lookup"><span data-stu-id="4713b-146">-Name</span></span>
<span data-ttu-id="4713b-147">Példány neve.</span><span class="sxs-lookup"><span data-stu-id="4713b-147">Instance name.</span></span>

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

### <span data-ttu-id="4713b-148">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="4713b-148">-ProxyOverride</span></span>
<span data-ttu-id="4713b-149">A példányhoz való csatlakozáshoz használt kapcsolattípus.</span><span class="sxs-lookup"><span data-stu-id="4713b-149">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="4713b-150">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="4713b-150">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="4713b-151">A nyilvános adatvégpont engedélyezett-e a példányban.</span><span class="sxs-lookup"><span data-stu-id="4713b-151">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="4713b-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4713b-152">-ResourceGroupName</span></span>
<span data-ttu-id="4713b-153">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4713b-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="4713b-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4713b-154">-ResourceId</span></span>
<span data-ttu-id="4713b-155">Az eltávolítható példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4713b-155">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="4713b-156">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="4713b-156">-StorageSizeInGB</span></span>
<span data-ttu-id="4713b-157">A példányhoz társítható tárterület méretét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4713b-157">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="4713b-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="4713b-158">-Tag</span></span>
<span data-ttu-id="4713b-159">A példányhoz társított címkék.</span><span class="sxs-lookup"><span data-stu-id="4713b-159">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="4713b-160">-VCore</span><span class="sxs-lookup"><span data-stu-id="4713b-160">-VCore</span></span>
<span data-ttu-id="4713b-161">A példányhoz társítható VCore-érték meghatározása</span><span class="sxs-lookup"><span data-stu-id="4713b-161">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="4713b-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4713b-162">-Confirm</span></span>
<span data-ttu-id="4713b-163">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4713b-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4713b-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4713b-164">-WhatIf</span></span>
<span data-ttu-id="4713b-165">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4713b-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4713b-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4713b-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4713b-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4713b-167">CommonParameters</span></span>
<span data-ttu-id="4713b-168">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4713b-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4713b-169">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4713b-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4713b-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4713b-170">INPUTS</span></span>

### <span data-ttu-id="4713b-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="4713b-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="4713b-172">System.String</span><span class="sxs-lookup"><span data-stu-id="4713b-172">System.String</span></span>

## <span data-ttu-id="4713b-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4713b-173">OUTPUTS</span></span>

### <span data-ttu-id="4713b-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="4713b-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="4713b-175">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4713b-175">NOTES</span></span>

## <span data-ttu-id="4713b-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4713b-176">RELATED LINKS</span></span>
