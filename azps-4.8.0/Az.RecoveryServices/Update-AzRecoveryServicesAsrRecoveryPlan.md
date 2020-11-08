---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 99c91f24bcc81ee6d6971b74779dfd116b90fdef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018069"
---
# <span data-ttu-id="c51c9-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c51c9-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="c51c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c51c9-102">SYNOPSIS</span></span>
<span data-ttu-id="c51c9-103">Az Azure webhely-helyreállítási csomag tartalmának frissítése.</span><span class="sxs-lookup"><span data-stu-id="c51c9-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="c51c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c51c9-104">SYNTAX</span></span>

### <span data-ttu-id="c51c9-105">ByRPObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c51c9-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c51c9-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="c51c9-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c51c9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c51c9-107">DESCRIPTION</span></span>
<span data-ttu-id="c51c9-108">Az **Update-AzRecoveryServicesAsrRecoveryPlan** parancsmag a helyreállítási terv tartalmát a megadott ASR-helyreállítási terv objektum vagy az ASR helyreállítási terv definíciós JSON-fájl tartalma alapján frissíti.</span><span class="sxs-lookup"><span data-stu-id="c51c9-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="c51c9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c51c9-109">EXAMPLES</span></span>

### <span data-ttu-id="c51c9-110">Példa 1: helyreállítási terv frissítése</span><span class="sxs-lookup"><span data-stu-id="c51c9-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="c51c9-111">Indítsa el a helyreállítási terv frissítésének műveletét a megadott ASR helyreállítási terv objektum tartalma alapján, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="c51c9-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c51c9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c51c9-112">PARAMETERS</span></span>

### <span data-ttu-id="c51c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c51c9-113">-DefaultProfile</span></span>
<span data-ttu-id="c51c9-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c51c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c51c9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c51c9-115">-InputObject</span></span>
<span data-ttu-id="c51c9-116">Bemeneti objektum a parancsmaghoz: Itt adhatja meg az ASR helyreállítási terv objektumát, amelynek tartalma az objektum által hivatkozott helyreállítási terv frissítéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="c51c9-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

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

### <span data-ttu-id="c51c9-117">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="c51c9-117">-Path</span></span>
<span data-ttu-id="c51c9-118">A helyreállítási terv frissítéséhez használt helyreállítási terv definíciójának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c51c9-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

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

### <span data-ttu-id="c51c9-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c51c9-119">-Confirm</span></span>
<span data-ttu-id="c51c9-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c51c9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c51c9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c51c9-121">-WhatIf</span></span>
<span data-ttu-id="c51c9-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c51c9-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c51c9-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c51c9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c51c9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c51c9-124">CommonParameters</span></span>
<span data-ttu-id="c51c9-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c51c9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c51c9-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c51c9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c51c9-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c51c9-127">INPUTS</span></span>

### <span data-ttu-id="c51c9-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c51c9-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="c51c9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c51c9-129">OUTPUTS</span></span>

### <span data-ttu-id="c51c9-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c51c9-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c51c9-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c51c9-131">NOTES</span></span>

## <span data-ttu-id="c51c9-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c51c9-132">RELATED LINKS</span></span>

[<span data-ttu-id="c51c9-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c51c9-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c51c9-134">Új – AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c51c9-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c51c9-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c51c9-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)
