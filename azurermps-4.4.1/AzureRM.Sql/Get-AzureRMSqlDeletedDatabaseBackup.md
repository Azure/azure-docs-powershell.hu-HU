---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 9ffccf1122ac9919758883100eacce7933f5fea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494631"
---
# <span data-ttu-id="cbcf7-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="cbcf7-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="cbcf7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cbcf7-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcf7-103">Visszaállíthatja a törölt adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbcf7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cbcf7-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbcf7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cbcf7-105">DESCRIPTION</span></span>
<span data-ttu-id="cbcf7-106">A **Get-AzureRMSqlDeletedDatabaseBackup** parancsmag egy meghatározott törölt SQL-adatbázis biztonsági másolatát kapja, amelyet visszaállíthat, vagy minden törölt biztonsági másolatot visszaadhat.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>

<span data-ttu-id="cbcf7-107">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cbcf7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cbcf7-108">EXAMPLES</span></span>

### <span data-ttu-id="cbcf7-109">Példa 1: az összes törölt adatbázis biztonsági másolatának beolvasása a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="cbcf7-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="cbcf7-110">Ez a parancs minden törölt adatbázis biztonsági másolatát beolvassa a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="cbcf7-111">2. példa: meghatározott törölt adatbázis biztonsági másolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="cbcf7-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="cbcf7-112">Ez a parancs a törölt adatbázis biztonsági másolatát a ContosoDatabase-ra vonatkozóan kapja.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="cbcf7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cbcf7-113">PARAMETERS</span></span>

### <span data-ttu-id="cbcf7-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cbcf7-114">-DatabaseName</span></span>
<span data-ttu-id="cbcf7-115">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-115">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="cbcf7-116">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="cbcf7-116">-DeletionDate</span></span>
<span data-ttu-id="cbcf7-117">Azt a dátumot adja meg **datetime** -objektumként, amelyet az adatbázis töröltek.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-117">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="cbcf7-118">A **datetime** objektum beszerzéséhez használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-118">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="cbcf7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbcf7-119">-ResourceGroupName</span></span>
<span data-ttu-id="cbcf7-120">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-120">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="cbcf7-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="cbcf7-121">-ServerName</span></span>
<span data-ttu-id="cbcf7-122">Az adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-122">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="cbcf7-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cbcf7-123">-Confirm</span></span>
<span data-ttu-id="cbcf7-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbcf7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbcf7-125">-WhatIf</span></span>
<span data-ttu-id="cbcf7-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbcf7-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbcf7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbcf7-128">-DefaultProfile</span></span>
<span data-ttu-id="cbcf7-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbcf7-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbcf7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcf7-130">CommonParameters</span></span>
<span data-ttu-id="cbcf7-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cbcf7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcf7-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbcf7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcf7-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbcf7-133">INPUTS</span></span>

## <span data-ttu-id="cbcf7-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbcf7-134">OUTPUTS</span></span>

## <span data-ttu-id="cbcf7-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cbcf7-135">NOTES</span></span>

## <span data-ttu-id="cbcf7-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbcf7-136">RELATED LINKS</span></span>

[<span data-ttu-id="cbcf7-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cbcf7-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="cbcf7-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="cbcf7-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
