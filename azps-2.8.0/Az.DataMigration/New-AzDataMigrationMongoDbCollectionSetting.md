---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 041f67940fbe79a751b969dd17223f453f4929d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666772"
---
# <span data-ttu-id="cf4de-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="cf4de-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="cf4de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf4de-102">SYNOPSIS</span></span>
<span data-ttu-id="cf4de-103">Gyűjtemény-beállítás létrehozása az áttelepítéshez az mongoDb-áttelepítés szerint</span><span class="sxs-lookup"><span data-stu-id="cf4de-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="cf4de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf4de-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="cf4de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf4de-105">DESCRIPTION</span></span>
<span data-ttu-id="cf4de-106">A New-AzDataMigrationMongoDbCollectionSetting parancsmag létrehoz egy áttelepítési beállítás objektumot, amely az átviteli sebesség és a törlés működését adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf4de-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="cf4de-107">A kimenet: a parancsmag egy kulcs érték párja a gyűjtemény nevével és a beállítás értékétől.</span><span class="sxs-lookup"><span data-stu-id="cf4de-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="cf4de-108">A kimenet az adatbázis-szint áttelepítési beállításainak összeállításakor használatos.</span><span class="sxs-lookup"><span data-stu-id="cf4de-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="cf4de-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cf4de-109">EXAMPLES</span></span>

### <span data-ttu-id="cf4de-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cf4de-110">Example 1</span></span>
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

## <span data-ttu-id="cf4de-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf4de-111">PARAMETERS</span></span>

### <span data-ttu-id="cf4de-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf4de-112">-Name</span></span>
<span data-ttu-id="cf4de-113">A gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="cf4de-113">Name of the collection</span></span>

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

### <span data-ttu-id="cf4de-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="cf4de-114">-ShardKey</span></span>
<span data-ttu-id="cf4de-115">A Szilánk-billentyűk vesszővel elválasztott listája.</span><span class="sxs-lookup"><span data-stu-id="cf4de-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="cf4de-116">A mongoDb Target esetében megadhatja a "ShardKeyName: Order" (": sorrend") bejárási sorrendjét, ahol a sorrend 1,-1 vagy üres az üzenetkivonat esetén (például "_id, e-mail:-1").</span><span class="sxs-lookup"><span data-stu-id="cf4de-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="cf4de-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="cf4de-117">-TargetRequestUnit</span></span>
<span data-ttu-id="cf4de-118">A dedikált Collection Request Unit érték</span><span class="sxs-lookup"><span data-stu-id="cf4de-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="cf4de-119">Ha nincs beállítva, a gyűjtemény az RU megosztott adatbázisát használja.</span><span class="sxs-lookup"><span data-stu-id="cf4de-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="cf4de-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="cf4de-120">-CanDelete</span></span>
<span data-ttu-id="cf4de-121">Annak megállapítása, hogy a célérték törlésre kerül-e, ha a kapcsoló be van állítva, akkor a rendszer az áttelepítés után kitakarítja.</span><span class="sxs-lookup"><span data-stu-id="cf4de-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

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


### <span data-ttu-id="cf4de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf4de-122">CommonParameters</span></span>
<span data-ttu-id="cf4de-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf4de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf4de-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf4de-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf4de-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf4de-125">INPUTS</span></span>

### <span data-ttu-id="cf4de-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="cf4de-126">None</span></span>

## <span data-ttu-id="cf4de-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf4de-127">OUTPUTS</span></span>

### <span data-ttu-id="cf4de-128">Microsoft. Azure. Command. DataMigration. models. MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="cf4de-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="cf4de-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf4de-129">NOTES</span></span>

## <span data-ttu-id="cf4de-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf4de-130">RELATED LINKS</span></span>
