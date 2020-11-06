---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 4de1861c3db804e7ffd4371f4e35c241843374cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492787"
---
# <span data-ttu-id="26c44-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="26c44-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="26c44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26c44-102">SYNOPSIS</span></span>
<span data-ttu-id="26c44-103">Törli a kijelölt Azure-webhely helyreállítási szolgáltatás-szolgáltatóját a helyreállítási szolgáltatások boltozatáról.</span><span class="sxs-lookup"><span data-stu-id="26c44-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26c44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26c44-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26c44-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="26c44-105">DESCRIPTION</span></span>
<span data-ttu-id="26c44-106">A **Remove-AzureRmRecoveryServicesAsrServicesProvider** parancsmag eltávolítja a megadott Azure webhely-helyreállítási helyreállítási szolgáltatót a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="26c44-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="26c44-107">Példák</span><span class="sxs-lookup"><span data-stu-id="26c44-107">EXAMPLES</span></span>

### <span data-ttu-id="26c44-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="26c44-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="26c44-109">Elindítja a megadott Azure webhely-helyreállítási szolgáltató törlését/regisztrációját, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="26c44-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="26c44-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26c44-110">PARAMETERS</span></span>

### <span data-ttu-id="26c44-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26c44-111">-DefaultProfile</span></span>
<span data-ttu-id="26c44-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26c44-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26c44-113">-Force</span><span class="sxs-lookup"><span data-stu-id="26c44-113">-Force</span></span>
<span data-ttu-id="26c44-114">Kényszerítse a parancsot, hogy ne adjon meg további figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="26c44-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="26c44-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26c44-115">-InputObject</span></span>
<span data-ttu-id="26c44-116">A bemeneti objektum a parancsmaghoz: az ASR helyreállítási szolgáltatója objektum, amely megfelel az ASR-helyreállítási szolgáltatás által törlendő helyreállítási szolgáltatásnak.</span><span class="sxs-lookup"><span data-stu-id="26c44-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="26c44-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="26c44-117">-Confirm</span></span>
<span data-ttu-id="26c44-118">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="26c44-118">Specify if confirmation is required.</span></span> <span data-ttu-id="26c44-119">Adja meg a megerősítési paraméter értékét $false a megerősítés kihagyása érdekében.</span><span class="sxs-lookup"><span data-stu-id="26c44-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="26c44-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26c44-120">-WhatIf</span></span>
<span data-ttu-id="26c44-121">Annak megjelenítése, hogy mi történik, ha a parancsmagot ténylegesen végrehajtják a parancsmag végrehajtása nélkül.</span><span class="sxs-lookup"><span data-stu-id="26c44-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="26c44-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26c44-122">CommonParameters</span></span>
<span data-ttu-id="26c44-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26c44-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26c44-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26c44-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26c44-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26c44-125">INPUTS</span></span>

### <span data-ttu-id="26c44-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="26c44-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="26c44-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26c44-127">OUTPUTS</span></span>

### <span data-ttu-id="26c44-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="26c44-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="26c44-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26c44-129">NOTES</span></span>

## <span data-ttu-id="26c44-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26c44-130">RELATED LINKS</span></span>

[<span data-ttu-id="26c44-131">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="26c44-131">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="26c44-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="26c44-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
