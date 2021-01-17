---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479797"
---
# <span data-ttu-id="a5036-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="a5036-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="a5036-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5036-102">SYNOPSIS</span></span>
<span data-ttu-id="a5036-103">Biztonsági felméréseket és azok eredményeit kapja meg egy előfizetésben</span><span class="sxs-lookup"><span data-stu-id="a5036-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="a5036-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a5036-104">SYNTAX</span></span>

### <span data-ttu-id="a5036-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5036-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5036-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a5036-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5036-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="a5036-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5036-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5036-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5036-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a5036-109">DESCRIPTION</span></span>
<span data-ttu-id="a5036-110">Biztonsági felmérést és az előfizetéssel kapcsolatos eredményeket kapja.</span><span class="sxs-lookup"><span data-stu-id="a5036-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="a5036-111">A biztonsági felmérésekből tudható, hogy mely ajánlott eljárásokat ajánlotta újra az Azure Biztonsági központ, hogy az Azure-előfizetését mérsékeljük.</span><span class="sxs-lookup"><span data-stu-id="a5036-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="a5036-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a5036-112">EXAMPLES</span></span>

### <span data-ttu-id="a5036-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="a5036-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="a5036-114">Az előfizetés összes biztonsági felmérésének lekérte</span><span class="sxs-lookup"><span data-stu-id="a5036-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="a5036-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5036-115">PARAMETERS</span></span>

### <span data-ttu-id="a5036-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="a5036-116">-AssessedResourceId</span></span>
<span data-ttu-id="a5036-117">Annak az erőforrásnak a teljes erőforrás-azonosítója, amely alapján a felmérést kiszámították.</span><span class="sxs-lookup"><span data-stu-id="a5036-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="a5036-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5036-118">-DefaultProfile</span></span>
<span data-ttu-id="a5036-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5036-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5036-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a5036-120">-Name</span></span>
<span data-ttu-id="a5036-121">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a5036-121">Resource name.</span></span>

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

### <span data-ttu-id="a5036-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5036-122">-ResourceId</span></span>
<span data-ttu-id="a5036-123">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="a5036-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a5036-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5036-124">CommonParameters</span></span>
<span data-ttu-id="a5036-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5036-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5036-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5036-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5036-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5036-127">INPUTS</span></span>

### <span data-ttu-id="a5036-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a5036-128">System.String</span></span>

## <span data-ttu-id="a5036-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5036-129">OUTPUTS</span></span>

### <span data-ttu-id="a5036-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="a5036-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="a5036-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a5036-131">NOTES</span></span>

## <span data-ttu-id="a5036-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5036-132">RELATED LINKS</span></span>
