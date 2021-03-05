---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: ff69cd6296dbd95f959beb48fef6e496866e54f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011686"
---
# <span data-ttu-id="5b1bc-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="5b1bc-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="5b1bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b1bc-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1bc-103">Egy előfizetés biztonsági felmérési eredményének törlése.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="5b1bc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5b1bc-104">SYNTAX</span></span>

### <span data-ttu-id="5b1bc-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b1bc-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1bc-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="5b1bc-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1bc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b1bc-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1bc-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="5b1bc-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b1bc-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5b1bc-109">DESCRIPTION</span></span>
<span data-ttu-id="5b1bc-110">Egy előfizetés biztonsági felmérési eredményének törlése, amely általában akkor használatos, amikor egy újrasortot törölnek, vagy ha a felmérés már nem releváns egy adott erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="5b1bc-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5b1bc-111">EXAMPLES</span></span>

### <span data-ttu-id="5b1bc-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="5b1bc-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="5b1bc-113">Felmérési eredmény törlése egy előfizetésben</span><span class="sxs-lookup"><span data-stu-id="5b1bc-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="5b1bc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b1bc-114">PARAMETERS</span></span>

### <span data-ttu-id="5b1bc-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="5b1bc-115">-AssessedResourceId</span></span>
<span data-ttu-id="5b1bc-116">Annak az erőforrásnak a teljes erőforrás-azonosítója, amely alapján a felmérést kiszámították.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1bc-117">-DefaultProfile</span></span>
<span data-ttu-id="5b1bc-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b1bc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b1bc-119">-InputObject</span></span>
<span data-ttu-id="5b1bc-120">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-120">Input Object.</span></span>

```yaml
Type: PSSecurityAssessment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1bc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5b1bc-121">-Name</span></span>
<span data-ttu-id="5b1bc-122">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1bc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b1bc-123">-PassThru</span></span>
<span data-ttu-id="5b1bc-124">Adja vissza, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="5b1bc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b1bc-125">-ResourceId</span></span>
<span data-ttu-id="5b1bc-126">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="5b1bc-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b1bc-127">-Confirm</span></span>
<span data-ttu-id="5b1bc-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b1bc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b1bc-129">-WhatIf</span></span>
<span data-ttu-id="5b1bc-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b1bc-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b1bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1bc-132">CommonParameters</span></span>
<span data-ttu-id="5b1bc-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1bc-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b1bc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1bc-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b1bc-135">INPUTS</span></span>

### <span data-ttu-id="5b1bc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5b1bc-136">System.String</span></span>

### <span data-ttu-id="5b1bc-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="5b1bc-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="5b1bc-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b1bc-138">OUTPUTS</span></span>

### <span data-ttu-id="5b1bc-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5b1bc-139">System.Boolean</span></span>

## <span data-ttu-id="5b1bc-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5b1bc-140">NOTES</span></span>

## <span data-ttu-id="5b1bc-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b1bc-141">RELATED LINKS</span></span>
