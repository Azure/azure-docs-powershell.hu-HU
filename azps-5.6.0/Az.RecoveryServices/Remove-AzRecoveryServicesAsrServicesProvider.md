---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: f3c18813cd3c002270d655b88fbc9285338a4338
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919186"
---
# <span data-ttu-id="c17e1-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c17e1-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="c17e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c17e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c17e1-103">Törli/törli a megadott Azure-webhely-helyreállítási helyreállítási szolgáltatót a helyreállítási szolgáltatások tárolóból.</span><span class="sxs-lookup"><span data-stu-id="c17e1-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="c17e1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c17e1-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c17e1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c17e1-105">DESCRIPTION</span></span>
<span data-ttu-id="c17e1-106">A **Remove-AzRecoveryServicesAsrServicesProvider** parancsmag eltávolítja a megadott Azure Site Recovery helyreállítási szolgáltatót a tárolóból.</span><span class="sxs-lookup"><span data-stu-id="c17e1-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="c17e1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c17e1-107">EXAMPLES</span></span>

### <span data-ttu-id="c17e1-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c17e1-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="c17e1-109">Elindítja a megadott Azure-webhely-helyreállítási szolgáltató törlését/törlését, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="c17e1-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c17e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c17e1-110">PARAMETERS</span></span>

### <span data-ttu-id="c17e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c17e1-111">-DefaultProfile</span></span>
<span data-ttu-id="c17e1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c17e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c17e1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c17e1-113">-Force</span></span>
<span data-ttu-id="c17e1-114">A parancs futtatását további figyelmeztetés nélkül kényszeríti.</span><span class="sxs-lookup"><span data-stu-id="c17e1-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="c17e1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c17e1-115">-InputObject</span></span>
<span data-ttu-id="c17e1-116">A parancsmag bemeneti objektuma: A törölt ASR helyreállítási szolgáltatónak megfelelő ASR helyreállítási szolgáltatás-objektum.</span><span class="sxs-lookup"><span data-stu-id="c17e1-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c17e1-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c17e1-117">-Confirm</span></span>
<span data-ttu-id="c17e1-118">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="c17e1-118">Specify if confirmation is required.</span></span> <span data-ttu-id="c17e1-119">A megerősítési paraméter értékét állítsa $false a megerősítés kihagyása érdekében.</span><span class="sxs-lookup"><span data-stu-id="c17e1-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="c17e1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c17e1-120">-WhatIf</span></span>
<span data-ttu-id="c17e1-121">Azt mutatja meg, mi történik, ha a parancsmag végrehajtása a parancsmag végrehajtása nélkül történik.</span><span class="sxs-lookup"><span data-stu-id="c17e1-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="c17e1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c17e1-122">CommonParameters</span></span>
<span data-ttu-id="c17e1-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c17e1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c17e1-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c17e1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c17e1-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c17e1-125">INPUTS</span></span>

### <span data-ttu-id="c17e1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c17e1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="c17e1-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c17e1-127">OUTPUTS</span></span>

### <span data-ttu-id="c17e1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="c17e1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c17e1-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c17e1-129">NOTES</span></span>

## <span data-ttu-id="c17e1-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c17e1-130">RELATED LINKS</span></span>

[<span data-ttu-id="c17e1-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c17e1-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="c17e1-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c17e1-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
