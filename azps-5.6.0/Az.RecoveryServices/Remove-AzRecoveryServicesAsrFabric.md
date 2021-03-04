---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: ed06852e2ce0342502d01bd7f5ae17c0c3b8f4e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919258"
---
# <span data-ttu-id="b661b-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b661b-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="b661b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b661b-102">SYNOPSIS</span></span>
<span data-ttu-id="b661b-103">Törli a megadott Azure-webhely-helyreállítási hálót a helyreállítási szolgáltatások tárolóból.</span><span class="sxs-lookup"><span data-stu-id="b661b-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="b661b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b661b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b661b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b661b-105">DESCRIPTION</span></span>
<span data-ttu-id="b661b-106">A **Remove-AzRecoveryServicesAsrFabric** parancsmag eltávolítja a megadott Azure-webhely-helyreállítási hálót a helyreállítási szolgáltatások tárolóból.</span><span class="sxs-lookup"><span data-stu-id="b661b-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="b661b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b661b-107">EXAMPLES</span></span>

### <span data-ttu-id="b661b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b661b-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="b661b-109">Megkezdi a megadott anyag törlését, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="b661b-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b661b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b661b-110">PARAMETERS</span></span>

### <span data-ttu-id="b661b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b661b-111">-DefaultProfile</span></span>
<span data-ttu-id="b661b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b661b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b661b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b661b-113">-Force</span></span>
<span data-ttu-id="b661b-114">A parancs futtatását további figyelmeztetés nélkül kényszeríti.</span><span class="sxs-lookup"><span data-stu-id="b661b-114">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b661b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b661b-115">-InputObject</span></span>
<span data-ttu-id="b661b-116">A parancsmag bemeneti objektuma: A törölt anyagnak megfelelő ASR-anyag.</span><span class="sxs-lookup"><span data-stu-id="b661b-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b661b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b661b-117">-Confirm</span></span>
<span data-ttu-id="b661b-118">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="b661b-118">Specify if confirmation is required.</span></span> <span data-ttu-id="b661b-119">A megerősítési paraméter értékét állítsa $false a megerősítés kihagyása érdekében.</span><span class="sxs-lookup"><span data-stu-id="b661b-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="b661b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b661b-120">-WhatIf</span></span>
<span data-ttu-id="b661b-121">Azt mutatja meg, mi történik, ha a parancsmag végrehajtása a parancsmag végrehajtása nélkül történik.</span><span class="sxs-lookup"><span data-stu-id="b661b-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="b661b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b661b-122">CommonParameters</span></span>
<span data-ttu-id="b661b-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b661b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b661b-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b661b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b661b-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b661b-125">INPUTS</span></span>

### <span data-ttu-id="b661b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="b661b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="b661b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b661b-127">OUTPUTS</span></span>

### <span data-ttu-id="b661b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="b661b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b661b-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b661b-129">NOTES</span></span>

## <span data-ttu-id="b661b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b661b-130">RELATED LINKS</span></span>

[<span data-ttu-id="b661b-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b661b-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="b661b-132">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b661b-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
