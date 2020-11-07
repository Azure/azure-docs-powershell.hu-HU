---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: ccb40de9ef5e9e68cf62b7b05edeaac9ae10efbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666716"
---
# <span data-ttu-id="3b6a5-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="3b6a5-101">New-AzDataShare</span></span>

## <span data-ttu-id="3b6a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b6a5-102">SYNOPSIS</span></span>
<span data-ttu-id="3b6a5-103">Azure-adatmegosztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3b6a5-103">Creates a azure data share.</span></span>

## <span data-ttu-id="3b6a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b6a5-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b6a5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b6a5-105">DESCRIPTION</span></span>
<span data-ttu-id="3b6a5-106">A **New-AzDataShare** parancsmag egy megadott Azure-adatmegosztási fiókon belül hoz létre adatmegosztást az erőforráscsoport nevének, a fióknév, a megosztási név és a megosztás megadásával.</span><span class="sxs-lookup"><span data-stu-id="3b6a5-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="3b6a5-107">A leírás és a használati feltétel az adatmegosztás létrehozásakor megadható választható paraméterek.</span><span class="sxs-lookup"><span data-stu-id="3b6a5-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="3b6a5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3b6a5-108">EXAMPLES</span></span>

### <span data-ttu-id="3b6a5-109">Példa 1: adatmegosztás létrehozása</span><span class="sxs-lookup"><span data-stu-id="3b6a5-109">Example 1 : Create a data share</span></span>
```
PS C:\>New-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -ShareKind "CopyBased" -Description "Example of description" -TermsOfUse "This should not be shared"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="3b6a5-110">Ez a parancs létrehoz egy AdsShare nevű adatmegosztást az adatmegosztási fiók WikiAdsAccount az CopyBased-hirdetések csoportban, a leírás és a használati feltételek szerint.</span><span class="sxs-lookup"><span data-stu-id="3b6a5-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="3b6a5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b6a5-111">PARAMETERS</span></span>

### <span data-ttu-id="3b6a5-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3b6a5-112">-AccountName</span></span>
<span data-ttu-id="3b6a5-113">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="3b6a5-113">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b6a5-114">-DefaultProfile</span></span>
<span data-ttu-id="3b6a5-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b6a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b6a5-116">-Leírás</span><span class="sxs-lookup"><span data-stu-id="3b6a5-116">-Description</span></span>
<span data-ttu-id="3b6a5-117">Az Azure-adatmegosztás leírása</span><span class="sxs-lookup"><span data-stu-id="3b6a5-117">Description of azure data share</span></span>

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

### <span data-ttu-id="3b6a5-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3b6a5-118">-Name</span></span>
<span data-ttu-id="3b6a5-119">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="3b6a5-119">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6a5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b6a5-120">-ResourceGroupName</span></span>
<span data-ttu-id="3b6a5-121">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="3b6a5-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6a5-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="3b6a5-122">-TermsOfUse</span></span>
<span data-ttu-id="3b6a5-123">Az Azure-adatok megosztására vonatkozó használati feltételei</span><span class="sxs-lookup"><span data-stu-id="3b6a5-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="3b6a5-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b6a5-124">-Confirm</span></span>
<span data-ttu-id="3b6a5-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b6a5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b6a5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b6a5-126">-WhatIf</span></span>
<span data-ttu-id="3b6a5-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b6a5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b6a5-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b6a5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b6a5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b6a5-129">CommonParameters</span></span>
<span data-ttu-id="3b6a5-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b6a5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b6a5-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b6a5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b6a5-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b6a5-132">INPUTS</span></span>

### <span data-ttu-id="3b6a5-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="3b6a5-133">None</span></span>

## <span data-ttu-id="3b6a5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b6a5-134">OUTPUTS</span></span>

### <span data-ttu-id="3b6a5-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="3b6a5-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="3b6a5-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b6a5-136">NOTES</span></span>

## <span data-ttu-id="3b6a5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b6a5-137">RELATED LINKS</span></span>
