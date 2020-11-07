---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: f10aaca629519d40334aabdac604531b726edd69
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666680"
---
# <span data-ttu-id="49dff-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="49dff-101">Set-AzDataShare</span></span>

## <span data-ttu-id="49dff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49dff-102">SYNOPSIS</span></span>
<span data-ttu-id="49dff-103">Meglévő adatmegosztás frissítése</span><span class="sxs-lookup"><span data-stu-id="49dff-103">Updates an existing data share</span></span>

## <span data-ttu-id="49dff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49dff-104">SYNTAX</span></span>

### <span data-ttu-id="49dff-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49dff-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49dff-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49dff-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49dff-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49dff-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49dff-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="49dff-108">DESCRIPTION</span></span>
<span data-ttu-id="49dff-109">A **set-AzDataShare** parancsmag olyan adatmegosztást frissít, amely egy megadott Azure-adatmegosztási fiókon belül található.</span><span class="sxs-lookup"><span data-stu-id="49dff-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="49dff-110">Példák</span><span class="sxs-lookup"><span data-stu-id="49dff-110">EXAMPLES</span></span>

### <span data-ttu-id="49dff-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="49dff-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="49dff-112">Ez a parancs frissíti a AdsShare nevű meglévő adatmegosztást.</span><span class="sxs-lookup"><span data-stu-id="49dff-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="49dff-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49dff-113">PARAMETERS</span></span>

### <span data-ttu-id="49dff-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="49dff-114">-AccountName</span></span>
<span data-ttu-id="49dff-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="49dff-115">Azure data share account name</span></span>

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

### <span data-ttu-id="49dff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49dff-116">-DefaultProfile</span></span>
<span data-ttu-id="49dff-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49dff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49dff-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="49dff-118">-Description</span></span>
<span data-ttu-id="49dff-119">Az adatmegosztás leírása</span><span class="sxs-lookup"><span data-stu-id="49dff-119">Description of Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49dff-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49dff-120">-InputObject</span></span>
<span data-ttu-id="49dff-121">Azure Data Share objektum</span><span class="sxs-lookup"><span data-stu-id="49dff-121">Azure data share object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49dff-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49dff-122">-Name</span></span>
<span data-ttu-id="49dff-123">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="49dff-123">Azure data share name</span></span>

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

### <span data-ttu-id="49dff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49dff-124">-ResourceGroupName</span></span>
<span data-ttu-id="49dff-125">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="49dff-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="49dff-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49dff-126">-ResourceId</span></span>
<span data-ttu-id="49dff-127">Az Azure-adatmegosztás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="49dff-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="49dff-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="49dff-128">-TermsOfUse</span></span>
<span data-ttu-id="49dff-129">Az adatmegosztás használati feltételei</span><span class="sxs-lookup"><span data-stu-id="49dff-129">Terms of Use for Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49dff-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49dff-130">-Confirm</span></span>
<span data-ttu-id="49dff-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49dff-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49dff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49dff-132">-WhatIf</span></span>
<span data-ttu-id="49dff-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49dff-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49dff-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49dff-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49dff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49dff-135">CommonParameters</span></span>
<span data-ttu-id="49dff-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49dff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49dff-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49dff-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49dff-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49dff-138">INPUTS</span></span>

### <span data-ttu-id="49dff-139">System. String</span><span class="sxs-lookup"><span data-stu-id="49dff-139">System.String</span></span>

### <span data-ttu-id="49dff-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="49dff-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="49dff-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49dff-141">OUTPUTS</span></span>

### <span data-ttu-id="49dff-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="49dff-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="49dff-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49dff-143">NOTES</span></span>

## <span data-ttu-id="49dff-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49dff-144">RELATED LINKS</span></span>
