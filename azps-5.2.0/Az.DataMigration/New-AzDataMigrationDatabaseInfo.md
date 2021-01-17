---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327652"
---
# <span data-ttu-id="46a3c-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="46a3c-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="46a3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="46a3c-103">Létrehozza az Azure Adatbázis-áttelepítési szolgáltatás DatabaseInfo objektumát, amely megadja az áttelepítés adatbázis-forrását.</span><span class="sxs-lookup"><span data-stu-id="46a3c-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="46a3c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="46a3c-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46a3c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="46a3c-105">DESCRIPTION</span></span>
<span data-ttu-id="46a3c-106">A New-AzDataMigrationDatabaseInfo parancsmag létrehoz egy DatabaseInfo objektumot, amely megadja az áttelepíteni megfelelő forrásadatbázis-példányt.</span><span class="sxs-lookup"><span data-stu-id="46a3c-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="46a3c-107">Az adatbázisnevet bemeneti paraméterként adja meg a rendszer.</span><span class="sxs-lookup"><span data-stu-id="46a3c-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="46a3c-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="46a3c-108">EXAMPLES</span></span>

### <span data-ttu-id="46a3c-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="46a3c-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="46a3c-110">Az előző példa új DatabaseInfo objektumot hoz létre az **AdventureWorks2016 forrásadatbázishoz.**</span><span class="sxs-lookup"><span data-stu-id="46a3c-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="46a3c-111">Ez a parancsfájl abból indul ki, hogy Már be van jelentkezve az Azure-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="46a3c-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="46a3c-112">A bejelentkezési állapotát a Get-AzSubscription meg.</span><span class="sxs-lookup"><span data-stu-id="46a3c-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="46a3c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46a3c-113">PARAMETERS</span></span>

### <span data-ttu-id="46a3c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a3c-114">-DefaultProfile</span></span>
<span data-ttu-id="46a3c-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46a3c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46a3c-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="46a3c-116">-SourceDatabaseName</span></span>
<span data-ttu-id="46a3c-117">Forrásadatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="46a3c-117">Source Database Name.</span></span>

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

### <span data-ttu-id="46a3c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a3c-118">CommonParameters</span></span>
<span data-ttu-id="46a3c-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46a3c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a3c-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46a3c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a3c-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46a3c-121">INPUTS</span></span>

### <span data-ttu-id="46a3c-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="46a3c-122">None</span></span>

## <span data-ttu-id="46a3c-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46a3c-123">OUTPUTS</span></span>

### <span data-ttu-id="46a3c-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="46a3c-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="46a3c-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="46a3c-125">NOTES</span></span>

## <span data-ttu-id="46a3c-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46a3c-126">RELATED LINKS</span></span>
