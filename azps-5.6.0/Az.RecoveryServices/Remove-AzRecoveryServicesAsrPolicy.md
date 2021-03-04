---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 5743d1d9288f0045755aab752274c24640b3c548
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919250"
---
# <span data-ttu-id="135db-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="135db-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="135db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="135db-102">SYNOPSIS</span></span>
<span data-ttu-id="135db-103">Törli a megadott ASR replikációs házirendet a helyreállítási szolgáltatások tárolóból.</span><span class="sxs-lookup"><span data-stu-id="135db-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="135db-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="135db-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="135db-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="135db-105">DESCRIPTION</span></span>
<span data-ttu-id="135db-106">A **Remove-AzRecoveryServicesAsrPolicy** parancsmag törölte a megadott replikációs házirendet a helyreállítási szolgáltatások tárolóból.</span><span class="sxs-lookup"><span data-stu-id="135db-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="135db-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="135db-107">EXAMPLES</span></span>

### <span data-ttu-id="135db-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="135db-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="135db-109">Elindítja a megadott replikációs házirend törlését, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="135db-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="135db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="135db-110">PARAMETERS</span></span>

### <span data-ttu-id="135db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="135db-111">-DefaultProfile</span></span>
<span data-ttu-id="135db-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="135db-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="135db-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="135db-113">-InputObject</span></span>
<span data-ttu-id="135db-114">A parancsmag bemeneti objektuma: A törölt replikációs házirendnek megfelelő ASR replikációs házirend-objektum.</span><span class="sxs-lookup"><span data-stu-id="135db-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="135db-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="135db-115">-Confirm</span></span>
<span data-ttu-id="135db-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="135db-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="135db-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="135db-117">-WhatIf</span></span>
<span data-ttu-id="135db-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="135db-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="135db-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="135db-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="135db-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="135db-120">CommonParameters</span></span>
<span data-ttu-id="135db-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="135db-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="135db-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="135db-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="135db-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="135db-123">INPUTS</span></span>

### <span data-ttu-id="135db-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="135db-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="135db-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="135db-125">OUTPUTS</span></span>

### <span data-ttu-id="135db-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="135db-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="135db-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="135db-127">NOTES</span></span>

## <span data-ttu-id="135db-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="135db-128">RELATED LINKS</span></span>

[<span data-ttu-id="135db-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="135db-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="135db-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="135db-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
