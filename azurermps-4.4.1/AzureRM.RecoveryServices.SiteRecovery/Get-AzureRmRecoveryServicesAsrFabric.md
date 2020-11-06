---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: dde3873c7fe7ee18ee4745af967eb222833029d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493391"
---
# <span data-ttu-id="7e838-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="7e838-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="7e838-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e838-102">SYNOPSIS</span></span>
<span data-ttu-id="7e838-103">Információkat kaphat az Azure webhely-helyreállítási anyagról.</span><span class="sxs-lookup"><span data-stu-id="7e838-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e838-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e838-104">SYNTAX</span></span>

### <span data-ttu-id="7e838-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e838-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [<CommonParameters>]
```

### <span data-ttu-id="7e838-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7e838-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="7e838-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7e838-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="7e838-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e838-108">DESCRIPTION</span></span>
<span data-ttu-id="7e838-109">A **Get-AzureRmRecoveryServicesAsrFabric** parancsmag egy megadott Azure-webhely helyreállítási szövetének vagy minden Azure webhely-helyreállítási szövetnek a tulajdonságait adja meg helyreállítási szolgáltatás-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="7e838-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="7e838-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7e838-110">EXAMPLES</span></span>

### <span data-ttu-id="7e838-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7e838-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="7e838-112">Az Azure-webhely helyreállítási szövetét számítja ki a boltozatban.</span><span class="sxs-lookup"><span data-stu-id="7e838-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

## <span data-ttu-id="7e838-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e838-113">PARAMETERS</span></span>

### <span data-ttu-id="7e838-114">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="7e838-114">-FriendlyName</span></span>
<span data-ttu-id="7e838-115">Az ASR-szövetet az anyag rövid nevével keresheti meg.</span><span class="sxs-lookup"><span data-stu-id="7e838-115">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e838-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7e838-116">-Name</span></span>
<span data-ttu-id="7e838-117">Az ASR-anyag keresése a szövet nevével</span><span class="sxs-lookup"><span data-stu-id="7e838-117">Search for the ASR fabric by the name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e838-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e838-118">CommonParameters</span></span>
<span data-ttu-id="7e838-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e838-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e838-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e838-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e838-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e838-121">INPUTS</span></span>

### <span data-ttu-id="7e838-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="7e838-122">None</span></span>

## <span data-ttu-id="7e838-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e838-123">OUTPUTS</span></span>

### <span data-ttu-id="7e838-124">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7e838-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7e838-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e838-125">NOTES</span></span>

## <span data-ttu-id="7e838-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e838-126">RELATED LINKS</span></span>

[<span data-ttu-id="7e838-127">Új – AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="7e838-127">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="7e838-128">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="7e838-128">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
