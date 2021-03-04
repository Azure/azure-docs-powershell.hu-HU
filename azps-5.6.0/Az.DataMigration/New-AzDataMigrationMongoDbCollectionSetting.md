---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 817a4c8469d1d3652dade426857f88f9249f82b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925898"
---
# <span data-ttu-id="33d25-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="33d25-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="33d25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33d25-102">SYNOPSIS</span></span>
<span data-ttu-id="33d25-103">Gyűjteménybeállítás létrehozása az áttelepítéshez a mongóDb-áttelepítésnek megfelelően</span><span class="sxs-lookup"><span data-stu-id="33d25-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="33d25-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="33d25-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="33d25-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="33d25-105">DESCRIPTION</span></span>
<span data-ttu-id="33d25-106">A New-AzDataMigrationMongoDbCollectionSetting parancsmag létrehoz egy áttelepítési beállításobjektumot, amely megadja az átviteli sebességet és a törlés viselkedését.</span><span class="sxs-lookup"><span data-stu-id="33d25-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="33d25-107">A parancsmag kimenete a kulcsérték pár a gyűjtemény nevével és a beállítás értékével.</span><span class="sxs-lookup"><span data-stu-id="33d25-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="33d25-108">A kimenet az adatbázisszintű áttelepítési beállítások összeállításához használatos.</span><span class="sxs-lookup"><span data-stu-id="33d25-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="33d25-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="33d25-109">EXAMPLES</span></span>

### <span data-ttu-id="33d25-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="33d25-110">Example 1</span></span>
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

## <span data-ttu-id="33d25-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33d25-111">PARAMETERS</span></span>

### <span data-ttu-id="33d25-112">-Name</span><span class="sxs-lookup"><span data-stu-id="33d25-112">-Name</span></span>
<span data-ttu-id="33d25-113">A gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="33d25-113">Name of the collection</span></span>

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

### <span data-ttu-id="33d25-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="33d25-114">-ShardKey</span></span>
<span data-ttu-id="33d25-115">A shard billentyűk vesszővel elválasztott listája.</span><span class="sxs-lookup"><span data-stu-id="33d25-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="33d25-116">A mongoDb célhoz megadhatja a "ShardKeyName:Order" shard billentyű sorrendjét, ahol a sorrend 1, -1 vagy üres a kivonatoláshoz, például "_id;email:-1".</span><span class="sxs-lookup"><span data-stu-id="33d25-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="33d25-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="33d25-117">-TargetRequestUnit</span></span>
<span data-ttu-id="33d25-118">A dedikált gyűjteménykérési egység értéke.</span><span class="sxs-lookup"><span data-stu-id="33d25-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="33d25-119">Ha nincs beállítva, akkor a gyűjtemény megosztott adatbázist (RU) használ.</span><span class="sxs-lookup"><span data-stu-id="33d25-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="33d25-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="33d25-120">-CanDelete</span></span>
<span data-ttu-id="33d25-121">Ha a kapcsoló be van állítva, akkor törlődnek-e a céladatok az áttelepítéskor</span><span class="sxs-lookup"><span data-stu-id="33d25-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

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


### <span data-ttu-id="33d25-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d25-122">CommonParameters</span></span>
<span data-ttu-id="33d25-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33d25-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d25-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d25-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d25-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33d25-125">INPUTS</span></span>

### <span data-ttu-id="33d25-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="33d25-126">None</span></span>

## <span data-ttu-id="33d25-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33d25-127">OUTPUTS</span></span>

### <span data-ttu-id="33d25-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="33d25-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="33d25-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="33d25-129">NOTES</span></span>

## <span data-ttu-id="33d25-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33d25-130">RELATED LINKS</span></span>
