---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: a341e634c9c426843b5eb217c2f13102abc30ae4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669718"
---
# <span data-ttu-id="7ecb2-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="7ecb2-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="7ecb2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ecb2-102">SYNOPSIS</span></span>
<span data-ttu-id="7ecb2-103">Az ASR-tárolók osztályozási megfeleltetésének beolvasása</span><span class="sxs-lookup"><span data-stu-id="7ecb2-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="7ecb2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ecb2-104">SYNTAX</span></span>

### <span data-ttu-id="7ecb2-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ecb2-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ecb2-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="7ecb2-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ecb2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ecb2-107">DESCRIPTION</span></span>
<span data-ttu-id="7ecb2-108">A **Get-AzRecoveryServicesAsrStorageClassificationMapping** PARANCSMAG az ASR-tárolók besorolási megfeleltetésének részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7ecb2-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="7ecb2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7ecb2-109">EXAMPLES</span></span>

### <span data-ttu-id="7ecb2-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7ecb2-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="7ecb2-111">A megadott tárterület-besorolásnak megfelelő tárolási besorolási megfeleltetések felsorolása.</span><span class="sxs-lookup"><span data-stu-id="7ecb2-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="7ecb2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ecb2-112">PARAMETERS</span></span>

### <span data-ttu-id="7ecb2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ecb2-113">-DefaultProfile</span></span>
<span data-ttu-id="7ecb2-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ecb2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7ecb2-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ecb2-115">-Name</span></span>
<span data-ttu-id="7ecb2-116">A beszerzéshez a tárterület-osztályozási megfeleltetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ecb2-116">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb2-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="7ecb2-117">-StorageClassification</span></span>
<span data-ttu-id="7ecb2-118">Az ASR-tárolók osztályozási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ecb2-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="7ecb2-119">A parancsmag beolvassa az ASR-tárolók osztályozását, amely megfelel a megadott tárterület-besorolásnak</span><span class="sxs-lookup"><span data-stu-id="7ecb2-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="7ecb2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ecb2-120">CommonParameters</span></span>
<span data-ttu-id="7ecb2-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ecb2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ecb2-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ecb2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ecb2-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ecb2-123">INPUTS</span></span>

### <span data-ttu-id="7ecb2-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="7ecb2-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="7ecb2-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ecb2-125">OUTPUTS</span></span>

### <span data-ttu-id="7ecb2-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="7ecb2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="7ecb2-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ecb2-127">NOTES</span></span>

## <span data-ttu-id="7ecb2-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ecb2-128">RELATED LINKS</span></span>

[<span data-ttu-id="7ecb2-129">Új – AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="7ecb2-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="7ecb2-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="7ecb2-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
