---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
ms.openlocfilehash: 6ebf76e339b90ab40576262807f85b85897284d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498747"
---
# <span data-ttu-id="17963-101">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="17963-101">Get-AzureRmSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="17963-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17963-102">SYNOPSIS</span></span>
<span data-ttu-id="17963-103">Rugalmas Pool-javaslatokat kap.</span><span class="sxs-lookup"><span data-stu-id="17963-103">Gets elastic pool recommendations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17963-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17963-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17963-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="17963-105">DESCRIPTION</span></span>
<span data-ttu-id="17963-106">A **Get-AzureRmSqlElasticPoolRecommendation** parancsmag rugalmas Pool-javaslatokat kap a kiszolgálókhoz.</span><span class="sxs-lookup"><span data-stu-id="17963-106">The **Get-AzureRmSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="17963-107">Ezek az ajánlások a következő értékeket tartalmazzák:</span><span class="sxs-lookup"><span data-stu-id="17963-107">These recommendations include the following values:</span></span>

- <span data-ttu-id="17963-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="17963-108">DatabaseCollection.</span></span> <span data-ttu-id="17963-109">A gyűjtőhöz tartozó adatbázis-nevek gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="17963-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="17963-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="17963-110">DatabaseDtuMin.</span></span> <span data-ttu-id="17963-111">Adatátviteli egység (DTU) garancia a rugalmas készletben lévő adatbázisokra.</span><span class="sxs-lookup"><span data-stu-id="17963-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="17963-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="17963-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="17963-113">DTU sapka a rugalmas készlet adatbázisaihoz.</span><span class="sxs-lookup"><span data-stu-id="17963-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="17963-114">Dtu.</span><span class="sxs-lookup"><span data-stu-id="17963-114">Dtu.</span></span> <span data-ttu-id="17963-115">DTU-garancia a rugalmas készletre.</span><span class="sxs-lookup"><span data-stu-id="17963-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="17963-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="17963-116">StorageMb.</span></span> <span data-ttu-id="17963-117">A rugalmas készlet megabájtban történő tárolása</span><span class="sxs-lookup"><span data-stu-id="17963-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="17963-118">Edition.</span><span class="sxs-lookup"><span data-stu-id="17963-118">Edition.</span></span> <span data-ttu-id="17963-119">A rugalmas készlethez tartozó kiadás</span><span class="sxs-lookup"><span data-stu-id="17963-119">Edition for the elastic pool.</span></span> <span data-ttu-id="17963-120">A paraméter elfogadható értékei a következők: Basic, standard és prémium.</span><span class="sxs-lookup"><span data-stu-id="17963-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="17963-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="17963-121">IncludeAllDatabases.</span></span> <span data-ttu-id="17963-122">Azt jelzi, hogy a rugalmas készlet minden adatbázisát visszaadják-e.</span><span class="sxs-lookup"><span data-stu-id="17963-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="17963-123">név.</span><span class="sxs-lookup"><span data-stu-id="17963-123">Name.</span></span> <span data-ttu-id="17963-124">A rugalmas készlet neve.</span><span class="sxs-lookup"><span data-stu-id="17963-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="17963-125">Példák</span><span class="sxs-lookup"><span data-stu-id="17963-125">EXAMPLES</span></span>

### <span data-ttu-id="17963-126">Példa 1: javaslatok kérése egy kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="17963-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="17963-127">Ez a parancs a Server01 nevű kiszolgálóhoz tartozó rugalmas Pool-javaslatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="17963-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="17963-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17963-128">PARAMETERS</span></span>

### <span data-ttu-id="17963-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17963-129">-DefaultProfile</span></span>
<span data-ttu-id="17963-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="17963-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17963-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17963-131">-ResourceGroupName</span></span>
<span data-ttu-id="17963-132">Annak az erőforráscsoportnek a nevét adja meg, amelyhez a kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="17963-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="17963-133">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="17963-133">-ServerName</span></span>
<span data-ttu-id="17963-134">Itt adhatja meg annak a kiszolgálónak a nevét, amelyhez a parancsmag javaslatot tesz.</span><span class="sxs-lookup"><span data-stu-id="17963-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17963-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="17963-135">-Confirm</span></span>
<span data-ttu-id="17963-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="17963-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17963-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17963-137">-WhatIf</span></span>
<span data-ttu-id="17963-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="17963-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17963-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17963-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17963-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17963-140">CommonParameters</span></span>
<span data-ttu-id="17963-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17963-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17963-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17963-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17963-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17963-143">INPUTS</span></span>

### <span data-ttu-id="17963-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="17963-144">None</span></span>
<span data-ttu-id="17963-145">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="17963-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="17963-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17963-146">OUTPUTS</span></span>

## <span data-ttu-id="17963-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17963-147">NOTES</span></span>

## <span data-ttu-id="17963-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17963-148">RELATED LINKS</span></span>
