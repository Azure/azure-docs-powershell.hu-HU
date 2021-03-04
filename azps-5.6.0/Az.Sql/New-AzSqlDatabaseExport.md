---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 198692c73609f6e3e88be0ccbe270c60bc679020
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932218"
---
# <span data-ttu-id="fac18-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="fac18-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="fac18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fac18-102">SYNOPSIS</span></span>
<span data-ttu-id="fac18-103">Egy Azure SQL-adatbázist .bacpac fájlként exportál egy tárfiókba.</span><span class="sxs-lookup"><span data-stu-id="fac18-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="fac18-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fac18-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fac18-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fac18-105">DESCRIPTION</span></span>
<span data-ttu-id="fac18-106">A **New-AzSqlDatabaseExport parancsmag** .bacpac fájlként exportál egy Azure SQL-adatbázist egy tárfiókba.</span><span class="sxs-lookup"><span data-stu-id="fac18-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="fac18-107">Az exportálási adatbázis állapotkérése elküldhető a kérelem állapotinformációinak lekérése érdekében.</span><span class="sxs-lookup"><span data-stu-id="fac18-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="fac18-108">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="fac18-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fac18-109">A parancsmag használatának érdekében az Azure SQL Server tűzfalát "Az Azure-szolgáltatások és erőforrások hozzáférésének engedélyezése a kiszolgálóhoz" beállítással kell konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="fac18-109">In order to make use of this cmdlet the firewall on the Azure SQL Server will need to be configured to "Allow Azure services and resources to access this server".</span></span> <span data-ttu-id="fac18-110">Ha ez nincs beállítva, akkor a rendszer átjáróidőtúllépési hibákat fog tapasztalni.</span><span class="sxs-lookup"><span data-stu-id="fac18-110">If this is not configured then GatewayTimeout errors will be experienced.</span></span>

## <span data-ttu-id="fac18-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fac18-111">EXAMPLES</span></span>

### <span data-ttu-id="fac18-112">1. példa: Adatbázis exportálási kérelmének létrehozása</span><span class="sxs-lookup"><span data-stu-id="fac18-112">Example 1: Create an export request for a database</span></span>
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

<span data-ttu-id="fac18-113">Ez a parancs egy exportálási kérelmet hoz létre a megadott adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="fac18-113">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="fac18-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fac18-114">PARAMETERS</span></span>

### <span data-ttu-id="fac18-115">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="fac18-115">-AdministratorLogin</span></span>
<span data-ttu-id="fac18-116">Az SQL-rendszergazda nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fac18-116">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="fac18-117">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="fac18-117">-AdministratorLoginPassword</span></span>
<span data-ttu-id="fac18-118">Az SQL-rendszergazda jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fac18-118">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="fac18-119">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="fac18-119">-AuthenticationType</span></span>
<span data-ttu-id="fac18-120">A kiszolgáló eléréséhez használt hitelesítés típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fac18-120">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="fac18-121">Az alapértelmezett érték az SQL, ha nincs beállítva hitelesítési típus.</span><span class="sxs-lookup"><span data-stu-id="fac18-121">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="fac18-122">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="fac18-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fac18-123">Sql.</span><span class="sxs-lookup"><span data-stu-id="fac18-123">Sql.</span></span>
<span data-ttu-id="fac18-124">SQL-hitelesítés.</span><span class="sxs-lookup"><span data-stu-id="fac18-124">SQL authentication.</span></span>
<span data-ttu-id="fac18-125">Állítsa be *a AdministratorLogin és* *a AdministratorLoginPassword* parancsot az SQL-rendszergazda felhasználónevére és jelszavára.</span><span class="sxs-lookup"><span data-stu-id="fac18-125">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="fac18-126">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="fac18-126">ADPassword.</span></span>
<span data-ttu-id="fac18-127">Azure Active Directory-hitelesítés.</span><span class="sxs-lookup"><span data-stu-id="fac18-127">Azure Active Directory authentication.</span></span>
<span data-ttu-id="fac18-128">Állítsa *be a AdministratorLogin* és *a AdministratorLoginPassword* nevet az Azure AD rendszergazdai felhasználónevére és jelszavára.</span><span class="sxs-lookup"><span data-stu-id="fac18-128">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="fac18-129">Ez a paraméter csak SQL Database V12-kiszolgálókon érhető el.</span><span class="sxs-lookup"><span data-stu-id="fac18-129">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="fac18-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fac18-130">-DatabaseName</span></span>
<span data-ttu-id="fac18-131">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fac18-131">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="fac18-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fac18-132">-DefaultProfile</span></span>
<span data-ttu-id="fac18-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fac18-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fac18-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fac18-134">-ResourceGroupName</span></span>
<span data-ttu-id="fac18-135">Az SQL-adatbázis-kiszolgáló erőforráscsoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fac18-135">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="fac18-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fac18-136">-ServerName</span></span>
<span data-ttu-id="fac18-137">Az SQL-adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fac18-137">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="fac18-138">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="fac18-138">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="fac18-139">Az SQL Server-erőforrásazonosító a személyes hivatkozás létrehozásához</span><span class="sxs-lookup"><span data-stu-id="fac18-139">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="fac18-140">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="fac18-140">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="fac18-141">A tárfiók erőforrás-azonosítója privát hivatkozás létrehozásához</span><span class="sxs-lookup"><span data-stu-id="fac18-141">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="fac18-142">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="fac18-142">-StorageKey</span></span>
<span data-ttu-id="fac18-143">A tárfiók hozzáférési kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fac18-143">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="fac18-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="fac18-144">-StorageKeyType</span></span>
<span data-ttu-id="fac18-145">A tárfiók hozzáférési kulcsának típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fac18-145">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="fac18-146">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="fac18-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fac18-147">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="fac18-147">StorageAccessKey.</span></span>
<span data-ttu-id="fac18-148">Ez az érték egy tárfiókkulcsot használ.</span><span class="sxs-lookup"><span data-stu-id="fac18-148">This value uses a storage account key.</span></span> 
- <span data-ttu-id="fac18-149">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="fac18-149">SharedAccessKey.</span></span>
<span data-ttu-id="fac18-150">Ez az érték egy SAS-kulcsot használ.</span><span class="sxs-lookup"><span data-stu-id="fac18-150">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="fac18-151">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="fac18-151">-StorageUri</span></span>
<span data-ttu-id="fac18-152">A .bacpac fájl blobhivatkozását adja meg URL-ként.</span><span class="sxs-lookup"><span data-stu-id="fac18-152">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="fac18-153">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="fac18-153">-UseNetworkIsolation</span></span>
<span data-ttu-id="fac18-154">Ha be van állítva, személyes hivatkozást hoz létre a tárfiókhoz és/vagy az SQL-kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="fac18-154">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="fac18-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fac18-155">-Confirm</span></span>
<span data-ttu-id="fac18-156">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fac18-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fac18-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fac18-157">-WhatIf</span></span>
<span data-ttu-id="fac18-158">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fac18-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fac18-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fac18-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fac18-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fac18-160">CommonParameters</span></span>
<span data-ttu-id="fac18-161">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fac18-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fac18-162">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fac18-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fac18-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fac18-163">INPUTS</span></span>

### <span data-ttu-id="fac18-164">System.String</span><span class="sxs-lookup"><span data-stu-id="fac18-164">System.String</span></span>

## <span data-ttu-id="fac18-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fac18-165">OUTPUTS</span></span>

### <span data-ttu-id="fac18-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="fac18-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="fac18-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fac18-167">NOTES</span></span>
* <span data-ttu-id="fac18-168">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, sql, adatbázis, mssql</span><span class="sxs-lookup"><span data-stu-id="fac18-168">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="fac18-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fac18-169">RELATED LINKS</span></span>

[<span data-ttu-id="fac18-170">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="fac18-170">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="fac18-171">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="fac18-171">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="fac18-172">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fac18-172">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
