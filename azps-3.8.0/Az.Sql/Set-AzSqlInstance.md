---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: e17c6b226f7ed4fe17842c93d03828d53c0bb22c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845173"
---
# <span data-ttu-id="376ef-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="376ef-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="376ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="376ef-102">SYNOPSIS</span></span>
<span data-ttu-id="376ef-103">Az Azure SQL-adatbázis felügyelt példányának tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="376ef-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="376ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="376ef-104">SYNTAX</span></span>

### <span data-ttu-id="376ef-105">SetInstanceFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="376ef-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="376ef-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="376ef-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="376ef-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="376ef-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="376ef-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="376ef-108">DESCRIPTION</span></span>
<span data-ttu-id="376ef-109">A **set-AzSqlInstance** parancsmag egy Azure SQL-adatbázis felügyelt példányának tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="376ef-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="376ef-110">Példák</span><span class="sxs-lookup"><span data-stu-id="376ef-110">EXAMPLES</span></span>

### <span data-ttu-id="376ef-111">1. példa: a meglévő példány beállítása új AdministratorPassword,-LicenseType,-StorageSizeInGB,-VCore és-kiadásban.</span><span class="sxs-lookup"><span data-stu-id="376ef-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="376ef-112">2. példa: a meglévő példány hardver-generálásának módosítása új ComputeGeneration-érték használatával</span><span class="sxs-lookup"><span data-stu-id="376ef-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="376ef-113">Ez a parancs a meglévő példányt a-AdministratorPassword, a-LicenseType, a-StorageSizeInGB és a-VCore új értékekkel állítja be.</span><span class="sxs-lookup"><span data-stu-id="376ef-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="376ef-114">3. példa: a meglévő példány beállítása új értékekkel – AdministratorPassword,-LicenseType,-StorageSizeInGB és-VCore egy példányban egy példányon belül</span><span class="sxs-lookup"><span data-stu-id="376ef-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="376ef-115">Ez a parancs a meglévő példányokat a-AdministratorPassword, a-LicenseType, a-StorageSizeInGB és-VCore új értékekkel állítja be egy adott példányon belül.</span><span class="sxs-lookup"><span data-stu-id="376ef-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="376ef-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="376ef-116">PARAMETERS</span></span>

### <span data-ttu-id="376ef-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="376ef-117">-AdministratorPassword</span></span>
<span data-ttu-id="376ef-118">Az új SQL-rendszergazdai jelszó a példányhoz.</span><span class="sxs-lookup"><span data-stu-id="376ef-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="376ef-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="376ef-119">-AsJob</span></span>
<span data-ttu-id="376ef-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="376ef-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="376ef-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="376ef-121">-AssignIdentity</span></span>
<span data-ttu-id="376ef-122">Hozzon létre és rendeljen el egy Azure Active Directory-identitást ebben a példányban a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="376ef-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="376ef-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="376ef-123">-ComputeGeneration</span></span>
<span data-ttu-id="376ef-124">A példány számítási generációja.</span><span class="sxs-lookup"><span data-stu-id="376ef-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="376ef-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376ef-125">-DefaultProfile</span></span>
<span data-ttu-id="376ef-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="376ef-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="376ef-127">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="376ef-127">-Edition</span></span>
<span data-ttu-id="376ef-128">A példányhoz hozzárendelni kívánt kiadás.</span><span class="sxs-lookup"><span data-stu-id="376ef-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="376ef-129">-Force</span><span class="sxs-lookup"><span data-stu-id="376ef-129">-Force</span></span>
<span data-ttu-id="376ef-130">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="376ef-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="376ef-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="376ef-131">-InputObject</span></span>
<span data-ttu-id="376ef-132">Az eltávolítandó AzureSqlManagedInstanceModel objektum</span><span class="sxs-lookup"><span data-stu-id="376ef-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="376ef-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="376ef-133">-InstancePoolName</span></span>
<span data-ttu-id="376ef-134">A példány-gyűjtő neve.</span><span class="sxs-lookup"><span data-stu-id="376ef-134">The instance pool name.</span></span>

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

### <span data-ttu-id="376ef-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="376ef-135">-LicenseType</span></span>
<span data-ttu-id="376ef-136">Meghatározza, hogy melyik licenc-típust szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="376ef-136">Determines which License Type to use.</span></span> <span data-ttu-id="376ef-137">A lehetséges értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="376ef-137">Possible values are:</span></span>
- <span data-ttu-id="376ef-138">BasePrice – Azure hibrid haszon (AHB) a meglévő SQL Server-licenccel rendelkező tulajdonosok kedvezményes árait alkalmazzák.</span><span class="sxs-lookup"><span data-stu-id="376ef-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="376ef-139">A felügyelt példányok szolgáltatási ára a meglévő SQL Server-licenccel rendelkező tulajdonosok esetében diszkontálva lesz.</span><span class="sxs-lookup"><span data-stu-id="376ef-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="376ef-140">A LicenseIncluded-Azure Hybrid haszon (AHB) árengedménye nem érvényes a meglévő SQL Server-licenccel rendelkező tulajdonosok esetében.</span><span class="sxs-lookup"><span data-stu-id="376ef-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="376ef-141">A felügyelt példány szolgáltatás ára tartalmazni fog egy új SQL Server-licenc költségeit.</span><span class="sxs-lookup"><span data-stu-id="376ef-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="376ef-142">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="376ef-142">-MinimalTlsVersion</span></span>
<span data-ttu-id="376ef-143">A felügyelt példány érvényesítéséhez szükséges minimális TLS-verzió</span><span class="sxs-lookup"><span data-stu-id="376ef-143">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="376ef-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="376ef-144">-Name</span></span>
<span data-ttu-id="376ef-145">Példány neve.</span><span class="sxs-lookup"><span data-stu-id="376ef-145">Instance name.</span></span>

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

### <span data-ttu-id="376ef-146">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="376ef-146">-ProxyOverride</span></span>
<span data-ttu-id="376ef-147">A példányhoz való csatlakozáshoz használt kapcsolattípus.</span><span class="sxs-lookup"><span data-stu-id="376ef-147">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="376ef-148">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="376ef-148">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="376ef-149">Megadja, hogy engedélyezve van-e a nyilvános adatvégpont a példányhoz.</span><span class="sxs-lookup"><span data-stu-id="376ef-149">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="376ef-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="376ef-150">-ResourceGroupName</span></span>
<span data-ttu-id="376ef-151">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="376ef-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="376ef-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="376ef-152">-ResourceId</span></span>
<span data-ttu-id="376ef-153">Az eltávolítandó példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="376ef-153">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="376ef-154">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="376ef-154">-StorageSizeInGB</span></span>
<span data-ttu-id="376ef-155">Azt határozza meg, hogy mekkora tárterületet társíthat a példányhoz</span><span class="sxs-lookup"><span data-stu-id="376ef-155">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="376ef-156">-Címke</span><span class="sxs-lookup"><span data-stu-id="376ef-156">-Tag</span></span>
<span data-ttu-id="376ef-157">A példánnyal társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="376ef-157">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="376ef-158">-VCore</span><span class="sxs-lookup"><span data-stu-id="376ef-158">-VCore</span></span>
<span data-ttu-id="376ef-159">Meghatározza, hogy mennyi VCore társítson a példányhoz</span><span class="sxs-lookup"><span data-stu-id="376ef-159">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="376ef-160">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="376ef-160">-Confirm</span></span>
<span data-ttu-id="376ef-161">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="376ef-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="376ef-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="376ef-162">-WhatIf</span></span>
<span data-ttu-id="376ef-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="376ef-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="376ef-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="376ef-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="376ef-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376ef-165">CommonParameters</span></span>
<span data-ttu-id="376ef-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="376ef-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376ef-167">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="376ef-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376ef-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="376ef-168">INPUTS</span></span>

### <span data-ttu-id="376ef-169">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="376ef-169">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="376ef-170">System. String</span><span class="sxs-lookup"><span data-stu-id="376ef-170">System.String</span></span>

## <span data-ttu-id="376ef-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="376ef-171">OUTPUTS</span></span>

### <span data-ttu-id="376ef-172">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="376ef-172">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="376ef-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="376ef-173">NOTES</span></span>

## <span data-ttu-id="376ef-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="376ef-174">RELATED LINKS</span></span>
