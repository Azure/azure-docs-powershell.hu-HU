---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 53a877543cc3811ccf52d240025135fefa3ede0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495316"
---
# <span data-ttu-id="9140c-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="9140c-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="9140c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9140c-102">SYNOPSIS</span></span>
<span data-ttu-id="9140c-103">Az ASR-tárolók osztályozási megfeleltetésének beolvasása</span><span class="sxs-lookup"><span data-stu-id="9140c-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9140c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9140c-104">SYNTAX</span></span>

### <span data-ttu-id="9140c-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9140c-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9140c-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="9140c-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9140c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9140c-107">DESCRIPTION</span></span>
<span data-ttu-id="9140c-108">A **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** PARANCSMAG az ASR-tárolók besorolási megfeleltetésének részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9140c-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="9140c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9140c-109">EXAMPLES</span></span>

### <span data-ttu-id="9140c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9140c-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="9140c-111">A megadott tárterület-besorolásnak megfelelő tárolási besorolási megfeleltetések felsorolása.</span><span class="sxs-lookup"><span data-stu-id="9140c-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="9140c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9140c-112">PARAMETERS</span></span>

### <span data-ttu-id="9140c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9140c-113">-DefaultProfile</span></span>
<span data-ttu-id="9140c-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9140c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="9140c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9140c-115">-Name</span></span>
<span data-ttu-id="9140c-116">A beszerzéshez a tárterület-osztályozási megfeleltetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9140c-116">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9140c-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="9140c-117">-StorageClassification</span></span>
<span data-ttu-id="9140c-118">Az ASR-tárolók osztályozási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9140c-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="9140c-119">A parancsmag beolvassa az ASR-tárolók osztályozását, amely megfelel a megadott tárterület-besorolásnak</span><span class="sxs-lookup"><span data-stu-id="9140c-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9140c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9140c-120">CommonParameters</span></span>
<span data-ttu-id="9140c-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9140c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9140c-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9140c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9140c-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9140c-123">INPUTS</span></span>

### <span data-ttu-id="9140c-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="9140c-124">None</span></span>

## <span data-ttu-id="9140c-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9140c-125">OUTPUTS</span></span>

### <span data-ttu-id="9140c-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9140c-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9140c-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9140c-127">NOTES</span></span>

## <span data-ttu-id="9140c-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9140c-128">RELATED LINKS</span></span>

[<span data-ttu-id="9140c-129">Új – AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="9140c-129">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="9140c-130">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="9140c-130">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
