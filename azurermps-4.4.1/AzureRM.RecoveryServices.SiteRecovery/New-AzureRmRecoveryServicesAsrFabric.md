---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 28c038a6dfd29f9daaeb942afa8fcb4c479cd0aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680236"
---
# <span data-ttu-id="f9209-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="f9209-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="f9209-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9209-102">SYNOPSIS</span></span>
<span data-ttu-id="f9209-103">Azure-webhely-helyreállítási szövetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f9209-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9209-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9209-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9209-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9209-105">DESCRIPTION</span></span>
<span data-ttu-id="f9209-106">A **New-AzureRmRecoveryServicesAsrFabric** parancsmag a megadott típusú Azure webhely-helyreállítási szerkezetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f9209-106">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="f9209-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f9209-107">EXAMPLES</span></span>

### <span data-ttu-id="f9209-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f9209-108">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="f9209-109">Az átadott névvel elindítja a szerkezet-készítést, és visszaadja a kelme-létrehozási művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="f9209-109">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="f9209-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9209-110">PARAMETERS</span></span>

### <span data-ttu-id="f9209-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f9209-111">-Name</span></span>
<span data-ttu-id="f9209-112">Az Azure webhely-helyreállítási anyag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9209-112">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9209-113">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="f9209-113">-Type</span></span>
<span data-ttu-id="f9209-114">Az Azure webhely-helyreállítási anyag típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9209-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9209-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f9209-115">-Confirm</span></span>
<span data-ttu-id="f9209-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f9209-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9209-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9209-117">-WhatIf</span></span>
<span data-ttu-id="f9209-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f9209-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9209-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9209-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9209-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9209-120">CommonParameters</span></span>
<span data-ttu-id="f9209-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9209-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9209-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9209-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9209-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9209-123">INPUTS</span></span>

### <span data-ttu-id="f9209-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="f9209-124">None</span></span>

## <span data-ttu-id="f9209-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9209-125">OUTPUTS</span></span>

### <span data-ttu-id="f9209-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f9209-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f9209-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9209-127">NOTES</span></span>

## <span data-ttu-id="f9209-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9209-128">RELATED LINKS</span></span>

[<span data-ttu-id="f9209-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="f9209-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="f9209-130">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="f9209-130">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
