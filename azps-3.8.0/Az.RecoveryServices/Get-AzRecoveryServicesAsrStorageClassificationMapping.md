---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010605"
---
# <span data-ttu-id="34a3e-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="34a3e-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="34a3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="34a3e-103">Az ASR-tárolók osztályozási megfeleltetésének beolvasása</span><span class="sxs-lookup"><span data-stu-id="34a3e-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="34a3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34a3e-104">SYNTAX</span></span>

### <span data-ttu-id="34a3e-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="34a3e-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34a3e-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="34a3e-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34a3e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="34a3e-107">DESCRIPTION</span></span>
<span data-ttu-id="34a3e-108">A **Get-AzRecoveryServicesAsrStorageClassificationMapping** PARANCSMAG az ASR-tárolók besorolási megfeleltetésének részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="34a3e-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="34a3e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="34a3e-109">EXAMPLES</span></span>

### <span data-ttu-id="34a3e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="34a3e-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="34a3e-111">A megadott tárterület-besorolásnak megfelelő tárolási besorolási megfeleltetések felsorolása.</span><span class="sxs-lookup"><span data-stu-id="34a3e-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="34a3e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34a3e-112">PARAMETERS</span></span>

### <span data-ttu-id="34a3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a3e-113">-DefaultProfile</span></span>
<span data-ttu-id="34a3e-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="34a3e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="34a3e-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="34a3e-115">-Name</span></span>
<span data-ttu-id="34a3e-116">A beszerzéshez a tárterület-osztályozási megfeleltetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="34a3e-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="34a3e-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="34a3e-117">-StorageClassification</span></span>
<span data-ttu-id="34a3e-118">Az ASR-tárolók osztályozási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="34a3e-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="34a3e-119">A parancsmag beolvassa az ASR-tárolók osztályozását, amely megfelel a megadott tárterület-besorolásnak</span><span class="sxs-lookup"><span data-stu-id="34a3e-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="34a3e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a3e-120">CommonParameters</span></span>
<span data-ttu-id="34a3e-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="34a3e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a3e-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="34a3e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a3e-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34a3e-123">INPUTS</span></span>

### <span data-ttu-id="34a3e-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="34a3e-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="34a3e-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34a3e-125">OUTPUTS</span></span>

### <span data-ttu-id="34a3e-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="34a3e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="34a3e-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34a3e-127">NOTES</span></span>

## <span data-ttu-id="34a3e-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34a3e-128">RELATED LINKS</span></span>

[<span data-ttu-id="34a3e-129">Új – AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="34a3e-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="34a3e-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="34a3e-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
