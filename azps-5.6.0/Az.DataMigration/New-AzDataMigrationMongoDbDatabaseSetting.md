---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: cf034b01d0cc7bd707d65cb2ddd90e9567003861
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934186"
---
# <span data-ttu-id="8d299-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="8d299-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="8d299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d299-102">SYNOPSIS</span></span>
<span data-ttu-id="8d299-103">Adatbázis-beállítást hoz létre a mongoDb-áttelepítéshez</span><span class="sxs-lookup"><span data-stu-id="8d299-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="8d299-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d299-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="8d299-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d299-105">DESCRIPTION</span></span>
<span data-ttu-id="8d299-106">A New-AzDataMigrationMongoDbDatabaseSetting parancsmag létrehoz egy áttelepítési beállításobjektumot, amely megadja az átviteli sebességet és a törlés viselkedését.</span><span class="sxs-lookup"><span data-stu-id="8d299-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="8d299-107">A kimenet egy kulcsérték pár, amely a gyűjtemény nevét és a beállítás értékét használja, és amellyel meg lehet invokinging the migration task.</span><span class="sxs-lookup"><span data-stu-id="8d299-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="8d299-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d299-108">EXAMPLES</span></span>

### <span data-ttu-id="8d299-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="8d299-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="8d299-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d299-110">PARAMETERS</span></span>

### <span data-ttu-id="8d299-111">-Name</span><span class="sxs-lookup"><span data-stu-id="8d299-111">-Name</span></span>
<span data-ttu-id="8d299-112">Az adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="8d299-112">Name of the database</span></span>

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
### <span data-ttu-id="8d299-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="8d299-113">-TargetRequestUnit</span></span>
<span data-ttu-id="8d299-114">A dedikált adatbázisszintű kérési egység értéke.</span><span class="sxs-lookup"><span data-stu-id="8d299-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="8d299-115">Ha nincs beállítva, akkor a gyűjtemény megosztott adatbázist (RU) használ.</span><span class="sxs-lookup"><span data-stu-id="8d299-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="8d299-116">-Gyűjtemények</span><span class="sxs-lookup"><span data-stu-id="8d299-116">-Collections</span></span>
<span data-ttu-id="8d299-117">A MongoDb gyűjtemény beállítási objektumtömbje, amelyet a hívás New-AzureRmDmsMongoDbDatabaseSetting vissza.</span><span class="sxs-lookup"><span data-stu-id="8d299-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="8d299-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d299-118">CommonParameters</span></span>
<span data-ttu-id="8d299-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d299-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d299-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d299-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d299-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d299-121">INPUTS</span></span>

### <span data-ttu-id="8d299-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="8d299-122">None</span></span>

## <span data-ttu-id="8d299-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d299-123">OUTPUTS</span></span>

### <span data-ttu-id="8d299-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="8d299-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="8d299-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d299-125">NOTES</span></span>

## <span data-ttu-id="8d299-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d299-126">RELATED LINKS</span></span>
