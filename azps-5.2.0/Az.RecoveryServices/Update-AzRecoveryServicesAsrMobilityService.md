---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358062"
---
# <span data-ttu-id="282a3-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="282a3-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="282a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="282a3-102">SYNOPSIS</span></span>
<span data-ttu-id="282a3-103">Push mobility service agent updates to protected machines.</span><span class="sxs-lookup"><span data-stu-id="282a3-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="282a3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="282a3-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="282a3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="282a3-105">DESCRIPTION</span></span>
<span data-ttu-id="282a3-106">Az **Update-AzRecoveryServicesAsrMobilityService** parancsmag megkísérli leküldeni a mobilszolgáltatás ügynökének frissítéseit a védett gépekre (ha elérhető frissítés.)</span><span class="sxs-lookup"><span data-stu-id="282a3-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="282a3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="282a3-107">EXAMPLES</span></span>

### <span data-ttu-id="282a3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="282a3-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="282a3-109">A frissítési replikációval védett elem mobilitási szolgáltatási ügynökének nyomon követése.</span><span class="sxs-lookup"><span data-stu-id="282a3-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="282a3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="282a3-110">PARAMETERS</span></span>

### <span data-ttu-id="282a3-111">-Account</span><span class="sxs-lookup"><span data-stu-id="282a3-111">-Account</span></span>
<span data-ttu-id="282a3-112">A frissítés leküldéséhez használt futtatás fiókazonosítóként.</span><span class="sxs-lookup"><span data-stu-id="282a3-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="282a3-113">A frissítésnek megfelelő ASR-anyagban fiókként futtatott fiókok listájából kell egynek lennie.</span><span class="sxs-lookup"><span data-stu-id="282a3-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="282a3-114">-DefaultProfile</span></span>
<span data-ttu-id="282a3-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="282a3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="282a3-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="282a3-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="282a3-117">Az Azure-webhely-helyreállítás replikációja által védett, frissíthető elem.</span><span class="sxs-lookup"><span data-stu-id="282a3-117">Azure Site Recovery replication protected item to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="282a3-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="282a3-118">-Confirm</span></span>
<span data-ttu-id="282a3-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="282a3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="282a3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="282a3-120">-WhatIf</span></span>
<span data-ttu-id="282a3-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="282a3-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="282a3-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="282a3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="282a3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="282a3-123">CommonParameters</span></span>
<span data-ttu-id="282a3-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="282a3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="282a3-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="282a3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="282a3-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="282a3-126">INPUTS</span></span>

### <span data-ttu-id="282a3-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="282a3-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="282a3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="282a3-128">OUTPUTS</span></span>

### <span data-ttu-id="282a3-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="282a3-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="282a3-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="282a3-130">NOTES</span></span>

## <span data-ttu-id="282a3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="282a3-131">RELATED LINKS</span></span>
