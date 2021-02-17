---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208334"
---
# <span data-ttu-id="66fd2-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="66fd2-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="66fd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="66fd2-103">Biztonsági felméréseket és azok eredményeit kapja meg egy előfizetésben</span><span class="sxs-lookup"><span data-stu-id="66fd2-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="66fd2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="66fd2-104">SYNTAX</span></span>

### <span data-ttu-id="66fd2-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66fd2-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66fd2-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="66fd2-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66fd2-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="66fd2-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66fd2-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="66fd2-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66fd2-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="66fd2-109">DESCRIPTION</span></span>
<span data-ttu-id="66fd2-110">Biztonsági felmérést és az előfizetéssel kapcsolatos eredményeket kapja.</span><span class="sxs-lookup"><span data-stu-id="66fd2-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="66fd2-111">A biztonsági felmérésekből tudható, hogy az Azure Biztonsági központ milyen ajánlott eljárásokat ajánl fel az Azure-előfizetése csökkentése érdekében.</span><span class="sxs-lookup"><span data-stu-id="66fd2-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="66fd2-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="66fd2-112">EXAMPLES</span></span>

### <span data-ttu-id="66fd2-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="66fd2-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="66fd2-114">Az összes biztonsági felmérést megkapja egy előfizetésben</span><span class="sxs-lookup"><span data-stu-id="66fd2-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="66fd2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66fd2-115">PARAMETERS</span></span>

### <span data-ttu-id="66fd2-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="66fd2-116">-AssessedResourceId</span></span>
<span data-ttu-id="66fd2-117">Annak az erőforrásnak a teljes erőforrás-azonosítója, amely alapján a felmérést kiszámították.</span><span class="sxs-lookup"><span data-stu-id="66fd2-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66fd2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66fd2-118">-DefaultProfile</span></span>
<span data-ttu-id="66fd2-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66fd2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66fd2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="66fd2-120">-Name</span></span>
<span data-ttu-id="66fd2-121">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="66fd2-121">Resource name.</span></span>

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
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fd2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66fd2-122">-ResourceId</span></span>
<span data-ttu-id="66fd2-123">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="66fd2-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="66fd2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66fd2-124">CommonParameters</span></span>
<span data-ttu-id="66fd2-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66fd2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66fd2-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66fd2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66fd2-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66fd2-127">INPUTS</span></span>

### <span data-ttu-id="66fd2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="66fd2-128">System.String</span></span>

## <span data-ttu-id="66fd2-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66fd2-129">OUTPUTS</span></span>

### <span data-ttu-id="66fd2-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="66fd2-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="66fd2-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="66fd2-131">NOTES</span></span>

## <span data-ttu-id="66fd2-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66fd2-132">RELATED LINKS</span></span>
