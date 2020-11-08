---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011001"
---
# <span data-ttu-id="cf477-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="cf477-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="cf477-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf477-102">SYNOPSIS</span></span>
<span data-ttu-id="cf477-103">A már védett Azure Virtual Machine-alapú védelemhez adja hozzá a lemezt.</span><span class="sxs-lookup"><span data-stu-id="cf477-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="cf477-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf477-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf477-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf477-105">DESCRIPTION</span></span>
<span data-ttu-id="cf477-106">A **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** parancsmaggal a védett Azure Virtual Machine védelemhez hozzáadhatja a lemezt.</span><span class="sxs-lookup"><span data-stu-id="cf477-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="cf477-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cf477-107">EXAMPLES</span></span>

### <span data-ttu-id="cf477-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cf477-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="cf477-109">A művelet indításához adja meg a megfelelő lemezkezelő-konfigurációt a védelemhez.</span><span class="sxs-lookup"><span data-stu-id="cf477-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="cf477-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="cf477-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="cf477-111">A művelet indításához adja meg a megfelelő lemezkezelő-konfigurációt a védelemhez. Csővezetéken keresztüli többszörözéssel védett elem</span><span class="sxs-lookup"><span data-stu-id="cf477-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="cf477-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf477-112">PARAMETERS</span></span>

### <span data-ttu-id="cf477-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf477-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="cf477-114">Itt adhatja meg az Azure rendszerhez az Azure katasztrófa-elhárítási forgatókönyvek esetén a Lemezkezelés esetén használt Disk-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="cf477-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf477-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf477-115">-DefaultProfile</span></span>
<span data-ttu-id="cf477-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf477-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf477-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf477-117">-InputObject</span></span>
<span data-ttu-id="cf477-118">A bemeneti objektum a parancsmaghoz: az ASR-replikációval védett elem objektum, amely megfelel az új lemez védelmének.</span><span class="sxs-lookup"><span data-stu-id="cf477-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf477-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="cf477-119">-WaitForCompletion</span></span>
<span data-ttu-id="cf477-120">Várakozás a befejezésre</span><span class="sxs-lookup"><span data-stu-id="cf477-120">Wait For Completion</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf477-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf477-121">-Confirm</span></span>
<span data-ttu-id="cf477-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf477-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf477-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf477-123">-WhatIf</span></span>
<span data-ttu-id="cf477-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf477-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf477-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf477-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf477-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf477-126">CommonParameters</span></span>
<span data-ttu-id="cf477-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf477-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf477-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cf477-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf477-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf477-129">INPUTS</span></span>

### <span data-ttu-id="cf477-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="cf477-130">None</span></span>

## <span data-ttu-id="cf477-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf477-131">OUTPUTS</span></span>

### <span data-ttu-id="cf477-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cf477-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cf477-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf477-133">NOTES</span></span>

## <span data-ttu-id="cf477-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf477-134">RELATED LINKS</span></span>
