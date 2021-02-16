---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 9765afd55ea94bda672d5e1ce43ac3d8d535510d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165811"
---
# <span data-ttu-id="0495a-101">Get-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="0495a-101">Get-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="0495a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0495a-102">SYNOPSIS</span></span>
<span data-ttu-id="0495a-103">Beolvassa a különálló visszaállítási pontokat, amelyekből az SQL-adattárhely visszaállítható.</span><span class="sxs-lookup"><span data-stu-id="0495a-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

## <span data-ttu-id="0495a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0495a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRestorePoint [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0495a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0495a-105">DESCRIPTION</span></span>
<span data-ttu-id="0495a-106">A **Get-AzSqlDatabaseRestorePoint** parancsmag beolvassa az Azure SQL Data Warehouse helyreállítható visszaállítási pontjait.</span><span class="sxs-lookup"><span data-stu-id="0495a-106">The **Get-AzSqlDatabaseRestorePoint** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="0495a-107">Azure SQL-adatbázis esetén a visszaállítási ablak folyamatos.</span><span class="sxs-lookup"><span data-stu-id="0495a-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="0495a-108">Ez azt jelenti, hogy az adatbázis biztonsági mentési megőrzési időszakának bármely pontját felhasználhatja visszaállítási pontként.</span><span class="sxs-lookup"><span data-stu-id="0495a-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="0495a-109">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="0495a-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0495a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0495a-110">EXAMPLES</span></span>

### <span data-ttu-id="0495a-111">1. példa: Az összes visszaállítási pont lekérte</span><span class="sxs-lookup"><span data-stu-id="0495a-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="0495a-112">Ez a parancs visszaadja az Adatbázis01 nevű Azure SQL-adatbázis összes rendelkezésre álló visszaállítási pontot.</span><span class="sxs-lookup"><span data-stu-id="0495a-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="0495a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0495a-113">PARAMETERS</span></span>

### <span data-ttu-id="0495a-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0495a-114">-DatabaseName</span></span>
<span data-ttu-id="0495a-115">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0495a-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="0495a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0495a-116">-DefaultProfile</span></span>
<span data-ttu-id="0495a-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0495a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0495a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0495a-118">-ResourceGroupName</span></span>
<span data-ttu-id="0495a-119">Annak az erőforráscsoportnak a neve, amelyhez az SQL-adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="0495a-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="0495a-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0495a-120">-ServerName</span></span>
<span data-ttu-id="0495a-121">Az adatbázist tartalmazó AzureSQL-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0495a-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="0495a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0495a-122">-Confirm</span></span>
<span data-ttu-id="0495a-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0495a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0495a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0495a-124">-WhatIf</span></span>
<span data-ttu-id="0495a-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0495a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0495a-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0495a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0495a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0495a-127">CommonParameters</span></span>
<span data-ttu-id="0495a-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0495a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0495a-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0495a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0495a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0495a-130">INPUTS</span></span>

### <span data-ttu-id="0495a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0495a-131">System.String</span></span>

## <span data-ttu-id="0495a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0495a-132">OUTPUTS</span></span>

### <span data-ttu-id="0495a-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="0495a-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="0495a-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0495a-134">NOTES</span></span>

## <span data-ttu-id="0495a-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0495a-135">RELATED LINKS</span></span>
