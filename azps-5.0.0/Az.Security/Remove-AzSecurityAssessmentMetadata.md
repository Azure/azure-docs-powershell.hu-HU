---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186728"
---
# <span data-ttu-id="8d0f6-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="8d0f6-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="8d0f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d0f6-102">SYNOPSIS</span></span>
<span data-ttu-id="8d0f6-103">Törli a biztonsági felmérés metaadatait az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="8d0f6-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="8d0f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d0f6-104">SYNTAX</span></span>

### <span data-ttu-id="8d0f6-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d0f6-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d0f6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d0f6-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d0f6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8d0f6-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d0f6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d0f6-108">DESCRIPTION</span></span>
<span data-ttu-id="8d0f6-109">Törli a biztonsági felmérés metaadatait az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="8d0f6-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="8d0f6-110">Ezzel a lépéssel törli az értékelés típusát, valamint az előfizetésből származó összes releváns felmérési találatot.</span><span class="sxs-lookup"><span data-stu-id="8d0f6-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="8d0f6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8d0f6-111">EXAMPLES</span></span>

### <span data-ttu-id="8d0f6-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8d0f6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="8d0f6-113">Értékelés típusának törlése az előfizetésből</span><span class="sxs-lookup"><span data-stu-id="8d0f6-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="8d0f6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d0f6-114">PARAMETERS</span></span>

### <span data-ttu-id="8d0f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d0f6-115">-DefaultProfile</span></span>
<span data-ttu-id="8d0f6-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d0f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d0f6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d0f6-117">-InputObject</span></span>
<span data-ttu-id="8d0f6-118">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="8d0f6-118">Input Object.</span></span>

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

### <span data-ttu-id="8d0f6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d0f6-119">-Name</span></span>
<span data-ttu-id="8d0f6-120">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="8d0f6-120">Resource name.</span></span>

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

### <span data-ttu-id="8d0f6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d0f6-121">-PassThru</span></span>
<span data-ttu-id="8d0f6-122">Adja meg, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="8d0f6-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="8d0f6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d0f6-123">-ResourceId</span></span>
<span data-ttu-id="8d0f6-124">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="8d0f6-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="8d0f6-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8d0f6-125">-Confirm</span></span>
<span data-ttu-id="8d0f6-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8d0f6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d0f6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d0f6-127">-WhatIf</span></span>
<span data-ttu-id="8d0f6-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8d0f6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d0f6-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d0f6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d0f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d0f6-130">CommonParameters</span></span>
<span data-ttu-id="8d0f6-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d0f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d0f6-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8d0f6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d0f6-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d0f6-133">INPUTS</span></span>

### <span data-ttu-id="8d0f6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8d0f6-134">System.String</span></span>

### <span data-ttu-id="8d0f6-135">Microsoft. Azure. commands. Security. models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="8d0f6-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="8d0f6-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d0f6-136">OUTPUTS</span></span>

### <span data-ttu-id="8d0f6-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d0f6-137">System.Boolean</span></span>

## <span data-ttu-id="8d0f6-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d0f6-138">NOTES</span></span>

## <span data-ttu-id="8d0f6-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d0f6-139">RELATED LINKS</span></span>