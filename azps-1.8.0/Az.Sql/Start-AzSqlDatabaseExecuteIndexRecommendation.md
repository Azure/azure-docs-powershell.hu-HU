---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 1ab1e223ec173cf5727011956f52979026159594
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399515"
---
# <span data-ttu-id="dcc14-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="dcc14-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="dcc14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcc14-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc14-103">Elindítja az ajánlott indexműveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="dcc14-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="dcc14-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dcc14-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dcc14-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dcc14-105">DESCRIPTION</span></span>
<span data-ttu-id="dcc14-106">A **Start-AzSqlDatabaseExecuteIndexRecommendation** parancsmag elindítja azt a munkafolyamatot, amely egy Azure SQL-adatbázishoz ajánlott indexműveletet futtat.</span><span class="sxs-lookup"><span data-stu-id="dcc14-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="dcc14-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dcc14-107">EXAMPLES</span></span>

### <span data-ttu-id="dcc14-108">1. példa: Index-javaslat futtatása</span><span class="sxs-lookup"><span data-stu-id="dcc14-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="dcc14-109">Ez a parancs egy ajánlott indexet futtat.</span><span class="sxs-lookup"><span data-stu-id="dcc14-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="dcc14-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcc14-110">PARAMETERS</span></span>

### <span data-ttu-id="dcc14-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dcc14-111">-DatabaseName</span></span>
<span data-ttu-id="dcc14-112">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja elindítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="dcc14-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="dcc14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc14-113">-DefaultProfile</span></span>
<span data-ttu-id="dcc14-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dcc14-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcc14-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="dcc14-115">-IndexRecommendationName</span></span>
<span data-ttu-id="dcc14-116">A parancsmag által futtatott index-javaslat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dcc14-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="dcc14-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcc14-117">-ResourceGroupName</span></span>
<span data-ttu-id="dcc14-118">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="dcc14-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="dcc14-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dcc14-119">-ServerName</span></span>
<span data-ttu-id="dcc14-120">Azt az adatbázist tartalmazó kiszolgálót adja meg, amelyhez a parancsmag elindít egy munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="dcc14-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="dcc14-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc14-121">CommonParameters</span></span>
<span data-ttu-id="dcc14-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcc14-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc14-123">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcc14-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc14-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcc14-124">INPUTS</span></span>

### <span data-ttu-id="dcc14-125">System.String</span><span class="sxs-lookup"><span data-stu-id="dcc14-125">System.String</span></span>

## <span data-ttu-id="dcc14-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcc14-126">OUTPUTS</span></span>

### <span data-ttu-id="dcc14-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="dcc14-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="dcc14-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dcc14-128">NOTES</span></span>

## <span data-ttu-id="dcc14-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dcc14-129">RELATED LINKS</span></span>


[<span data-ttu-id="dcc14-130">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="dcc14-130">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="dcc14-131">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="dcc14-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


