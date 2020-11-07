---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: ad98b764eac08c9fb1f6d3dd367d78ca1b5d45d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668772"
---
# <span data-ttu-id="e0542-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e0542-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="e0542-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0542-102">SYNOPSIS</span></span>
<span data-ttu-id="e0542-103">Az Azure SQL-adatbázis felügyelt példányának tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="e0542-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="e0542-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0542-104">SYNTAX</span></span>

### <span data-ttu-id="e0542-105">SetInstanceFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0542-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0542-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e0542-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0542-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e0542-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0542-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0542-108">DESCRIPTION</span></span>
<span data-ttu-id="e0542-109">A **set-AzSqlInstance** parancsmag egy Azure SQL-adatbázis felügyelt példányának tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="e0542-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="e0542-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e0542-110">EXAMPLES</span></span>

### <span data-ttu-id="e0542-111">1. példa: a meglévő példány beállítása új értékekkel – AdministratorPassword,-LicenseType,-StorageSizeInGB és-VCore</span><span class="sxs-lookup"><span data-stu-id="e0542-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
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

<span data-ttu-id="e0542-112">Ez a parancs a meglévő példányt a-AdministratorPassword, a-LicenseType, a-StorageSizeInGB és a-VCore új értékekkel állítja be.</span><span class="sxs-lookup"><span data-stu-id="e0542-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

## <span data-ttu-id="e0542-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0542-113">PARAMETERS</span></span>

### <span data-ttu-id="e0542-114">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="e0542-114">-AdministratorPassword</span></span>
<span data-ttu-id="e0542-115">Az új SQL-rendszergazdai jelszó a példányhoz.</span><span class="sxs-lookup"><span data-stu-id="e0542-115">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="e0542-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e0542-116">-AssignIdentity</span></span>
<span data-ttu-id="e0542-117">Hozzon létre és rendeljen el egy Azure Active Directory-identitást ebben a példányban a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="e0542-117">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="e0542-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0542-118">-DefaultProfile</span></span>
<span data-ttu-id="e0542-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0542-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0542-120">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="e0542-120">-Edition</span></span>
<span data-ttu-id="e0542-121">A példányhoz hozzárendelni kívánt kiadás.</span><span class="sxs-lookup"><span data-stu-id="e0542-121">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="e0542-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e0542-122">-Force</span></span>
<span data-ttu-id="e0542-123">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="e0542-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e0542-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0542-124">-InputObject</span></span>
<span data-ttu-id="e0542-125">Az eltávolítandó AzureSqlManagedInstanceModel objektum</span><span class="sxs-lookup"><span data-stu-id="e0542-125">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="e0542-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e0542-126">-LicenseType</span></span>
<span data-ttu-id="e0542-127">Meghatározza, hogy melyik licenc-típust szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="e0542-127">Determines which License Type to use.</span></span> <span data-ttu-id="e0542-128">A lehetséges értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="e0542-128">Possible values are:</span></span>
- <span data-ttu-id="e0542-129">BasePrice – Azure hibrid haszon (AHB) a meglévő SQL Server-licenccel rendelkező tulajdonosok kedvezményes árait alkalmazzák.</span><span class="sxs-lookup"><span data-stu-id="e0542-129">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="e0542-130">A felügyelt példányok szolgáltatási ára a meglévő SQL Server-licenccel rendelkező tulajdonosok esetében diszkontálva lesz.</span><span class="sxs-lookup"><span data-stu-id="e0542-130">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="e0542-131">A LicenseIncluded-Azure Hybrid haszon (AHB) árengedménye nem érvényes a meglévő SQL Server-licenccel rendelkező tulajdonosok esetében.</span><span class="sxs-lookup"><span data-stu-id="e0542-131">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="e0542-132">A felügyelt példány szolgáltatás ára tartalmazni fog egy új SQL Server-licenc költségeit.</span><span class="sxs-lookup"><span data-stu-id="e0542-132">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="e0542-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0542-133">-Name</span></span>
<span data-ttu-id="e0542-134">Példány neve.</span><span class="sxs-lookup"><span data-stu-id="e0542-134">Instance name.</span></span>

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

### <span data-ttu-id="e0542-135">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="e0542-135">-ProxyOverride</span></span>
<span data-ttu-id="e0542-136">A példányhoz való csatlakozáshoz használt kapcsolattípus.</span><span class="sxs-lookup"><span data-stu-id="e0542-136">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="e0542-137">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="e0542-137">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="e0542-138">Megadja, hogy engedélyezve van-e a nyilvános adatvégpont a példányhoz.</span><span class="sxs-lookup"><span data-stu-id="e0542-138">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="e0542-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0542-139">-ResourceGroupName</span></span>
<span data-ttu-id="e0542-140">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0542-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="e0542-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0542-141">-ResourceId</span></span>
<span data-ttu-id="e0542-142">Az eltávolítandó példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e0542-142">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="e0542-143">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="e0542-143">-StorageSizeInGB</span></span>
<span data-ttu-id="e0542-144">Azt határozza meg, hogy mekkora tárterületet társíthat a példányhoz</span><span class="sxs-lookup"><span data-stu-id="e0542-144">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="e0542-145">-Címke</span><span class="sxs-lookup"><span data-stu-id="e0542-145">-Tag</span></span>
<span data-ttu-id="e0542-146">A példánnyal társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="e0542-146">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="e0542-147">-VCore</span><span class="sxs-lookup"><span data-stu-id="e0542-147">-VCore</span></span>
<span data-ttu-id="e0542-148">Meghatározza, hogy mennyi VCore társítson a példányhoz</span><span class="sxs-lookup"><span data-stu-id="e0542-148">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="e0542-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0542-149">-Confirm</span></span>
<span data-ttu-id="e0542-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0542-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0542-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0542-151">-WhatIf</span></span>
<span data-ttu-id="e0542-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0542-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0542-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0542-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0542-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0542-154">CommonParameters</span></span>
<span data-ttu-id="e0542-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0542-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0542-156">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e0542-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0542-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0542-157">INPUTS</span></span>

### <span data-ttu-id="e0542-158">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="e0542-158">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="e0542-159">System. String</span><span class="sxs-lookup"><span data-stu-id="e0542-159">System.String</span></span>

## <span data-ttu-id="e0542-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0542-160">OUTPUTS</span></span>

### <span data-ttu-id="e0542-161">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="e0542-161">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="e0542-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0542-162">NOTES</span></span>

## <span data-ttu-id="e0542-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0542-163">RELATED LINKS</span></span>
