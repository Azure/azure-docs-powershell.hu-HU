---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195554"
---
# <span data-ttu-id="696cc-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="696cc-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="696cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="696cc-102">SYNOPSIS</span></span>
<span data-ttu-id="696cc-103">Információt kap a webhelyek helyreállítása által kezelt hálózatokról az aktuális boltozatra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="696cc-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="696cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="696cc-104">SYNTAX</span></span>

### <span data-ttu-id="696cc-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="696cc-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="696cc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="696cc-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="696cc-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="696cc-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="696cc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="696cc-108">DESCRIPTION</span></span>
<span data-ttu-id="696cc-109">A **Get-AzRecoveryServicesAsrNetwork** parancsmag információkat kap az Azure webhely-helyreállítási hálózatról az Azure jelenlegi webhely-helyreállítási pincéjében.</span><span class="sxs-lookup"><span data-stu-id="696cc-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="696cc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="696cc-110">EXAMPLES</span></span>

### <span data-ttu-id="696cc-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="696cc-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="696cc-112">Az összes ismert hálózat beolvasása a megadott anyagból.</span><span class="sxs-lookup"><span data-stu-id="696cc-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="696cc-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="696cc-113">PARAMETERS</span></span>

### <span data-ttu-id="696cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696cc-114">-DefaultProfile</span></span>
<span data-ttu-id="696cc-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="696cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="696cc-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="696cc-116">-Fabric</span></span>
<span data-ttu-id="696cc-117">ASR-szövet objektum</span><span class="sxs-lookup"><span data-stu-id="696cc-117">ASR fabric object</span></span>

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

### <span data-ttu-id="696cc-118">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="696cc-118">-FriendlyName</span></span>
<span data-ttu-id="696cc-119">A hálózati ASR-objektum rövid neve.</span><span class="sxs-lookup"><span data-stu-id="696cc-119">Friendly name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696cc-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="696cc-120">-Name</span></span>
<span data-ttu-id="696cc-121">Hálózati ASR-objektum neve.</span><span class="sxs-lookup"><span data-stu-id="696cc-121">Name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696cc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696cc-122">CommonParameters</span></span>
<span data-ttu-id="696cc-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="696cc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696cc-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="696cc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696cc-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="696cc-125">INPUTS</span></span>

### <span data-ttu-id="696cc-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="696cc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="696cc-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="696cc-127">OUTPUTS</span></span>

### <span data-ttu-id="696cc-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="696cc-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="696cc-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="696cc-129">NOTES</span></span>

## <span data-ttu-id="696cc-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="696cc-130">RELATED LINKS</span></span>
