---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182819"
---
# <span data-ttu-id="81bd4-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="81bd4-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="81bd4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="81bd4-103">Adatbázis-beállítás létrehozása az áttelepítés mongoDb-áttelepítéshez</span><span class="sxs-lookup"><span data-stu-id="81bd4-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="81bd4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81bd4-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="81bd4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="81bd4-105">DESCRIPTION</span></span>
<span data-ttu-id="81bd4-106">A New-AzDataMigrationMongoDbDatabaseSetting parancsmag létrehoz egy áttelepítési beállítás objektumot, amely az átviteli sebesség és a törlés működését adja meg.</span><span class="sxs-lookup"><span data-stu-id="81bd4-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="81bd4-107">A kimenet egy fontos érték párja a gyűjtemény nevével és a beállítás értékével, amelyet az áttelepítési feladat meghívásakor használhat.</span><span class="sxs-lookup"><span data-stu-id="81bd4-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="81bd4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="81bd4-108">EXAMPLES</span></span>

### <span data-ttu-id="81bd4-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="81bd4-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="81bd4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81bd4-110">PARAMETERS</span></span>

### <span data-ttu-id="81bd4-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81bd4-111">-Name</span></span>
<span data-ttu-id="81bd4-112">Az adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="81bd4-112">Name of the database</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="81bd4-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="81bd4-113">-TargetRequestUnit</span></span>
<span data-ttu-id="81bd4-114">A dedikált adatbázis-szint Request Unit érték</span><span class="sxs-lookup"><span data-stu-id="81bd4-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="81bd4-115">Ha nincs beállítva, a gyűjtemény az RU megosztott adatbázisát használja.</span><span class="sxs-lookup"><span data-stu-id="81bd4-115">If not set, that collection uses shared database RU.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bd4-116">-Gyűjtemények</span><span class="sxs-lookup"><span data-stu-id="81bd4-116">-Collections</span></span>
<span data-ttu-id="81bd4-117">New-AzureRmDmsMongoDbDatabaseSetting hívás által visszaadott objektumok MongoDb-gyűjteményének tömbje.</span><span class="sxs-lookup"><span data-stu-id="81bd4-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

```yaml
Type: System.Collections.Generic.KeyValuePair<string, MongoDbCollectionSettings>[]
Parameter Sets: (All)
Aliases: colls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81bd4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bd4-118">CommonParameters</span></span>
<span data-ttu-id="81bd4-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81bd4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bd4-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81bd4-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bd4-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81bd4-121">INPUTS</span></span>

### <span data-ttu-id="81bd4-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="81bd4-122">None</span></span>

## <span data-ttu-id="81bd4-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81bd4-123">OUTPUTS</span></span>

### <span data-ttu-id="81bd4-124">Microsoft. Azure. Command. DataMigration. models. MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="81bd4-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="81bd4-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81bd4-125">NOTES</span></span>

## <span data-ttu-id="81bd4-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81bd4-126">RELATED LINKS</span></span>
