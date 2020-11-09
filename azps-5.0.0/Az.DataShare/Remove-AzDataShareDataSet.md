---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: c3d5105fc3b43a3f6b7ff8b45c5ba8236fed656b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297407"
---
# <span data-ttu-id="51bc3-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="51bc3-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="51bc3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="51bc3-103">Adatkészlet-megfeleltetés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="51bc3-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="51bc3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51bc3-104">SYNTAX</span></span>

### <span data-ttu-id="51bc3-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51bc3-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51bc3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51bc3-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51bc3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51bc3-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51bc3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="51bc3-108">DESCRIPTION</span></span>
<span data-ttu-id="51bc3-109">A **Remove-AzDataShareDataSet** parancsmag eltávolítja az adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="51bc3-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="51bc3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="51bc3-110">EXAMPLES</span></span>

### <span data-ttu-id="51bc3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="51bc3-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="51bc3-112">Ez a parancs eltávolítja a DS nevű adatkészletet a megosztás WikiAds.</span><span class="sxs-lookup"><span data-stu-id="51bc3-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="51bc3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51bc3-113">PARAMETERS</span></span>

### <span data-ttu-id="51bc3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="51bc3-114">-AccountName</span></span>
<span data-ttu-id="51bc3-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="51bc3-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="51bc3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51bc3-116">-DefaultProfile</span></span>
<span data-ttu-id="51bc3-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51bc3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51bc3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51bc3-118">-InputObject</span></span>
<span data-ttu-id="51bc3-119">Az Azure Data Set objektum.</span><span class="sxs-lookup"><span data-stu-id="51bc3-119">The azure data set object.</span></span>


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

### <span data-ttu-id="51bc3-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51bc3-120">-Name</span></span>
<span data-ttu-id="51bc3-121">Azure-adathalmaz neve</span><span class="sxs-lookup"><span data-stu-id="51bc3-121">Azure data set name.</span></span>

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

### <span data-ttu-id="51bc3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51bc3-122">-PassThru</span></span>
<span data-ttu-id="51bc3-123">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="51bc3-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="51bc3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51bc3-124">-ResourceGroupName</span></span>
<span data-ttu-id="51bc3-125">Az Azure Data Share-fiók erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="51bc3-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="51bc3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51bc3-126">-ResourceId</span></span>
<span data-ttu-id="51bc3-127">Az Azure-adathalmaz erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="51bc3-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="51bc3-128">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="51bc3-128">-ShareName</span></span>
<span data-ttu-id="51bc3-129">Azure-adatmegosztás neve.</span><span class="sxs-lookup"><span data-stu-id="51bc3-129">Azure data share name.</span></span>

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

### <span data-ttu-id="51bc3-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="51bc3-130">-Confirm</span></span>
<span data-ttu-id="51bc3-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51bc3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51bc3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51bc3-132">-WhatIf</span></span>
<span data-ttu-id="51bc3-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="51bc3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51bc3-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51bc3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51bc3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51bc3-135">CommonParameters</span></span>
<span data-ttu-id="51bc3-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51bc3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51bc3-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="51bc3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51bc3-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51bc3-138">INPUTS</span></span>

### <span data-ttu-id="51bc3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="51bc3-139">System.String</span></span>

### <span data-ttu-id="51bc3-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="51bc3-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="51bc3-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51bc3-141">OUTPUTS</span></span>

### <span data-ttu-id="51bc3-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51bc3-142">System.Boolean</span></span>

## <span data-ttu-id="51bc3-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51bc3-143">NOTES</span></span>

## <span data-ttu-id="51bc3-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51bc3-144">RELATED LINKS</span></span>
