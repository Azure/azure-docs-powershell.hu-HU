---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: c64f726e8ff553aa42cb8580cee2349b35de519e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011547"
---
# <span data-ttu-id="c109e-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="c109e-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="c109e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c109e-102">SYNOPSIS</span></span>
<span data-ttu-id="c109e-103">Egy Azure SQL-adatbázis importálásának és exportálásának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c109e-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="c109e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c109e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c109e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c109e-105">DESCRIPTION</span></span>
<span data-ttu-id="c109e-106">A **Get-AzSqlDatabaseImportExportStatus** parancsmag az bacpac-fájlok egy Azure SQL-adatbázisba való importálását, illetve egy Azure SQL-adatbázis exportálását bacpac-fájlként kapja meg a tároló fiókba.</span><span class="sxs-lookup"><span data-stu-id="c109e-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="c109e-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="c109e-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c109e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="c109e-108">EXAMPLES</span></span>

### <span data-ttu-id="c109e-109">Példa 1: SQL-adatbázis importálási és exportálási állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c109e-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="c109e-110">Ez a parancs egy adatbázis importálási vagy exportálási kérelmének állapotát a megadott URL-címen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c109e-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="c109e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c109e-111">PARAMETERS</span></span>

### <span data-ttu-id="c109e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c109e-112">-DefaultProfile</span></span>
<span data-ttu-id="c109e-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c109e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c109e-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="c109e-114">-OperationStatusLink</span></span>
<span data-ttu-id="c109e-115">A New-AzSqlDatabaseExport vagy New-AzSqlDatabaseImport parancsmagokból visszaadott állapot hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c109e-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="c109e-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c109e-116">-Confirm</span></span>
<span data-ttu-id="c109e-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c109e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c109e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c109e-118">-WhatIf</span></span>
<span data-ttu-id="c109e-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c109e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c109e-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c109e-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c109e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c109e-121">CommonParameters</span></span>
<span data-ttu-id="c109e-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c109e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c109e-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c109e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c109e-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c109e-124">INPUTS</span></span>

### <span data-ttu-id="c109e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c109e-125">System.String</span></span>

## <span data-ttu-id="c109e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c109e-126">OUTPUTS</span></span>

### <span data-ttu-id="c109e-127">Microsoft. Azure. Command. SQL. ImportExport. Model. AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="c109e-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="c109e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c109e-128">NOTES</span></span>
* <span data-ttu-id="c109e-129">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, adatbázis, MSSQL</span><span class="sxs-lookup"><span data-stu-id="c109e-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="c109e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c109e-130">RELATED LINKS</span></span>

[<span data-ttu-id="c109e-131">Új – AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="c109e-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="c109e-132">Új – AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="c109e-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="c109e-133">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="c109e-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
