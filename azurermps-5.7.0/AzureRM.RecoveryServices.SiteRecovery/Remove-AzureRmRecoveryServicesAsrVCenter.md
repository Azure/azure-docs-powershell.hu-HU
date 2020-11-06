---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: eaa357e6dd216b62a2c8e8f1cd78ff15387be57a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495307"
---
# <span data-ttu-id="735d9-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="735d9-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="735d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="735d9-102">SYNOPSIS</span></span>
<span data-ttu-id="735d9-103">Eltávolítja a vCenter-kiszolgálót az ASR szövetből, és leállítja a virtuális gépek felderítését az vCenter-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="735d9-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="735d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="735d9-104">SYNTAX</span></span>

### <span data-ttu-id="735d9-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="735d9-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="735d9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="735d9-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="735d9-107">ByName</span><span class="sxs-lookup"><span data-stu-id="735d9-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="735d9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="735d9-108">DESCRIPTION</span></span>
<span data-ttu-id="735d9-109">A **Remove-AzureRmRecoveryServicesAsrvCenter** parancsmag eltávolítja az vCenter-kiszolgálót az ASR-anyagból, és a virtuális gépek felfedezését a vCenter-kiszolgálóról leállítja.</span><span class="sxs-lookup"><span data-stu-id="735d9-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="735d9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="735d9-110">EXAMPLES</span></span>

### <span data-ttu-id="735d9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="735d9-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="735d9-112">Eltávolítja a vCenter-kiszolgálót az ASR-anyagból.</span><span class="sxs-lookup"><span data-stu-id="735d9-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="735d9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="735d9-113">PARAMETERS</span></span>

### <span data-ttu-id="735d9-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="735d9-114">-Confirm</span></span>
<span data-ttu-id="735d9-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="735d9-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="735d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735d9-116">-DefaultProfile</span></span>
<span data-ttu-id="735d9-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="735d9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735d9-118">-Szövet</span><span class="sxs-lookup"><span data-stu-id="735d9-118">-Fabric</span></span>
<span data-ttu-id="735d9-119">A konfigurációs kiszolgálót jelképező ASR-anyag objektum.</span><span class="sxs-lookup"><span data-stu-id="735d9-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="735d9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="735d9-120">-InputObject</span></span>
<span data-ttu-id="735d9-121">Az vCenter-kiszolgáló eltávolítását jelző ASR vCenter objektum.</span><span class="sxs-lookup"><span data-stu-id="735d9-121">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="735d9-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="735d9-122">-Name</span></span>
<span data-ttu-id="735d9-123">A vCenter-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="735d9-123">Name of the vCenter Server.</span></span>

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

### <span data-ttu-id="735d9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="735d9-124">-ResourceId</span></span>
<span data-ttu-id="735d9-125">Az eltávolítandó vCenter resourceId adja meg.</span><span class="sxs-lookup"><span data-stu-id="735d9-125">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="735d9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="735d9-126">-WhatIf</span></span>
<span data-ttu-id="735d9-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="735d9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="735d9-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="735d9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="735d9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735d9-129">CommonParameters</span></span>
<span data-ttu-id="735d9-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="735d9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735d9-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="735d9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735d9-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="735d9-132">INPUTS</span></span>

### <span data-ttu-id="735d9-133">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="735d9-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="735d9-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="735d9-134">OUTPUTS</span></span>

### <span data-ttu-id="735d9-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 0.1.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="735d9-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="735d9-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="735d9-136">NOTES</span></span>

## <span data-ttu-id="735d9-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="735d9-137">RELATED LINKS</span></span>
