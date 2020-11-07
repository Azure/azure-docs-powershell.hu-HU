---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 9f0021658784c767e35d903a0a191ba28932f57a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838602"
---
# <span data-ttu-id="6ff32-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="6ff32-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="6ff32-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ff32-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff32-103">A rendelkezésre álló (észlelt) ASR-tárolók besorolását a helyreállítási szolgáltatások pincéjében kapja.</span><span class="sxs-lookup"><span data-stu-id="6ff32-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="6ff32-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ff32-104">SYNTAX</span></span>

### <span data-ttu-id="6ff32-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ff32-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ff32-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="6ff32-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ff32-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6ff32-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ff32-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ff32-108">DESCRIPTION</span></span>
<span data-ttu-id="6ff32-109">A **Get-AzRecoveryServicesAsrStorageClassification** parancsmag részletesen ismerteti a helyreállítási szolgáltatások tárolójában felfedezett ASR-tárolási besorolásokat.</span><span class="sxs-lookup"><span data-stu-id="6ff32-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="6ff32-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6ff32-110">EXAMPLES</span></span>

### <span data-ttu-id="6ff32-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6ff32-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="6ff32-112">A megadott ASR-anyagnak megfelelő észlelt tárolási besorolások listája.</span><span class="sxs-lookup"><span data-stu-id="6ff32-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="6ff32-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ff32-113">PARAMETERS</span></span>

### <span data-ttu-id="6ff32-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff32-114">-DefaultProfile</span></span>
<span data-ttu-id="6ff32-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ff32-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6ff32-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="6ff32-116">-Fabric</span></span>
<span data-ttu-id="6ff32-117">Egy ASR-szövet objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6ff32-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="6ff32-118">A parancsmag a megadott ASR-anyaghoz tartozó, felfedezett tárolási kategóriák részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6ff32-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="6ff32-119">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="6ff32-119">-FriendlyName</span></span>
<span data-ttu-id="6ff32-120">A beolvasott tárterület-besorolási objektum rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ff32-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="6ff32-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6ff32-121">-Name</span></span>
<span data-ttu-id="6ff32-122">A beolvasott tárterület-osztályozási objektum nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6ff32-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="6ff32-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff32-123">CommonParameters</span></span>
<span data-ttu-id="6ff32-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ff32-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff32-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ff32-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff32-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ff32-126">INPUTS</span></span>

### <span data-ttu-id="6ff32-127">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6ff32-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="6ff32-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ff32-128">OUTPUTS</span></span>

### <span data-ttu-id="6ff32-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="6ff32-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="6ff32-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ff32-130">NOTES</span></span>

## <span data-ttu-id="6ff32-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ff32-131">RELATED LINKS</span></span>
