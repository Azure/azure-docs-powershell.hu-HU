---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208279"
---
# <span data-ttu-id="2c0e7-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="2c0e7-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="2c0e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c0e7-102">SYNOPSIS</span></span>
<span data-ttu-id="2c0e7-103">Egy biztonsági felmérés metaadatainak törlése az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="2c0e7-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="2c0e7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2c0e7-104">SYNTAX</span></span>

### <span data-ttu-id="2c0e7-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c0e7-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c0e7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c0e7-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c0e7-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2c0e7-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c0e7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2c0e7-108">DESCRIPTION</span></span>
<span data-ttu-id="2c0e7-109">Egy biztonsági felmérés metaadatainak törlése az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="2c0e7-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="2c0e7-110">Ez a művelet törli a felmérés típusát és az előfizetésből származó összes releváns felmérési eredményt.</span><span class="sxs-lookup"><span data-stu-id="2c0e7-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="2c0e7-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2c0e7-111">EXAMPLES</span></span>

### <span data-ttu-id="2c0e7-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="2c0e7-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="2c0e7-113">Felméréstípus törlése egy előfizetésből</span><span class="sxs-lookup"><span data-stu-id="2c0e7-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="2c0e7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c0e7-114">PARAMETERS</span></span>

### <span data-ttu-id="2c0e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c0e7-115">-DefaultProfile</span></span>
<span data-ttu-id="2c0e7-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c0e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c0e7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c0e7-117">-InputObject</span></span>
<span data-ttu-id="2c0e7-118">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="2c0e7-118">Input Object.</span></span>

```yaml
Type: PSSecurityAssessmentMetadata
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c0e7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2c0e7-119">-Name</span></span>
<span data-ttu-id="2c0e7-120">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2c0e7-120">Resource name.</span></span>

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

### <span data-ttu-id="2c0e7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c0e7-121">-PassThru</span></span>
<span data-ttu-id="2c0e7-122">Adja vissza, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="2c0e7-122">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c0e7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c0e7-123">-ResourceId</span></span>
<span data-ttu-id="2c0e7-124">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="2c0e7-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2c0e7-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c0e7-125">-Confirm</span></span>
<span data-ttu-id="2c0e7-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2c0e7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c0e7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c0e7-127">-WhatIf</span></span>
<span data-ttu-id="2c0e7-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2c0e7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c0e7-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c0e7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c0e7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c0e7-130">CommonParameters</span></span>
<span data-ttu-id="2c0e7-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c0e7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c0e7-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c0e7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c0e7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c0e7-133">INPUTS</span></span>

### <span data-ttu-id="2c0e7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2c0e7-134">System.String</span></span>

### <span data-ttu-id="2c0e7-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="2c0e7-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="2c0e7-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c0e7-136">OUTPUTS</span></span>

### <span data-ttu-id="2c0e7-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2c0e7-137">System.Boolean</span></span>

## <span data-ttu-id="2c0e7-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2c0e7-138">NOTES</span></span>

## <span data-ttu-id="2c0e7-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c0e7-139">RELATED LINKS</span></span>
