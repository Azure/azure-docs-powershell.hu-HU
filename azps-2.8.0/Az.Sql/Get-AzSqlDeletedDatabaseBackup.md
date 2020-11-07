---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: ebe9b48b5495b1357086e189b20c2b047a99556d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839217"
---
# <span data-ttu-id="29e45-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="29e45-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="29e45-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29e45-102">SYNOPSIS</span></span>
<span data-ttu-id="29e45-103">Visszaállíthatja a törölt adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="29e45-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="29e45-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29e45-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29e45-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="29e45-105">DESCRIPTION</span></span>
<span data-ttu-id="29e45-106">A **Get-AzSqlDeletedDatabaseBackup** parancsmag egy meghatározott törölt SQL-adatbázis biztonsági másolatát kapja, amelyet visszaállíthat, vagy minden törölt biztonsági másolatot visszaadhat.</span><span class="sxs-lookup"><span data-stu-id="29e45-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="29e45-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="29e45-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="29e45-108">Példák</span><span class="sxs-lookup"><span data-stu-id="29e45-108">EXAMPLES</span></span>

### <span data-ttu-id="29e45-109">Példa 1: az összes törölt adatbázis biztonsági másolatának beolvasása a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="29e45-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="29e45-110">Ez a parancs minden törölt adatbázis biztonsági másolatát beolvassa a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="29e45-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="29e45-111">2. példa: meghatározott törölt adatbázis biztonsági másolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="29e45-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="29e45-112">Ez a parancs a törölt adatbázis biztonsági másolatát a ContosoDatabase-ra vonatkozóan kapja.</span><span class="sxs-lookup"><span data-stu-id="29e45-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="29e45-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29e45-113">PARAMETERS</span></span>

### <span data-ttu-id="29e45-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29e45-114">-DatabaseName</span></span>
<span data-ttu-id="29e45-115">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29e45-115">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e45-116">-DefaultProfile</span></span>
<span data-ttu-id="29e45-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="29e45-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29e45-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="29e45-118">-DeletionDate</span></span>
<span data-ttu-id="29e45-119">Azt a dátumot adja meg **datetime** -objektumként, amelyet az adatbázis töröltek.</span><span class="sxs-lookup"><span data-stu-id="29e45-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="29e45-120">A **datetime** objektum beszerzéséhez használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="29e45-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e45-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29e45-121">-ResourceGroupName</span></span>
<span data-ttu-id="29e45-122">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="29e45-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="29e45-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="29e45-123">-ServerName</span></span>
<span data-ttu-id="29e45-124">Az adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29e45-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="29e45-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29e45-125">-Confirm</span></span>
<span data-ttu-id="29e45-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29e45-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29e45-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29e45-127">-WhatIf</span></span>
<span data-ttu-id="29e45-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29e45-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29e45-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29e45-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29e45-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e45-130">CommonParameters</span></span>
<span data-ttu-id="29e45-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29e45-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e45-132">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="29e45-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e45-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29e45-133">INPUTS</span></span>

### <span data-ttu-id="29e45-134">System. String</span><span class="sxs-lookup"><span data-stu-id="29e45-134">System.String</span></span>

### <span data-ttu-id="29e45-135">System. null ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="29e45-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="29e45-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29e45-136">OUTPUTS</span></span>

### <span data-ttu-id="29e45-137">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="29e45-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="29e45-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29e45-138">NOTES</span></span>

## <span data-ttu-id="29e45-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29e45-139">RELATED LINKS</span></span>

[<span data-ttu-id="29e45-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="29e45-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="29e45-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="29e45-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
