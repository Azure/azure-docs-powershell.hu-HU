---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 25475bd87579b693555280f3c465f157d69c807a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012637"
---
# <span data-ttu-id="b4280-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b4280-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="b4280-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4280-102">SYNOPSIS</span></span>
<span data-ttu-id="b4280-103">A megadott Azure webhely-helyreállítási védelmi tároló megfeleltetésének törlése.</span><span class="sxs-lookup"><span data-stu-id="b4280-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="b4280-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4280-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4280-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4280-105">DESCRIPTION</span></span>
<span data-ttu-id="b4280-106">A **Remove-AzRecoveryServicesAsrProtectionContainerMapping** parancsmag törli a megadott Azure site Recovery Protection Container-megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="b4280-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="b4280-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b4280-107">EXAMPLES</span></span>

### <span data-ttu-id="b4280-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b4280-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="b4280-109">Elindítja a kijelölt védelmi tároló megfeleltetésének törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b4280-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b4280-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4280-110">PARAMETERS</span></span>

### <span data-ttu-id="b4280-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4280-111">-DefaultProfile</span></span>
<span data-ttu-id="b4280-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4280-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b4280-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b4280-113">-Force</span></span>
<span data-ttu-id="b4280-114">Kényszerítse a parancsot, hogy ne adjon meg további figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="b4280-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="b4280-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4280-115">-InputObject</span></span>
<span data-ttu-id="b4280-116">A bemeneti objektum a parancsmag: az ASR-védelmi tároló társítása, amely a törlendő védelmi tárolóhoz tartozó objektum.</span><span class="sxs-lookup"><span data-stu-id="b4280-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

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

### <span data-ttu-id="b4280-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4280-117">-Confirm</span></span>
<span data-ttu-id="b4280-118">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="b4280-118">Specify if confirmation is required.</span></span> <span data-ttu-id="b4280-119">A megerősítési paraméter értékének beállítása $falsera a megerősítés kihagyása érdekében</span><span class="sxs-lookup"><span data-stu-id="b4280-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="b4280-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4280-120">-WhatIf</span></span>
<span data-ttu-id="b4280-121">Annak megjelenítése, hogy mi történik, ha a parancsmagot ténylegesen végrehajtják a parancsmag végrehajtása nélkül.</span><span class="sxs-lookup"><span data-stu-id="b4280-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="b4280-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4280-122">CommonParameters</span></span>
<span data-ttu-id="b4280-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4280-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4280-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b4280-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4280-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4280-125">INPUTS</span></span>

### <span data-ttu-id="b4280-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b4280-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="b4280-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4280-127">OUTPUTS</span></span>

### <span data-ttu-id="b4280-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b4280-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b4280-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4280-129">NOTES</span></span>

## <span data-ttu-id="b4280-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4280-130">RELATED LINKS</span></span>

[<span data-ttu-id="b4280-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b4280-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="b4280-132">Új – AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b4280-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
