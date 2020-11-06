---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationsqlserversqldbselecteddb
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
ms.openlocfilehash: 1be43b5d08011a71ec093df2f93c63dd04c6004d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495384"
---
# <span data-ttu-id="46f5d-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span><span class="sxs-lookup"><span data-stu-id="46f5d-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span></span>

## <span data-ttu-id="46f5d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="46f5d-103">Létrehoz egy MigrateSqlServerSqlDbDatabaseInput objektumot, amely információt tartalmaz az áttelepítéshez használt forrás-és céladatbázis-adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="46f5d-103">Creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46f5d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46f5d-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationSqlServerSqlDbSelectedDB [-Id <String>] [-Name <String>] [-TargetDatabaseName <String>]
 [-MakeSourceDbReadOnly] [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="46f5d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="46f5d-105">DESCRIPTION</span></span>
<span data-ttu-id="46f5d-106">Az New-AzureRmDataMigrationSqlServerSqlDbSelectedDB parancsmag létrehoz egy MigrateSqlServerSqlDbDatabaseInput objektumot, amely információkat tartalmaz a forrás-és a célként megadott adatbázisokról, valamint a tábla megfeleltetéséről az áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="46f5d-106">The New-AzureRmDataMigrationSqlServerSqlDbSelectedDB cmdlet creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="46f5d-107">Ezt a parancsmagot a New-AzureRmDataMigrationTask parancsmag paraméterként használhatja.</span><span class="sxs-lookup"><span data-stu-id="46f5d-107">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="46f5d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="46f5d-108">EXAMPLES</span></span>

### <span data-ttu-id="46f5d-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="46f5d-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSqlServerSqlDbSelectedDB  -Name AdventuerWorks2016 -TargetDatabaseName AdventureWorks2016
 -MakeSourceDbReadOnly -TableMap $tableMap
```

<span data-ttu-id="46f5d-110">A fenti példa létrehoz egy MigrateSqlServerSqlDbDatabaseInput objektumot, amely a **AdventureWorks2016** -adatbázis áttelepítéséhez ugyanazt a nevet adja az SQL Azure-adatbázisnak.</span><span class="sxs-lookup"><span data-stu-id="46f5d-110">The above example creates MigrateSqlServerSqlDbDatabaseInput object for migrating the **AdventureWorks2016** database to a SQL Azure database with the same name.</span></span>

## <span data-ttu-id="46f5d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46f5d-111">PARAMETERS</span></span>

### <span data-ttu-id="46f5d-112">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="46f5d-112">-Confirm</span></span>
<span data-ttu-id="46f5d-113">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="46f5d-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f5d-114">-DefaultProfile</span></span>
<span data-ttu-id="46f5d-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46f5d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46f5d-116">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="46f5d-116">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="46f5d-117">Az adatbázis írásvédett állapotba beállítása az áttelepítés előtt</span><span class="sxs-lookup"><span data-stu-id="46f5d-117">Set Database to readonly before migration</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f5d-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46f5d-118">-Name</span></span>
<span data-ttu-id="46f5d-119">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="46f5d-119">The name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f5d-120">-TableMap</span><span class="sxs-lookup"><span data-stu-id="46f5d-120">-TableMap</span></span>
<span data-ttu-id="46f5d-121">a forrás hozzárendelése a cél táblákhoz</span><span class="sxs-lookup"><span data-stu-id="46f5d-121">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f5d-122">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="46f5d-122">-TargetDatabaseName</span></span>
<span data-ttu-id="46f5d-123">A cél-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="46f5d-123">The name of the target Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="46f5d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46f5d-124">INPUTS</span></span>

### <span data-ttu-id="46f5d-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="46f5d-125">None</span></span>


## <span data-ttu-id="46f5d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46f5d-126">OUTPUTS</span></span>

### <span data-ttu-id="46f5d-127">Microsoft. Azure. Management. DataMigration. models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="46f5d-127">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>


## <span data-ttu-id="46f5d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46f5d-128">NOTES</span></span>

## <span data-ttu-id="46f5d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46f5d-129">RELATED LINKS</span></span>


