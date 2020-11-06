---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 45979620ea4067af3fc906dfd7348d27b4850f06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498891"
---
# <span data-ttu-id="94eeb-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="94eeb-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="94eeb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="94eeb-103">A megadott Azure webhely-helyreállítási anyag törlése a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="94eeb-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94eeb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94eeb-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94eeb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94eeb-105">DESCRIPTION</span></span>
<span data-ttu-id="94eeb-106">A **Remove-AzureRmRecoveryServicesAsrFabric** parancsmag eltávolítja a megadott Azure webhely-helyreállítási szövetet a helyreállítási szolgáltatások boltozatból.</span><span class="sxs-lookup"><span data-stu-id="94eeb-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="94eeb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="94eeb-107">EXAMPLES</span></span>

### <span data-ttu-id="94eeb-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="94eeb-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="94eeb-109">Elindítja a megadott anyag törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="94eeb-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="94eeb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94eeb-110">PARAMETERS</span></span>

### <span data-ttu-id="94eeb-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94eeb-111">-Confirm</span></span>
<span data-ttu-id="94eeb-112">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="94eeb-112">Specify if confirmation is required.</span></span> <span data-ttu-id="94eeb-113">Adja meg a megerősítési paraméter értékét $false a megerősítés kihagyása érdekében.</span><span class="sxs-lookup"><span data-stu-id="94eeb-113">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94eeb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94eeb-114">-DefaultProfile</span></span>
<span data-ttu-id="94eeb-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94eeb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94eeb-116">-Force</span><span class="sxs-lookup"><span data-stu-id="94eeb-116">-Force</span></span>
<span data-ttu-id="94eeb-117">Kényszerítse a parancsot, hogy ne adjon meg további figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="94eeb-117">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94eeb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94eeb-118">-InputObject</span></span>
<span data-ttu-id="94eeb-119">A bemeneti objektum a parancsmaghoz: az ASR-szövet objektum, amely megfelel a törlendő anyagnak.</span><span class="sxs-lookup"><span data-stu-id="94eeb-119">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94eeb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94eeb-120">-WhatIf</span></span>
<span data-ttu-id="94eeb-121">Annak megjelenítése, hogy mi történik, ha a parancsmagot ténylegesen végrehajtják a parancsmag végrehajtása nélkül.</span><span class="sxs-lookup"><span data-stu-id="94eeb-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94eeb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94eeb-122">CommonParameters</span></span>
<span data-ttu-id="94eeb-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94eeb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94eeb-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94eeb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94eeb-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94eeb-125">INPUTS</span></span>

### <span data-ttu-id="94eeb-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="94eeb-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="94eeb-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94eeb-127">OUTPUTS</span></span>

### <span data-ttu-id="94eeb-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="94eeb-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="94eeb-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94eeb-129">NOTES</span></span>

## <span data-ttu-id="94eeb-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94eeb-130">RELATED LINKS</span></span>

[<span data-ttu-id="94eeb-131">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="94eeb-131">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="94eeb-132">Új – AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="94eeb-132">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
