---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: bafa671431c617807fa28e2d4fbfed57236fc6a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495755"
---
# <span data-ttu-id="8f5ae-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8f5ae-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="8f5ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f5ae-102">SYNOPSIS</span></span>
<span data-ttu-id="8f5ae-103">Törli a megadott ASR-tárolási besorolási megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="8f5ae-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f5ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f5ae-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f5ae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f5ae-105">DESCRIPTION</span></span>
<span data-ttu-id="8f5ae-106">A **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** parancsmag törli a megadott Azure-webhely helyreállítási tárterület-osztályozási megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="8f5ae-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="8f5ae-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8f5ae-107">EXAMPLES</span></span>

### <span data-ttu-id="8f5ae-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8f5ae-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="8f5ae-109">Elindítja a megadott tárolási besorolási megfeleltetések törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8f5ae-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8f5ae-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f5ae-110">PARAMETERS</span></span>

### <span data-ttu-id="8f5ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f5ae-111">-DefaultProfile</span></span>
<span data-ttu-id="8f5ae-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f5ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8f5ae-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f5ae-113">-InputObject</span></span>
<span data-ttu-id="8f5ae-114">A bemeneti objektum a parancsmag: az ASR-tárolók osztályozása objektum, amely megfelel az ASR tárterület-hozzárendelésének, amelyet törölni kell.</span><span class="sxs-lookup"><span data-stu-id="8f5ae-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f5ae-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8f5ae-115">-Confirm</span></span>
<span data-ttu-id="8f5ae-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f5ae-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f5ae-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f5ae-117">-WhatIf</span></span>
<span data-ttu-id="8f5ae-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8f5ae-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f5ae-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f5ae-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f5ae-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f5ae-120">CommonParameters</span></span>
<span data-ttu-id="8f5ae-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f5ae-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f5ae-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f5ae-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f5ae-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f5ae-123">INPUTS</span></span>

### <span data-ttu-id="8f5ae-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8f5ae-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="8f5ae-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f5ae-125">OUTPUTS</span></span>

### <span data-ttu-id="8f5ae-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8f5ae-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8f5ae-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f5ae-127">NOTES</span></span>

## <span data-ttu-id="8f5ae-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f5ae-128">RELATED LINKS</span></span>

[<span data-ttu-id="8f5ae-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8f5ae-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="8f5ae-130">Új – AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8f5ae-130">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
