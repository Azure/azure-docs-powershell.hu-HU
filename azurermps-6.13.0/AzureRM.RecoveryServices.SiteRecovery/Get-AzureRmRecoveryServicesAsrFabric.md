---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: db93d022d2abd6d3c6cecfe32b1f82be4483e850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499439"
---
# <span data-ttu-id="7f98b-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="7f98b-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="7f98b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f98b-102">SYNOPSIS</span></span>
<span data-ttu-id="7f98b-103">Információkat kaphat az Azure webhely-helyreállítási anyagról.</span><span class="sxs-lookup"><span data-stu-id="7f98b-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f98b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f98b-104">SYNTAX</span></span>

### <span data-ttu-id="7f98b-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f98b-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f98b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7f98b-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f98b-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7f98b-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f98b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f98b-108">DESCRIPTION</span></span>
<span data-ttu-id="7f98b-109">A **Get-AzureRmRecoveryServicesAsrFabric** parancsmag egy megadott Azure-webhely helyreállítási szövetének vagy minden Azure webhely-helyreállítási szövetnek a tulajdonságait adja meg helyreállítási szolgáltatás-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="7f98b-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="7f98b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7f98b-110">EXAMPLES</span></span>

### <span data-ttu-id="7f98b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7f98b-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="7f98b-112">Az Azure-webhely helyreállítási szövetét számítja ki a boltozatban.</span><span class="sxs-lookup"><span data-stu-id="7f98b-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="7f98b-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7f98b-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="7f98b-114">Adja vissza az Azure-webhely helyreállítási szövetét az XXXX névvel.</span><span class="sxs-lookup"><span data-stu-id="7f98b-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="7f98b-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="7f98b-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="7f98b-116">Adja vissza az Azure-webhely helyreállítási szövetét a felhasználóbarát név XXXX értékkel.</span><span class="sxs-lookup"><span data-stu-id="7f98b-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="7f98b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f98b-117">PARAMETERS</span></span>

### <span data-ttu-id="7f98b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f98b-118">-DefaultProfile</span></span>
<span data-ttu-id="7f98b-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f98b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f98b-120">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="7f98b-120">-FriendlyName</span></span>
<span data-ttu-id="7f98b-121">Az ASR-szövetet az anyag rövid nevével keresheti meg.</span><span class="sxs-lookup"><span data-stu-id="7f98b-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="7f98b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7f98b-122">-Name</span></span>
<span data-ttu-id="7f98b-123">Az ASR-anyag keresése a szövet nevével</span><span class="sxs-lookup"><span data-stu-id="7f98b-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="7f98b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f98b-124">CommonParameters</span></span>
<span data-ttu-id="7f98b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f98b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f98b-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f98b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f98b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f98b-127">INPUTS</span></span>

### <span data-ttu-id="7f98b-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="7f98b-128">None</span></span>

## <span data-ttu-id="7f98b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f98b-129">OUTPUTS</span></span>

### <span data-ttu-id="7f98b-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7f98b-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7f98b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f98b-131">NOTES</span></span>

## <span data-ttu-id="7f98b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f98b-132">RELATED LINKS</span></span>

[<span data-ttu-id="7f98b-133">Új – AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="7f98b-133">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="7f98b-134">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="7f98b-134">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
