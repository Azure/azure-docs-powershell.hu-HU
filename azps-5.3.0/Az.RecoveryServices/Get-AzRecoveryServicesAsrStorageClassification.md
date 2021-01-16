---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476730"
---
# <span data-ttu-id="6b029-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="6b029-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="6b029-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b029-102">SYNOPSIS</span></span>
<span data-ttu-id="6b029-103">A helyreállítási szolgáltatások tárolóban elérhető(felfedezett) ASR-tárterületbesorolásokat kap.</span><span class="sxs-lookup"><span data-stu-id="6b029-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="6b029-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b029-104">SYNTAX</span></span>

### <span data-ttu-id="6b029-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b029-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b029-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="6b029-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b029-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b029-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b029-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b029-108">DESCRIPTION</span></span>
<span data-ttu-id="6b029-109">A **Get-AzRecoveryServicesAsrStorageClassification** parancsmag lekérte a helyreállítási szolgáltatások tárolóban talált ASR-tárolóbesorolások részleteit.</span><span class="sxs-lookup"><span data-stu-id="6b029-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="6b029-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b029-110">EXAMPLES</span></span>

### <span data-ttu-id="6b029-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6b029-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="6b029-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span><span class="sxs-lookup"><span data-stu-id="6b029-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="6b029-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b029-113">PARAMETERS</span></span>

### <span data-ttu-id="6b029-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b029-114">-DefaultProfile</span></span>
<span data-ttu-id="6b029-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b029-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6b029-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="6b029-116">-Fabric</span></span>
<span data-ttu-id="6b029-117">ASR-anyagobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6b029-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="6b029-118">A parancsmag lekérte a megadott ASR-anyagnak megfelelő tárterületbesorolásokat.</span><span class="sxs-lookup"><span data-stu-id="6b029-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="6b029-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b029-119">-FriendlyName</span></span>
<span data-ttu-id="6b029-120">A lekért tárbesorolási objektum rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b029-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="6b029-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6b029-121">-Name</span></span>
<span data-ttu-id="6b029-122">A lekért tárbesorolási objektum nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b029-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="6b029-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b029-123">CommonParameters</span></span>
<span data-ttu-id="6b029-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b029-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b029-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b029-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b029-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b029-126">INPUTS</span></span>

### <span data-ttu-id="6b029-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6b029-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="6b029-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b029-128">OUTPUTS</span></span>

### <span data-ttu-id="6b029-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="6b029-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="6b029-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b029-130">NOTES</span></span>

## <span data-ttu-id="6b029-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b029-131">RELATED LINKS</span></span>
