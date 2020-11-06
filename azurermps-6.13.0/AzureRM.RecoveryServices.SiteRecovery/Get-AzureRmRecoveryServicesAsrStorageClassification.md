---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: dc6e0cba8103884fc36413c0a2980892411852ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492796"
---
# <span data-ttu-id="4f852-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="4f852-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="4f852-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f852-102">SYNOPSIS</span></span>
<span data-ttu-id="4f852-103">A rendelkezésre álló (észlelt) ASR-tárolók besorolását a helyreállítási szolgáltatások pincéjében kapja.</span><span class="sxs-lookup"><span data-stu-id="4f852-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f852-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f852-104">SYNTAX</span></span>

### <span data-ttu-id="4f852-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4f852-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f852-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4f852-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f852-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4f852-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f852-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f852-108">DESCRIPTION</span></span>
<span data-ttu-id="4f852-109">A **Get-AzureRmRecoveryServicesAsrStorageClassification** parancsmag részletesen ismerteti a helyreállítási szolgáltatások tárolójában felfedezett ASR-tárolási besorolásokat.</span><span class="sxs-lookup"><span data-stu-id="4f852-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="4f852-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4f852-110">EXAMPLES</span></span>

### <span data-ttu-id="4f852-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4f852-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="4f852-112">A megadott ASR-anyagnak megfelelő észlelt tárolási besorolások listája.</span><span class="sxs-lookup"><span data-stu-id="4f852-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="4f852-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f852-113">PARAMETERS</span></span>

### <span data-ttu-id="4f852-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f852-114">-DefaultProfile</span></span>
<span data-ttu-id="4f852-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4f852-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4f852-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="4f852-116">-Fabric</span></span>
<span data-ttu-id="4f852-117">Egy ASR-szövet objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4f852-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="4f852-118">A parancsmag a megadott ASR-anyaghoz tartozó, felfedezett tárolási kategóriák részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4f852-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f852-119">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="4f852-119">-FriendlyName</span></span>
<span data-ttu-id="4f852-120">A beolvasott tárterület-besorolási objektum rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f852-120">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f852-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4f852-121">-Name</span></span>
<span data-ttu-id="4f852-122">A beolvasott tárterület-osztályozási objektum nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f852-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="4f852-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f852-123">CommonParameters</span></span>
<span data-ttu-id="4f852-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f852-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f852-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f852-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f852-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f852-126">INPUTS</span></span>

### <span data-ttu-id="4f852-127">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4f852-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="4f852-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f852-128">OUTPUTS</span></span>

### <span data-ttu-id="4f852-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRStorageClassification, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4f852-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4f852-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f852-130">NOTES</span></span>

## <span data-ttu-id="4f852-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f852-131">RELATED LINKS</span></span>
