---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: c61f1bd988410b696eddd12162958333022dd892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494871"
---
# <span data-ttu-id="166b8-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="166b8-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="166b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="166b8-102">SYNOPSIS</span></span>
<span data-ttu-id="166b8-103">Elindítja az ajánlott indexelési műveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="166b8-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="166b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="166b8-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="166b8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="166b8-105">DESCRIPTION</span></span>
<span data-ttu-id="166b8-106">A **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** parancsmag elindítja azt a munkafolyamatot, amely egy Azure SQL-adatbázis ajánlott indexelési műveletét futtatja.</span><span class="sxs-lookup"><span data-stu-id="166b8-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="166b8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="166b8-107">EXAMPLES</span></span>

### <span data-ttu-id="166b8-108">1. példa: tárgymutató-ajánlás futtatása</span><span class="sxs-lookup"><span data-stu-id="166b8-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="166b8-109">Ez a parancs tárgymutató-ajánlást futtat.</span><span class="sxs-lookup"><span data-stu-id="166b8-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="166b8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="166b8-110">PARAMETERS</span></span>

### <span data-ttu-id="166b8-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="166b8-111">-DatabaseName</span></span>
<span data-ttu-id="166b8-112">Annak az adatbázisnak a nevét adja meg, amelyhez ez a parancsmag indítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="166b8-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="166b8-113">-DefaultProfile</span></span>
<span data-ttu-id="166b8-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="166b8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="166b8-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="166b8-115">-IndexRecommendationName</span></span>
<span data-ttu-id="166b8-116">A parancsmag által futtatott tárgymutató-ajánlás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="166b8-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166b8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="166b8-117">-ResourceGroupName</span></span>
<span data-ttu-id="166b8-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="166b8-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166b8-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="166b8-119">-ServerName</span></span>
<span data-ttu-id="166b8-120">Azt a kiszolgálót adja meg, amelyen az az adatbázis található, amelynek a parancsmagja elindítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="166b8-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166b8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="166b8-121">CommonParameters</span></span>
<span data-ttu-id="166b8-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="166b8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="166b8-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="166b8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="166b8-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="166b8-124">INPUTS</span></span>

### <span data-ttu-id="166b8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="166b8-125">System.String</span></span>

## <span data-ttu-id="166b8-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="166b8-126">OUTPUTS</span></span>

### <span data-ttu-id="166b8-127">Microsoft. Azure. Command. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="166b8-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="166b8-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="166b8-128">NOTES</span></span>

## <span data-ttu-id="166b8-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="166b8-129">RELATED LINKS</span></span>

[<span data-ttu-id="166b8-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="166b8-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="166b8-131">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="166b8-131">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="166b8-132">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="166b8-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


