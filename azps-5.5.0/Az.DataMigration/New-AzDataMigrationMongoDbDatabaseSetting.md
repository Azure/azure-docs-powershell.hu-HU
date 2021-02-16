---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163778"
---
# <span data-ttu-id="6b863-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="6b863-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="6b863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b863-102">SYNOPSIS</span></span>
<span data-ttu-id="6b863-103">Adatbázis-beállítást hoz létre a mongoDb-áttelepítéshez</span><span class="sxs-lookup"><span data-stu-id="6b863-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="6b863-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b863-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="6b863-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b863-105">DESCRIPTION</span></span>
<span data-ttu-id="6b863-106">A New-AzDataMigrationMongoDbDatabaseSetting parancsmag létrehoz egy áttelepítési beállításobjektumot, amely megadja az átviteli sebességet és a törlés viselkedését.</span><span class="sxs-lookup"><span data-stu-id="6b863-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="6b863-107">A kimenet egy olyan kulcsérték-pár, amely a beállítás gyűjteményének és értékének nevét használja, és amely az áttelepítési feladat megíratása során használható.</span><span class="sxs-lookup"><span data-stu-id="6b863-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="6b863-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b863-108">EXAMPLES</span></span>

### <span data-ttu-id="6b863-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="6b863-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="6b863-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b863-110">PARAMETERS</span></span>

### <span data-ttu-id="6b863-111">-Name</span><span class="sxs-lookup"><span data-stu-id="6b863-111">-Name</span></span>
<span data-ttu-id="6b863-112">Az adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="6b863-112">Name of the database</span></span>

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
### <span data-ttu-id="6b863-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="6b863-113">-TargetRequestUnit</span></span>
<span data-ttu-id="6b863-114">A dedikált adatbázisszintű kérési egység értéke.</span><span class="sxs-lookup"><span data-stu-id="6b863-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="6b863-115">Ha nincs beállítva, akkor a gyűjtemény megosztott adatbázist (RU) használ.</span><span class="sxs-lookup"><span data-stu-id="6b863-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="6b863-116">-Gyűjtemények</span><span class="sxs-lookup"><span data-stu-id="6b863-116">-Collections</span></span>
<span data-ttu-id="6b863-117">A MongoDb gyűjtemény beállítási objektumtömbje, amelyet a hívás New-AzureRmDmsMongoDbDatabaseSetting vissza.</span><span class="sxs-lookup"><span data-stu-id="6b863-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="6b863-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b863-118">CommonParameters</span></span>
<span data-ttu-id="6b863-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b863-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b863-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b863-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b863-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b863-121">INPUTS</span></span>

### <span data-ttu-id="6b863-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="6b863-122">None</span></span>

## <span data-ttu-id="6b863-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b863-123">OUTPUTS</span></span>

### <span data-ttu-id="6b863-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="6b863-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="6b863-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b863-125">NOTES</span></span>

## <span data-ttu-id="6b863-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b863-126">RELATED LINKS</span></span>
