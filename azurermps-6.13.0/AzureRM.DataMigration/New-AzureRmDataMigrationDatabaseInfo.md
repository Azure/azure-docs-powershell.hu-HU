---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: c04a79a54e42c64fe897a419565e4816964879b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680678"
---
# <span data-ttu-id="904c0-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="904c0-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="904c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="904c0-102">SYNOPSIS</span></span>
<span data-ttu-id="904c0-103">Létrehozza az Azure Database áttelepítési szolgáltatás DatabaseInfo objektumát, amely az áttelepítéshez szükséges adatbázis-forrást adja meg.</span><span class="sxs-lookup"><span data-stu-id="904c0-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="904c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="904c0-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="904c0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="904c0-105">DESCRIPTION</span></span>
<span data-ttu-id="904c0-106">A New-AzureRmDataMigrationDatabaseInfo parancsmag létrehozza a DatabaseInfo objektumot, amely az áttelepítendő forrás-példányt adja meg.</span><span class="sxs-lookup"><span data-stu-id="904c0-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="904c0-107">Az adatbázis neve bemeneti paraméterként jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="904c0-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="904c0-108">Példák</span><span class="sxs-lookup"><span data-stu-id="904c0-108">EXAMPLES</span></span>

### <span data-ttu-id="904c0-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="904c0-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="904c0-110">Az előző példa létrehoz egy új DatabaseInfo objektumot a forrás adatbázis **AdventureWorks2016**.</span><span class="sxs-lookup"><span data-stu-id="904c0-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="904c0-111">Ez a parancsfájl feltételezi, hogy már bejelentkezett az Azure-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="904c0-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="904c0-112">A bejelentkezési állapotát az Get-AzureSubscription parancsmag használatával ellenőrizheti.</span><span class="sxs-lookup"><span data-stu-id="904c0-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="904c0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="904c0-113">PARAMETERS</span></span>

### <span data-ttu-id="904c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="904c0-114">-DefaultProfile</span></span>
<span data-ttu-id="904c0-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="904c0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="904c0-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="904c0-116">-SourceDatabaseName</span></span>
<span data-ttu-id="904c0-117">Forrás-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="904c0-117">Source Database Name.</span></span>

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

### <span data-ttu-id="904c0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="904c0-118">CommonParameters</span></span>
<span data-ttu-id="904c0-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="904c0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="904c0-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="904c0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="904c0-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="904c0-121">INPUTS</span></span>

### <span data-ttu-id="904c0-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="904c0-122">None</span></span>

## <span data-ttu-id="904c0-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="904c0-123">OUTPUTS</span></span>

### <span data-ttu-id="904c0-124">Microsoft. Azure. Management. DataMigration. models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="904c0-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="904c0-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="904c0-125">NOTES</span></span>

## <span data-ttu-id="904c0-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="904c0-126">RELATED LINKS</span></span>
