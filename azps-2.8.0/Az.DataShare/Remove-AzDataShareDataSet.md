---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: 122d5118761e3a4b7a400b4bc73daa29d218c4ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666696"
---
# <span data-ttu-id="62c17-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="62c17-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="62c17-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62c17-102">SYNOPSIS</span></span>
<span data-ttu-id="62c17-103">Adatkészlet-megfeleltetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="62c17-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="62c17-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62c17-104">SYNTAX</span></span>

### <span data-ttu-id="62c17-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="62c17-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62c17-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62c17-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62c17-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62c17-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62c17-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="62c17-108">DESCRIPTION</span></span>
<span data-ttu-id="62c17-109">A **Remove-AzDataShareDataSet** parancsmag eltávolítja az adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="62c17-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="62c17-110">Példák</span><span class="sxs-lookup"><span data-stu-id="62c17-110">EXAMPLES</span></span>

### <span data-ttu-id="62c17-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="62c17-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="62c17-112">Ez a parancs eltávolítja a DS nevű adatkészletet a megosztás WikiAds.</span><span class="sxs-lookup"><span data-stu-id="62c17-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="62c17-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62c17-113">PARAMETERS</span></span>

### <span data-ttu-id="62c17-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="62c17-114">-AccountName</span></span>
<span data-ttu-id="62c17-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="62c17-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="62c17-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c17-116">-DefaultProfile</span></span>
<span data-ttu-id="62c17-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62c17-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62c17-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62c17-118">-InputObject</span></span>
<span data-ttu-id="62c17-119">Az Azure Data Set objektum.</span><span class="sxs-lookup"><span data-stu-id="62c17-119">The azure data set object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62c17-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62c17-120">-Name</span></span>
<span data-ttu-id="62c17-121">Azure-adathalmaz neve</span><span class="sxs-lookup"><span data-stu-id="62c17-121">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c17-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62c17-122">-PassThru</span></span>
<span data-ttu-id="62c17-123">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="62c17-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="62c17-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c17-124">-ResourceGroupName</span></span>
<span data-ttu-id="62c17-125">Az Azure Data Share-fiók erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="62c17-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="62c17-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62c17-126">-ResourceId</span></span>
<span data-ttu-id="62c17-127">Az Azure-adathalmaz erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="62c17-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="62c17-128">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="62c17-128">-ShareName</span></span>
<span data-ttu-id="62c17-129">Azure-adatmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="62c17-129">Azure data share name.</span></span>

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

### <span data-ttu-id="62c17-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="62c17-130">-Confirm</span></span>
<span data-ttu-id="62c17-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62c17-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62c17-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62c17-132">-WhatIf</span></span>
<span data-ttu-id="62c17-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="62c17-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62c17-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62c17-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62c17-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c17-135">CommonParameters</span></span>
<span data-ttu-id="62c17-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62c17-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c17-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62c17-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c17-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62c17-138">INPUTS</span></span>

### <span data-ttu-id="62c17-139">System. String</span><span class="sxs-lookup"><span data-stu-id="62c17-139">System.String</span></span>

### <span data-ttu-id="62c17-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="62c17-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="62c17-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62c17-141">OUTPUTS</span></span>

### <span data-ttu-id="62c17-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62c17-142">System.Boolean</span></span>

## <span data-ttu-id="62c17-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62c17-143">NOTES</span></span>

## <span data-ttu-id="62c17-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62c17-144">RELATED LINKS</span></span>
