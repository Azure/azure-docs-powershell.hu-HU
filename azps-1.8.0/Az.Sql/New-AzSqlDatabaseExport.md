---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 85f74609fe4075ef42e2b417b2d8ac2099df721b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668900"
---
# <span data-ttu-id="7aed9-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="7aed9-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="7aed9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7aed9-102">SYNOPSIS</span></span>
<span data-ttu-id="7aed9-103">Azure SQL-adatbázis exportálása. bacpac fájlként a tároló fiókba.</span><span class="sxs-lookup"><span data-stu-id="7aed9-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="7aed9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7aed9-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7aed9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7aed9-105">DESCRIPTION</span></span>
<span data-ttu-id="7aed9-106">A **New-AzSqlDatabaseExport** parancsmag az Azure SQL-adatbázist. bacpac fájlként exportálja a tároló fiókba.</span><span class="sxs-lookup"><span data-stu-id="7aed9-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="7aed9-107">Előfordulhat, hogy az exportálási adatbázis-állapot kérése elküldve van a kérés állapotára vonatkozó adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="7aed9-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="7aed9-108">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="7aed9-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7aed9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7aed9-109">EXAMPLES</span></span>

### <span data-ttu-id="7aed9-110">1. példa: exportálási kérés létrehozása adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="7aed9-110">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.azure.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="7aed9-111">Ez a parancs a megadott adatbázis exportálási kérését hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7aed9-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="7aed9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7aed9-112">PARAMETERS</span></span>

### <span data-ttu-id="7aed9-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="7aed9-113">-AdministratorLogin</span></span>
<span data-ttu-id="7aed9-114">Az SQL-rendszergazda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aed9-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="7aed9-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="7aed9-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="7aed9-116">Az SQL-rendszergazda jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aed9-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="7aed9-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="7aed9-117">-AuthenticationType</span></span>
<span data-ttu-id="7aed9-118">A kiszolgáló eléréséhez használt hitelesítés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aed9-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="7aed9-119">Az alapértelmezett érték az SQL, ha nincs beállítva a hitelesítési típus.</span><span class="sxs-lookup"><span data-stu-id="7aed9-119">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="7aed9-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7aed9-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7aed9-121">SQL.</span><span class="sxs-lookup"><span data-stu-id="7aed9-121">Sql.</span></span>
<span data-ttu-id="7aed9-122">SQL-hitelesítés.</span><span class="sxs-lookup"><span data-stu-id="7aed9-122">SQL authentication.</span></span>
<span data-ttu-id="7aed9-123">Adja meg a *AdministratorLogin* és a *AdministratorLoginPassword* az SQL-rendszergazdai felhasználónevével és jelszavával.</span><span class="sxs-lookup"><span data-stu-id="7aed9-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="7aed9-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="7aed9-124">ADPassword.</span></span>
<span data-ttu-id="7aed9-125">Azure Active Directory-hitelesítés</span><span class="sxs-lookup"><span data-stu-id="7aed9-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="7aed9-126">Állítsa be a *AdministratorLogin* és a *ADMINISTRATORLOGINPASSWORD* az Azure ad Administrator felhasználónevére és jelszavára.</span><span class="sxs-lookup"><span data-stu-id="7aed9-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="7aed9-127">Ez a paraméter csak SQL Database V12-kiszolgálókon érhető el.</span><span class="sxs-lookup"><span data-stu-id="7aed9-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="7aed9-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7aed9-128">-DatabaseName</span></span>
<span data-ttu-id="7aed9-129">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aed9-129">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aed9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aed9-130">-DefaultProfile</span></span>
<span data-ttu-id="7aed9-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7aed9-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7aed9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aed9-132">-ResourceGroupName</span></span>
<span data-ttu-id="7aed9-133">Az SQL adatbázis-kiszolgáló erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aed9-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="7aed9-134">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="7aed9-134">-ServerName</span></span>
<span data-ttu-id="7aed9-135">Az SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aed9-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="7aed9-136">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="7aed9-136">-StorageKey</span></span>
<span data-ttu-id="7aed9-137">A tárolási fiók elérési kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aed9-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="7aed9-138">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="7aed9-138">-StorageKeyType</span></span>
<span data-ttu-id="7aed9-139">A tárolási fiókhoz tartozó hozzáférési kulcs típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aed9-139">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="7aed9-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7aed9-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7aed9-141">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="7aed9-141">StorageAccessKey.</span></span>
<span data-ttu-id="7aed9-142">Ez az érték a tárolási fiók kulcsát használja.</span><span class="sxs-lookup"><span data-stu-id="7aed9-142">This value uses a storage account key.</span></span> 
- <span data-ttu-id="7aed9-143">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="7aed9-143">SharedAccessKey.</span></span>
<span data-ttu-id="7aed9-144">Ez az érték egy megosztott Access-aláírást (SAS) használ.</span><span class="sxs-lookup"><span data-stu-id="7aed9-144">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="7aed9-145">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="7aed9-145">-StorageUri</span></span>
<span data-ttu-id="7aed9-146">A blob hivatkozást adja meg URL-ként az. bacpac fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="7aed9-146">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="7aed9-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7aed9-147">-Confirm</span></span>
<span data-ttu-id="7aed9-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7aed9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7aed9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aed9-149">-WhatIf</span></span>
<span data-ttu-id="7aed9-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7aed9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7aed9-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7aed9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7aed9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aed9-152">CommonParameters</span></span>
<span data-ttu-id="7aed9-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7aed9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aed9-154">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7aed9-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aed9-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7aed9-155">INPUTS</span></span>

### <span data-ttu-id="7aed9-156">System. String</span><span class="sxs-lookup"><span data-stu-id="7aed9-156">System.String</span></span>

## <span data-ttu-id="7aed9-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7aed9-157">OUTPUTS</span></span>

### <span data-ttu-id="7aed9-158">Microsoft. Azure. Command. SQL. ImportExport. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="7aed9-158">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="7aed9-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7aed9-159">NOTES</span></span>
* <span data-ttu-id="7aed9-160">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, adatbázis, MSSQL</span><span class="sxs-lookup"><span data-stu-id="7aed9-160">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="7aed9-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7aed9-161">RELATED LINKS</span></span>

[<span data-ttu-id="7aed9-162">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="7aed9-162">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="7aed9-163">Új – AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="7aed9-163">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="7aed9-164">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="7aed9-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
