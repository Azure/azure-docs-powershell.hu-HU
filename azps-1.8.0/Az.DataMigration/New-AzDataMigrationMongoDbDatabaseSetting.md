---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: d05b6507ea8e1d5244e23ab7b8b6222848a1d088
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836226"
---
# <span data-ttu-id="4593d-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="4593d-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="4593d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4593d-102">SYNOPSIS</span></span>
<span data-ttu-id="4593d-103">Adatbázis-beállítás létrehozása az áttelepítés mongoDb-áttelepítéshez</span><span class="sxs-lookup"><span data-stu-id="4593d-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="4593d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4593d-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="4593d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4593d-105">DESCRIPTION</span></span>
<span data-ttu-id="4593d-106">A New-AzDataMigrationMongoDbDatabaseSetting parancsmag létrehoz egy áttelepítési beállítás objektumot, amely az átviteli sebesség és a törlés működését adja meg.</span><span class="sxs-lookup"><span data-stu-id="4593d-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="4593d-107">A kimenet egy fontos érték párja a gyűjtemény nevével és a beállítás értékével, amelyet az áttelepítési feladat meghívásakor használhat.</span><span class="sxs-lookup"><span data-stu-id="4593d-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="4593d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4593d-108">EXAMPLES</span></span>

### <span data-ttu-id="4593d-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4593d-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="4593d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4593d-110">PARAMETERS</span></span>

### <span data-ttu-id="4593d-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4593d-111">-Name</span></span>
<span data-ttu-id="4593d-112">Az adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="4593d-112">Name of the database</span></span>

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
### <span data-ttu-id="4593d-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="4593d-113">-TargetRequestUnit</span></span>
<span data-ttu-id="4593d-114">A dedikált adatbázis-szint Request Unit érték</span><span class="sxs-lookup"><span data-stu-id="4593d-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="4593d-115">Ha nincs beállítva, a gyűjtemény az RU megosztott adatbázisát használja.</span><span class="sxs-lookup"><span data-stu-id="4593d-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="4593d-116">-Gyűjtemények</span><span class="sxs-lookup"><span data-stu-id="4593d-116">-Collections</span></span>
<span data-ttu-id="4593d-117">New-AzureRmDmsMongoDbDatabaseSetting hívás által visszaadott objektumok MongoDb-gyűjteményének tömbje.</span><span class="sxs-lookup"><span data-stu-id="4593d-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="4593d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4593d-118">CommonParameters</span></span>
<span data-ttu-id="4593d-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4593d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4593d-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4593d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4593d-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4593d-121">INPUTS</span></span>

### <span data-ttu-id="4593d-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="4593d-122">None</span></span>

## <span data-ttu-id="4593d-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4593d-123">OUTPUTS</span></span>

### <span data-ttu-id="4593d-124">Microsoft. Azure. Command. DataMigration. models. MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="4593d-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="4593d-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4593d-125">NOTES</span></span>

## <span data-ttu-id="4593d-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4593d-126">RELATED LINKS</span></span>
