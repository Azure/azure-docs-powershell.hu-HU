---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: 265f917068237fee13f77eb8c87e0adf8cd12f08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153338"
---
# <span data-ttu-id="4df56-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="4df56-101">New-AzDataShare</span></span>

## <span data-ttu-id="4df56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4df56-102">SYNOPSIS</span></span>
<span data-ttu-id="4df56-103">Azure-adat megosztást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4df56-103">Creates a azure data share.</span></span>

## <span data-ttu-id="4df56-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4df56-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4df56-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4df56-105">DESCRIPTION</span></span>
<span data-ttu-id="4df56-106">A **New-AzDataShare** parancsmag egy megadott Azure-adatmegosztási fiókon belül hoz létre adatmegosztást az erőforráscsoport nevének, fióknevének, megosztási nevének és megosztási fajtának megadva.</span><span class="sxs-lookup"><span data-stu-id="4df56-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="4df56-107">A leírás és a használati feltételek opcionális paraméterek, amelyek beállíthatók az adatmegoszlás létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="4df56-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="4df56-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4df56-108">EXAMPLES</span></span>

### <span data-ttu-id="4df56-109">1. példa: Adat megosztás létrehozása</span><span class="sxs-lookup"><span data-stu-id="4df56-109">Example 1 : Create a data share</span></span>
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

<span data-ttu-id="4df56-110">Ez a parancs létrehoz egy AdsShare nevű adatmegosztást a WikiAdsAccount adatmegosztási fiókban, amely leírással és használati feltételekkel tartalmazza az Ads nevű erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="4df56-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="4df56-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4df56-111">PARAMETERS</span></span>

### <span data-ttu-id="4df56-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4df56-112">-AccountName</span></span>
<span data-ttu-id="4df56-113">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="4df56-113">Azure data share account name</span></span>

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

### <span data-ttu-id="4df56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df56-114">-DefaultProfile</span></span>
<span data-ttu-id="4df56-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4df56-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4df56-116">-Leírás</span><span class="sxs-lookup"><span data-stu-id="4df56-116">-Description</span></span>
<span data-ttu-id="4df56-117">Az Azure-adatok megosztásának leírása</span><span class="sxs-lookup"><span data-stu-id="4df56-117">Description of azure data share</span></span>

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

### <span data-ttu-id="4df56-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4df56-118">-Name</span></span>
<span data-ttu-id="4df56-119">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="4df56-119">Azure data share name</span></span>

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

### <span data-ttu-id="4df56-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4df56-120">-ResourceGroupName</span></span>
<span data-ttu-id="4df56-121">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="4df56-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4df56-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="4df56-122">-TermsOfUse</span></span>
<span data-ttu-id="4df56-123">Az Azure-adatok megosztására vonatkozó használati feltételek</span><span class="sxs-lookup"><span data-stu-id="4df56-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="4df56-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4df56-124">-Confirm</span></span>
<span data-ttu-id="4df56-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4df56-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4df56-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4df56-126">-WhatIf</span></span>
<span data-ttu-id="4df56-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4df56-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4df56-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4df56-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4df56-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df56-129">CommonParameters</span></span>
<span data-ttu-id="4df56-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4df56-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df56-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4df56-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df56-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4df56-132">INPUTS</span></span>

### <span data-ttu-id="4df56-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="4df56-133">None</span></span>

## <span data-ttu-id="4df56-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4df56-134">OUTPUTS</span></span>

### <span data-ttu-id="4df56-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="4df56-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="4df56-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4df56-136">NOTES</span></span>

## <span data-ttu-id="4df56-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4df56-137">RELATED LINKS</span></span>
