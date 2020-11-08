---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010611"
---
# <span data-ttu-id="7ea21-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="7ea21-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="7ea21-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ea21-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea21-103">A rendelkezésre álló (észlelt) ASR-tárolók besorolását a helyreállítási szolgáltatások pincéjében kapja.</span><span class="sxs-lookup"><span data-stu-id="7ea21-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="7ea21-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ea21-104">SYNTAX</span></span>

### <span data-ttu-id="7ea21-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ea21-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ea21-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="7ea21-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ea21-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7ea21-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ea21-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ea21-108">DESCRIPTION</span></span>
<span data-ttu-id="7ea21-109">A **Get-AzRecoveryServicesAsrStorageClassification** parancsmag részletesen ismerteti a helyreállítási szolgáltatások tárolójában felfedezett ASR-tárolási besorolásokat.</span><span class="sxs-lookup"><span data-stu-id="7ea21-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="7ea21-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7ea21-110">EXAMPLES</span></span>

### <span data-ttu-id="7ea21-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7ea21-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="7ea21-112">A megadott ASR-anyagnak megfelelő észlelt tárolási besorolások listája.</span><span class="sxs-lookup"><span data-stu-id="7ea21-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="7ea21-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ea21-113">PARAMETERS</span></span>

### <span data-ttu-id="7ea21-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea21-114">-DefaultProfile</span></span>
<span data-ttu-id="7ea21-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ea21-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7ea21-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="7ea21-116">-Fabric</span></span>
<span data-ttu-id="7ea21-117">Egy ASR-szövet objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7ea21-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="7ea21-118">A parancsmag a megadott ASR-anyaghoz tartozó, felfedezett tárolási kategóriák részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7ea21-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="7ea21-119">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="7ea21-119">-FriendlyName</span></span>
<span data-ttu-id="7ea21-120">A beolvasott tárterület-besorolási objektum rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ea21-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="7ea21-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ea21-121">-Name</span></span>
<span data-ttu-id="7ea21-122">A beolvasott tárterület-osztályozási objektum nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ea21-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="7ea21-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea21-123">CommonParameters</span></span>
<span data-ttu-id="7ea21-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ea21-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea21-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7ea21-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea21-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ea21-126">INPUTS</span></span>

### <span data-ttu-id="7ea21-127">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="7ea21-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="7ea21-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ea21-128">OUTPUTS</span></span>

### <span data-ttu-id="7ea21-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="7ea21-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="7ea21-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ea21-130">NOTES</span></span>

## <span data-ttu-id="7ea21-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ea21-131">RELATED LINKS</span></span>
