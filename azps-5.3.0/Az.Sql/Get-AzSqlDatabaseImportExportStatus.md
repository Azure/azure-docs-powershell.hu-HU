---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: c64f726e8ff553aa42cb8580cee2349b35de519e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374974"
---
# <span data-ttu-id="b9004-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="b9004-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="b9004-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9004-102">SYNOPSIS</span></span>
<span data-ttu-id="b9004-103">Az Azure SQL-adatbázis importálásának vagy exportálásának részleteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b9004-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="b9004-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b9004-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9004-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b9004-105">DESCRIPTION</span></span>
<span data-ttu-id="b9004-106">A **Get-AzSqlDatabaseImportExportStatus** parancsmag részleteket kap egy tárolási fiókból azure SQL-adatbázisba vagy Egy Azure SQL-adatbázis bacpac-fájlként való exportálásából egy tárfiókba.</span><span class="sxs-lookup"><span data-stu-id="b9004-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="b9004-107">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="b9004-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b9004-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b9004-108">EXAMPLES</span></span>

### <span data-ttu-id="b9004-109">1. példa: SQL-adatbázis importálási és exportálási állapotának lekérte</span><span class="sxs-lookup"><span data-stu-id="b9004-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="b9004-110">Ez a parancs egy adatbázis importálási vagy exportálási kérelmének állapotát kapja meg a megadott URL-címen.</span><span class="sxs-lookup"><span data-stu-id="b9004-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="b9004-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9004-111">PARAMETERS</span></span>

### <span data-ttu-id="b9004-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9004-112">-DefaultProfile</span></span>
<span data-ttu-id="b9004-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b9004-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9004-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="b9004-114">-OperationStatusLink</span></span>
<span data-ttu-id="b9004-115">A parancsmagok által visszaadott állapothivatkozást New-AzSqlDatabaseExport New-AzSqlDatabaseImport adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9004-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="b9004-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9004-116">-Confirm</span></span>
<span data-ttu-id="b9004-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b9004-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9004-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9004-118">-WhatIf</span></span>
<span data-ttu-id="b9004-119">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b9004-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9004-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9004-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9004-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9004-121">CommonParameters</span></span>
<span data-ttu-id="b9004-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9004-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9004-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9004-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9004-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9004-124">INPUTS</span></span>

### <span data-ttu-id="b9004-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b9004-125">System.String</span></span>

## <span data-ttu-id="b9004-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9004-126">OUTPUTS</span></span>

### <span data-ttu-id="b9004-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="b9004-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="b9004-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b9004-128">NOTES</span></span>
* <span data-ttu-id="b9004-129">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, sql, adatbázis, mssql</span><span class="sxs-lookup"><span data-stu-id="b9004-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="b9004-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9004-130">RELATED LINKS</span></span>

[<span data-ttu-id="b9004-131">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="b9004-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="b9004-132">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="b9004-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="b9004-133">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b9004-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
