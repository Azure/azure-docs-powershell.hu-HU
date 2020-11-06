---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 2358383cd7cfdbf547ae14476e788d6919baacd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492158"
---
# <span data-ttu-id="ff481-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="ff481-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="ff481-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff481-102">SYNOPSIS</span></span>
<span data-ttu-id="ff481-103">Visszaállíthatja a törölt adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="ff481-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff481-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff481-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff481-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff481-105">DESCRIPTION</span></span>
<span data-ttu-id="ff481-106">A **Get-AzureRMSqlDeletedDatabaseBackup** parancsmag egy meghatározott törölt SQL-adatbázis biztonsági másolatát kapja, amelyet visszaállíthat, vagy minden törölt biztonsági másolatot visszaadhat.</span><span class="sxs-lookup"><span data-stu-id="ff481-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>

<span data-ttu-id="ff481-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="ff481-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ff481-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ff481-108">EXAMPLES</span></span>

### <span data-ttu-id="ff481-109">Példa 1: az összes törölt adatbázis biztonsági másolatának beolvasása a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="ff481-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="ff481-110">Ez a parancs minden törölt adatbázis biztonsági másolatát beolvassa a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="ff481-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="ff481-111">2. példa: meghatározott törölt adatbázis biztonsági másolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ff481-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="ff481-112">Ez a parancs a törölt adatbázis biztonsági másolatát a ContosoDatabase-ra vonatkozóan kapja.</span><span class="sxs-lookup"><span data-stu-id="ff481-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="ff481-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff481-113">PARAMETERS</span></span>

### <span data-ttu-id="ff481-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ff481-114">-DatabaseName</span></span>
<span data-ttu-id="ff481-115">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff481-115">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff481-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff481-116">-DefaultProfile</span></span>
<span data-ttu-id="ff481-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ff481-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff481-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="ff481-118">-DeletionDate</span></span>
<span data-ttu-id="ff481-119">Azt a dátumot adja meg **datetime** -objektumként, amelyet az adatbázis töröltek.</span><span class="sxs-lookup"><span data-stu-id="ff481-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="ff481-120">A **datetime** objektum beszerzéséhez használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ff481-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff481-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff481-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff481-122">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="ff481-122">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff481-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ff481-123">-ServerName</span></span>
<span data-ttu-id="ff481-124">Az adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff481-124">Specifies the name of the database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff481-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff481-125">-Confirm</span></span>
<span data-ttu-id="ff481-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff481-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff481-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff481-127">-WhatIf</span></span>
<span data-ttu-id="ff481-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff481-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff481-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff481-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff481-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff481-130">CommonParameters</span></span>
<span data-ttu-id="ff481-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff481-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff481-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff481-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff481-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff481-133">INPUTS</span></span>

### <span data-ttu-id="ff481-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="ff481-134">None</span></span>
<span data-ttu-id="ff481-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ff481-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff481-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff481-136">OUTPUTS</span></span>

## <span data-ttu-id="ff481-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff481-137">NOTES</span></span>

## <span data-ttu-id="ff481-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff481-138">RELATED LINKS</span></span>

[<span data-ttu-id="ff481-139">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff481-139">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="ff481-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="ff481-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
