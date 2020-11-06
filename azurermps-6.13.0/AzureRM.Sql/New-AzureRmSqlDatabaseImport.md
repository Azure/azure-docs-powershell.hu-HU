---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
ms.openlocfilehash: 4ea8a6aca74634e8105026e45c25b861e8c060f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495595"
---
# <span data-ttu-id="91a3c-101">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="91a3c-101">New-AzureRmSqlDatabaseImport</span></span>

## <span data-ttu-id="91a3c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="91a3c-103">Importálja a. bacpac fájlt, és hozzon létre egy új adatbázist a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="91a3c-103">Imports a .bacpac file and create a new database on the server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91a3c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91a3c-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91a3c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="91a3c-105">DESCRIPTION</span></span>
<span data-ttu-id="91a3c-106">A **New-AzureRmSqlDatabaseImport** parancsmag az Azure Storage-fiókból származó bacpac-fájlokat importálja egy új Azure SQL-adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="91a3c-106">The **New-AzureRmSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="91a3c-107">Előfordulhat, hogy a kéréshez az adatbázis-importálási állapot kérése lekérdezhető.</span><span class="sxs-lookup"><span data-stu-id="91a3c-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="91a3c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="91a3c-108">EXAMPLES</span></span>

### <span data-ttu-id="91a3c-109">1. példa: bacpac-fájl importálási kérésének létrehozása</span><span class="sxs-lookup"><span data-stu-id="91a3c-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzureRmSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
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

<span data-ttu-id="91a3c-110">Ez a parancs importálási kérést hoz létre a. bacpac importálásához egy új adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="91a3c-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="91a3c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91a3c-111">PARAMETERS</span></span>

### <span data-ttu-id="91a3c-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="91a3c-112">-AdministratorLogin</span></span>
<span data-ttu-id="91a3c-113">Az SQL-rendszergazda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91a3c-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="91a3c-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="91a3c-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="91a3c-115">Az SQL-rendszergazda jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="91a3c-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="91a3c-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="91a3c-116">-AuthenticationType</span></span>
<span data-ttu-id="91a3c-117">A kiszolgáló eléréséhez használt hitelesítés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="91a3c-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="91a3c-118">Ez a paraméter alapértelmezés szerint az SQL, ha nincs beállítva hitelesítési típus.</span><span class="sxs-lookup"><span data-stu-id="91a3c-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="91a3c-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="91a3c-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91a3c-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="91a3c-120">SQL.</span></span>
<span data-ttu-id="91a3c-121">SQL-hitelesítés.</span><span class="sxs-lookup"><span data-stu-id="91a3c-121">SQL authentication.</span></span>
<span data-ttu-id="91a3c-122">Állítsa a *AdministratorLogin* és a *AdministratorLoginPassword* paramétert az SQL-rendszergazda felhasználónevére és jelszavára.</span><span class="sxs-lookup"><span data-stu-id="91a3c-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="91a3c-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="91a3c-123">ADPassword.</span></span>
<span data-ttu-id="91a3c-124">Azure Active Directory-hitelesítés</span><span class="sxs-lookup"><span data-stu-id="91a3c-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="91a3c-125">Adja meg a *AdministratorLogin* és a *AdministratorLoginPassword* az Azure Active Directory rendszergazdai felhasználónevével és jelszavával.</span><span class="sxs-lookup"><span data-stu-id="91a3c-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="91a3c-126">Ez a paraméter csak SQL Database V12-kiszolgálókon érhető el.</span><span class="sxs-lookup"><span data-stu-id="91a3c-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="91a3c-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="91a3c-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="91a3c-128">Az újonnan importált adatbázis maximális méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91a3c-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="91a3c-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="91a3c-129">-DatabaseName</span></span>
<span data-ttu-id="91a3c-130">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91a3c-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="91a3c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91a3c-131">-DefaultProfile</span></span>
<span data-ttu-id="91a3c-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="91a3c-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a3c-133">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="91a3c-133">-Edition</span></span>
<span data-ttu-id="91a3c-134">Annak az új adatbázisnak a kiadását adja meg, amelybe importálni kívánja.</span><span class="sxs-lookup"><span data-stu-id="91a3c-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="91a3c-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="91a3c-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91a3c-136">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="91a3c-136">Premium</span></span>
- <span data-ttu-id="91a3c-137">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="91a3c-137">Basic</span></span>
- <span data-ttu-id="91a3c-138">Standard</span><span class="sxs-lookup"><span data-stu-id="91a3c-138">Standard</span></span>
- <span data-ttu-id="91a3c-139">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="91a3c-139">DataWarehouse</span></span>
- <span data-ttu-id="91a3c-140">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="91a3c-140">Free</span></span>

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

### <span data-ttu-id="91a3c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91a3c-141">-ResourceGroupName</span></span>
<span data-ttu-id="91a3c-142">Az SQL adatbázis-kiszolgáló erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91a3c-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="91a3c-143">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="91a3c-143">-ServerName</span></span>
<span data-ttu-id="91a3c-144">Az SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91a3c-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="91a3c-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="91a3c-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="91a3c-146">Annak a szolgáltatási célnak a nevét adja meg, amelyet az Azure SQL-adatbázishoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="91a3c-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="91a3c-147">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="91a3c-147">-StorageKey</span></span>
<span data-ttu-id="91a3c-148">A tárolási fiók elérési kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="91a3c-148">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="91a3c-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="91a3c-149">-StorageKeyType</span></span>
<span data-ttu-id="91a3c-150">A tárolási fiókhoz tartozó hozzáférési kulcs típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="91a3c-150">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="91a3c-151">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="91a3c-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91a3c-152">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="91a3c-152">StorageAccessKey.</span></span>
<span data-ttu-id="91a3c-153">A tárolási fiók kulcsát használja.</span><span class="sxs-lookup"><span data-stu-id="91a3c-153">Uses the storage account key.</span></span> 
- <span data-ttu-id="91a3c-154">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="91a3c-154">SharedAccessKey.</span></span>
<span data-ttu-id="91a3c-155">A megosztott hozzáférés-aláírás (SAS) kulcsát használja.</span><span class="sxs-lookup"><span data-stu-id="91a3c-155">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="91a3c-156">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="91a3c-156">-StorageUri</span></span>
<span data-ttu-id="91a3c-157">A. bacpac fájl blob-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="91a3c-157">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="91a3c-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="91a3c-158">-Confirm</span></span>
<span data-ttu-id="91a3c-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="91a3c-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91a3c-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91a3c-160">-WhatIf</span></span>
<span data-ttu-id="91a3c-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="91a3c-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91a3c-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91a3c-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91a3c-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a3c-163">CommonParameters</span></span>
<span data-ttu-id="91a3c-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91a3c-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a3c-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91a3c-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a3c-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91a3c-166">INPUTS</span></span>

### <span data-ttu-id="91a3c-167">System. String</span><span class="sxs-lookup"><span data-stu-id="91a3c-167">System.String</span></span>

## <span data-ttu-id="91a3c-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91a3c-168">OUTPUTS</span></span>

### <span data-ttu-id="91a3c-169">Microsoft. Azure. Command. SQL. ImportExport. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="91a3c-169">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="91a3c-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91a3c-170">NOTES</span></span>
* <span data-ttu-id="91a3c-171">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, adatbázis, MSSQL</span><span class="sxs-lookup"><span data-stu-id="91a3c-171">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="91a3c-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91a3c-172">RELATED LINKS</span></span>

[<span data-ttu-id="91a3c-173">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="91a3c-173">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="91a3c-174">Új – AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="91a3c-174">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="91a3c-175">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="91a3c-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

