---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 6ab8102de0deb27c18c6e50f8d78db2f23a5155a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672459"
---
# <span data-ttu-id="af217-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="af217-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="af217-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af217-102">SYNOPSIS</span></span>
<span data-ttu-id="af217-103">Az ASR-tárolók osztályozási megfeleltetését hozza létre a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="af217-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af217-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af217-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af217-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af217-105">DESCRIPTION</span></span>
<span data-ttu-id="af217-106">A **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** parancsmag létrehoz egy tárterület-osztályozási társítást a helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="af217-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="af217-107">Példák</span><span class="sxs-lookup"><span data-stu-id="af217-107">EXAMPLES</span></span>

### <span data-ttu-id="af217-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="af217-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="af217-109">A megadott paraméterekkel elindítja a tárolási osztályozási hozzárendelés-készítési műveletet, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="af217-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="af217-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af217-110">PARAMETERS</span></span>

### <span data-ttu-id="af217-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af217-111">-DefaultProfile</span></span>
<span data-ttu-id="af217-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af217-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="af217-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af217-113">-Name</span></span>
<span data-ttu-id="af217-114">Az ASR-tárolók besorolási megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af217-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="af217-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="af217-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="af217-116">A megfeleltetés elsődleges ASR-tárterület-osztályozási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="af217-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="af217-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="af217-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="af217-118">Megadja a megfeleltetés helyreállítási ASR-tárolási osztályozási objektumát.</span><span class="sxs-lookup"><span data-stu-id="af217-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="af217-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af217-119">-Confirm</span></span>
<span data-ttu-id="af217-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af217-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af217-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af217-121">-WhatIf</span></span>
<span data-ttu-id="af217-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af217-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af217-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af217-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af217-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af217-124">CommonParameters</span></span>
<span data-ttu-id="af217-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af217-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af217-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af217-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af217-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af217-127">INPUTS</span></span>

### <span data-ttu-id="af217-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="af217-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="af217-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af217-129">OUTPUTS</span></span>

### <span data-ttu-id="af217-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="af217-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="af217-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af217-131">NOTES</span></span>

## <span data-ttu-id="af217-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af217-132">RELATED LINKS</span></span>

[<span data-ttu-id="af217-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="af217-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="af217-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="af217-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
