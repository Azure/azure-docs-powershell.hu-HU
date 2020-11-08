---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025954"
---
# <span data-ttu-id="df259-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="df259-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="df259-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df259-102">SYNOPSIS</span></span>
<span data-ttu-id="df259-103">Rugalmas Pool-javaslatokat kap.</span><span class="sxs-lookup"><span data-stu-id="df259-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="df259-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df259-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df259-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="df259-105">DESCRIPTION</span></span>
<span data-ttu-id="df259-106">A **Get-AzSqlElasticPoolRecommendation** parancsmag rugalmas Pool-javaslatokat kap a kiszolgálókhoz.</span><span class="sxs-lookup"><span data-stu-id="df259-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="df259-107">Ezek az ajánlások a következő értékeket tartalmazzák:</span><span class="sxs-lookup"><span data-stu-id="df259-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="df259-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="df259-108">DatabaseCollection.</span></span> <span data-ttu-id="df259-109">A gyűjtőhöz tartozó adatbázis-nevek gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="df259-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="df259-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="df259-110">DatabaseDtuMin.</span></span> <span data-ttu-id="df259-111">Adatátviteli egység (DTU) garancia a rugalmas készletben lévő adatbázisokra.</span><span class="sxs-lookup"><span data-stu-id="df259-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="df259-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="df259-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="df259-113">DTU sapka a rugalmas készlet adatbázisaihoz.</span><span class="sxs-lookup"><span data-stu-id="df259-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="df259-114">Dtu.</span><span class="sxs-lookup"><span data-stu-id="df259-114">Dtu.</span></span> <span data-ttu-id="df259-115">DTU-garancia a rugalmas készletre.</span><span class="sxs-lookup"><span data-stu-id="df259-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="df259-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="df259-116">StorageMb.</span></span> <span data-ttu-id="df259-117">A rugalmas készlet megabájtban történő tárolása</span><span class="sxs-lookup"><span data-stu-id="df259-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="df259-118">Edition.</span><span class="sxs-lookup"><span data-stu-id="df259-118">Edition.</span></span> <span data-ttu-id="df259-119">A rugalmas készlethez tartozó kiadás</span><span class="sxs-lookup"><span data-stu-id="df259-119">Edition for the elastic pool.</span></span> <span data-ttu-id="df259-120">A paraméter elfogadható értékei a következők: Basic, standard és prémium.</span><span class="sxs-lookup"><span data-stu-id="df259-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="df259-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="df259-121">IncludeAllDatabases.</span></span> <span data-ttu-id="df259-122">Azt jelzi, hogy a rugalmas készlet minden adatbázisát visszaadják-e.</span><span class="sxs-lookup"><span data-stu-id="df259-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="df259-123">név.</span><span class="sxs-lookup"><span data-stu-id="df259-123">Name.</span></span> <span data-ttu-id="df259-124">A rugalmas készlet neve.</span><span class="sxs-lookup"><span data-stu-id="df259-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="df259-125">Példák</span><span class="sxs-lookup"><span data-stu-id="df259-125">EXAMPLES</span></span>

### <span data-ttu-id="df259-126">Példa 1: javaslatok kérése egy kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="df259-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="df259-127">Ez a parancs a Server01 nevű kiszolgálóhoz tartozó rugalmas Pool-javaslatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="df259-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="df259-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df259-128">PARAMETERS</span></span>

### <span data-ttu-id="df259-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df259-129">-DefaultProfile</span></span>
<span data-ttu-id="df259-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="df259-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df259-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df259-131">-ResourceGroupName</span></span>
<span data-ttu-id="df259-132">Annak az erőforráscsoportnek a nevét adja meg, amelyhez a kiszolgáló van rendelve.</span><span class="sxs-lookup"><span data-stu-id="df259-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="df259-133">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="df259-133">-ServerName</span></span>
<span data-ttu-id="df259-134">Itt adhatja meg annak a kiszolgálónak a nevét, amelyhez a parancsmag javaslatot tesz.</span><span class="sxs-lookup"><span data-stu-id="df259-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df259-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df259-135">-Confirm</span></span>
<span data-ttu-id="df259-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df259-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df259-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df259-137">-WhatIf</span></span>
<span data-ttu-id="df259-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="df259-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df259-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df259-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df259-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df259-140">CommonParameters</span></span>
<span data-ttu-id="df259-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df259-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df259-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="df259-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df259-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df259-143">INPUTS</span></span>

### <span data-ttu-id="df259-144">System. String</span><span class="sxs-lookup"><span data-stu-id="df259-144">System.String</span></span>

## <span data-ttu-id="df259-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df259-145">OUTPUTS</span></span>

### <span data-ttu-id="df259-146">Microsoft. Azure. Management. SQL. LegacySdk. models. UpgradeRecommendedElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="df259-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="df259-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df259-147">NOTES</span></span>

## <span data-ttu-id="df259-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df259-148">RELATED LINKS</span></span>
