---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 095759ca2753cac4f7155430a241e0554e910fd6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184247"
---
# <span data-ttu-id="81bad-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="81bad-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="81bad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81bad-102">SYNOPSIS</span></span>
<span data-ttu-id="81bad-103">A megadott Azure webhely-helyreállítási anyag törlése a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="81bad-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="81bad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81bad-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81bad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="81bad-105">DESCRIPTION</span></span>
<span data-ttu-id="81bad-106">A **Remove-AzRecoveryServicesAsrFabric** parancsmag eltávolítja a megadott Azure webhely-helyreállítási szövetet a helyreállítási szolgáltatások boltozatból.</span><span class="sxs-lookup"><span data-stu-id="81bad-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="81bad-107">Példák</span><span class="sxs-lookup"><span data-stu-id="81bad-107">EXAMPLES</span></span>

### <span data-ttu-id="81bad-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="81bad-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="81bad-109">Elindítja a megadott anyag törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="81bad-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="81bad-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81bad-110">PARAMETERS</span></span>

### <span data-ttu-id="81bad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81bad-111">-DefaultProfile</span></span>
<span data-ttu-id="81bad-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81bad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="81bad-113">-Force</span><span class="sxs-lookup"><span data-stu-id="81bad-113">-Force</span></span>
<span data-ttu-id="81bad-114">Kényszerítse a parancsot, hogy ne adjon meg további figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="81bad-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="81bad-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81bad-115">-InputObject</span></span>
<span data-ttu-id="81bad-116">A bemeneti objektum a parancsmaghoz: az ASR-szövet objektum, amely megfelel a törlendő anyagnak.</span><span class="sxs-lookup"><span data-stu-id="81bad-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

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

### <span data-ttu-id="81bad-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81bad-117">-Confirm</span></span>
<span data-ttu-id="81bad-118">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="81bad-118">Specify if confirmation is required.</span></span> <span data-ttu-id="81bad-119">Adja meg a megerősítési paraméter értékét $false a megerősítés kihagyása érdekében.</span><span class="sxs-lookup"><span data-stu-id="81bad-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="81bad-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81bad-120">-WhatIf</span></span>
<span data-ttu-id="81bad-121">Annak megjelenítése, hogy mi történik, ha a parancsmagot ténylegesen végrehajtják a parancsmag végrehajtása nélkül.</span><span class="sxs-lookup"><span data-stu-id="81bad-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="81bad-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bad-122">CommonParameters</span></span>
<span data-ttu-id="81bad-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81bad-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bad-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="81bad-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bad-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81bad-125">INPUTS</span></span>

### <span data-ttu-id="81bad-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="81bad-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="81bad-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81bad-127">OUTPUTS</span></span>

### <span data-ttu-id="81bad-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="81bad-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="81bad-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81bad-129">NOTES</span></span>

## <span data-ttu-id="81bad-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81bad-130">RELATED LINKS</span></span>

[<span data-ttu-id="81bad-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="81bad-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="81bad-132">Új – AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="81bad-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
