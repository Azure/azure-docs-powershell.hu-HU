---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 2373a076e6edd97314e08c9170f9584a904ad902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494892"
---
# <span data-ttu-id="d4ab9-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="d4ab9-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="d4ab9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4ab9-102">SYNOPSIS</span></span>
<span data-ttu-id="d4ab9-103">Visszaállíthatja a törölt adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4ab9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4ab9-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4ab9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4ab9-105">DESCRIPTION</span></span>
<span data-ttu-id="d4ab9-106">A **Get-AzureRMSqlDeletedDatabaseBackup** parancsmag egy meghatározott törölt SQL-adatbázis biztonsági másolatát kapja, amelyet visszaállíthat, vagy minden törölt biztonsági másolatot visszaadhat.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="d4ab9-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d4ab9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d4ab9-108">EXAMPLES</span></span>

### <span data-ttu-id="d4ab9-109">Példa 1: az összes törölt adatbázis biztonsági másolatának beolvasása a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="d4ab9-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="d4ab9-110">Ez a parancs minden törölt adatbázis biztonsági másolatát beolvassa a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="d4ab9-111">2. példa: meghatározott törölt adatbázis biztonsági másolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d4ab9-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="d4ab9-112">Ez a parancs a törölt adatbázis biztonsági másolatát a ContosoDatabase-ra vonatkozóan kapja.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="d4ab9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4ab9-113">PARAMETERS</span></span>

### <span data-ttu-id="d4ab9-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d4ab9-114">-DatabaseName</span></span>
<span data-ttu-id="d4ab9-115">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-115">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="d4ab9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4ab9-116">-DefaultProfile</span></span>
<span data-ttu-id="d4ab9-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d4ab9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4ab9-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="d4ab9-118">-DeletionDate</span></span>
<span data-ttu-id="d4ab9-119">Azt a dátumot adja meg **datetime** -objektumként, amelyet az adatbázis töröltek.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="d4ab9-120">A **datetime** objektum beszerzéséhez használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="d4ab9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4ab9-121">-ResourceGroupName</span></span>
<span data-ttu-id="d4ab9-122">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d4ab9-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d4ab9-123">-ServerName</span></span>
<span data-ttu-id="d4ab9-124">Az adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="d4ab9-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4ab9-125">-Confirm</span></span>
<span data-ttu-id="d4ab9-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4ab9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4ab9-127">-WhatIf</span></span>
<span data-ttu-id="d4ab9-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4ab9-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4ab9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4ab9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4ab9-130">CommonParameters</span></span>
<span data-ttu-id="d4ab9-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4ab9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4ab9-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4ab9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4ab9-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4ab9-133">INPUTS</span></span>

### <span data-ttu-id="d4ab9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d4ab9-134">System.String</span></span>

### <span data-ttu-id="d4ab9-135">System. null ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d4ab9-135">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d4ab9-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4ab9-136">OUTPUTS</span></span>

### <span data-ttu-id="d4ab9-137">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="d4ab9-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="d4ab9-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4ab9-138">NOTES</span></span>

## <span data-ttu-id="d4ab9-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4ab9-139">RELATED LINKS</span></span>

[<span data-ttu-id="d4ab9-140">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d4ab9-140">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="d4ab9-141">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d4ab9-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
