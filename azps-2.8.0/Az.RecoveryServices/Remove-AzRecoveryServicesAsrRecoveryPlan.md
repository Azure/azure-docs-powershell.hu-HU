---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4931b32cf2c74180ad06b071d19ef57f4be2285e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838546"
---
# <span data-ttu-id="bce9e-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bce9e-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="bce9e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bce9e-102">SYNOPSIS</span></span>
<span data-ttu-id="bce9e-103">Törli a megadott ASR-helyreállítási csomagot a helyreállítási szolgáltatások boltozatból.</span><span class="sxs-lookup"><span data-stu-id="bce9e-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="bce9e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bce9e-104">SYNTAX</span></span>

### <span data-ttu-id="bce9e-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bce9e-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bce9e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bce9e-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bce9e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bce9e-107">DESCRIPTION</span></span>
<span data-ttu-id="bce9e-108">A **Remove-AzRecoveryServicesAsrRecoveryPlan** parancsmag törli a megadott helyreállítási csomagot a helyreállítási szolgáltatások boltozatból.</span><span class="sxs-lookup"><span data-stu-id="bce9e-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="bce9e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bce9e-109">EXAMPLES</span></span>

### <span data-ttu-id="bce9e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bce9e-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="bce9e-111">Elindítja a megadott helyreállítási terv törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="bce9e-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="bce9e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bce9e-112">PARAMETERS</span></span>

### <span data-ttu-id="bce9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce9e-113">-DefaultProfile</span></span>
<span data-ttu-id="bce9e-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bce9e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bce9e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bce9e-115">-InputObject</span></span>
<span data-ttu-id="bce9e-116">A bemeneti objektum a parancsmag: az ASR-helyreállítási terv objektuma, amely megfelel a törlendő helyreállítási tervnek.</span><span class="sxs-lookup"><span data-stu-id="bce9e-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="bce9e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bce9e-117">-Name</span></span>
<span data-ttu-id="bce9e-118">A törlendő helyreállítási terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bce9e-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="bce9e-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bce9e-119">-Confirm</span></span>
<span data-ttu-id="bce9e-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bce9e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bce9e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bce9e-121">-WhatIf</span></span>
<span data-ttu-id="bce9e-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bce9e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bce9e-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bce9e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bce9e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce9e-124">CommonParameters</span></span>
<span data-ttu-id="bce9e-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bce9e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce9e-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bce9e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce9e-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bce9e-127">INPUTS</span></span>

### <span data-ttu-id="bce9e-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bce9e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="bce9e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bce9e-129">OUTPUTS</span></span>

### <span data-ttu-id="bce9e-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bce9e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bce9e-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bce9e-131">NOTES</span></span>

## <span data-ttu-id="bce9e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bce9e-132">RELATED LINKS</span></span>

[<span data-ttu-id="bce9e-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bce9e-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="bce9e-134">Új – AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bce9e-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="bce9e-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bce9e-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


