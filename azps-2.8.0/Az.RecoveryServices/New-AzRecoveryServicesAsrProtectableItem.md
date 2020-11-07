---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 57f9009ead66eb87685aaf0142c6dbd8b125f307
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838548"
---
# <span data-ttu-id="1bb6c-101">New-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1bb6c-101">New-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="1bb6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1bb6c-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb6c-103">Vegye fel a fizikai kiszolgálót a védett elemek listájára.</span><span class="sxs-lookup"><span data-stu-id="1bb6c-103">Add(Discover) a physical server to the list of protectable items.</span></span>

## <span data-ttu-id="1bb6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1bb6c-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer> -FriendlyName <String>
 -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1bb6c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1bb6c-105">DESCRIPTION</span></span>
<span data-ttu-id="1bb6c-106">Az **új AzRecoveryServicesAsrProtectableItem** felvesz egy új, védelemmel ellátott elemet az ASR-anyagban lévő védett elemek listájára (csak a VMware Fabric típus esetében alkalmazható).</span><span class="sxs-lookup"><span data-stu-id="1bb6c-106">The **New-AzRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="1bb6c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1bb6c-107">EXAMPLES</span></span>

### <span data-ttu-id="1bb6c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1bb6c-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="1bb6c-109">Új Azure Recovery Service ProtectableItem hozzáadása vagy felfedezése</span><span class="sxs-lookup"><span data-stu-id="1bb6c-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="1bb6c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1bb6c-110">PARAMETERS</span></span>

### <span data-ttu-id="1bb6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb6c-111">-DefaultProfile</span></span>
<span data-ttu-id="1bb6c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1bb6c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bb6c-113">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="1bb6c-113">-FriendlyName</span></span>
<span data-ttu-id="1bb6c-114">A védelemmel ellátott elem rövid neve.</span><span class="sxs-lookup"><span data-stu-id="1bb6c-114">Friendly name for the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb6c-115">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="1bb6c-115">-IPAddress</span></span>
<span data-ttu-id="1bb6c-116">A védelemmel ellátott elem IP-címe.</span><span class="sxs-lookup"><span data-stu-id="1bb6c-116">IP address of the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb6c-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="1bb6c-117">-OSType</span></span>
<span data-ttu-id="1bb6c-118">A védelemmel ellátott elem operációs rendszer típusa (Windows/Linux).</span><span class="sxs-lookup"><span data-stu-id="1bb6c-118">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb6c-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1bb6c-119">-ProtectionContainer</span></span>
<span data-ttu-id="1bb6c-120">Az ASR-védelmi tároló objektum, amelyhez a védelemmel ellátott elemet hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="1bb6c-120">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb6c-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1bb6c-121">-Confirm</span></span>
<span data-ttu-id="1bb6c-122">Megerősítés kérése a parancsmag futtatása előtt.</span><span class="sxs-lookup"><span data-stu-id="1bb6c-122">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bb6c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bb6c-123">-WhatIf</span></span>
<span data-ttu-id="1bb6c-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1bb6c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bb6c-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1bb6c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bb6c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb6c-126">CommonParameters</span></span>
<span data-ttu-id="1bb6c-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1bb6c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb6c-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb6c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb6c-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bb6c-129">INPUTS</span></span>

### <span data-ttu-id="1bb6c-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1bb6c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="1bb6c-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bb6c-131">OUTPUTS</span></span>

### <span data-ttu-id="1bb6c-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1bb6c-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1bb6c-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1bb6c-133">NOTES</span></span>

## <span data-ttu-id="1bb6c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1bb6c-134">RELATED LINKS</span></span>
