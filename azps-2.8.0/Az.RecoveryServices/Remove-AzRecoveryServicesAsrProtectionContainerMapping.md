---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 9ff992231e48efdfa9873aae75fc602ccd53a64e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839047"
---
# <span data-ttu-id="57c0f-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="57c0f-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="57c0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="57c0f-103">A megadott Azure webhely-helyreállítási védelmi tároló megfeleltetésének törlése.</span><span class="sxs-lookup"><span data-stu-id="57c0f-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="57c0f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57c0f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57c0f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="57c0f-105">DESCRIPTION</span></span>
<span data-ttu-id="57c0f-106">A **Remove-AzRecoveryServicesAsrProtectionContainerMapping** parancsmag törli a megadott Azure site Recovery Protection Container-megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="57c0f-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="57c0f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="57c0f-107">EXAMPLES</span></span>

### <span data-ttu-id="57c0f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="57c0f-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="57c0f-109">Elindítja a kijelölt védelmi tároló megfeleltetésének törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="57c0f-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="57c0f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57c0f-110">PARAMETERS</span></span>

### <span data-ttu-id="57c0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c0f-111">-DefaultProfile</span></span>
<span data-ttu-id="57c0f-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57c0f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="57c0f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="57c0f-113">-Force</span></span>
<span data-ttu-id="57c0f-114">Kényszerítse a parancsot, hogy ne adjon meg további figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="57c0f-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="57c0f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57c0f-115">-InputObject</span></span>
<span data-ttu-id="57c0f-116">A bemeneti objektum a parancsmag: az ASR-védelmi tároló társítása, amely a törlendő védelmi tárolóhoz tartozó objektum.</span><span class="sxs-lookup"><span data-stu-id="57c0f-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57c0f-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="57c0f-117">-Confirm</span></span>
<span data-ttu-id="57c0f-118">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="57c0f-118">Specify if confirmation is required.</span></span> <span data-ttu-id="57c0f-119">A megerősítési paraméter értékének beállítása $falsera a megerősítés kihagyása érdekében</span><span class="sxs-lookup"><span data-stu-id="57c0f-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="57c0f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57c0f-120">-WhatIf</span></span>
<span data-ttu-id="57c0f-121">Annak megjelenítése, hogy mi történik, ha a parancsmagot ténylegesen végrehajtják a parancsmag végrehajtása nélkül.</span><span class="sxs-lookup"><span data-stu-id="57c0f-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="57c0f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c0f-122">CommonParameters</span></span>
<span data-ttu-id="57c0f-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57c0f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c0f-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57c0f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c0f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57c0f-125">INPUTS</span></span>

### <span data-ttu-id="57c0f-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="57c0f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="57c0f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57c0f-127">OUTPUTS</span></span>

### <span data-ttu-id="57c0f-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="57c0f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="57c0f-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57c0f-129">NOTES</span></span>

## <span data-ttu-id="57c0f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57c0f-130">RELATED LINKS</span></span>

[<span data-ttu-id="57c0f-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="57c0f-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="57c0f-132">Új – AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="57c0f-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
