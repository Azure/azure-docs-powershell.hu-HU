---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ae4564b1f583b8057438ee631de6b13d38e008ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679920"
---
# <span data-ttu-id="622b3-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="622b3-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="622b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="622b3-102">SYNOPSIS</span></span>
<span data-ttu-id="622b3-103">Elindítja az ajánlott indexelési műveletet futtató munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="622b3-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="622b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="622b3-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="622b3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="622b3-105">DESCRIPTION</span></span>
<span data-ttu-id="622b3-106">A **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** parancsmag elindítja azt a munkafolyamatot, amely egy Azure SQL-adatbázis ajánlott indexelési műveletét futtatja.</span><span class="sxs-lookup"><span data-stu-id="622b3-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="622b3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="622b3-107">EXAMPLES</span></span>

### <span data-ttu-id="622b3-108">1. példa: tárgymutató-ajánlás futtatása</span><span class="sxs-lookup"><span data-stu-id="622b3-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="622b3-109">Ez a parancs tárgymutató-ajánlást futtat.</span><span class="sxs-lookup"><span data-stu-id="622b3-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="622b3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="622b3-110">PARAMETERS</span></span>

### <span data-ttu-id="622b3-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="622b3-111">-DatabaseName</span></span>
<span data-ttu-id="622b3-112">Annak az adatbázisnak a nevét adja meg, amelyhez ez a parancsmag indítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="622b3-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="622b3-113">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="622b3-113">-IndexRecommendationName</span></span>
<span data-ttu-id="622b3-114">A parancsmag által futtatott tárgymutató-ajánlás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="622b3-114">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="622b3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="622b3-115">-ResourceGroupName</span></span>
<span data-ttu-id="622b3-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="622b3-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="622b3-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="622b3-117">-ServerName</span></span>
<span data-ttu-id="622b3-118">Azt a kiszolgálót adja meg, amelyen az az adatbázis található, amelynek a parancsmagja elindítja a munkafolyamatot.</span><span class="sxs-lookup"><span data-stu-id="622b3-118">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="622b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622b3-119">-DefaultProfile</span></span>
<span data-ttu-id="622b3-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="622b3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="622b3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622b3-121">CommonParameters</span></span>
<span data-ttu-id="622b3-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="622b3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622b3-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="622b3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622b3-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="622b3-124">INPUTS</span></span>

## <span data-ttu-id="622b3-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="622b3-125">OUTPUTS</span></span>

## <span data-ttu-id="622b3-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="622b3-126">NOTES</span></span>

## <span data-ttu-id="622b3-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="622b3-127">RELATED LINKS</span></span>

[<span data-ttu-id="622b3-128">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="622b3-128">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="622b3-129">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="622b3-129">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="622b3-130">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="622b3-130">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


