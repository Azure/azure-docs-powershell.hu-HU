---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 9a67729b384703ccc102b14d521d4422825bdb6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669644"
---
# <span data-ttu-id="453d2-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="453d2-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="453d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="453d2-102">SYNOPSIS</span></span>
<span data-ttu-id="453d2-103">A megadott Azure webhely-helyreállítási anyag törlése a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="453d2-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="453d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="453d2-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="453d2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="453d2-105">DESCRIPTION</span></span>
<span data-ttu-id="453d2-106">A **Remove-AzRecoveryServicesAsrFabric** parancsmag eltávolítja a megadott Azure webhely-helyreállítási szövetet a helyreállítási szolgáltatások boltozatból.</span><span class="sxs-lookup"><span data-stu-id="453d2-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="453d2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="453d2-107">EXAMPLES</span></span>

### <span data-ttu-id="453d2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="453d2-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="453d2-109">Elindítja a megadott anyag törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="453d2-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="453d2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="453d2-110">PARAMETERS</span></span>

### <span data-ttu-id="453d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="453d2-111">-DefaultProfile</span></span>
<span data-ttu-id="453d2-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="453d2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="453d2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="453d2-113">-Force</span></span>
<span data-ttu-id="453d2-114">Kényszerítse a parancsot, hogy ne adjon meg további figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="453d2-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="453d2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="453d2-115">-InputObject</span></span>
<span data-ttu-id="453d2-116">A bemeneti objektum a parancsmaghoz: az ASR-szövet objektum, amely megfelel a törlendő anyagnak.</span><span class="sxs-lookup"><span data-stu-id="453d2-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

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

### <span data-ttu-id="453d2-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="453d2-117">-Confirm</span></span>
<span data-ttu-id="453d2-118">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="453d2-118">Specify if confirmation is required.</span></span> <span data-ttu-id="453d2-119">Adja meg a megerősítési paraméter értékét $false a megerősítés kihagyása érdekében.</span><span class="sxs-lookup"><span data-stu-id="453d2-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="453d2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="453d2-120">-WhatIf</span></span>
<span data-ttu-id="453d2-121">Annak megjelenítése, hogy mi történik, ha a parancsmagot ténylegesen végrehajtják a parancsmag végrehajtása nélkül.</span><span class="sxs-lookup"><span data-stu-id="453d2-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="453d2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="453d2-122">CommonParameters</span></span>
<span data-ttu-id="453d2-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="453d2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="453d2-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="453d2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="453d2-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="453d2-125">INPUTS</span></span>

### <span data-ttu-id="453d2-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="453d2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="453d2-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="453d2-127">OUTPUTS</span></span>

### <span data-ttu-id="453d2-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="453d2-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="453d2-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="453d2-129">NOTES</span></span>

## <span data-ttu-id="453d2-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="453d2-130">RELATED LINKS</span></span>

[<span data-ttu-id="453d2-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="453d2-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="453d2-132">Új – AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="453d2-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
