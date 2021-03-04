---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 96c50c812dcb73c92dc3704e576bfc45fbf21bba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919234"
---
# <span data-ttu-id="d7201-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d7201-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="d7201-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7201-102">SYNOPSIS</span></span>
<span data-ttu-id="d7201-103">Törli a megadott ASR helyreállítási tervet a Helyreállítási szolgáltatások tárolóból.</span><span class="sxs-lookup"><span data-stu-id="d7201-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="d7201-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d7201-104">SYNTAX</span></span>

### <span data-ttu-id="d7201-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7201-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7201-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d7201-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7201-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d7201-107">DESCRIPTION</span></span>
<span data-ttu-id="d7201-108">A **Remove-AzRecoveryServicesAsrRecoveryPlan** parancsmag törli a megadott helyreállítási tervet a Helyreállítási szolgáltatások tárolóból.</span><span class="sxs-lookup"><span data-stu-id="d7201-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="d7201-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d7201-109">EXAMPLES</span></span>

### <span data-ttu-id="d7201-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d7201-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="d7201-111">Elindítja a megadott helyreállítási terv törlését, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="d7201-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d7201-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7201-112">PARAMETERS</span></span>

### <span data-ttu-id="d7201-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7201-113">-DefaultProfile</span></span>
<span data-ttu-id="d7201-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7201-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7201-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7201-115">-InputObject</span></span>
<span data-ttu-id="d7201-116">A parancsmag bemeneti objektuma: A törölt helyreállítási tervnek megfelelő ASR helyreállítási terv objektum.</span><span class="sxs-lookup"><span data-stu-id="d7201-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7201-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d7201-117">-Name</span></span>
<span data-ttu-id="d7201-118">A törölni szükséges helyreállítási terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7201-118">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7201-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7201-119">-Confirm</span></span>
<span data-ttu-id="d7201-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d7201-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7201-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7201-121">-WhatIf</span></span>
<span data-ttu-id="d7201-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d7201-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7201-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7201-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7201-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7201-124">CommonParameters</span></span>
<span data-ttu-id="d7201-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7201-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7201-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7201-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7201-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7201-127">INPUTS</span></span>

### <span data-ttu-id="d7201-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d7201-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="d7201-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7201-129">OUTPUTS</span></span>

### <span data-ttu-id="d7201-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="d7201-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d7201-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d7201-131">NOTES</span></span>

## <span data-ttu-id="d7201-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7201-132">RELATED LINKS</span></span>

[<span data-ttu-id="d7201-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d7201-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d7201-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d7201-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d7201-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d7201-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


