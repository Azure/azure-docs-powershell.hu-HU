---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: e69cffe6955a5bf19636dd519c0906be64ce4413
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362458"
---
# <span data-ttu-id="79465-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="79465-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="79465-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79465-102">SYNOPSIS</span></span>
<span data-ttu-id="79465-103">Elindítja az ajánlott indexműveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="79465-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="79465-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79465-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79465-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79465-105">DESCRIPTION</span></span>
<span data-ttu-id="79465-106">A **Start-AzSqlDatabaseExecuteIndexRecommendation** parancsmag elindítja azt a munkafolyamatot, amely egy Azure SQL-adatbázishoz ajánlott indexműveletet futtat.</span><span class="sxs-lookup"><span data-stu-id="79465-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="79465-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79465-107">EXAMPLES</span></span>

### <span data-ttu-id="79465-108">1. példa: Index-javaslat futtatása</span><span class="sxs-lookup"><span data-stu-id="79465-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="79465-109">Ez a parancs egy ajánlott indexet futtat.</span><span class="sxs-lookup"><span data-stu-id="79465-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="79465-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79465-110">PARAMETERS</span></span>

### <span data-ttu-id="79465-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="79465-111">-DatabaseName</span></span>
<span data-ttu-id="79465-112">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja elindítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="79465-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="79465-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79465-113">-DefaultProfile</span></span>
<span data-ttu-id="79465-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="79465-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79465-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="79465-115">-IndexRecommendationName</span></span>
<span data-ttu-id="79465-116">A parancsmag által futtatott index-javaslat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="79465-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="79465-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79465-117">-ResourceGroupName</span></span>
<span data-ttu-id="79465-118">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="79465-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="79465-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="79465-119">-ServerName</span></span>
<span data-ttu-id="79465-120">Azt az adatbázist tartalmazó kiszolgálót adja meg, amelyen a parancsmag elindít egy munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="79465-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="79465-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79465-121">CommonParameters</span></span>
<span data-ttu-id="79465-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79465-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79465-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79465-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79465-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79465-124">INPUTS</span></span>

### <span data-ttu-id="79465-125">System.String</span><span class="sxs-lookup"><span data-stu-id="79465-125">System.String</span></span>

## <span data-ttu-id="79465-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79465-126">OUTPUTS</span></span>

### <span data-ttu-id="79465-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="79465-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="79465-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79465-128">NOTES</span></span>

## <span data-ttu-id="79465-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79465-129">RELATED LINKS</span></span>

[<span data-ttu-id="79465-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="79465-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="79465-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="79465-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="79465-132">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="79465-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


