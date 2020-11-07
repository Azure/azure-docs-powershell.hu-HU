---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: 3b12fdd4b82446f67eaaaec7a46bbc7f49307e94
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836833"
---
# <span data-ttu-id="37d59-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="37d59-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="37d59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37d59-102">SYNOPSIS</span></span>
<span data-ttu-id="37d59-103">Ismerje meg a kognitív Services-fiók jelenlegi használatát.</span><span class="sxs-lookup"><span data-stu-id="37d59-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="37d59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37d59-104">SYNTAX</span></span>

### <span data-ttu-id="37d59-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="37d59-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37d59-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37d59-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37d59-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37d59-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37d59-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="37d59-108">DESCRIPTION</span></span>
<span data-ttu-id="37d59-109">A **Get-AzCognitiveServicesAccountUsage** parancsmag a kognitív Services-fiók aktuális használati adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="37d59-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="37d59-110">Példák</span><span class="sxs-lookup"><span data-stu-id="37d59-110">EXAMPLES</span></span>

### <span data-ttu-id="37d59-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="37d59-111">Example 1</span></span>
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

### <span data-ttu-id="37d59-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="37d59-112">Example 2</span></span>
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

### <span data-ttu-id="37d59-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="37d59-113">Example 3</span></span>
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

## <span data-ttu-id="37d59-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37d59-114">PARAMETERS</span></span>

### <span data-ttu-id="37d59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d59-115">-DefaultProfile</span></span>
<span data-ttu-id="37d59-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37d59-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37d59-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37d59-117">-InputObject</span></span>
<span data-ttu-id="37d59-118">A kognitív szolgáltatások fiók objektuma.</span><span class="sxs-lookup"><span data-stu-id="37d59-118">Cognitive Services Account Object.</span></span>

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

### <span data-ttu-id="37d59-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="37d59-119">-Name</span></span>
<span data-ttu-id="37d59-120">A kognitív szolgáltatások fiók neve.</span><span class="sxs-lookup"><span data-stu-id="37d59-120">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="37d59-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37d59-121">-ResourceGroupName</span></span>
<span data-ttu-id="37d59-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="37d59-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="37d59-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37d59-123">-ResourceId</span></span>
<span data-ttu-id="37d59-124">A kognitív szolgáltatások fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="37d59-124">Cognitive Services Account Resource ID.</span></span>

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

### <span data-ttu-id="37d59-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d59-125">CommonParameters</span></span>
<span data-ttu-id="37d59-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37d59-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d59-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37d59-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d59-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37d59-128">INPUTS</span></span>

### <span data-ttu-id="37d59-129">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="37d59-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="37d59-130">System. String</span><span class="sxs-lookup"><span data-stu-id="37d59-130">System.String</span></span>

## <span data-ttu-id="37d59-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37d59-131">OUTPUTS</span></span>

### <span data-ttu-id="37d59-132">Microsoft. Azure. Command. Management. CognitiveServices. models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="37d59-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="37d59-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37d59-133">NOTES</span></span>

## <span data-ttu-id="37d59-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37d59-134">RELATED LINKS</span></span>
