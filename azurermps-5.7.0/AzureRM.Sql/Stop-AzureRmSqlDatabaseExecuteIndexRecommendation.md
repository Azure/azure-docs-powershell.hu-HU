---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: d4cb344f63b871f55668c4de7205ada80ff04f35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678917"
---
# <span data-ttu-id="7314f-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7314f-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="7314f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7314f-102">SYNOPSIS</span></span>
<span data-ttu-id="7314f-103">Leállítja az ajánlott indexelési műveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="7314f-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7314f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7314f-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7314f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7314f-105">DESCRIPTION</span></span>
<span data-ttu-id="7314f-106">A **stop-AzureRmSqlDatabaseExecuteIndexRecommendation** parancsmag leállítja a javasolt indexelési műveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="7314f-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="7314f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7314f-107">EXAMPLES</span></span>

### <span data-ttu-id="7314f-108">1. példa: az index-ajánlás futásának leállítása</span><span class="sxs-lookup"><span data-stu-id="7314f-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="7314f-109">Ez a parancs tárgymutató-ajánlást futtat.</span><span class="sxs-lookup"><span data-stu-id="7314f-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="7314f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7314f-110">PARAMETERS</span></span>

### <span data-ttu-id="7314f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7314f-111">-DatabaseName</span></span>
<span data-ttu-id="7314f-112">Annak az adatbázisnak a nevét adja meg, amelyhez ez a parancsmag leállítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="7314f-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7314f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7314f-113">-DefaultProfile</span></span>
<span data-ttu-id="7314f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7314f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7314f-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="7314f-115">-IndexRecommendationName</span></span>
<span data-ttu-id="7314f-116">Annak a tárgymutató-ajánlásnak a nevét adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="7314f-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7314f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7314f-117">-ResourceGroupName</span></span>
<span data-ttu-id="7314f-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="7314f-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7314f-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="7314f-119">-ServerName</span></span>
<span data-ttu-id="7314f-120">Azt a kiszolgálót adja meg, amelyen az az adatbázis található, amelynek a parancsmagja leállítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="7314f-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7314f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7314f-121">CommonParameters</span></span>
<span data-ttu-id="7314f-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7314f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7314f-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7314f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7314f-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7314f-124">INPUTS</span></span>

### <span data-ttu-id="7314f-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="7314f-125">None</span></span>
<span data-ttu-id="7314f-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7314f-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7314f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7314f-127">OUTPUTS</span></span>

## <span data-ttu-id="7314f-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7314f-128">NOTES</span></span>

## <span data-ttu-id="7314f-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7314f-129">RELATED LINKS</span></span>

[<span data-ttu-id="7314f-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="7314f-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="7314f-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7314f-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="7314f-132">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="7314f-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


