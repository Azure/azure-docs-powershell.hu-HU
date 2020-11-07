---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 249f166bcf4dd61d9b8da7cf4d67a2ac20f705ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666692"
---
# <span data-ttu-id="2a909-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="2a909-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="2a909-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a909-102">SYNOPSIS</span></span>
<span data-ttu-id="2a909-103">Adatkészlet-megfeleltetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2a909-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="2a909-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a909-104">SYNTAX</span></span>

### <span data-ttu-id="2a909-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a909-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a909-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a909-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a909-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a909-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a909-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a909-108">DESCRIPTION</span></span>
<span data-ttu-id="2a909-109">A **Remove-AzDataShareDataSetMapping** parancsmag eltávolít egy adatkészlet-megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="2a909-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="2a909-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2a909-110">EXAMPLES</span></span>

### <span data-ttu-id="2a909-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2a909-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="2a909-112">Ez a parancs eltávolítja a DSM nevű adatkészletet a sharesubscription WikiAds.</span><span class="sxs-lookup"><span data-stu-id="2a909-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="2a909-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a909-113">PARAMETERS</span></span>

### <span data-ttu-id="2a909-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2a909-114">-AccountName</span></span>
<span data-ttu-id="2a909-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="2a909-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a909-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a909-116">-DefaultProfile</span></span>
<span data-ttu-id="2a909-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a909-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a909-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a909-118">-InputObject</span></span>
<span data-ttu-id="2a909-119">Az Azure Data Set megfeleltetési objektum</span><span class="sxs-lookup"><span data-stu-id="2a909-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a909-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2a909-120">-Name</span></span>
<span data-ttu-id="2a909-121">Azure Data Set megfeleltetés neve</span><span class="sxs-lookup"><span data-stu-id="2a909-121">Azure data set mapping name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a909-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a909-122">-PassThru</span></span>
<span data-ttu-id="2a909-123">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="2a909-123">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a909-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a909-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a909-125">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="2a909-125">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a909-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a909-126">-ResourceId</span></span>
<span data-ttu-id="2a909-127">Az Azure adathalmaz megfeleltetésének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2a909-127">The resource id of the azure data set mapping</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a909-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2a909-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="2a909-129">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="2a909-129">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a909-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2a909-130">-Confirm</span></span>
<span data-ttu-id="2a909-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2a909-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a909-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a909-132">-WhatIf</span></span>
<span data-ttu-id="2a909-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2a909-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a909-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a909-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a909-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a909-135">CommonParameters</span></span>
<span data-ttu-id="2a909-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a909-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a909-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a909-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a909-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a909-138">INPUTS</span></span>

### <span data-ttu-id="2a909-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2a909-139">System.String</span></span>

### <span data-ttu-id="2a909-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="2a909-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="2a909-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a909-141">OUTPUTS</span></span>

### <span data-ttu-id="2a909-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a909-142">System.Boolean</span></span>

## <span data-ttu-id="2a909-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a909-143">NOTES</span></span>

## <span data-ttu-id="2a909-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a909-144">RELATED LINKS</span></span>
