---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: c3bd5ecf7e3561be5f9e6b8d990c40281135982c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846977"
---
# <span data-ttu-id="850c9-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="850c9-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="850c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="850c9-102">SYNOPSIS</span></span>
<span data-ttu-id="850c9-103">Információkat kaphat az Azure webhely-helyreállítási anyagról.</span><span class="sxs-lookup"><span data-stu-id="850c9-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="850c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="850c9-104">SYNTAX</span></span>

### <span data-ttu-id="850c9-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="850c9-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="850c9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="850c9-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="850c9-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="850c9-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="850c9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="850c9-108">DESCRIPTION</span></span>
<span data-ttu-id="850c9-109">A **Get-AzRecoveryServicesAsrFabric** parancsmag egy megadott Azure-webhely helyreállítási szövetének vagy minden Azure webhely-helyreállítási szövetnek a tulajdonságait adja meg helyreállítási szolgáltatás-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="850c9-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="850c9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="850c9-110">EXAMPLES</span></span>

### <span data-ttu-id="850c9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="850c9-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="850c9-112">Az Azure-webhely helyreállítási szövetét számítja ki a boltozatban.</span><span class="sxs-lookup"><span data-stu-id="850c9-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="850c9-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="850c9-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="850c9-114">Adja vissza az Azure-webhely helyreállítási szövetét az XXXX névvel.</span><span class="sxs-lookup"><span data-stu-id="850c9-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="850c9-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="850c9-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="850c9-116">Adja vissza az Azure-webhely helyreállítási szövetét a felhasználóbarát név XXXX értékkel.</span><span class="sxs-lookup"><span data-stu-id="850c9-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="850c9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="850c9-117">PARAMETERS</span></span>

### <span data-ttu-id="850c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="850c9-118">-DefaultProfile</span></span>
<span data-ttu-id="850c9-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="850c9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="850c9-120">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="850c9-120">-FriendlyName</span></span>
<span data-ttu-id="850c9-121">Az ASR-szövetet az anyag rövid nevével keresheti meg.</span><span class="sxs-lookup"><span data-stu-id="850c9-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="850c9-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="850c9-122">-Name</span></span>
<span data-ttu-id="850c9-123">Az ASR-anyag keresése a szövet nevével</span><span class="sxs-lookup"><span data-stu-id="850c9-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="850c9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="850c9-124">CommonParameters</span></span>
<span data-ttu-id="850c9-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="850c9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="850c9-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="850c9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="850c9-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="850c9-127">INPUTS</span></span>

### <span data-ttu-id="850c9-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="850c9-128">None</span></span>

## <span data-ttu-id="850c9-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="850c9-129">OUTPUTS</span></span>

### <span data-ttu-id="850c9-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="850c9-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="850c9-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="850c9-131">NOTES</span></span>

## <span data-ttu-id="850c9-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="850c9-132">RELATED LINKS</span></span>

[<span data-ttu-id="850c9-133">Új – AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="850c9-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="850c9-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="850c9-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
