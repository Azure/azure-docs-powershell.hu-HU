---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: eb42cdf74482a5161ab75df459c78d88749fde7e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495744"
---
# <span data-ttu-id="cd455-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cd455-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="cd455-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd455-102">SYNOPSIS</span></span>
<span data-ttu-id="cd455-103">Az Azure webhely-helyreállítási csomag tartalmának frissítése.</span><span class="sxs-lookup"><span data-stu-id="cd455-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd455-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd455-104">SYNTAX</span></span>

### <span data-ttu-id="cd455-105">ByRPObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd455-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd455-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="cd455-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd455-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd455-107">DESCRIPTION</span></span>
<span data-ttu-id="cd455-108">Az **Update-AzureRmRecoveryServicesAsrRecoveryPlan** parancsmag a helyreállítási terv tartalmát a megadott ASR-helyreállítási terv objektum vagy az ASR helyreállítási terv definíciós JSON-fájl tartalma alapján frissíti.</span><span class="sxs-lookup"><span data-stu-id="cd455-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="cd455-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cd455-109">EXAMPLES</span></span>

### <span data-ttu-id="cd455-110">Példa 1: helyreállítási terv frissítése</span><span class="sxs-lookup"><span data-stu-id="cd455-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="cd455-111">Indítsa el a helyreállítási terv frissítésének műveletét a megadott ASR helyreállítási terv objektum tartalma alapján, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="cd455-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="cd455-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd455-112">PARAMETERS</span></span>

### <span data-ttu-id="cd455-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd455-113">-DefaultProfile</span></span>
<span data-ttu-id="cd455-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd455-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd455-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd455-115">-InputObject</span></span>
<span data-ttu-id="cd455-116">Bemeneti objektum a parancsmaghoz: Itt adhatja meg az ASR helyreállítási terv objektumát, amelynek tartalma az objektum által hivatkozott helyreállítási terv frissítéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="cd455-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd455-117">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="cd455-117">-Path</span></span>
<span data-ttu-id="cd455-118">A helyreállítási terv frissítéséhez használt helyreállítási terv definíciójának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd455-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd455-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cd455-119">-Confirm</span></span>
<span data-ttu-id="cd455-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cd455-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd455-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd455-121">-WhatIf</span></span>
<span data-ttu-id="cd455-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cd455-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd455-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd455-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd455-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd455-124">CommonParameters</span></span>
<span data-ttu-id="cd455-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd455-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd455-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd455-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd455-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd455-127">INPUTS</span></span>

### <span data-ttu-id="cd455-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cd455-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="cd455-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd455-129">OUTPUTS</span></span>

### <span data-ttu-id="cd455-130">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="cd455-130">System.Object</span></span>

## <span data-ttu-id="cd455-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd455-131">NOTES</span></span>

## <span data-ttu-id="cd455-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd455-132">RELATED LINKS</span></span>

[<span data-ttu-id="cd455-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cd455-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="cd455-134">Új – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cd455-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="cd455-135">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cd455-135">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)
