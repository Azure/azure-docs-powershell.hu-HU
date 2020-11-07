---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: e344dd4b5284a29c84b4f4c4b90d5a99f5d8d4ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669741"
---
# <span data-ttu-id="c576b-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="c576b-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="c576b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c576b-102">SYNOPSIS</span></span>
<span data-ttu-id="c576b-103">Információt kap a webhelyek helyreállítása által kezelt hálózatokról az aktuális boltozatra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="c576b-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="c576b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c576b-104">SYNTAX</span></span>

### <span data-ttu-id="c576b-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c576b-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c576b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c576b-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c576b-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c576b-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c576b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c576b-108">DESCRIPTION</span></span>
<span data-ttu-id="c576b-109">A **Get-AzRecoveryServicesAsrNetwork** parancsmag információkat kap az Azure webhely-helyreállítási hálózatról az Azure jelenlegi webhely-helyreállítási pincéjében.</span><span class="sxs-lookup"><span data-stu-id="c576b-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c576b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c576b-110">EXAMPLES</span></span>

### <span data-ttu-id="c576b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c576b-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="c576b-112">Az összes ismert hálózat beolvasása a megadott anyagból.</span><span class="sxs-lookup"><span data-stu-id="c576b-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="c576b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c576b-113">PARAMETERS</span></span>

### <span data-ttu-id="c576b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c576b-114">-DefaultProfile</span></span>
<span data-ttu-id="c576b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c576b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c576b-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="c576b-116">-Fabric</span></span>
<span data-ttu-id="c576b-117">ASR-szövet objektum</span><span class="sxs-lookup"><span data-stu-id="c576b-117">ASR fabric object</span></span>

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

### <span data-ttu-id="c576b-118">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="c576b-118">-FriendlyName</span></span>
<span data-ttu-id="c576b-119">A hálózati ASR-objektum rövid neve.</span><span class="sxs-lookup"><span data-stu-id="c576b-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="c576b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c576b-120">-Name</span></span>
<span data-ttu-id="c576b-121">Hálózati ASR-objektum neve.</span><span class="sxs-lookup"><span data-stu-id="c576b-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="c576b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c576b-122">CommonParameters</span></span>
<span data-ttu-id="c576b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c576b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c576b-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c576b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c576b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c576b-125">INPUTS</span></span>

### <span data-ttu-id="c576b-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c576b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c576b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c576b-127">OUTPUTS</span></span>

### <span data-ttu-id="c576b-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="c576b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="c576b-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c576b-129">NOTES</span></span>

## <span data-ttu-id="c576b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c576b-130">RELATED LINKS</span></span>
