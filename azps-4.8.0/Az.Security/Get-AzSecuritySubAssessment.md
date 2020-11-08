---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181396"
---
# <span data-ttu-id="e7d67-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="e7d67-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="e7d67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7d67-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d67-103">Beolvassa a alkategóriákat az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e7d67-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="e7d67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7d67-104">SYNTAX</span></span>

### <span data-ttu-id="e7d67-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7d67-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7d67-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e7d67-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7d67-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="e7d67-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7d67-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="e7d67-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7d67-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7d67-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7d67-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7d67-110">DESCRIPTION</span></span>
<span data-ttu-id="e7d67-111">Beolvassa a alkategóriákat az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e7d67-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="e7d67-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e7d67-112">EXAMPLES</span></span>

### <span data-ttu-id="e7d67-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e7d67-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="e7d67-114">Az összes alfelmérés eredményét az előfizetésben kapja.</span><span class="sxs-lookup"><span data-stu-id="e7d67-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="e7d67-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7d67-115">PARAMETERS</span></span>

### <span data-ttu-id="e7d67-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="e7d67-116">-AssessedResourceId</span></span>
<span data-ttu-id="e7d67-117">Annak az erőforrásnak a teljes erőforrás-azonosítója, amelyre a felmérést kiszámítja.</span><span class="sxs-lookup"><span data-stu-id="e7d67-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="e7d67-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="e7d67-118">-AssessmentName</span></span>
<span data-ttu-id="e7d67-119">Az értékelési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e7d67-119">Name of the assessment resource.</span></span>

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

### <span data-ttu-id="e7d67-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d67-120">-DefaultProfile</span></span>
<span data-ttu-id="e7d67-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7d67-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7d67-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e7d67-122">-Name</span></span>
<span data-ttu-id="e7d67-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="e7d67-123">Resource name.</span></span>

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

### <span data-ttu-id="e7d67-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7d67-124">-ResourceId</span></span>
<span data-ttu-id="e7d67-125">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="e7d67-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e7d67-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d67-126">CommonParameters</span></span>
<span data-ttu-id="e7d67-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7d67-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d67-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e7d67-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d67-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7d67-129">INPUTS</span></span>

### <span data-ttu-id="e7d67-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e7d67-130">System.String</span></span>

## <span data-ttu-id="e7d67-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7d67-131">OUTPUTS</span></span>

### <span data-ttu-id="e7d67-132">Microsoft. Azure. commands. Security. models. reassessments. PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="e7d67-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="e7d67-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7d67-133">NOTES</span></span>

## <span data-ttu-id="e7d67-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7d67-134">RELATED LINKS</span></span>
