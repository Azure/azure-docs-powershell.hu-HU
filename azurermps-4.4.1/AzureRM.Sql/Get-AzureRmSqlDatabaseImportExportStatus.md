---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
ms.openlocfilehash: 5516556553931f7333e007edc6de1b4bd23b288d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672396"
---
# <span data-ttu-id="adab9-101">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="adab9-101">Get-AzureRmSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="adab9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="adab9-102">SYNOPSIS</span></span>
<span data-ttu-id="adab9-103">Egy Azure SQL-adatbázis importálásának és exportálásának részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="adab9-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adab9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="adab9-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseImportExportStatus [-OperationStatusLink] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adab9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="adab9-105">DESCRIPTION</span></span>
<span data-ttu-id="adab9-106">A **Get-AzureRmSqlDatabaseImportExportStatus** parancsmag az bacpac-fájlok egy Azure SQL-adatbázisba való importálását, illetve egy Azure SQL-adatbázis exportálását bacpac-fájlként kapja meg a tároló fiókba.</span><span class="sxs-lookup"><span data-stu-id="adab9-106">The **Get-AzureRmSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>

<span data-ttu-id="adab9-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="adab9-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="adab9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="adab9-108">EXAMPLES</span></span>

### <span data-ttu-id="adab9-109">Példa 1: SQL-adatbázis importálási és exportálási állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="adab9-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="adab9-110">Ez a parancs egy adatbázis importálási vagy exportálási kérelmének állapotát a megadott URL-címen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="adab9-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="adab9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="adab9-111">PARAMETERS</span></span>

### <span data-ttu-id="adab9-112">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="adab9-112">-OperationStatusLink</span></span>
<span data-ttu-id="adab9-113">A New-AzureRmSqlDatabaseExport vagy New-AzureRmSqlDatabaseImport parancsmagokból visszaadott állapot hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="adab9-113">Specifies the status link that is returned from the New-AzureRmSqlDatabaseExport or New-AzureRmSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="adab9-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="adab9-114">-Confirm</span></span>
<span data-ttu-id="adab9-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="adab9-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adab9-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adab9-116">-WhatIf</span></span>
<span data-ttu-id="adab9-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="adab9-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adab9-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="adab9-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adab9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adab9-119">-DefaultProfile</span></span>
<span data-ttu-id="adab9-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="adab9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adab9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adab9-121">CommonParameters</span></span>
<span data-ttu-id="adab9-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="adab9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adab9-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adab9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adab9-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="adab9-124">INPUTS</span></span>

## <span data-ttu-id="adab9-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adab9-125">OUTPUTS</span></span>

## <span data-ttu-id="adab9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="adab9-126">NOTES</span></span>
* <span data-ttu-id="adab9-127">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, adatbázis, MSSQL</span><span class="sxs-lookup"><span data-stu-id="adab9-127">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="adab9-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adab9-128">RELATED LINKS</span></span>

[<span data-ttu-id="adab9-129">Új – AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="adab9-129">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="adab9-130">Új – AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="adab9-130">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="adab9-131">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="adab9-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
