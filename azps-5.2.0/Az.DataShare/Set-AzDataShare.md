---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: 69d44ea88b34aba027933cb3015a203bf06070fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366924"
---
# <span data-ttu-id="96033-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="96033-101">Set-AzDataShare</span></span>

## <span data-ttu-id="96033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96033-102">SYNOPSIS</span></span>
<span data-ttu-id="96033-103">Meglévő adat megosztás frissítése</span><span class="sxs-lookup"><span data-stu-id="96033-103">Updates an existing data share</span></span>

## <span data-ttu-id="96033-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="96033-104">SYNTAX</span></span>

### <span data-ttu-id="96033-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="96033-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96033-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96033-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96033-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96033-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96033-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="96033-108">DESCRIPTION</span></span>
<span data-ttu-id="96033-109">A **Set-AzDataShare** parancsmag frissíti a megadott Azure-adatmegosztási fiókon belül létező adatmegosztást.</span><span class="sxs-lookup"><span data-stu-id="96033-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="96033-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="96033-110">EXAMPLES</span></span>

### <span data-ttu-id="96033-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="96033-111">Example 1</span></span>
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

<span data-ttu-id="96033-112">Ez a parancs frissíti az AdsShare nevű meglévő adatmegosztást</span><span class="sxs-lookup"><span data-stu-id="96033-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="96033-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96033-113">PARAMETERS</span></span>

### <span data-ttu-id="96033-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="96033-114">-AccountName</span></span>
<span data-ttu-id="96033-115">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="96033-115">Azure data share account name</span></span>

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

### <span data-ttu-id="96033-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96033-116">-DefaultProfile</span></span>
<span data-ttu-id="96033-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96033-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96033-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="96033-118">-Description</span></span>
<span data-ttu-id="96033-119">Az adatmegoszlott adatok leírása</span><span class="sxs-lookup"><span data-stu-id="96033-119">Description of Data Share</span></span>

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

### <span data-ttu-id="96033-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96033-120">-InputObject</span></span>
<span data-ttu-id="96033-121">Azure-adat-megosztási objektum</span><span class="sxs-lookup"><span data-stu-id="96033-121">Azure data share object</span></span>


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

### <span data-ttu-id="96033-122">-Name</span><span class="sxs-lookup"><span data-stu-id="96033-122">-Name</span></span>
<span data-ttu-id="96033-123">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="96033-123">Azure data share name</span></span>

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

### <span data-ttu-id="96033-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96033-124">-ResourceGroupName</span></span>
<span data-ttu-id="96033-125">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="96033-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="96033-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96033-126">-ResourceId</span></span>
<span data-ttu-id="96033-127">Az Azure-adat megosztásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="96033-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="96033-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="96033-128">-TermsOfUse</span></span>
<span data-ttu-id="96033-129">Az adat-megosztás használati feltételei</span><span class="sxs-lookup"><span data-stu-id="96033-129">Terms of Use for Data Share</span></span>

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

### <span data-ttu-id="96033-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96033-130">-Confirm</span></span>
<span data-ttu-id="96033-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="96033-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96033-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96033-132">-WhatIf</span></span>
<span data-ttu-id="96033-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="96033-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96033-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96033-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96033-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96033-135">CommonParameters</span></span>
<span data-ttu-id="96033-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96033-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96033-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96033-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96033-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96033-138">INPUTS</span></span>

### <span data-ttu-id="96033-139">System.String</span><span class="sxs-lookup"><span data-stu-id="96033-139">System.String</span></span>

### <span data-ttu-id="96033-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="96033-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="96033-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96033-141">OUTPUTS</span></span>

### <span data-ttu-id="96033-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="96033-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="96033-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="96033-143">NOTES</span></span>

## <span data-ttu-id="96033-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96033-144">RELATED LINKS</span></span>
