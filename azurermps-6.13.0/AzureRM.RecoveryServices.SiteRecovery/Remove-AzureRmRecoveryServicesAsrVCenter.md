---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 505d2d81eefed3132cd693ea6cd989fde173b8b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502916"
---
# <span data-ttu-id="13de3-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="13de3-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="13de3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13de3-102">SYNOPSIS</span></span>
<span data-ttu-id="13de3-103">Eltávolítja a vCenter-kiszolgálót az ASR szövetből, és leállítja a virtuális gépek felderítését az vCenter-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="13de3-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13de3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13de3-104">SYNTAX</span></span>

### <span data-ttu-id="13de3-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13de3-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13de3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="13de3-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13de3-107">ByName</span><span class="sxs-lookup"><span data-stu-id="13de3-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13de3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="13de3-108">DESCRIPTION</span></span>
<span data-ttu-id="13de3-109">A **Remove-AzureRmRecoveryServicesAsrvCenter** parancsmag eltávolítja az vCenter-kiszolgálót az ASR-anyagból, és a virtuális gépek felfedezését a vCenter-kiszolgálóról leállítja.</span><span class="sxs-lookup"><span data-stu-id="13de3-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="13de3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="13de3-110">EXAMPLES</span></span>

### <span data-ttu-id="13de3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="13de3-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="13de3-112">Eltávolítja a vCenter-kiszolgálót az ASR-anyagból.</span><span class="sxs-lookup"><span data-stu-id="13de3-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="13de3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13de3-113">PARAMETERS</span></span>

### <span data-ttu-id="13de3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13de3-114">-DefaultProfile</span></span>
<span data-ttu-id="13de3-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13de3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13de3-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="13de3-116">-Fabric</span></span>
<span data-ttu-id="13de3-117">A konfigurációs kiszolgálót jelképező ASR-anyag objektum.</span><span class="sxs-lookup"><span data-stu-id="13de3-117">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13de3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13de3-118">-InputObject</span></span>
<span data-ttu-id="13de3-119">Az vCenter-kiszolgáló eltávolítását jelző ASR vCenter objektum.</span><span class="sxs-lookup"><span data-stu-id="13de3-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13de3-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13de3-120">-Name</span></span>
<span data-ttu-id="13de3-121">A vCenter-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="13de3-121">Name of the vCenter Server.</span></span>

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

### <span data-ttu-id="13de3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13de3-122">-ResourceId</span></span>
<span data-ttu-id="13de3-123">Az eltávolítandó vCenter resourceId adja meg.</span><span class="sxs-lookup"><span data-stu-id="13de3-123">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13de3-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="13de3-124">-Confirm</span></span>
<span data-ttu-id="13de3-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13de3-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13de3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13de3-126">-WhatIf</span></span>
<span data-ttu-id="13de3-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13de3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13de3-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13de3-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13de3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13de3-129">CommonParameters</span></span>
<span data-ttu-id="13de3-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13de3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13de3-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13de3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13de3-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13de3-132">INPUTS</span></span>

### <span data-ttu-id="13de3-133">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="13de3-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="13de3-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13de3-134">OUTPUTS</span></span>

### <span data-ttu-id="13de3-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 0.1.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="13de3-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="13de3-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13de3-136">NOTES</span></span>

## <span data-ttu-id="13de3-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13de3-137">RELATED LINKS</span></span>
