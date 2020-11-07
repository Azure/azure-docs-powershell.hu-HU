---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: e69cffe6955a5bf19636dd519c0906be64ce4413
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846525"
---
# <span data-ttu-id="53126-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="53126-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="53126-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53126-102">SYNOPSIS</span></span>
<span data-ttu-id="53126-103">Elindítja az ajánlott indexelési műveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="53126-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="53126-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53126-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53126-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="53126-105">DESCRIPTION</span></span>
<span data-ttu-id="53126-106">A **Start-AzSqlDatabaseExecuteIndexRecommendation** parancsmag elindítja azt a munkafolyamatot, amely egy Azure SQL-adatbázis ajánlott indexelési műveletét futtatja.</span><span class="sxs-lookup"><span data-stu-id="53126-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="53126-107">Példák</span><span class="sxs-lookup"><span data-stu-id="53126-107">EXAMPLES</span></span>

### <span data-ttu-id="53126-108">1. példa: tárgymutató-ajánlás futtatása</span><span class="sxs-lookup"><span data-stu-id="53126-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="53126-109">Ez a parancs tárgymutató-ajánlást futtat.</span><span class="sxs-lookup"><span data-stu-id="53126-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="53126-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53126-110">PARAMETERS</span></span>

### <span data-ttu-id="53126-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="53126-111">-DatabaseName</span></span>
<span data-ttu-id="53126-112">Annak az adatbázisnak a nevét adja meg, amelyhez ez a parancsmag indítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="53126-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="53126-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53126-113">-DefaultProfile</span></span>
<span data-ttu-id="53126-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="53126-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53126-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="53126-115">-IndexRecommendationName</span></span>
<span data-ttu-id="53126-116">A parancsmag által futtatott tárgymutató-ajánlás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53126-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="53126-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53126-117">-ResourceGroupName</span></span>
<span data-ttu-id="53126-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="53126-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="53126-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="53126-119">-ServerName</span></span>
<span data-ttu-id="53126-120">Azt a kiszolgálót adja meg, amelyen az az adatbázis található, amelynek a parancsmagja elindítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="53126-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="53126-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53126-121">CommonParameters</span></span>
<span data-ttu-id="53126-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53126-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53126-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="53126-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53126-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53126-124">INPUTS</span></span>

### <span data-ttu-id="53126-125">System. String</span><span class="sxs-lookup"><span data-stu-id="53126-125">System.String</span></span>

## <span data-ttu-id="53126-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53126-126">OUTPUTS</span></span>

### <span data-ttu-id="53126-127">Microsoft. Azure. Command. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="53126-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="53126-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53126-128">NOTES</span></span>

## <span data-ttu-id="53126-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53126-129">RELATED LINKS</span></span>

[<span data-ttu-id="53126-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="53126-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="53126-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="53126-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="53126-132">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="53126-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


