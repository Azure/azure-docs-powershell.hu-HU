---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: c371749643952e8209b3cbec0721331a4d380d94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011702"
---
# <span data-ttu-id="6bd09-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="6bd09-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="6bd09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bd09-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd09-103">Részfelmérés eredményeit kapja meg egy előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="6bd09-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="6bd09-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6bd09-104">SYNTAX</span></span>

### <span data-ttu-id="6bd09-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6bd09-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6bd09-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="6bd09-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bd09-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="6bd09-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bd09-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="6bd09-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bd09-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bd09-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6bd09-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6bd09-110">DESCRIPTION</span></span>
<span data-ttu-id="6bd09-111">Részfelmérés eredményeit kapja meg egy előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="6bd09-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="6bd09-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6bd09-112">EXAMPLES</span></span>

### <span data-ttu-id="6bd09-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="6bd09-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="6bd09-114">Egy előfizetés összes alfelmérési eredményét megkapja.</span><span class="sxs-lookup"><span data-stu-id="6bd09-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="6bd09-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bd09-115">PARAMETERS</span></span>

### <span data-ttu-id="6bd09-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="6bd09-116">-AssessedResourceId</span></span>
<span data-ttu-id="6bd09-117">Annak az erőforrásnak a teljes erőforrás-azonosítója, amely alapján a felmérést kiszámították.</span><span class="sxs-lookup"><span data-stu-id="6bd09-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionScope, SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd09-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="6bd09-118">-AssessmentName</span></span>
<span data-ttu-id="6bd09-119">A felmérési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6bd09-119">Name of the assessment resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd09-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bd09-120">-DefaultProfile</span></span>
<span data-ttu-id="6bd09-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6bd09-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd09-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6bd09-122">-Name</span></span>
<span data-ttu-id="6bd09-123">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6bd09-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd09-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bd09-124">-ResourceId</span></span>
<span data-ttu-id="6bd09-125">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="6bd09-125">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd09-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd09-126">CommonParameters</span></span>
<span data-ttu-id="6bd09-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bd09-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd09-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bd09-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd09-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6bd09-129">INPUTS</span></span>

### <span data-ttu-id="6bd09-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6bd09-130">System.String</span></span>

## <span data-ttu-id="6bd09-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bd09-131">OUTPUTS</span></span>

### <span data-ttu-id="6bd09-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="6bd09-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="6bd09-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6bd09-133">NOTES</span></span>

## <span data-ttu-id="6bd09-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6bd09-134">RELATED LINKS</span></span>
