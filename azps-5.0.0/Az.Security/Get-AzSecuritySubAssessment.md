---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188172"
---
# <span data-ttu-id="4e6b9-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="4e6b9-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="4e6b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6b9-103">Beolvassa a alkategóriákat az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="4e6b9-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="4e6b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e6b9-104">SYNTAX</span></span>

### <span data-ttu-id="4e6b9-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e6b9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e6b9-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4e6b9-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e6b9-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="4e6b9-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e6b9-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="4e6b9-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e6b9-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e6b9-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e6b9-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e6b9-110">DESCRIPTION</span></span>
<span data-ttu-id="4e6b9-111">Beolvassa a alkategóriákat az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="4e6b9-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="4e6b9-112">Példák</span><span class="sxs-lookup"><span data-stu-id="4e6b9-112">EXAMPLES</span></span>

### <span data-ttu-id="4e6b9-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4e6b9-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="4e6b9-114">Az összes alfelmérés eredményét az előfizetésben kapja.</span><span class="sxs-lookup"><span data-stu-id="4e6b9-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="4e6b9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e6b9-115">PARAMETERS</span></span>

### <span data-ttu-id="4e6b9-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="4e6b9-116">-AssessedResourceId</span></span>
<span data-ttu-id="4e6b9-117">Annak az erőforrásnak a teljes erőforrás-azonosítója, amelyre a felmérést kiszámítja.</span><span class="sxs-lookup"><span data-stu-id="4e6b9-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="4e6b9-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="4e6b9-118">-AssessmentName</span></span>
<span data-ttu-id="4e6b9-119">Az értékelési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4e6b9-119">Name of the assessment resource.</span></span>

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

### <span data-ttu-id="4e6b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6b9-120">-DefaultProfile</span></span>
<span data-ttu-id="4e6b9-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e6b9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e6b9-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e6b9-122">-Name</span></span>
<span data-ttu-id="4e6b9-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="4e6b9-123">Resource name.</span></span>

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

### <span data-ttu-id="4e6b9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e6b9-124">-ResourceId</span></span>
<span data-ttu-id="4e6b9-125">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="4e6b9-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="4e6b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6b9-126">CommonParameters</span></span>
<span data-ttu-id="4e6b9-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e6b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6b9-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4e6b9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6b9-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e6b9-129">INPUTS</span></span>

### <span data-ttu-id="4e6b9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4e6b9-130">System.String</span></span>

## <span data-ttu-id="4e6b9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e6b9-131">OUTPUTS</span></span>

### <span data-ttu-id="4e6b9-132">Microsoft. Azure. commands. Security. models. reassessments. PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="4e6b9-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="4e6b9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e6b9-133">NOTES</span></span>

## <span data-ttu-id="4e6b9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e6b9-134">RELATED LINKS</span></span>
