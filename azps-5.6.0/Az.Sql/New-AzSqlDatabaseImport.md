---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: e0f23e1d41e27e7e16cf9a1cbead42a979f73eed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932210"
---
# <span data-ttu-id="28ba6-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="28ba6-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="28ba6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="28ba6-103">.bacpac fájlt importál, és új adatbázist hoz létre a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="28ba6-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="28ba6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="28ba6-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28ba6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="28ba6-105">DESCRIPTION</span></span>
<span data-ttu-id="28ba6-106">A **New-AzSqlDatabaseImport parancsmag** egy bacpac fájlt importál egy Azure-tárfiókból egy új Azure SQL-adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="28ba6-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="28ba6-107">Az importálási adatbázis állapotkérése elküldhető a kérelem állapotinformációinak lekérése érdekében.</span><span class="sxs-lookup"><span data-stu-id="28ba6-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="28ba6-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="28ba6-108">EXAMPLES</span></span>

### <span data-ttu-id="28ba6-109">1. példa: Import request for a bacpac file</span><span class="sxs-lookup"><span data-stu-id="28ba6-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="28ba6-110">Ez a parancs egy .bacpac importálási kérést hoz létre egy új adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="28ba6-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="28ba6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28ba6-111">PARAMETERS</span></span>

### <span data-ttu-id="28ba6-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="28ba6-112">-AdministratorLogin</span></span>
<span data-ttu-id="28ba6-113">Az SQL-rendszergazda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ba6-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="28ba6-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="28ba6-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="28ba6-115">Az SQL-rendszergazda jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ba6-115">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba6-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="28ba6-116">-AuthenticationType</span></span>
<span data-ttu-id="28ba6-117">A kiszolgáló eléréséhez használt hitelesítés típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="28ba6-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="28ba6-118">Ez a paraméter alapértelmezés szerint SQL, ha nincs beállítva hitelesítési típus.</span><span class="sxs-lookup"><span data-stu-id="28ba6-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="28ba6-119">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="28ba6-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28ba6-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="28ba6-120">SQL.</span></span>
<span data-ttu-id="28ba6-121">SQL-hitelesítés.</span><span class="sxs-lookup"><span data-stu-id="28ba6-121">SQL authentication.</span></span>
<span data-ttu-id="28ba6-122">Állítsa *be a AdministratorLogin* és *a AdministratorLoginPassword* paramétert az SQL-rendszergazda felhasználónevére és jelszavára.</span><span class="sxs-lookup"><span data-stu-id="28ba6-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="28ba6-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="28ba6-123">ADPassword.</span></span>
<span data-ttu-id="28ba6-124">Azure Active Directory-hitelesítés.</span><span class="sxs-lookup"><span data-stu-id="28ba6-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="28ba6-125">Állítsa *be a AdministratorLogin* és *a AdministratorLoginPassword* nevet az Azure Active Directory rendszergazdai felhasználónevére és jelszavára.</span><span class="sxs-lookup"><span data-stu-id="28ba6-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="28ba6-126">Ez a paraméter csak SQL Database V12-kiszolgálókon érhető el.</span><span class="sxs-lookup"><span data-stu-id="28ba6-126">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba6-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="28ba6-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="28ba6-128">Az újonnan importált adatbázis maximális méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ba6-128">Specifies the maximum size for the newly imported database.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba6-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="28ba6-129">-DatabaseName</span></span>
<span data-ttu-id="28ba6-130">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ba6-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="28ba6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ba6-131">-DefaultProfile</span></span>
<span data-ttu-id="28ba6-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="28ba6-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28ba6-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="28ba6-133">-Edition</span></span>
<span data-ttu-id="28ba6-134">Az új adatbázisnak azt a kiadását adja meg, amelybe importálni kell.</span><span class="sxs-lookup"><span data-stu-id="28ba6-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="28ba6-135">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="28ba6-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28ba6-136">Prémium</span><span class="sxs-lookup"><span data-stu-id="28ba6-136">Premium</span></span>
- <span data-ttu-id="28ba6-137">Alapszintű</span><span class="sxs-lookup"><span data-stu-id="28ba6-137">Basic</span></span>
- <span data-ttu-id="28ba6-138">Normál</span><span class="sxs-lookup"><span data-stu-id="28ba6-138">Standard</span></span>
- <span data-ttu-id="28ba6-139">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="28ba6-139">DataWarehouse</span></span>
- <span data-ttu-id="28ba6-140">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="28ba6-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical, Hyperscale

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba6-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28ba6-141">-ResourceGroupName</span></span>
<span data-ttu-id="28ba6-142">Az SQL-adatbázis-kiszolgáló erőforráscsoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ba6-142">Specifies the name of the resource group for the SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28ba6-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28ba6-143">-ServerName</span></span>
<span data-ttu-id="28ba6-144">Az SQL-adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ba6-144">Specifies the name of the SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28ba6-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="28ba6-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="28ba6-146">Az Azure SQL-adatbázishoz hozzárendelni szükséges szolgáltatás-célkiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ba6-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="28ba6-147">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="28ba6-147">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="28ba6-148">Az SQL Server-erőforrásazonosító a személyes hivatkozás létrehozásához</span><span class="sxs-lookup"><span data-stu-id="28ba6-148">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="28ba6-149">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="28ba6-149">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="28ba6-150">A tárfiók erőforrás-azonosítója privát hivatkozás létrehozásához</span><span class="sxs-lookup"><span data-stu-id="28ba6-150">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="28ba6-151">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="28ba6-151">-StorageKey</span></span>
<span data-ttu-id="28ba6-152">A tárfiók hozzáférési kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ba6-152">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="28ba6-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="28ba6-153">-StorageKeyType</span></span>
<span data-ttu-id="28ba6-154">A tárfiók hozzáférési kulcsának típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="28ba6-154">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="28ba6-155">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="28ba6-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28ba6-156">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="28ba6-156">StorageAccessKey.</span></span>
<span data-ttu-id="28ba6-157">A tárfiók kulcsát használja.</span><span class="sxs-lookup"><span data-stu-id="28ba6-157">Uses the storage account key.</span></span> 
- <span data-ttu-id="28ba6-158">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="28ba6-158">SharedAccessKey.</span></span>
<span data-ttu-id="28ba6-159">A Megosztott hozzáférés-aláírás (SAS) kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="28ba6-159">Uses the Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba6-160">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="28ba6-160">-StorageUri</span></span>
<span data-ttu-id="28ba6-161">A .bacpac fájl blob-URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ba6-161">Specifies the blob URI of the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba6-162">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="28ba6-162">-UseNetworkIsolation</span></span>
<span data-ttu-id="28ba6-163">Ha be van állítva, személyes hivatkozást hoz létre a tárfiókhoz és/vagy az SQL-kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="28ba6-163">If set, will create private link for storage account and/or SQL server</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba6-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28ba6-164">-Confirm</span></span>
<span data-ttu-id="28ba6-165">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="28ba6-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba6-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28ba6-166">-WhatIf</span></span>
<span data-ttu-id="28ba6-167">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="28ba6-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28ba6-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28ba6-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba6-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ba6-169">CommonParameters</span></span>
<span data-ttu-id="28ba6-170">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28ba6-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ba6-171">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28ba6-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ba6-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28ba6-172">INPUTS</span></span>

### <span data-ttu-id="28ba6-173">System.String</span><span class="sxs-lookup"><span data-stu-id="28ba6-173">System.String</span></span>

## <span data-ttu-id="28ba6-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28ba6-174">OUTPUTS</span></span>

### <span data-ttu-id="28ba6-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="28ba6-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="28ba6-176">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="28ba6-176">NOTES</span></span>
* <span data-ttu-id="28ba6-177">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, sql, adatbázis, mssql</span><span class="sxs-lookup"><span data-stu-id="28ba6-177">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="28ba6-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28ba6-178">RELATED LINKS</span></span>

[<span data-ttu-id="28ba6-179">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="28ba6-179">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="28ba6-180">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="28ba6-180">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="28ba6-181">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="28ba6-181">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

