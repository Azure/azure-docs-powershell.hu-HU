---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466668"
---
# <span data-ttu-id="0978f-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="0978f-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="0978f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0978f-102">SYNOPSIS</span></span>
<span data-ttu-id="0978f-103">Vegye fel a lemezt a már védett Azure virtuális gép védelme érdekében.</span><span class="sxs-lookup"><span data-stu-id="0978f-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="0978f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0978f-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0978f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0978f-105">DESCRIPTION</span></span>
<span data-ttu-id="0978f-106">Az **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** parancsmag hozzáadja a lemezeket a már védett Azure virtuális gép védelme érdekében.</span><span class="sxs-lookup"><span data-stu-id="0978f-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="0978f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0978f-107">EXAMPLES</span></span>

### <span data-ttu-id="0978f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0978f-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="0978f-109">Indítsa el a műveletet adott lemezkonfiguráció hozzáadásához a védelem érdekében.</span><span class="sxs-lookup"><span data-stu-id="0978f-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="0978f-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="0978f-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="0978f-111">Indítsa el a műveletet adott lemezkonfiguráció hozzáadásához a védelem érdekében. Piping input replication protected item.</span><span class="sxs-lookup"><span data-stu-id="0978f-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="0978f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0978f-112">PARAMETERS</span></span>

### <span data-ttu-id="0978f-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="0978f-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="0978f-114">Az Azure–Azure katasztrófa-helyreállítási forgatókönyv lemezvédelemhez használt lemezkonfigurációja.</span><span class="sxs-lookup"><span data-stu-id="0978f-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="0978f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0978f-115">-DefaultProfile</span></span>
<span data-ttu-id="0978f-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0978f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0978f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0978f-117">-InputObject</span></span>
<span data-ttu-id="0978f-118">A parancsmag bemeneti objektuma: A ASR replikációs védett elemobjektuma, amely megfelel az új lemeznek.</span><span class="sxs-lookup"><span data-stu-id="0978f-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

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

### <span data-ttu-id="0978f-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="0978f-119">-WaitForCompletion</span></span>
<span data-ttu-id="0978f-120">Várakozás a befejezésre</span><span class="sxs-lookup"><span data-stu-id="0978f-120">Wait For Completion</span></span>

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

### <span data-ttu-id="0978f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0978f-121">-Confirm</span></span>
<span data-ttu-id="0978f-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0978f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0978f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0978f-123">-WhatIf</span></span>
<span data-ttu-id="0978f-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0978f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0978f-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0978f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0978f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0978f-126">CommonParameters</span></span>
<span data-ttu-id="0978f-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0978f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0978f-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0978f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0978f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0978f-129">INPUTS</span></span>

### <span data-ttu-id="0978f-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="0978f-130">None</span></span>

## <span data-ttu-id="0978f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0978f-131">OUTPUTS</span></span>

### <span data-ttu-id="0978f-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="0978f-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0978f-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0978f-133">NOTES</span></span>

## <span data-ttu-id="0978f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0978f-134">RELATED LINKS</span></span>
