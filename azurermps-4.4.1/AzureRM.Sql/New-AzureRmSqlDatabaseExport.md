---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: f7ede8432f8e833b3d309925daab591889836257
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680464"
---
# <span data-ttu-id="1e3fb-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="1e3fb-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="1e3fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e3fb-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3fb-103">Azure SQL-adatbázis exportálása. bacpac fájlként a tároló fiókba.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e3fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e3fb-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e3fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e3fb-105">DESCRIPTION</span></span>
<span data-ttu-id="1e3fb-106">A **New-AzureRmSqlDatabaseExport** parancsmag az Azure SQL-adatbázist. bacpac fájlként exportálja a tároló fiókba.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="1e3fb-107">Előfordulhat, hogy az exportálási adatbázis-állapot kérése elküldve van a kérés állapotára vonatkozó adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-107">The get export database status request may be sent to retrieve status information for this request.</span></span>

<span data-ttu-id="1e3fb-108">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1e3fb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1e3fb-109">EXAMPLES</span></span>

### <span data-ttu-id="1e3fb-110">1. példa: exportálási kérés létrehozása adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="1e3fb-110">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
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

<span data-ttu-id="1e3fb-111">Ez a parancs a megadott adatbázis exportálási kérését hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="1e3fb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e3fb-112">PARAMETERS</span></span>

### <span data-ttu-id="1e3fb-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="1e3fb-113">-AdministratorLogin</span></span>
<span data-ttu-id="1e3fb-114">Az SQL-rendszergazda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="1e3fb-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="1e3fb-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="1e3fb-116">Az SQL-rendszergazda jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="1e3fb-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="1e3fb-117">-AuthenticationType</span></span>
<span data-ttu-id="1e3fb-118">A kiszolgáló eléréséhez használt hitelesítés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="1e3fb-119">Az alapértelmezett érték az SQL, ha nincs beállítva a hitelesítési típus.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-119">The default value is SQL if no authentication type is set.</span></span>

<span data-ttu-id="1e3fb-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="1e3fb-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e3fb-121">SQL.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-121">Sql.</span></span>
<span data-ttu-id="1e3fb-122">SQL-hitelesítés.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-122">SQL authentication.</span></span>
<span data-ttu-id="1e3fb-123">Adja meg a *AdministratorLogin* és a *AdministratorLoginPassword* az SQL-rendszergazdai felhasználónevével és jelszavával.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="1e3fb-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-124">ADPassword.</span></span>
<span data-ttu-id="1e3fb-125">Azure Active Directory-hitelesítés</span><span class="sxs-lookup"><span data-stu-id="1e3fb-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="1e3fb-126">Állítsa be a *AdministratorLogin* és a *ADMINISTRATORLOGINPASSWORD* az Azure ad Administrator felhasználónevére és jelszavára.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>

<span data-ttu-id="1e3fb-127">Ez a paraméter csak SQL Database V12-kiszolgálókon érhető el.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="1e3fb-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1e3fb-128">-DatabaseName</span></span>
<span data-ttu-id="1e3fb-129">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="1e3fb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e3fb-130">-ResourceGroupName</span></span>
<span data-ttu-id="1e3fb-131">Az SQL adatbázis-kiszolgáló erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-131">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="1e3fb-132">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1e3fb-132">-ServerName</span></span>
<span data-ttu-id="1e3fb-133">Az SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-133">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="1e3fb-134">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="1e3fb-134">-StorageKey</span></span>
<span data-ttu-id="1e3fb-135">A tárolási fiók elérési kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-135">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="1e3fb-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="1e3fb-136">-StorageKeyType</span></span>
<span data-ttu-id="1e3fb-137">A tárolási fiókhoz tartozó hozzáférési kulcs típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-137">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="1e3fb-138">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="1e3fb-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e3fb-139">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-139">StorageAccessKey.</span></span>
<span data-ttu-id="1e3fb-140">Ez az érték a tárolási fiók kulcsát használja.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-140">This value uses a storage account key.</span></span> 
- <span data-ttu-id="1e3fb-141">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-141">SharedAccessKey.</span></span>
<span data-ttu-id="1e3fb-142">Ez az érték egy megosztott Access-aláírást (SAS) használ.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-142">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="1e3fb-143">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="1e3fb-143">-StorageUri</span></span>
<span data-ttu-id="1e3fb-144">A blob hivatkozást adja meg URL-ként az. bacpac fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-144">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="1e3fb-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1e3fb-145">-Confirm</span></span>
<span data-ttu-id="1e3fb-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e3fb-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e3fb-147">-WhatIf</span></span>
<span data-ttu-id="1e3fb-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e3fb-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e3fb-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e3fb-150">-DefaultProfile</span></span>
<span data-ttu-id="1e3fb-151">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e3fb-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e3fb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3fb-152">CommonParameters</span></span>
<span data-ttu-id="1e3fb-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e3fb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3fb-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e3fb-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3fb-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e3fb-155">INPUTS</span></span>

## <span data-ttu-id="1e3fb-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e3fb-156">OUTPUTS</span></span>

### <span data-ttu-id="1e3fb-157">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="1e3fb-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="1e3fb-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e3fb-158">NOTES</span></span>
* <span data-ttu-id="1e3fb-159">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, adatbázis, MSSQL</span><span class="sxs-lookup"><span data-stu-id="1e3fb-159">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="1e3fb-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e3fb-160">RELATED LINKS</span></span>

[<span data-ttu-id="1e3fb-161">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="1e3fb-161">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="1e3fb-162">Új – AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="1e3fb-162">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="1e3fb-163">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="1e3fb-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
