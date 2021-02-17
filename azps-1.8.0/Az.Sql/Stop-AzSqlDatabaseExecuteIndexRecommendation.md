---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 7f13b1a1a5daad4e7c97de962943bb859f6a09df
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399481"
---
# <span data-ttu-id="ec9e2-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ec9e2-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="ec9e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ec9e2-103">Leállítja az ajánlott indexműveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="ec9e2-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="ec9e2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ec9e2-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec9e2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ec9e2-105">DESCRIPTION</span></span>
<span data-ttu-id="ec9e2-106">A **Stop-AzSqlDatabaseExecuteIndexRecommendation** parancsmag leállítja az ajánlott indexműveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="ec9e2-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="ec9e2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ec9e2-107">EXAMPLES</span></span>

### <span data-ttu-id="ec9e2-108">1. példa: Index-javaslat futtatásának leállítása</span><span class="sxs-lookup"><span data-stu-id="ec9e2-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="ec9e2-109">Ez a parancs nem futtatja a tárgymutató-javaslatot.</span><span class="sxs-lookup"><span data-stu-id="ec9e2-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="ec9e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec9e2-110">PARAMETERS</span></span>

### <span data-ttu-id="ec9e2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ec9e2-111">-DatabaseName</span></span>
<span data-ttu-id="ec9e2-112">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja leállítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="ec9e2-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="ec9e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec9e2-113">-DefaultProfile</span></span>
<span data-ttu-id="ec9e2-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ec9e2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec9e2-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="ec9e2-115">-IndexRecommendationName</span></span>
<span data-ttu-id="ec9e2-116">A parancsmag által leállítható index-javaslat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec9e2-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="ec9e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec9e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="ec9e2-118">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="ec9e2-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ec9e2-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ec9e2-119">-ServerName</span></span>
<span data-ttu-id="ec9e2-120">Azt az adatbázist tartalmazó kiszolgálót adja meg, amelynek a parancsmagja leállít egy munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="ec9e2-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="ec9e2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec9e2-121">CommonParameters</span></span>
<span data-ttu-id="ec9e2-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec9e2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec9e2-123">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec9e2-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec9e2-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec9e2-124">INPUTS</span></span>

### <span data-ttu-id="ec9e2-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ec9e2-125">System.String</span></span>

## <span data-ttu-id="ec9e2-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec9e2-126">OUTPUTS</span></span>

### <span data-ttu-id="ec9e2-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ec9e2-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="ec9e2-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ec9e2-128">NOTES</span></span>

## <span data-ttu-id="ec9e2-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec9e2-129">RELATED LINKS</span></span>


[<span data-ttu-id="ec9e2-130">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ec9e2-130">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="ec9e2-131">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="ec9e2-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


