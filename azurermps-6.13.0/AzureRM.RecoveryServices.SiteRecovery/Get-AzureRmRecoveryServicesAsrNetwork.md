---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 4eac63104f9e75643119c371d2a4d0e882945966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495759"
---
# <span data-ttu-id="9c2ff-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="9c2ff-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="9c2ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c2ff-102">SYNOPSIS</span></span>
<span data-ttu-id="9c2ff-103">Információt kap a webhelyek helyreállítása által kezelt hálózatokról az aktuális boltozatra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="9c2ff-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c2ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c2ff-104">SYNTAX</span></span>

### <span data-ttu-id="9c2ff-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c2ff-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c2ff-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9c2ff-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c2ff-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9c2ff-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c2ff-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c2ff-108">DESCRIPTION</span></span>
<span data-ttu-id="9c2ff-109">A **Get-AzureRmRecoveryServicesAsrNetwork** parancsmag információkat kap az Azure webhely-helyreállítási hálózatról az Azure jelenlegi webhely-helyreállítási pincéjében.</span><span class="sxs-lookup"><span data-stu-id="9c2ff-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="9c2ff-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9c2ff-110">EXAMPLES</span></span>

### <span data-ttu-id="9c2ff-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9c2ff-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="9c2ff-112">Az összes ismert hálózat beolvasása a megadott anyagból.</span><span class="sxs-lookup"><span data-stu-id="9c2ff-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="9c2ff-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c2ff-113">PARAMETERS</span></span>

### <span data-ttu-id="9c2ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c2ff-114">-DefaultProfile</span></span>
<span data-ttu-id="9c2ff-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c2ff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9c2ff-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="9c2ff-116">-Fabric</span></span>
<span data-ttu-id="9c2ff-117">ASR-szövet objektum</span><span class="sxs-lookup"><span data-stu-id="9c2ff-117">ASR fabric object</span></span>

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

### <span data-ttu-id="9c2ff-118">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="9c2ff-118">-FriendlyName</span></span>
<span data-ttu-id="9c2ff-119">A hálózati ASR-objektum rövid neve.</span><span class="sxs-lookup"><span data-stu-id="9c2ff-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="9c2ff-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9c2ff-120">-Name</span></span>
<span data-ttu-id="9c2ff-121">Hálózati ASR-objektum neve.</span><span class="sxs-lookup"><span data-stu-id="9c2ff-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="9c2ff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c2ff-122">CommonParameters</span></span>
<span data-ttu-id="9c2ff-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c2ff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c2ff-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c2ff-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c2ff-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c2ff-125">INPUTS</span></span>

### <span data-ttu-id="9c2ff-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="9c2ff-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="9c2ff-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c2ff-127">OUTPUTS</span></span>

### <span data-ttu-id="9c2ff-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRNetwork, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9c2ff-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9c2ff-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c2ff-129">NOTES</span></span>

## <span data-ttu-id="9c2ff-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c2ff-130">RELATED LINKS</span></span>
