---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: c287fd6aafcfe63a26c5f1dfd01503adb741428d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338718"
---
# <span data-ttu-id="e0f0e-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="e0f0e-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="e0f0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f0e-103">A Kognitív Szolgáltatások fiók aktuális használati adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="e0f0e-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="e0f0e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e0f0e-104">SYNTAX</span></span>

### <span data-ttu-id="e0f0e-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0f0e-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0f0e-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0f0e-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0f0e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0f0e-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0f0e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e0f0e-108">DESCRIPTION</span></span>
<span data-ttu-id="e0f0e-109">A **Get-AzCognitiveServicesAccountUsage** parancsmag aktuális használati adatokat kap a kognitív szolgáltatások fiókjához.</span><span class="sxs-lookup"><span data-stu-id="e0f0e-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="e0f0e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e0f0e-110">EXAMPLES</span></span>

### <span data-ttu-id="e0f0e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e0f0e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="e0f0e-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="e0f0e-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="e0f0e-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="e0f0e-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="e0f0e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0f0e-114">PARAMETERS</span></span>

### <span data-ttu-id="e0f0e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f0e-115">-DefaultProfile</span></span>
<span data-ttu-id="e0f0e-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0f0e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0f0e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0f0e-117">-InputObject</span></span>
<span data-ttu-id="e0f0e-118">Kognitív szolgáltatások fiókobjektuma.</span><span class="sxs-lookup"><span data-stu-id="e0f0e-118">Cognitive Services Account Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f0e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e0f0e-119">-Name</span></span>
<span data-ttu-id="e0f0e-120">Kognitív szolgáltatások fiókneve.</span><span class="sxs-lookup"><span data-stu-id="e0f0e-120">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f0e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0f0e-121">-ResourceGroupName</span></span>
<span data-ttu-id="e0f0e-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0f0e-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f0e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0f0e-123">-ResourceId</span></span>
<span data-ttu-id="e0f0e-124">Kognitív szolgáltatások fiókerőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e0f0e-124">Cognitive Services Account Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f0e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f0e-125">CommonParameters</span></span>
<span data-ttu-id="e0f0e-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0f0e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f0e-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0f0e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f0e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0f0e-128">INPUTS</span></span>

### <span data-ttu-id="e0f0e-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e0f0e-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="e0f0e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e0f0e-130">System.String</span></span>

## <span data-ttu-id="e0f0e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0f0e-131">OUTPUTS</span></span>

### <span data-ttu-id="e0f0e-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="e0f0e-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="e0f0e-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e0f0e-133">NOTES</span></span>

## <span data-ttu-id="e0f0e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0f0e-134">RELATED LINKS</span></span>
