---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9a9fbf8c25eba6206b3852476b5a72a2f96be423
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188031"
---
# <span data-ttu-id="872bd-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="872bd-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="872bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="872bd-102">SYNOPSIS</span></span>
<span data-ttu-id="872bd-103">Törli a kijelölt Azure-webhely helyreállítási szolgáltatás-szolgáltatóját a helyreállítási szolgáltatások boltozatáról.</span><span class="sxs-lookup"><span data-stu-id="872bd-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="872bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="872bd-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="872bd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="872bd-105">DESCRIPTION</span></span>
<span data-ttu-id="872bd-106">A **Remove-AzRecoveryServicesAsrServicesProvider** parancsmag eltávolítja a megadott Azure webhely-helyreállítási helyreállítási szolgáltatót a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="872bd-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="872bd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="872bd-107">EXAMPLES</span></span>

### <span data-ttu-id="872bd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="872bd-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="872bd-109">Elindítja a megadott Azure webhely-helyreállítási szolgáltató törlését/regisztrációját, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="872bd-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="872bd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="872bd-110">PARAMETERS</span></span>

### <span data-ttu-id="872bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="872bd-111">-DefaultProfile</span></span>
<span data-ttu-id="872bd-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="872bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="872bd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="872bd-113">-Force</span></span>
<span data-ttu-id="872bd-114">Kényszerítse a parancsot, hogy ne adjon meg további figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="872bd-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="872bd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="872bd-115">-InputObject</span></span>
<span data-ttu-id="872bd-116">A bemeneti objektum a parancsmaghoz: az ASR helyreállítási szolgáltatója objektum, amely megfelel az ASR-helyreállítási szolgáltatás által törlendő helyreállítási szolgáltatásnak.</span><span class="sxs-lookup"><span data-stu-id="872bd-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="872bd-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="872bd-117">-Confirm</span></span>
<span data-ttu-id="872bd-118">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="872bd-118">Specify if confirmation is required.</span></span> <span data-ttu-id="872bd-119">Adja meg a megerősítési paraméter értékét $false a megerősítés kihagyása érdekében.</span><span class="sxs-lookup"><span data-stu-id="872bd-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="872bd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="872bd-120">-WhatIf</span></span>
<span data-ttu-id="872bd-121">Annak megjelenítése, hogy mi történik, ha a parancsmagot ténylegesen végrehajtják a parancsmag végrehajtása nélkül.</span><span class="sxs-lookup"><span data-stu-id="872bd-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="872bd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872bd-122">CommonParameters</span></span>
<span data-ttu-id="872bd-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="872bd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872bd-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="872bd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872bd-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="872bd-125">INPUTS</span></span>

### <span data-ttu-id="872bd-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="872bd-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="872bd-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="872bd-127">OUTPUTS</span></span>

### <span data-ttu-id="872bd-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="872bd-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="872bd-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="872bd-129">NOTES</span></span>

## <span data-ttu-id="872bd-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="872bd-130">RELATED LINKS</span></span>

[<span data-ttu-id="872bd-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="872bd-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="872bd-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="872bd-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)