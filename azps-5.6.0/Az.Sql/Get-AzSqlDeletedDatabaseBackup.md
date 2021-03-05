---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: f64f7f7e16f18c9213c77df2903c17d8e7ea4ae1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999686"
---
# <span data-ttu-id="bb6a8-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="bb6a8-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="bb6a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="bb6a8-103">Visszaállítható törölt adatbázist kap.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="bb6a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bb6a8-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb6a8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bb6a8-105">DESCRIPTION</span></span>
<span data-ttu-id="bb6a8-106">A **Get-AzSqlDeletedDatabaseBackup** parancsmag egy megadott törölt SQL-adatbázis biztonsági másolatát kapja, amely visszaállítható, illetve az összes visszaállítható törölt biztonsági másolat.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="bb6a8-107">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="bb6a8-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bb6a8-108">EXAMPLES</span></span>

### <span data-ttu-id="bb6a8-109">1. példa: Az összes törölt adatbázis biztonsági mentése egy kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="bb6a8-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="bb6a8-110">Ez a parancs az összes törölt adatbázis biztonsági másolatát lekérte egy kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="bb6a8-111">2. példa: Törölt adatbázis biztonsági másolatának létrehozása</span><span class="sxs-lookup"><span data-stu-id="bb6a8-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="bb6a8-112">Ez a parancs a ContosoDatabase törölt adatbázisának biztonsági másolatát kapja vissza.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="bb6a8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb6a8-113">PARAMETERS</span></span>

### <span data-ttu-id="bb6a8-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bb6a8-114">-DatabaseName</span></span>
<span data-ttu-id="bb6a8-115">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-115">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="bb6a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb6a8-116">-DefaultProfile</span></span>
<span data-ttu-id="bb6a8-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bb6a8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb6a8-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="bb6a8-118">-DeletionDate</span></span>
<span data-ttu-id="bb6a8-119">Az adatbázis törlési dátumát adja meg **DateTime-objektumként.**</span><span class="sxs-lookup"><span data-stu-id="bb6a8-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="bb6a8-120">**DateTime-objektum** betöltéshez használja a Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="bb6a8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb6a8-121">-ResourceGroupName</span></span>
<span data-ttu-id="bb6a8-122">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="bb6a8-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bb6a8-123">-ServerName</span></span>
<span data-ttu-id="bb6a8-124">Az adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="bb6a8-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb6a8-125">-Confirm</span></span>
<span data-ttu-id="bb6a8-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb6a8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb6a8-127">-WhatIf</span></span>
<span data-ttu-id="bb6a8-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb6a8-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb6a8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb6a8-130">CommonParameters</span></span>
<span data-ttu-id="bb6a8-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb6a8-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb6a8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb6a8-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb6a8-133">INPUTS</span></span>

### <span data-ttu-id="bb6a8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bb6a8-134">System.String</span></span>

### <span data-ttu-id="bb6a8-135">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bb6a8-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bb6a8-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb6a8-136">OUTPUTS</span></span>

### <span data-ttu-id="bb6a8-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="bb6a8-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="bb6a8-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bb6a8-138">NOTES</span></span>

## <span data-ttu-id="bb6a8-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb6a8-139">RELATED LINKS</span></span>

[<span data-ttu-id="bb6a8-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bb6a8-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="bb6a8-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bb6a8-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
