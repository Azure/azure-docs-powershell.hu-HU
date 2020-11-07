---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 21a46346c681a6f184033d4f50d65e6c9a019844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679353"
---
# <span data-ttu-id="3819a-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3819a-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="3819a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3819a-102">SYNOPSIS</span></span>
<span data-ttu-id="3819a-103">Az Azure webhely-helyreállítási csomag tartalmának frissítése.</span><span class="sxs-lookup"><span data-stu-id="3819a-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3819a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3819a-104">SYNTAX</span></span>

### <span data-ttu-id="3819a-105">ByRPObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3819a-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3819a-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="3819a-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3819a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3819a-107">DESCRIPTION</span></span>
<span data-ttu-id="3819a-108">Az **Update-AzureRmRecoveryServicesAsrRecoveryPlan** parancsmag a helyreállítási terv tartalmát a megadott ASR-helyreállítási terv objektum vagy az ASR helyreállítási terv definíciós JSON-fájl tartalma alapján frissíti.</span><span class="sxs-lookup"><span data-stu-id="3819a-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="3819a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3819a-109">EXAMPLES</span></span>

### <span data-ttu-id="3819a-110">Példa 1: helyreállítási terv frissítése</span><span class="sxs-lookup"><span data-stu-id="3819a-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="3819a-111">Indítsa el a helyreállítási terv frissítésének műveletét a megadott ASR helyreállítási terv objektum tartalma alapján, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3819a-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3819a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3819a-112">PARAMETERS</span></span>

### <span data-ttu-id="3819a-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3819a-113">-InputObject</span></span>
<span data-ttu-id="3819a-114">Bemeneti objektum a parancsmaghoz: Itt adhatja meg az ASR helyreállítási terv objektumát, amelynek tartalma az objektum által hivatkozott helyreállítási terv frissítéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="3819a-114">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3819a-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="3819a-115">-Path</span></span>
<span data-ttu-id="3819a-116">A helyreállítási terv frissítéséhez használt helyreállítási terv definíciójának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3819a-116">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3819a-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3819a-117">-Confirm</span></span>
<span data-ttu-id="3819a-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3819a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3819a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3819a-119">-WhatIf</span></span>
<span data-ttu-id="3819a-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3819a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3819a-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3819a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3819a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3819a-122">CommonParameters</span></span>
<span data-ttu-id="3819a-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3819a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3819a-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3819a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3819a-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3819a-125">INPUTS</span></span>

### <span data-ttu-id="3819a-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3819a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="3819a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3819a-127">OUTPUTS</span></span>

### <span data-ttu-id="3819a-128">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="3819a-128">System.Object</span></span>

## <span data-ttu-id="3819a-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3819a-129">NOTES</span></span>

## <span data-ttu-id="3819a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3819a-130">RELATED LINKS</span></span>

[<span data-ttu-id="3819a-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3819a-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="3819a-132">Új – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3819a-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="3819a-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3819a-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)


