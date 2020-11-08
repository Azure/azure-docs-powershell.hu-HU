---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012554"
---
# <span data-ttu-id="6e058-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="6e058-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="6e058-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e058-102">SYNOPSIS</span></span>
<span data-ttu-id="6e058-103">Létrehozza az Azure Database áttelepítési szolgáltatás DatabaseInfo objektumát, amely az áttelepítéshez szükséges adatbázis-forrást adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e058-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="6e058-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e058-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e058-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e058-105">DESCRIPTION</span></span>
<span data-ttu-id="6e058-106">A New-AzDataMigrationDatabaseInfo parancsmag létrehozza a DatabaseInfo objektumot, amely az áttelepítendő forrás-példányt adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e058-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="6e058-107">Az adatbázis neve bemeneti paraméterként jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="6e058-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="6e058-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6e058-108">EXAMPLES</span></span>

### <span data-ttu-id="6e058-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6e058-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="6e058-110">Az előző példa létrehoz egy új DatabaseInfo objektumot a forrás adatbázis **AdventureWorks2016**.</span><span class="sxs-lookup"><span data-stu-id="6e058-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="6e058-111">Ez a parancsfájl feltételezi, hogy már bejelentkezett az Azure-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="6e058-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="6e058-112">A bejelentkezési állapotát az Get-AzSubscription parancsmag használatával ellenőrizheti.</span><span class="sxs-lookup"><span data-stu-id="6e058-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="6e058-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e058-113">PARAMETERS</span></span>

### <span data-ttu-id="6e058-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e058-114">-DefaultProfile</span></span>
<span data-ttu-id="6e058-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e058-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e058-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6e058-116">-SourceDatabaseName</span></span>
<span data-ttu-id="6e058-117">Forrás-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6e058-117">Source Database Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e058-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e058-118">CommonParameters</span></span>
<span data-ttu-id="6e058-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e058-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e058-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e058-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e058-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e058-121">INPUTS</span></span>

### <span data-ttu-id="6e058-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="6e058-122">None</span></span>

## <span data-ttu-id="6e058-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e058-123">OUTPUTS</span></span>

### <span data-ttu-id="6e058-124">Microsoft. Azure. Management. DataMigration. models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="6e058-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="6e058-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e058-125">NOTES</span></span>

## <span data-ttu-id="6e058-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e058-126">RELATED LINKS</span></span>
