---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8dcab2bcaeafbc5304de72b8bcf539a6f4a53934
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012624"
---
# <span data-ttu-id="3b208-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3b208-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="3b208-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b208-102">SYNOPSIS</span></span>
<span data-ttu-id="3b208-103">Törli a megadott ASR-tárolási besorolási megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="3b208-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="3b208-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b208-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b208-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b208-105">DESCRIPTION</span></span>
<span data-ttu-id="3b208-106">A **Remove-AzRecoveryServicesAsrStorageClassificationMapping** parancsmag törli a megadott Azure-webhely helyreállítási tárterület-osztályozási megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="3b208-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="3b208-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3b208-107">EXAMPLES</span></span>

### <span data-ttu-id="3b208-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3b208-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="3b208-109">Elindítja a megadott tárolási besorolási megfeleltetések törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3b208-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3b208-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b208-110">PARAMETERS</span></span>

### <span data-ttu-id="3b208-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b208-111">-DefaultProfile</span></span>
<span data-ttu-id="3b208-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b208-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3b208-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b208-113">-InputObject</span></span>
<span data-ttu-id="3b208-114">A bemeneti objektum a parancsmag: az ASR-tárolók osztályozása objektum, amely megfelel az ASR tárterület-hozzárendelésének, amelyet törölni kell.</span><span class="sxs-lookup"><span data-stu-id="3b208-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="3b208-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b208-115">-Confirm</span></span>
<span data-ttu-id="3b208-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b208-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b208-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b208-117">-WhatIf</span></span>
<span data-ttu-id="3b208-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b208-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b208-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b208-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b208-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b208-120">CommonParameters</span></span>
<span data-ttu-id="3b208-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b208-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b208-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3b208-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b208-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b208-123">INPUTS</span></span>

### <span data-ttu-id="3b208-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3b208-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="3b208-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b208-125">OUTPUTS</span></span>

### <span data-ttu-id="3b208-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3b208-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3b208-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b208-127">NOTES</span></span>

## <span data-ttu-id="3b208-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b208-128">RELATED LINKS</span></span>

[<span data-ttu-id="3b208-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3b208-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="3b208-130">Új – AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3b208-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
