---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 22e49dc0ebb5c38a1b260f72cc4fe97294bf5505
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669746"
---
# <span data-ttu-id="46a43-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="46a43-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="46a43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46a43-102">SYNOPSIS</span></span>
<span data-ttu-id="46a43-103">Információkat kaphat az Azure webhely-helyreállítási anyagról.</span><span class="sxs-lookup"><span data-stu-id="46a43-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="46a43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46a43-104">SYNTAX</span></span>

### <span data-ttu-id="46a43-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="46a43-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46a43-106">ByName</span><span class="sxs-lookup"><span data-stu-id="46a43-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46a43-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="46a43-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46a43-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="46a43-108">DESCRIPTION</span></span>
<span data-ttu-id="46a43-109">A **Get-AzRecoveryServicesAsrFabric** parancsmag egy megadott Azure-webhely helyreállítási szövetének vagy minden Azure webhely-helyreállítási szövetnek a tulajdonságait adja meg helyreállítási szolgáltatás-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="46a43-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="46a43-110">Példák</span><span class="sxs-lookup"><span data-stu-id="46a43-110">EXAMPLES</span></span>

### <span data-ttu-id="46a43-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="46a43-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="46a43-112">Az Azure-webhely helyreállítási szövetét számítja ki a boltozatban.</span><span class="sxs-lookup"><span data-stu-id="46a43-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="46a43-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="46a43-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="46a43-114">Adja vissza az Azure-webhely helyreállítási szövetét az XXXX névvel.</span><span class="sxs-lookup"><span data-stu-id="46a43-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="46a43-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="46a43-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="46a43-116">Adja vissza az Azure-webhely helyreállítási szövetét a felhasználóbarát név XXXX értékkel.</span><span class="sxs-lookup"><span data-stu-id="46a43-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="46a43-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46a43-117">PARAMETERS</span></span>

### <span data-ttu-id="46a43-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a43-118">-DefaultProfile</span></span>
<span data-ttu-id="46a43-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46a43-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46a43-120">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="46a43-120">-FriendlyName</span></span>
<span data-ttu-id="46a43-121">Az ASR-szövetet az anyag rövid nevével keresheti meg.</span><span class="sxs-lookup"><span data-stu-id="46a43-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="46a43-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46a43-122">-Name</span></span>
<span data-ttu-id="46a43-123">Az ASR-anyag keresése a szövet nevével</span><span class="sxs-lookup"><span data-stu-id="46a43-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="46a43-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a43-124">CommonParameters</span></span>
<span data-ttu-id="46a43-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46a43-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a43-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46a43-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a43-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46a43-127">INPUTS</span></span>

### <span data-ttu-id="46a43-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="46a43-128">None</span></span>

## <span data-ttu-id="46a43-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46a43-129">OUTPUTS</span></span>

### <span data-ttu-id="46a43-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="46a43-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="46a43-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46a43-131">NOTES</span></span>

## <span data-ttu-id="46a43-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46a43-132">RELATED LINKS</span></span>

[<span data-ttu-id="46a43-133">Új – AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="46a43-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="46a43-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="46a43-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
