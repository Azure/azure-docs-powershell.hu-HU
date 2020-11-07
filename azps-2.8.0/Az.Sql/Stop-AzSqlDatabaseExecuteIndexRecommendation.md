---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 9b21c290b2d5e5b6056297bba7d4196dd68d68d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839516"
---
# <span data-ttu-id="adefa-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="adefa-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="adefa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="adefa-102">SYNOPSIS</span></span>
<span data-ttu-id="adefa-103">Leállítja az ajánlott indexelési műveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="adefa-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="adefa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="adefa-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="adefa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="adefa-105">DESCRIPTION</span></span>
<span data-ttu-id="adefa-106">A **stop-AzSqlDatabaseExecuteIndexRecommendation** parancsmag leállítja a javasolt indexelési műveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="adefa-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="adefa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="adefa-107">EXAMPLES</span></span>

### <span data-ttu-id="adefa-108">1. példa: az index-ajánlás futásának leállítása</span><span class="sxs-lookup"><span data-stu-id="adefa-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="adefa-109">Ez a parancs tárgymutató-ajánlást futtat.</span><span class="sxs-lookup"><span data-stu-id="adefa-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="adefa-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="adefa-110">PARAMETERS</span></span>

### <span data-ttu-id="adefa-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="adefa-111">-DatabaseName</span></span>
<span data-ttu-id="adefa-112">Annak az adatbázisnak a nevét adja meg, amelyhez ez a parancsmag leállítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="adefa-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="adefa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adefa-113">-DefaultProfile</span></span>
<span data-ttu-id="adefa-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="adefa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adefa-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="adefa-115">-IndexRecommendationName</span></span>
<span data-ttu-id="adefa-116">Annak a tárgymutató-ajánlásnak a nevét adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="adefa-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="adefa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adefa-117">-ResourceGroupName</span></span>
<span data-ttu-id="adefa-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="adefa-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="adefa-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="adefa-119">-ServerName</span></span>
<span data-ttu-id="adefa-120">Azt a kiszolgálót adja meg, amelyen az az adatbázis található, amelynek a parancsmagja leállítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="adefa-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="adefa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adefa-121">CommonParameters</span></span>
<span data-ttu-id="adefa-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="adefa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adefa-123">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="adefa-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adefa-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="adefa-124">INPUTS</span></span>

### <span data-ttu-id="adefa-125">System. String</span><span class="sxs-lookup"><span data-stu-id="adefa-125">System.String</span></span>

## <span data-ttu-id="adefa-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adefa-126">OUTPUTS</span></span>

### <span data-ttu-id="adefa-127">Microsoft. Azure. Command. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="adefa-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="adefa-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="adefa-128">NOTES</span></span>

## <span data-ttu-id="adefa-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adefa-129">RELATED LINKS</span></span>

[<span data-ttu-id="adefa-130">Get-AzSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="adefa-130">Get-AzSqlDatabaseIndexRecommendations</span></span>](./Get-AzSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="adefa-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="adefa-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="adefa-132">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="adefa-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


