---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bfa1785004e13400395bd6a6fc93bdec29a69809
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668891"
---
# <span data-ttu-id="8ecf1-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8ecf1-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="8ecf1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ecf1-102">SYNOPSIS</span></span>
<span data-ttu-id="8ecf1-103">Azure SQL-adatbázishoz tartozó felügyelt példány létrehozása.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="8ecf1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ecf1-104">SYNTAX</span></span>

### <span data-ttu-id="8ecf1-105">NewByEditionAndComputeGenerationParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ecf1-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ecf1-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="8ecf1-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ecf1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ecf1-107">DESCRIPTION</span></span>
<span data-ttu-id="8ecf1-108">A **New-AzSqlInstance** parancsmag létrehoz egy Azure SQL-adatbázis felügyelt példányát.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-108">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="8ecf1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8ecf1-109">EXAMPLES</span></span>

### <span data-ttu-id="8ecf1-110">Példa 1: új példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="8ecf1-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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
```

<span data-ttu-id="8ecf1-111">Ezzel a paranccsal új példányt hozhat létre a kiadási és az ComputeGeneration paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="8ecf1-112">2. példa: új példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="8ecf1-112">Example 2: Create a new instance</span></span>
```
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
```

<span data-ttu-id="8ecf1-113">Ezzel a paranccsal új példányt hozhat létre a kiadási és az ComputeGeneration paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="8ecf1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ecf1-114">PARAMETERS</span></span>

### <span data-ttu-id="8ecf1-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="8ecf1-115">-AdministratorCredential</span></span>
<span data-ttu-id="8ecf1-116">A példány SQL-hitelesítési hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-116">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="8ecf1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ecf1-117">-AsJob</span></span>
<span data-ttu-id="8ecf1-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8ecf1-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ecf1-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8ecf1-119">-AssignIdentity</span></span>
<span data-ttu-id="8ecf1-120">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást ehhez a felügyelt példányhoz, amely a kulcskezelő szolgáltatásokhoz (például Azure-tároló) használható.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="8ecf1-121">-Szétválogatás</span><span class="sxs-lookup"><span data-stu-id="8ecf1-121">-Collation</span></span>
<span data-ttu-id="8ecf1-122">A használni kívánt Azure SQL-példány egybevetése.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-122">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="8ecf1-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="8ecf1-123">-ComputeGeneration</span></span>
<span data-ttu-id="8ecf1-124">A példány számítási generációja.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="8ecf1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ecf1-125">-DefaultProfile</span></span>
<span data-ttu-id="8ecf1-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ecf1-127">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="8ecf1-127">-Edition</span></span>
<span data-ttu-id="8ecf1-128">A példány kiadását.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-128">The edition for the instance.</span></span>

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

### <span data-ttu-id="8ecf1-129">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8ecf1-129">-LicenseType</span></span>
<span data-ttu-id="8ecf1-130">Meghatározza, hogy melyik licenc-típust szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-130">Determines which License Type to use.</span></span> <span data-ttu-id="8ecf1-131">A lehetséges értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="8ecf1-131">Possible values are:</span></span>
- <span data-ttu-id="8ecf1-132">BasePrice – Azure hibrid haszon (AHB) a meglévő SQL Server-licenccel rendelkező tulajdonosok kedvezményes árait alkalmazzák.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-132">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="8ecf1-133">A felügyelt példányok szolgáltatási ára a meglévő SQL Server-licenccel rendelkező tulajdonosok esetében diszkontálva lesz.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-133">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="8ecf1-134">A LicenseIncluded-Azure Hybrid haszon (AHB) árengedménye nem érvényes a meglévő SQL Server-licenccel rendelkező tulajdonosok esetében.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-134">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="8ecf1-135">A felügyelt példány szolgáltatás ára tartalmazni fog egy új SQL Server-licenc költségeit.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-135">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecf1-136">-Hely</span><span class="sxs-lookup"><span data-stu-id="8ecf1-136">-Location</span></span>
<span data-ttu-id="8ecf1-137">A példány létrehozásának helye</span><span class="sxs-lookup"><span data-stu-id="8ecf1-137">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecf1-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8ecf1-138">-Name</span></span>
<span data-ttu-id="8ecf1-139">Példány neve.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-139">Instance name.</span></span>

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

### <span data-ttu-id="8ecf1-140">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="8ecf1-140">-ProxyOverride</span></span>
<span data-ttu-id="8ecf1-141">A példányhoz való csatlakozáshoz használt kapcsolattípus.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-141">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="8ecf1-142">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="8ecf1-142">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="8ecf1-143">Megadja, hogy engedélyezve van-e a nyilvános adatvégpont a példányhoz.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-143">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="8ecf1-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ecf1-144">-ResourceGroupName</span></span>
<span data-ttu-id="8ecf1-145">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecf1-146">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8ecf1-146">-SkuName</span></span>
<span data-ttu-id="8ecf1-147">A példány SKU-neve (például "GP_Gen4", "BC_Gen4").</span><span class="sxs-lookup"><span data-stu-id="8ecf1-147">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="8ecf1-148">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="8ecf1-148">-StorageSizeInGB</span></span>
<span data-ttu-id="8ecf1-149">Azt határozza meg, hogy mekkora tárterületet társíthat a példányhoz</span><span class="sxs-lookup"><span data-stu-id="8ecf1-149">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="8ecf1-150">– NetI</span><span class="sxs-lookup"><span data-stu-id="8ecf1-150">-SubnetId</span></span>
<span data-ttu-id="8ecf1-151">A példány létrehozásához használandó alhálózat-azonosító</span><span class="sxs-lookup"><span data-stu-id="8ecf1-151">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecf1-152">-Címke</span><span class="sxs-lookup"><span data-stu-id="8ecf1-152">-Tag</span></span>
<span data-ttu-id="8ecf1-153">A példánnyal társítani kívánt Címkék</span><span class="sxs-lookup"><span data-stu-id="8ecf1-153">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="8ecf1-154">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="8ecf1-154">-TimezoneId</span></span>
<span data-ttu-id="8ecf1-155">A beállítani kívánt példány időzóna-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-155">The time zone id for the instance to set.</span></span> <span data-ttu-id="8ecf1-156">Az időzóna-azonosítók listája a sys.time_zone_info (Transact-SQL) nézetben van kitéve.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-156">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="8ecf1-157">-VCore</span><span class="sxs-lookup"><span data-stu-id="8ecf1-157">-VCore</span></span>
<span data-ttu-id="8ecf1-158">Meghatározza, hogy mennyi VCore társítson a példányhoz</span><span class="sxs-lookup"><span data-stu-id="8ecf1-158">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="8ecf1-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8ecf1-159">-Confirm</span></span>
<span data-ttu-id="8ecf1-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ecf1-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ecf1-161">-WhatIf</span></span>
<span data-ttu-id="8ecf1-162">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ecf1-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ecf1-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ecf1-164">CommonParameters</span></span>
<span data-ttu-id="8ecf1-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ecf1-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ecf1-166">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8ecf1-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ecf1-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ecf1-167">INPUTS</span></span>

### <span data-ttu-id="8ecf1-168">Nincs</span><span class="sxs-lookup"><span data-stu-id="8ecf1-168">None</span></span>

## <span data-ttu-id="8ecf1-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ecf1-169">OUTPUTS</span></span>

### <span data-ttu-id="8ecf1-170">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="8ecf1-170">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="8ecf1-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ecf1-171">NOTES</span></span>

## <span data-ttu-id="8ecf1-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ecf1-172">RELATED LINKS</span></span>
