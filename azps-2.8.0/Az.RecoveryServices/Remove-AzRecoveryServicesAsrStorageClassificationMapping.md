---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c76c2ebf40f360820ec3eef719b33142daacdbac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839039"
---
# <span data-ttu-id="9ed7c-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="9ed7c-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="9ed7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ed7c-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed7c-103">Törli a megadott ASR-tárolási besorolási megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="9ed7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ed7c-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ed7c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ed7c-105">DESCRIPTION</span></span>
<span data-ttu-id="9ed7c-106">A **Remove-AzRecoveryServicesAsrStorageClassificationMapping** parancsmag törli a megadott Azure-webhely helyreállítási tárterület-osztályozási megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="9ed7c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9ed7c-107">EXAMPLES</span></span>

### <span data-ttu-id="9ed7c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9ed7c-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="9ed7c-109">Elindítja a megadott tárolási besorolási megfeleltetések törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9ed7c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ed7c-110">PARAMETERS</span></span>

### <span data-ttu-id="9ed7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed7c-111">-DefaultProfile</span></span>
<span data-ttu-id="9ed7c-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9ed7c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ed7c-113">-InputObject</span></span>
<span data-ttu-id="9ed7c-114">A bemeneti objektum a parancsmag: az ASR-tárolók osztályozása objektum, amely megfelel az ASR tárterület-hozzárendelésének, amelyet törölni kell.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="9ed7c-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9ed7c-115">-Confirm</span></span>
<span data-ttu-id="9ed7c-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ed7c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ed7c-117">-WhatIf</span></span>
<span data-ttu-id="9ed7c-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ed7c-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ed7c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ed7c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed7c-120">CommonParameters</span></span>
<span data-ttu-id="9ed7c-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ed7c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed7c-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ed7c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed7c-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ed7c-123">INPUTS</span></span>

### <span data-ttu-id="9ed7c-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="9ed7c-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="9ed7c-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ed7c-125">OUTPUTS</span></span>

### <span data-ttu-id="9ed7c-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9ed7c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9ed7c-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ed7c-127">NOTES</span></span>

## <span data-ttu-id="9ed7c-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ed7c-128">RELATED LINKS</span></span>

[<span data-ttu-id="9ed7c-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="9ed7c-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="9ed7c-130">Új – AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="9ed7c-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
