---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 091f8892238d88554d0e0c3502ffbeb8e8d4c154
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187687"
---
# <span data-ttu-id="6fe65-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="6fe65-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="6fe65-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6fe65-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe65-103">Az ASR-tárolók osztályozási megfeleltetését hozza létre a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="6fe65-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="6fe65-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6fe65-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fe65-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6fe65-105">DESCRIPTION</span></span>
<span data-ttu-id="6fe65-106">A **New-AzRecoveryServicesAsrStorageClassificationMapping** parancsmag létrehoz egy tárterület-osztályozási társítást a helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="6fe65-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="6fe65-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6fe65-107">EXAMPLES</span></span>

### <span data-ttu-id="6fe65-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6fe65-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="6fe65-109">A megadott paraméterekkel elindítja a tárolási osztályozási hozzárendelés-készítési műveletet, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="6fe65-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6fe65-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6fe65-110">PARAMETERS</span></span>

### <span data-ttu-id="6fe65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe65-111">-DefaultProfile</span></span>
<span data-ttu-id="6fe65-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6fe65-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6fe65-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6fe65-113">-Name</span></span>
<span data-ttu-id="6fe65-114">Az ASR-tárolók besorolási megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fe65-114">Specifies a name for the ASR storage classification mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe65-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="6fe65-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="6fe65-116">A megfeleltetés elsődleges ASR-tárterület-osztályozási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fe65-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe65-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="6fe65-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="6fe65-118">Megadja a megfeleltetés helyreállítási ASR-tárolási osztályozási objektumát.</span><span class="sxs-lookup"><span data-stu-id="6fe65-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe65-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6fe65-119">-Confirm</span></span>
<span data-ttu-id="6fe65-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6fe65-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fe65-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fe65-121">-WhatIf</span></span>
<span data-ttu-id="6fe65-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6fe65-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fe65-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6fe65-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fe65-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe65-124">CommonParameters</span></span>
<span data-ttu-id="6fe65-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6fe65-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe65-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6fe65-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe65-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fe65-127">INPUTS</span></span>

### <span data-ttu-id="6fe65-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="6fe65-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="6fe65-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fe65-129">OUTPUTS</span></span>

### <span data-ttu-id="6fe65-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6fe65-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6fe65-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6fe65-131">NOTES</span></span>

## <span data-ttu-id="6fe65-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fe65-132">RELATED LINKS</span></span>

[<span data-ttu-id="6fe65-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="6fe65-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="6fe65-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="6fe65-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)