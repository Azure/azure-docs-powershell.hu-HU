---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: 8b898d401c9c20efdd25fd09b5a6eedaf3e2b422
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012473"
---
# <span data-ttu-id="39f6f-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="39f6f-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="39f6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="39f6f-103">Importálja a. bacpac fájlt, és hozzon létre egy új adatbázist a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="39f6f-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="39f6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39f6f-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39f6f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="39f6f-105">DESCRIPTION</span></span>
<span data-ttu-id="39f6f-106">A **New-AzSqlDatabaseImport** parancsmag az Azure Storage-fiókból származó bacpac-fájlokat importálja egy új Azure SQL-adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="39f6f-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="39f6f-107">Előfordulhat, hogy a kéréshez az adatbázis-importálási állapot kérése lekérdezhető.</span><span class="sxs-lookup"><span data-stu-id="39f6f-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="39f6f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="39f6f-108">EXAMPLES</span></span>

### <span data-ttu-id="39f6f-109">1. példa: bacpac-fájl importálási kérésének létrehozása</span><span class="sxs-lookup"><span data-stu-id="39f6f-109">Example 1: Create an import request for a bacpac file</span></span>
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

<span data-ttu-id="39f6f-110">Ez a parancs importálási kérést hoz létre a. bacpac importálásához egy új adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="39f6f-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="39f6f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39f6f-111">PARAMETERS</span></span>

### <span data-ttu-id="39f6f-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="39f6f-112">-AdministratorLogin</span></span>
<span data-ttu-id="39f6f-113">Az SQL-rendszergazda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="39f6f-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="39f6f-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="39f6f-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="39f6f-115">Az SQL-rendszergazda jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="39f6f-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="39f6f-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="39f6f-116">-AuthenticationType</span></span>
<span data-ttu-id="39f6f-117">A kiszolgáló eléréséhez használt hitelesítés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="39f6f-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="39f6f-118">Ez a paraméter alapértelmezés szerint az SQL, ha nincs beállítva hitelesítési típus.</span><span class="sxs-lookup"><span data-stu-id="39f6f-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="39f6f-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="39f6f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="39f6f-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="39f6f-120">SQL.</span></span>
<span data-ttu-id="39f6f-121">SQL-hitelesítés.</span><span class="sxs-lookup"><span data-stu-id="39f6f-121">SQL authentication.</span></span>
<span data-ttu-id="39f6f-122">Állítsa a *AdministratorLogin* és a *AdministratorLoginPassword* paramétert az SQL-rendszergazda felhasználónevére és jelszavára.</span><span class="sxs-lookup"><span data-stu-id="39f6f-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="39f6f-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="39f6f-123">ADPassword.</span></span>
<span data-ttu-id="39f6f-124">Azure Active Directory-hitelesítés</span><span class="sxs-lookup"><span data-stu-id="39f6f-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="39f6f-125">Adja meg a *AdministratorLogin* és a *AdministratorLoginPassword* az Azure Active Directory rendszergazdai felhasználónevével és jelszavával.</span><span class="sxs-lookup"><span data-stu-id="39f6f-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="39f6f-126">Ez a paraméter csak SQL Database V12-kiszolgálókon érhető el.</span><span class="sxs-lookup"><span data-stu-id="39f6f-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="39f6f-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="39f6f-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="39f6f-128">Az újonnan importált adatbázis maximális méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="39f6f-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="39f6f-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="39f6f-129">-DatabaseName</span></span>
<span data-ttu-id="39f6f-130">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="39f6f-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="39f6f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f6f-131">-DefaultProfile</span></span>
<span data-ttu-id="39f6f-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="39f6f-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39f6f-133">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="39f6f-133">-Edition</span></span>
<span data-ttu-id="39f6f-134">Annak az új adatbázisnak a kiadását adja meg, amelybe importálni kívánja.</span><span class="sxs-lookup"><span data-stu-id="39f6f-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="39f6f-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="39f6f-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="39f6f-136">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="39f6f-136">Premium</span></span>
- <span data-ttu-id="39f6f-137">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="39f6f-137">Basic</span></span>
- <span data-ttu-id="39f6f-138">Standard</span><span class="sxs-lookup"><span data-stu-id="39f6f-138">Standard</span></span>
- <span data-ttu-id="39f6f-139">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="39f6f-139">DataWarehouse</span></span>
- <span data-ttu-id="39f6f-140">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="39f6f-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f6f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f6f-141">-ResourceGroupName</span></span>
<span data-ttu-id="39f6f-142">Az SQL adatbázis-kiszolgáló erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="39f6f-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="39f6f-143">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="39f6f-143">-ServerName</span></span>
<span data-ttu-id="39f6f-144">Az SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="39f6f-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="39f6f-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="39f6f-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="39f6f-146">Annak a szolgáltatási célnak a nevét adja meg, amelyet az Azure SQL-adatbázishoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="39f6f-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="39f6f-147">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="39f6f-147">-StorageKey</span></span>
<span data-ttu-id="39f6f-148">A tárolási fiók elérési kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="39f6f-148">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="39f6f-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="39f6f-149">-StorageKeyType</span></span>
<span data-ttu-id="39f6f-150">A tárolási fiókhoz tartozó hozzáférési kulcs típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="39f6f-150">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="39f6f-151">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="39f6f-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="39f6f-152">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="39f6f-152">StorageAccessKey.</span></span>
<span data-ttu-id="39f6f-153">A tárolási fiók kulcsát használja.</span><span class="sxs-lookup"><span data-stu-id="39f6f-153">Uses the storage account key.</span></span> 
- <span data-ttu-id="39f6f-154">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="39f6f-154">SharedAccessKey.</span></span>
<span data-ttu-id="39f6f-155">A megosztott hozzáférés-aláírás (SAS) kulcsát használja.</span><span class="sxs-lookup"><span data-stu-id="39f6f-155">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="39f6f-156">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="39f6f-156">-StorageUri</span></span>
<span data-ttu-id="39f6f-157">A. bacpac fájl blob-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="39f6f-157">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="39f6f-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="39f6f-158">-Confirm</span></span>
<span data-ttu-id="39f6f-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="39f6f-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39f6f-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39f6f-160">-WhatIf</span></span>
<span data-ttu-id="39f6f-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="39f6f-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39f6f-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39f6f-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39f6f-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f6f-163">CommonParameters</span></span>
<span data-ttu-id="39f6f-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39f6f-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f6f-165">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="39f6f-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f6f-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39f6f-166">INPUTS</span></span>

### <span data-ttu-id="39f6f-167">System. String</span><span class="sxs-lookup"><span data-stu-id="39f6f-167">System.String</span></span>

## <span data-ttu-id="39f6f-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39f6f-168">OUTPUTS</span></span>

### <span data-ttu-id="39f6f-169">Microsoft. Azure. Command. SQL. ImportExport. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="39f6f-169">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="39f6f-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39f6f-170">NOTES</span></span>
* <span data-ttu-id="39f6f-171">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, adatbázis, MSSQL</span><span class="sxs-lookup"><span data-stu-id="39f6f-171">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="39f6f-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39f6f-172">RELATED LINKS</span></span>

[<span data-ttu-id="39f6f-173">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="39f6f-173">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="39f6f-174">Új – AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="39f6f-174">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="39f6f-175">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="39f6f-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

