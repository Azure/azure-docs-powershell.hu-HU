---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: c1ac3ae34e92feb2b356d5946a7b9f0a30a0a2aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838544"
---
# <span data-ttu-id="935cd-101">Remove-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="935cd-101">Remove-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="935cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="935cd-102">SYNOPSIS</span></span>
<span data-ttu-id="935cd-103">Eltávolítja a vCenter-kiszolgálót az ASR szövetből, és leállítja a virtuális gépek felderítését az vCenter-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="935cd-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="935cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="935cd-104">SYNTAX</span></span>

### <span data-ttu-id="935cd-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="935cd-105">Default (Default)</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="935cd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="935cd-106">ByResourceId</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="935cd-107">ByName</span><span class="sxs-lookup"><span data-stu-id="935cd-107">ByName</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="935cd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="935cd-108">DESCRIPTION</span></span>
<span data-ttu-id="935cd-109">A **Remove-AzRecoveryServicesAsrvCenter** parancsmag eltávolítja az vCenter-kiszolgálót az ASR-anyagból, és a virtuális gépek felfedezését a vCenter-kiszolgálóról leállítja.</span><span class="sxs-lookup"><span data-stu-id="935cd-109">The **Remove-AzRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="935cd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="935cd-110">EXAMPLES</span></span>

### <span data-ttu-id="935cd-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="935cd-111">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="935cd-112">Eltávolítja a vCenter-kiszolgálót az ASR-anyagból.</span><span class="sxs-lookup"><span data-stu-id="935cd-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="935cd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="935cd-113">PARAMETERS</span></span>

### <span data-ttu-id="935cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935cd-114">-DefaultProfile</span></span>
<span data-ttu-id="935cd-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="935cd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="935cd-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="935cd-116">-Fabric</span></span>
<span data-ttu-id="935cd-117">A konfigurációs kiszolgálót jelképező ASR-anyag objektum.</span><span class="sxs-lookup"><span data-stu-id="935cd-117">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="935cd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="935cd-118">-InputObject</span></span>
<span data-ttu-id="935cd-119">Az vCenter-kiszolgáló eltávolítását jelző ASR vCenter objektum.</span><span class="sxs-lookup"><span data-stu-id="935cd-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

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

### <span data-ttu-id="935cd-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="935cd-120">-Name</span></span>
<span data-ttu-id="935cd-121">A vCenter-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="935cd-121">Name of the vCenter Server.</span></span>

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

### <span data-ttu-id="935cd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="935cd-122">-ResourceId</span></span>
<span data-ttu-id="935cd-123">Az eltávolítandó vCenter resourceId adja meg.</span><span class="sxs-lookup"><span data-stu-id="935cd-123">Specifies the resourceId of vCenter to remove.</span></span>

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

### <span data-ttu-id="935cd-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="935cd-124">-Confirm</span></span>
<span data-ttu-id="935cd-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="935cd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="935cd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="935cd-126">-WhatIf</span></span>
<span data-ttu-id="935cd-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="935cd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="935cd-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="935cd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="935cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935cd-129">CommonParameters</span></span>
<span data-ttu-id="935cd-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="935cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935cd-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="935cd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935cd-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="935cd-132">INPUTS</span></span>

### <span data-ttu-id="935cd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="935cd-133">System.String</span></span>

### <span data-ttu-id="935cd-134">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="935cd-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

### <span data-ttu-id="935cd-135">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="935cd-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="935cd-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="935cd-136">OUTPUTS</span></span>

### <span data-ttu-id="935cd-137">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="935cd-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="935cd-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="935cd-138">NOTES</span></span>

## <span data-ttu-id="935cd-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="935cd-139">RELATED LINKS</span></span>
