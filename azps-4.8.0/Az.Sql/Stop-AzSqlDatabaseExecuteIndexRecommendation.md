---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ca7aeed13627bba3c380b3f1062ee80fcc7c3ebf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017548"
---
# <span data-ttu-id="ad570-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ad570-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="ad570-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad570-102">SYNOPSIS</span></span>
<span data-ttu-id="ad570-103">Leállítja az ajánlott indexelési műveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="ad570-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="ad570-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad570-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad570-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad570-105">DESCRIPTION</span></span>
<span data-ttu-id="ad570-106">A **stop-AzSqlDatabaseExecuteIndexRecommendation** parancsmag leállítja a javasolt indexelési műveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="ad570-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="ad570-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ad570-107">EXAMPLES</span></span>

### <span data-ttu-id="ad570-108">1. példa: az index-ajánlás futásának leállítása</span><span class="sxs-lookup"><span data-stu-id="ad570-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="ad570-109">Ez a parancs tárgymutató-ajánlást futtat.</span><span class="sxs-lookup"><span data-stu-id="ad570-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="ad570-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad570-110">PARAMETERS</span></span>

### <span data-ttu-id="ad570-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ad570-111">-DatabaseName</span></span>
<span data-ttu-id="ad570-112">Annak az adatbázisnak a nevét adja meg, amelyhez ez a parancsmag leállítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="ad570-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="ad570-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad570-113">-DefaultProfile</span></span>
<span data-ttu-id="ad570-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ad570-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad570-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="ad570-115">-IndexRecommendationName</span></span>
<span data-ttu-id="ad570-116">Annak a tárgymutató-ajánlásnak a nevét adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="ad570-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="ad570-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad570-117">-ResourceGroupName</span></span>
<span data-ttu-id="ad570-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="ad570-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ad570-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ad570-119">-ServerName</span></span>
<span data-ttu-id="ad570-120">Azt a kiszolgálót adja meg, amelyen az az adatbázis található, amelynek a parancsmagja leállítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="ad570-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="ad570-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad570-121">CommonParameters</span></span>
<span data-ttu-id="ad570-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad570-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad570-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ad570-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad570-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad570-124">INPUTS</span></span>

### <span data-ttu-id="ad570-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ad570-125">System.String</span></span>

## <span data-ttu-id="ad570-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad570-126">OUTPUTS</span></span>

### <span data-ttu-id="ad570-127">Microsoft. Azure. Command. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ad570-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="ad570-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad570-128">NOTES</span></span>

## <span data-ttu-id="ad570-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad570-129">RELATED LINKS</span></span>

[<span data-ttu-id="ad570-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ad570-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="ad570-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ad570-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="ad570-132">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="ad570-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


