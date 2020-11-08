---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 9765afd55ea94bda672d5e1ce43ac3d8d535510d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011627"
---
# <span data-ttu-id="78f0e-101">Get-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="78f0e-101">Get-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="78f0e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="78f0e-103">Lekérdezi az SQL-adattárház visszaállítási pontjait.</span><span class="sxs-lookup"><span data-stu-id="78f0e-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

## <span data-ttu-id="78f0e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78f0e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRestorePoint [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78f0e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="78f0e-105">DESCRIPTION</span></span>
<span data-ttu-id="78f0e-106">A **Get-AzSqlDatabaseRestorePoint** parancsmag kikeresi azokat a különálló visszaállítási pontokat, amelyeket egy Azure SQL-adattárházból lehet visszaállítani.</span><span class="sxs-lookup"><span data-stu-id="78f0e-106">The **Get-AzSqlDatabaseRestorePoint** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="78f0e-107">Azure SQL-adatbázis esetén a visszaállítási ablak folytonos.</span><span class="sxs-lookup"><span data-stu-id="78f0e-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="78f0e-108">Ez azt jelenti, hogy az adatbázis biztonsági adatmegőrzési időszakában bármely időpontban használható visszaállítási pontként.</span><span class="sxs-lookup"><span data-stu-id="78f0e-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="78f0e-109">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="78f0e-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="78f0e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="78f0e-110">EXAMPLES</span></span>

### <span data-ttu-id="78f0e-111">Példa 1: az összes visszaállítási pont beolvasása</span><span class="sxs-lookup"><span data-stu-id="78f0e-111">Example 1: Get all restore points</span></span>
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

<span data-ttu-id="78f0e-112">Ez a parancs a Database01 nevű Azure SQL-adatbázis minden elérhető visszaállítási pontját visszaadja.</span><span class="sxs-lookup"><span data-stu-id="78f0e-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="78f0e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78f0e-113">PARAMETERS</span></span>

### <span data-ttu-id="78f0e-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="78f0e-114">-DatabaseName</span></span>
<span data-ttu-id="78f0e-115">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78f0e-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="78f0e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f0e-116">-DefaultProfile</span></span>
<span data-ttu-id="78f0e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="78f0e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78f0e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f0e-118">-ResourceGroupName</span></span>
<span data-ttu-id="78f0e-119">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="78f0e-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="78f0e-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="78f0e-120">-ServerName</span></span>
<span data-ttu-id="78f0e-121">Az adatbázist tároló AzureSQL-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78f0e-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="78f0e-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="78f0e-122">-Confirm</span></span>
<span data-ttu-id="78f0e-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="78f0e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78f0e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f0e-124">-WhatIf</span></span>
<span data-ttu-id="78f0e-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="78f0e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78f0e-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78f0e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78f0e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f0e-127">CommonParameters</span></span>
<span data-ttu-id="78f0e-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78f0e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f0e-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="78f0e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f0e-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78f0e-130">INPUTS</span></span>

### <span data-ttu-id="78f0e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="78f0e-131">System.String</span></span>

## <span data-ttu-id="78f0e-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78f0e-132">OUTPUTS</span></span>

### <span data-ttu-id="78f0e-133">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="78f0e-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="78f0e-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78f0e-134">NOTES</span></span>

## <span data-ttu-id="78f0e-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78f0e-135">RELATED LINKS</span></span>
