---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 441e3108053aa55c93ab0f9ee150bebd592a091e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935569"
---
# <span data-ttu-id="6761a-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="6761a-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="6761a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6761a-102">SYNOPSIS</span></span>
<span data-ttu-id="6761a-103">A helyreállítási szolgáltatások tárolóban elérhető(felfedezett) ASR-tárterületbesorolásokat kap.</span><span class="sxs-lookup"><span data-stu-id="6761a-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="6761a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6761a-104">SYNTAX</span></span>

### <span data-ttu-id="6761a-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6761a-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6761a-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="6761a-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6761a-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6761a-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6761a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6761a-108">DESCRIPTION</span></span>
<span data-ttu-id="6761a-109">A **Get-AzRecoveryServicesAsrStorageClassification** parancsmag lekérte a helyreállítási szolgáltatások tárolóban talált ASR-tárolóbesorolások részleteit.</span><span class="sxs-lookup"><span data-stu-id="6761a-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="6761a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6761a-110">EXAMPLES</span></span>

### <span data-ttu-id="6761a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6761a-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="6761a-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span><span class="sxs-lookup"><span data-stu-id="6761a-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="6761a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6761a-113">PARAMETERS</span></span>

### <span data-ttu-id="6761a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6761a-114">-DefaultProfile</span></span>
<span data-ttu-id="6761a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6761a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6761a-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="6761a-116">-Fabric</span></span>
<span data-ttu-id="6761a-117">ASR-anyagobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6761a-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="6761a-118">A parancsmag lekérte a megadott ASR-anyagnak megfelelő tárterületbesorolásokat.</span><span class="sxs-lookup"><span data-stu-id="6761a-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="6761a-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6761a-119">-FriendlyName</span></span>
<span data-ttu-id="6761a-120">A lekért tárbesorolási objektum rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6761a-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="6761a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6761a-121">-Name</span></span>
<span data-ttu-id="6761a-122">A lekért tárbesorolási objektum nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6761a-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="6761a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6761a-123">CommonParameters</span></span>
<span data-ttu-id="6761a-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6761a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6761a-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6761a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6761a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6761a-126">INPUTS</span></span>

### <span data-ttu-id="6761a-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6761a-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="6761a-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6761a-128">OUTPUTS</span></span>

### <span data-ttu-id="6761a-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="6761a-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="6761a-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6761a-130">NOTES</span></span>

## <span data-ttu-id="6761a-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6761a-131">RELATED LINKS</span></span>
