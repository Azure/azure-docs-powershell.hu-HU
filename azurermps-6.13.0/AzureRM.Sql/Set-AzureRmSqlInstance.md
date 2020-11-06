---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
ms.openlocfilehash: 1e992e33591f5c993bfdda1bf9934245b2f5f2c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501951"
---
# <span data-ttu-id="d7616-101">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d7616-101">Set-AzureRmSqlInstance</span></span>

## <span data-ttu-id="d7616-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7616-102">SYNOPSIS</span></span>
<span data-ttu-id="d7616-103">Az Azure SQL-adatbázis felügyelt példányának tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="d7616-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7616-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7616-104">SYNTAX</span></span>

### <span data-ttu-id="d7616-105">SetInstanceFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7616-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7616-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="d7616-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7616-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="d7616-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzureRmSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>] [-AssignIdentity]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7616-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7616-108">DESCRIPTION</span></span>
<span data-ttu-id="d7616-109">A **set-AzureRmSqlInstance** parancsmag egy Azure SQL-adatbázis felügyelt példányának tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="d7616-109">The **Set-AzureRmSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="d7616-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d7616-110">EXAMPLES</span></span>

### <span data-ttu-id="d7616-111">1. példa: a meglévő példány beállítása új értékekkel – AdministratorPassword,-LicenseType,-StorageSizeInGB és-VCore</span><span class="sxs-lookup"><span data-stu-id="d7616-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
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

<span data-ttu-id="d7616-112">Ez a parancs a meglévő példányt a-AdministratorPassword, a-LicenseType, a-StorageSizeInGB és a-VCore új értékekkel állítja be.</span><span class="sxs-lookup"><span data-stu-id="d7616-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

## <span data-ttu-id="d7616-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7616-113">PARAMETERS</span></span>

### <span data-ttu-id="d7616-114">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="d7616-114">-AdministratorPassword</span></span>
<span data-ttu-id="d7616-115">Az új SQL-rendszergazdai jelszó a példányhoz.</span><span class="sxs-lookup"><span data-stu-id="d7616-115">The new SQL administrator password for the instance.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7616-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d7616-116">-AssignIdentity</span></span>
<span data-ttu-id="d7616-117">Hozzon létre és rendeljen el egy Azure Active Directory-identitást ebben a példányban a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="d7616-117">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7616-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7616-118">-DefaultProfile</span></span>
<span data-ttu-id="d7616-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7616-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7616-120">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="d7616-120">-Edition</span></span>
<span data-ttu-id="d7616-121">A példányhoz hozzárendelni kívánt kiadás.</span><span class="sxs-lookup"><span data-stu-id="d7616-121">The edition to assign to the instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7616-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d7616-122">-Force</span></span>
<span data-ttu-id="d7616-123">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="d7616-123">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7616-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7616-124">-InputObject</span></span>
<span data-ttu-id="d7616-125">Az eltávolítandó AzureSqlManagedInstanceModel objektum</span><span class="sxs-lookup"><span data-stu-id="d7616-125">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7616-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d7616-126">-LicenseType</span></span>
<span data-ttu-id="d7616-127">A használandó példány típusának meghatározása</span><span class="sxs-lookup"><span data-stu-id="d7616-127">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7616-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7616-128">-Name</span></span>
<span data-ttu-id="d7616-129">Példány neve.</span><span class="sxs-lookup"><span data-stu-id="d7616-129">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7616-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7616-130">-ResourceGroupName</span></span>
<span data-ttu-id="d7616-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d7616-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7616-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7616-132">-ResourceId</span></span>
<span data-ttu-id="d7616-133">Az eltávolítandó példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d7616-133">The resource id of instance to remove</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7616-134">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="d7616-134">-StorageSizeInGB</span></span>
<span data-ttu-id="d7616-135">Azt határozza meg, hogy mekkora tárterületet társíthat a példányhoz</span><span class="sxs-lookup"><span data-stu-id="d7616-135">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7616-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="d7616-136">-Tag</span></span>
<span data-ttu-id="d7616-137">A példánnyal társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="d7616-137">The tags to associate with the instance.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7616-138">-VCore</span><span class="sxs-lookup"><span data-stu-id="d7616-138">-VCore</span></span>
<span data-ttu-id="d7616-139">Meghatározza, hogy mennyi VCore társítson a példányhoz</span><span class="sxs-lookup"><span data-stu-id="d7616-139">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7616-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7616-140">-Confirm</span></span>
<span data-ttu-id="d7616-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7616-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7616-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7616-142">-WhatIf</span></span>
<span data-ttu-id="d7616-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7616-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7616-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7616-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7616-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7616-145">CommonParameters</span></span>
<span data-ttu-id="d7616-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7616-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7616-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7616-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7616-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7616-148">INPUTS</span></span>

### <span data-ttu-id="d7616-149">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d7616-149">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="d7616-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d7616-150">System.String</span></span>

## <span data-ttu-id="d7616-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7616-151">OUTPUTS</span></span>

### <span data-ttu-id="d7616-152">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d7616-152">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="d7616-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7616-153">NOTES</span></span>

## <span data-ttu-id="d7616-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7616-154">RELATED LINKS</span></span>
