---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188002"
---
# <span data-ttu-id="23833-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="23833-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="23833-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23833-102">SYNOPSIS</span></span>
<span data-ttu-id="23833-103">Biztonsági felmérési típust hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="23833-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="23833-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23833-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23833-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="23833-105">DESCRIPTION</span></span>
<span data-ttu-id="23833-106">A biztonsági felmérés metaadatait hozza létre vagy frissít, így különféle értékelési tulajdonságokat hozhat létre és kezelhet.</span><span class="sxs-lookup"><span data-stu-id="23833-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="23833-107">A műveletek után az előfizetésben szereplő bármely erőforrásban jelentést tehet a felmérés eredményéről.</span><span class="sxs-lookup"><span data-stu-id="23833-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="23833-108">Példák</span><span class="sxs-lookup"><span data-stu-id="23833-108">EXAMPLES</span></span>

### <span data-ttu-id="23833-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="23833-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="23833-110">Új értékelési típus létrehozása az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="23833-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="23833-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23833-111">PARAMETERS</span></span>

### <span data-ttu-id="23833-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23833-112">-DefaultProfile</span></span>
<span data-ttu-id="23833-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23833-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23833-114">-Leírás</span><span class="sxs-lookup"><span data-stu-id="23833-114">-Description</span></span>
<span data-ttu-id="23833-115">Részletes karakterlánc, amely segítséget nyújt a felhasználóknak a felmérés jelentésének értelmezéséhez és kiszámításához.</span><span class="sxs-lookup"><span data-stu-id="23833-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

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

### <span data-ttu-id="23833-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="23833-116">-DisplayName</span></span>
<span data-ttu-id="23833-117">Az objektum olvasható címe.</span><span class="sxs-lookup"><span data-stu-id="23833-117">Human readable title for this object.</span></span>

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

### <span data-ttu-id="23833-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="23833-118">-Name</span></span>
<span data-ttu-id="23833-119">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="23833-119">Resource name.</span></span>

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

### <span data-ttu-id="23833-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="23833-120">-RemediationDescription</span></span>
<span data-ttu-id="23833-121">Részletes karakterlánc, amely segítséget nyújt a felhasználóknak a biztonsági probléma enyhítésének és javításának különböző módjairól.</span><span class="sxs-lookup"><span data-stu-id="23833-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

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

### <span data-ttu-id="23833-122">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="23833-122">-Severity</span></span>
<span data-ttu-id="23833-123">A biztonsági kockázat fontosságát jelzi, ha az értékelés egészségtelen.</span><span class="sxs-lookup"><span data-stu-id="23833-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

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

### <span data-ttu-id="23833-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="23833-124">-Confirm</span></span>
<span data-ttu-id="23833-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="23833-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23833-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23833-126">-WhatIf</span></span>
<span data-ttu-id="23833-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="23833-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23833-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="23833-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23833-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23833-129">CommonParameters</span></span>
<span data-ttu-id="23833-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23833-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23833-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="23833-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23833-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23833-132">INPUTS</span></span>

### <span data-ttu-id="23833-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="23833-133">None</span></span>

## <span data-ttu-id="23833-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23833-134">OUTPUTS</span></span>

### <span data-ttu-id="23833-135">Microsoft. Azure. commands. Security. models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="23833-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="23833-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23833-136">NOTES</span></span>

## <span data-ttu-id="23833-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23833-137">RELATED LINKS</span></span>
