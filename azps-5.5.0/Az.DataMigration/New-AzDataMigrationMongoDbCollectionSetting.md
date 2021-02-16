---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148130"
---
# <span data-ttu-id="26f3b-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="26f3b-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="26f3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="26f3b-103">Gyűjteménybeállítás létrehozása az áttelepítéshez a mongoDb-áttelepítésnek megfelelően</span><span class="sxs-lookup"><span data-stu-id="26f3b-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="26f3b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26f3b-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="26f3b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26f3b-105">DESCRIPTION</span></span>
<span data-ttu-id="26f3b-106">A New-AzDataMigrationMongoDbCollectionSetting parancsmag létrehoz egy áttelepítési beállításobjektumot, amely megadja az átviteli sebességet és a törlés viselkedését.</span><span class="sxs-lookup"><span data-stu-id="26f3b-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="26f3b-107">A parancsmag kimenete a kulcsérték pár a gyűjtemény nevével és a beállítás értékével.</span><span class="sxs-lookup"><span data-stu-id="26f3b-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="26f3b-108">A kimenet az adatbázisszintű áttelepítési beállítások összeállításához használatos.</span><span class="sxs-lookup"><span data-stu-id="26f3b-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="26f3b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26f3b-109">EXAMPLES</span></span>

### <span data-ttu-id="26f3b-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="26f3b-110">Example 1</span></span>
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## <span data-ttu-id="26f3b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26f3b-111">PARAMETERS</span></span>

### <span data-ttu-id="26f3b-112">-Name</span><span class="sxs-lookup"><span data-stu-id="26f3b-112">-Name</span></span>
<span data-ttu-id="26f3b-113">A gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="26f3b-113">Name of the collection</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f3b-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="26f3b-114">-ShardKey</span></span>
<span data-ttu-id="26f3b-115">A shard billentyűk vesszővel elválasztott listája.</span><span class="sxs-lookup"><span data-stu-id="26f3b-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="26f3b-116">A mongoDb célhoz megadhatja a "ShardKeyName:Order" shard billentyű sorrendjét, ahol a sorrend 1, -1 vagy üres a kivonatoláshoz, például "_id;email:-1".</span><span class="sxs-lookup"><span data-stu-id="26f3b-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f3b-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="26f3b-117">-TargetRequestUnit</span></span>
<span data-ttu-id="26f3b-118">A dedikált gyűjteménykérési egység értéke.</span><span class="sxs-lookup"><span data-stu-id="26f3b-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="26f3b-119">Ha nincs beállítva, akkor a gyűjtemény megosztott adatbázist (RU) használ.</span><span class="sxs-lookup"><span data-stu-id="26f3b-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="26f3b-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="26f3b-120">-CanDelete</span></span>
<span data-ttu-id="26f3b-121">Ha a kapcsoló be van állítva, akkor törlődnek-e a céladatok az áttelepítéskor</span><span class="sxs-lookup"><span data-stu-id="26f3b-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="26f3b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f3b-122">CommonParameters</span></span>
<span data-ttu-id="26f3b-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26f3b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f3b-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26f3b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f3b-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26f3b-125">INPUTS</span></span>

### <span data-ttu-id="26f3b-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="26f3b-126">None</span></span>

## <span data-ttu-id="26f3b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26f3b-127">OUTPUTS</span></span>

### <span data-ttu-id="26f3b-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="26f3b-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="26f3b-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26f3b-129">NOTES</span></span>

## <span data-ttu-id="26f3b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26f3b-130">RELATED LINKS</span></span>
