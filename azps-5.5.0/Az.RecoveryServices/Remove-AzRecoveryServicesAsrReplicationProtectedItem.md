---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 71731c0a6f4f0bb917cb7490c1647add71b9a893
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153843"
---
# <span data-ttu-id="d37b4-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d37b4-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="d37b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d37b4-102">SYNOPSIS</span></span>
<span data-ttu-id="d37b4-103">Leállítja/letiltja a replikációt egy azure-webhely-helyreállítási replikációval védett elemhez.</span><span class="sxs-lookup"><span data-stu-id="d37b4-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="d37b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d37b4-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d37b4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d37b4-105">DESCRIPTION</span></span>
<span data-ttu-id="d37b4-106">A **Remove-AzRecoveryServicesAsrReplicationProtectedItem** parancsmag letiltja a megadott Azure-webhely-helyreállítási replikációval védett elem replikációját.</span><span class="sxs-lookup"><span data-stu-id="d37b4-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="d37b4-107">Ez a művelet leállítja a replikációt a védett elemhez.</span><span class="sxs-lookup"><span data-stu-id="d37b4-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="d37b4-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d37b4-108">EXAMPLES</span></span>

### <span data-ttu-id="d37b4-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="d37b4-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="d37b4-110">Elindítja a replikáció letiltását a megadott replikációs védett elemhez, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="d37b4-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d37b4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d37b4-111">PARAMETERS</span></span>

### <span data-ttu-id="d37b4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37b4-112">-DefaultProfile</span></span>
<span data-ttu-id="d37b4-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d37b4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d37b4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d37b4-114">-Force</span></span>
<span data-ttu-id="d37b4-115">A parancs futtatását további figyelmeztetés nélkül kényszeríti.</span><span class="sxs-lookup"><span data-stu-id="d37b4-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="d37b4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d37b4-116">-InputObject</span></span>
<span data-ttu-id="d37b4-117">A parancsmag bemeneti objektuma: Az ASR replikációs védett elemobjektuma annak a replikációval védett elemnek megfelelően, amelyhez a replikációt le kell tiltani.</span><span class="sxs-lookup"><span data-stu-id="d37b4-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d37b4-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="d37b4-118">-WaitForCompletion</span></span>
<span data-ttu-id="d37b4-119">Azt jelzi, hogy a parancsmagnak a visszatérés előtt meg kell várnia, amíg befejeződik a művelet.</span><span class="sxs-lookup"><span data-stu-id="d37b4-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="d37b4-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d37b4-120">-Confirm</span></span>
<span data-ttu-id="d37b4-121">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="d37b4-121">Specify if confirmation is required.</span></span> <span data-ttu-id="d37b4-122">A megerősítési paraméter értékét állítsa $false a megerősítés kihagyása érdekében.</span><span class="sxs-lookup"><span data-stu-id="d37b4-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="d37b4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37b4-123">-WhatIf</span></span>
<span data-ttu-id="d37b4-124">Azt mutatja, mi történik, ha a parancsmag végrehajtása a parancsmag végrehajtása nélkül történik.</span><span class="sxs-lookup"><span data-stu-id="d37b4-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="d37b4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37b4-125">CommonParameters</span></span>
<span data-ttu-id="d37b4-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d37b4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37b4-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d37b4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37b4-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d37b4-128">INPUTS</span></span>

### <span data-ttu-id="d37b4-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d37b4-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="d37b4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d37b4-130">OUTPUTS</span></span>

### <span data-ttu-id="d37b4-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="d37b4-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d37b4-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d37b4-132">NOTES</span></span>

## <span data-ttu-id="d37b4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d37b4-133">RELATED LINKS</span></span>

[<span data-ttu-id="d37b4-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d37b4-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="d37b4-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d37b4-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="d37b4-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d37b4-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
