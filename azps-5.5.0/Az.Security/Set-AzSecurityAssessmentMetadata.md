---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208223"
---
# <span data-ttu-id="748d2-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="748d2-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="748d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="748d2-102">SYNOPSIS</span></span>
<span data-ttu-id="748d2-103">Biztonsági felmérési típust hoz létre vagy frissítéseket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="748d2-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="748d2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="748d2-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="748d2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="748d2-105">DESCRIPTION</span></span>
<span data-ttu-id="748d2-106">Létrehozza vagy frissíti a biztonsági felmérés metaadatait, amelyek különféle felmérési tulajdonságok létrehozására és kezelésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="748d2-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="748d2-107">A művelet után az előfizetésben bármely erőforrásról jelentést tud majd tenni a felmérés eredményeiről.</span><span class="sxs-lookup"><span data-stu-id="748d2-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="748d2-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="748d2-108">EXAMPLES</span></span>

### <span data-ttu-id="748d2-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="748d2-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="748d2-110">Új felmérési típus létrehozása az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="748d2-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="748d2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="748d2-111">PARAMETERS</span></span>

### <span data-ttu-id="748d2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="748d2-112">-DefaultProfile</span></span>
<span data-ttu-id="748d2-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="748d2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="748d2-114">-Leírás</span><span class="sxs-lookup"><span data-stu-id="748d2-114">-Description</span></span>
<span data-ttu-id="748d2-115">Részletes karakterlánc, amely segít a felhasználóknak megérteni ennek a felmérésnek a jelentését és a számítás módját.</span><span class="sxs-lookup"><span data-stu-id="748d2-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="748d2-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="748d2-116">-DisplayName</span></span>
<span data-ttu-id="748d2-117">Az objektum emberi olvasásra használható címe.</span><span class="sxs-lookup"><span data-stu-id="748d2-117">Human readable title for this object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="748d2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="748d2-118">-Name</span></span>
<span data-ttu-id="748d2-119">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="748d2-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="748d2-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="748d2-120">-RemediationDescription</span></span>
<span data-ttu-id="748d2-121">Részletes karakterlánc, amely segít a felhasználóknak megérteni a biztonsági probléma csökkentésének vagy megoldásának különböző módjait.</span><span class="sxs-lookup"><span data-stu-id="748d2-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="748d2-122">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="748d2-122">-Severity</span></span>
<span data-ttu-id="748d2-123">A biztonsági kockázat fontosságának jelzése, ha a felmérés nem megfelelő.</span><span class="sxs-lookup"><span data-stu-id="748d2-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="748d2-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="748d2-124">-Confirm</span></span>
<span data-ttu-id="748d2-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="748d2-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="748d2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="748d2-126">-WhatIf</span></span>
<span data-ttu-id="748d2-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="748d2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="748d2-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="748d2-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="748d2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="748d2-129">CommonParameters</span></span>
<span data-ttu-id="748d2-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="748d2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="748d2-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="748d2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="748d2-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="748d2-132">INPUTS</span></span>

### <span data-ttu-id="748d2-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="748d2-133">None</span></span>

## <span data-ttu-id="748d2-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="748d2-134">OUTPUTS</span></span>

### <span data-ttu-id="748d2-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="748d2-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="748d2-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="748d2-136">NOTES</span></span>

## <span data-ttu-id="748d2-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="748d2-137">RELATED LINKS</span></span>
