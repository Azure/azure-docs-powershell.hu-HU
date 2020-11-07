---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 4fef918efd69d1ef5506efb70f1db94903845a8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679918"
---
# <span data-ttu-id="72923-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="72923-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="72923-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72923-102">SYNOPSIS</span></span>
<span data-ttu-id="72923-103">Leállítja az ajánlott indexelési műveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="72923-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72923-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72923-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72923-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72923-105">DESCRIPTION</span></span>
<span data-ttu-id="72923-106">A **stop-AzureRmSqlDatabaseExecuteIndexRecommendation** parancsmag leállítja a javasolt indexelési műveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="72923-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="72923-107">Példák</span><span class="sxs-lookup"><span data-stu-id="72923-107">EXAMPLES</span></span>

### <span data-ttu-id="72923-108">1. példa: az index-ajánlás futásának leállítása</span><span class="sxs-lookup"><span data-stu-id="72923-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="72923-109">Ez a parancs tárgymutató-ajánlást futtat.</span><span class="sxs-lookup"><span data-stu-id="72923-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="72923-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72923-110">PARAMETERS</span></span>

### <span data-ttu-id="72923-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="72923-111">-DatabaseName</span></span>
<span data-ttu-id="72923-112">Annak az adatbázisnak a nevét adja meg, amelyhez ez a parancsmag leállítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="72923-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="72923-113">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="72923-113">-IndexRecommendationName</span></span>
<span data-ttu-id="72923-114">Annak a tárgymutató-ajánlásnak a nevét adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="72923-114">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="72923-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72923-115">-ResourceGroupName</span></span>
<span data-ttu-id="72923-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="72923-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="72923-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="72923-117">-ServerName</span></span>
<span data-ttu-id="72923-118">Azt a kiszolgálót adja meg, amelyen az az adatbázis található, amelynek a parancsmagja leállítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="72923-118">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="72923-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72923-119">-DefaultProfile</span></span>
<span data-ttu-id="72923-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72923-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72923-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72923-121">CommonParameters</span></span>
<span data-ttu-id="72923-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72923-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72923-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72923-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72923-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72923-124">INPUTS</span></span>

## <span data-ttu-id="72923-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72923-125">OUTPUTS</span></span>

## <span data-ttu-id="72923-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72923-126">NOTES</span></span>

## <span data-ttu-id="72923-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72923-127">RELATED LINKS</span></span>

[<span data-ttu-id="72923-128">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="72923-128">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="72923-129">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="72923-129">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="72923-130">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="72923-130">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


