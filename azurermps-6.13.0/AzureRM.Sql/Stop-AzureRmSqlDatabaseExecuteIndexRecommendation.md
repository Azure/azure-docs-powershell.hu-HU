---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 2922edf4f7b7cfd0d814a5559bb1e6e7bb9ef3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494861"
---
# <span data-ttu-id="33adc-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="33adc-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="33adc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33adc-102">SYNOPSIS</span></span>
<span data-ttu-id="33adc-103">Leállítja az ajánlott indexelési műveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="33adc-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33adc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33adc-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33adc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="33adc-105">DESCRIPTION</span></span>
<span data-ttu-id="33adc-106">A **stop-AzureRmSqlDatabaseExecuteIndexRecommendation** parancsmag leállítja a javasolt indexelési műveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="33adc-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="33adc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="33adc-107">EXAMPLES</span></span>

### <span data-ttu-id="33adc-108">1. példa: az index-ajánlás futásának leállítása</span><span class="sxs-lookup"><span data-stu-id="33adc-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="33adc-109">Ez a parancs tárgymutató-ajánlást futtat.</span><span class="sxs-lookup"><span data-stu-id="33adc-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="33adc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33adc-110">PARAMETERS</span></span>

### <span data-ttu-id="33adc-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="33adc-111">-DatabaseName</span></span>
<span data-ttu-id="33adc-112">Annak az adatbázisnak a nevét adja meg, amelyhez ez a parancsmag leállítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="33adc-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="33adc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33adc-113">-DefaultProfile</span></span>
<span data-ttu-id="33adc-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="33adc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33adc-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="33adc-115">-IndexRecommendationName</span></span>
<span data-ttu-id="33adc-116">Annak a tárgymutató-ajánlásnak a nevét adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="33adc-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="33adc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33adc-117">-ResourceGroupName</span></span>
<span data-ttu-id="33adc-118">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="33adc-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="33adc-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="33adc-119">-ServerName</span></span>
<span data-ttu-id="33adc-120">Azt a kiszolgálót adja meg, amelyen az az adatbázis található, amelynek a parancsmagja leállítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="33adc-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="33adc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33adc-121">CommonParameters</span></span>
<span data-ttu-id="33adc-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33adc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33adc-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33adc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33adc-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33adc-124">INPUTS</span></span>

### <span data-ttu-id="33adc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="33adc-125">System.String</span></span>

## <span data-ttu-id="33adc-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33adc-126">OUTPUTS</span></span>

### <span data-ttu-id="33adc-127">Microsoft. Azure. Command. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="33adc-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="33adc-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33adc-128">NOTES</span></span>

## <span data-ttu-id="33adc-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33adc-129">RELATED LINKS</span></span>

[<span data-ttu-id="33adc-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="33adc-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="33adc-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="33adc-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="33adc-132">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="33adc-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


