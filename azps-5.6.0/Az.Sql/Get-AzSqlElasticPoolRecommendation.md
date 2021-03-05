---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 03f2d7b9ae97282d0144ca19b493081fd2d8d774
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999510"
---
# <span data-ttu-id="12ad6-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="12ad6-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="12ad6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="12ad6-103">Rugalmas készletjavaslatokat kap.</span><span class="sxs-lookup"><span data-stu-id="12ad6-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="12ad6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="12ad6-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12ad6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="12ad6-105">DESCRIPTION</span></span>
<span data-ttu-id="12ad6-106">A **Get-AzSqlElasticPoolRecommendation** parancsmag rugalmas készletjavaslatokat kap egy kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="12ad6-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="12ad6-107">Ezek a javaslatok az alábbi értékeket tartalmazzák:</span><span class="sxs-lookup"><span data-stu-id="12ad6-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="12ad6-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="12ad6-108">DatabaseCollection.</span></span> <span data-ttu-id="12ad6-109">A készlethez tartozó adatbázisnevek gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="12ad6-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="12ad6-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="12ad6-110">DatabaseDtuMin.</span></span> <span data-ttu-id="12ad6-111">Az adatátviteli egység (DTU) garanciája a rugalmas készletben található adatbázisokra.</span><span class="sxs-lookup"><span data-stu-id="12ad6-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="12ad6-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="12ad6-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="12ad6-113">DTU cap for databases in the rugalmassági készlet.</span><span class="sxs-lookup"><span data-stu-id="12ad6-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="12ad6-114">Dtu.</span><span class="sxs-lookup"><span data-stu-id="12ad6-114">Dtu.</span></span> <span data-ttu-id="12ad6-115">DTU garancia a rugalmas készletre.</span><span class="sxs-lookup"><span data-stu-id="12ad6-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="12ad6-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="12ad6-116">StorageMb.</span></span> <span data-ttu-id="12ad6-117">A rugalmas készlet tárterülete megabájtban.</span><span class="sxs-lookup"><span data-stu-id="12ad6-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="12ad6-118">Kiadás.</span><span class="sxs-lookup"><span data-stu-id="12ad6-118">Edition.</span></span> <span data-ttu-id="12ad6-119">A rugalmas készlet kiadását.</span><span class="sxs-lookup"><span data-stu-id="12ad6-119">Edition for the elastic pool.</span></span> <span data-ttu-id="12ad6-120">A paraméter elfogadható értékei a következőek: Alapszintű, Standard és Premium.</span><span class="sxs-lookup"><span data-stu-id="12ad6-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="12ad6-121">Tartalmazza az ÖsszesAdatbázist.</span><span class="sxs-lookup"><span data-stu-id="12ad6-121">IncludeAllDatabases.</span></span> <span data-ttu-id="12ad6-122">Azt jelzi, hogy a rugalmas készletben található összes adatbázist visszaadja-e a rendszer.</span><span class="sxs-lookup"><span data-stu-id="12ad6-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="12ad6-123">név.</span><span class="sxs-lookup"><span data-stu-id="12ad6-123">Name.</span></span> <span data-ttu-id="12ad6-124">A rugalmas készlet neve.</span><span class="sxs-lookup"><span data-stu-id="12ad6-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="12ad6-125">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="12ad6-125">EXAMPLES</span></span>

### <span data-ttu-id="12ad6-126">1. példa: Javaslatok lekérte egy kiszolgálóra</span><span class="sxs-lookup"><span data-stu-id="12ad6-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="12ad6-127">Ez a parancs a Kiszolgáló01 nevű kiszolgáló rugalmas készlet-javaslatait kapja.</span><span class="sxs-lookup"><span data-stu-id="12ad6-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="12ad6-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12ad6-128">PARAMETERS</span></span>

### <span data-ttu-id="12ad6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ad6-129">-DefaultProfile</span></span>
<span data-ttu-id="12ad6-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="12ad6-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12ad6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12ad6-131">-ResourceGroupName</span></span>
<span data-ttu-id="12ad6-132">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="12ad6-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="12ad6-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="12ad6-133">-ServerName</span></span>
<span data-ttu-id="12ad6-134">Annak a kiszolgálónak a neve, amelyre a parancsmag javaslatot kap.</span><span class="sxs-lookup"><span data-stu-id="12ad6-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="12ad6-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12ad6-135">-Confirm</span></span>
<span data-ttu-id="12ad6-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="12ad6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12ad6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12ad6-137">-WhatIf</span></span>
<span data-ttu-id="12ad6-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="12ad6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12ad6-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12ad6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12ad6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ad6-140">CommonParameters</span></span>
<span data-ttu-id="12ad6-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12ad6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ad6-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12ad6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ad6-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12ad6-143">INPUTS</span></span>

### <span data-ttu-id="12ad6-144">System.String</span><span class="sxs-lookup"><span data-stu-id="12ad6-144">System.String</span></span>

## <span data-ttu-id="12ad6-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12ad6-145">OUTPUTS</span></span>

### <span data-ttu-id="12ad6-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecomasticElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="12ad6-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="12ad6-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="12ad6-147">NOTES</span></span>

## <span data-ttu-id="12ad6-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12ad6-148">RELATED LINKS</span></span>
