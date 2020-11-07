---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationdatabaseinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: 3b0729b07667e634f060293bd8593ed237606460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680169"
---
# <span data-ttu-id="d645a-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="d645a-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="d645a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d645a-102">SYNOPSIS</span></span>
<span data-ttu-id="d645a-103">Létrehozza az Azure Database áttelepítési szolgáltatás DatabaseInfo objektumát, amely az áttelepítéshez szükséges adatbázis-forrást adja meg.</span><span class="sxs-lookup"><span data-stu-id="d645a-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d645a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d645a-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="d645a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d645a-105">DESCRIPTION</span></span>
<span data-ttu-id="d645a-106">A New-AzureRmDataMigrationDatabaseInfo parancsmag létrehozza a DatabaseInfo objektumot, amely az áttelepítendő forrás-példányt adja meg.</span><span class="sxs-lookup"><span data-stu-id="d645a-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="d645a-107">Az adatbázis neve bemeneti paraméterként jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="d645a-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="d645a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d645a-108">EXAMPLES</span></span>

### <span data-ttu-id="d645a-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d645a-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="d645a-110">Az előző példa létrehoz egy új DatabaseInfo objektumot a forrás adatbázis **AdventureWorks2016**.</span><span class="sxs-lookup"><span data-stu-id="d645a-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>

<span data-ttu-id="d645a-111">Ez a parancsfájl feltételezi, hogy már bejelentkezett az Azure-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="d645a-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="d645a-112">A bejelentkezési állapotát az Get-AzureSubscription parancsmag használatával ellenőrizheti.</span><span class="sxs-lookup"><span data-stu-id="d645a-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="d645a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d645a-113">PARAMETERS</span></span>

### <span data-ttu-id="d645a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d645a-114">-DefaultProfile</span></span>
<span data-ttu-id="d645a-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d645a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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
### <span data-ttu-id="d645a-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d645a-116">-Confirm</span></span>
<span data-ttu-id="d645a-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d645a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d645a-118">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d645a-118">-SourceDatabaseName</span></span>
<span data-ttu-id="d645a-119">Forrás-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d645a-119">Source Database Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d645a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d645a-120">-WhatIf</span></span>
<span data-ttu-id="d645a-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d645a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d645a-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d645a-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="d645a-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d645a-123">INPUTS</span></span>

### <span data-ttu-id="d645a-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="d645a-124">None</span></span>


## <span data-ttu-id="d645a-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d645a-125">OUTPUTS</span></span>

### <span data-ttu-id="d645a-126">Microsoft. Azure. Management. DataMigration. models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="d645a-126">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>


## <span data-ttu-id="d645a-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d645a-127">NOTES</span></span>

## <span data-ttu-id="d645a-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d645a-128">RELATED LINKS</span></span>


