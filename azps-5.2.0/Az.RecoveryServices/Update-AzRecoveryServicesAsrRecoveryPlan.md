---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 99c91f24bcc81ee6d6971b74779dfd116b90fdef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364753"
---
# <span data-ttu-id="d0ffc-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d0ffc-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="d0ffc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="d0ffc-103">Frissíti egy Azure-webhely helyreállítási terv tartalmát.</span><span class="sxs-lookup"><span data-stu-id="d0ffc-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="d0ffc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d0ffc-104">SYNTAX</span></span>

### <span data-ttu-id="d0ffc-105">ByRPObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0ffc-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0ffc-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="d0ffc-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0ffc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d0ffc-107">DESCRIPTION</span></span>
<span data-ttu-id="d0ffc-108">Az **Update-AzRecoveryServicesAsrRecoveryPlan** parancsmag frissíti a helyreállítási terv tartalmát a megadott ASR helyreállítási terv objektum vagy ASR helyreállítási terv definíciója json fájljának tartalma alapján.</span><span class="sxs-lookup"><span data-stu-id="d0ffc-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="d0ffc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d0ffc-109">EXAMPLES</span></span>

### <span data-ttu-id="d0ffc-110">1. példa: Helyreállítási terv frissítése</span><span class="sxs-lookup"><span data-stu-id="d0ffc-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="d0ffc-111">Indítsa el a helyreállítási terv frissítését a megadott ASR helyreállítási terv objektum tartalmával, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="d0ffc-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d0ffc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0ffc-112">PARAMETERS</span></span>

### <span data-ttu-id="d0ffc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0ffc-113">-DefaultProfile</span></span>
<span data-ttu-id="d0ffc-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0ffc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d0ffc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0ffc-115">-InputObject</span></span>
<span data-ttu-id="d0ffc-116">Bemeneti objektum a parancsmaghoz: Egy ASR helyreállítási tervobjektumot ad meg, amelynek tartalma az objektum által hivatkozott helyreállítási terv frissítéséhez használatos.</span><span class="sxs-lookup"><span data-stu-id="d0ffc-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

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

### <span data-ttu-id="d0ffc-117">-Path</span><span class="sxs-lookup"><span data-stu-id="d0ffc-117">-Path</span></span>
<span data-ttu-id="d0ffc-118">A helyreállítási terv frissítéséhez használt json-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0ffc-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

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

### <span data-ttu-id="d0ffc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0ffc-119">-Confirm</span></span>
<span data-ttu-id="d0ffc-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d0ffc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0ffc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0ffc-121">-WhatIf</span></span>
<span data-ttu-id="d0ffc-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d0ffc-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0ffc-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0ffc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0ffc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0ffc-124">CommonParameters</span></span>
<span data-ttu-id="d0ffc-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0ffc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0ffc-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0ffc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0ffc-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0ffc-127">INPUTS</span></span>

### <span data-ttu-id="d0ffc-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d0ffc-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="d0ffc-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0ffc-129">OUTPUTS</span></span>

### <span data-ttu-id="d0ffc-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="d0ffc-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d0ffc-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d0ffc-131">NOTES</span></span>

## <span data-ttu-id="d0ffc-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0ffc-132">RELATED LINKS</span></span>

[<span data-ttu-id="d0ffc-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d0ffc-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d0ffc-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d0ffc-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d0ffc-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d0ffc-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)
